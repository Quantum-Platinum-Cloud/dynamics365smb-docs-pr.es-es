---
title: 'Detalles de diseño: Registro inventario | Documentos de Microsoft'
description: 'Cada transacción de inventario, como un albarán de compra o un albarán de venta, registra dos movimientos de distintos tipos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-posting" />Detalles de diseño: Registro de inventario

Cada transacción de inventario, como un albarán de compra o un albarán de venta, registra dos movimientos de distintos tipos.  

|Tipo movimiento|Description|  
|----------|-----------|  
|Cantidad|Refleja el cambio de la cantidad de existencias. Esta información se almacena en los movimientos de producto.<br /><br /> Acompañado por entradas de solicitud de productos.|  
|Valor|Refleja el cambio del valor de inventario. Esta información se almacena en los movimientos de valoración.<br /><br /> Puede haber uno o más movimientos de valor por cada movimiento de producto o cada movimiento de capacidad.<br /><br /> Para obtener información acerca de los movimientos de valores de capacidad relacionados con el uso de los recursos de producción o de ensamblado, consulte [Detalles de diseño: Registro de órdenes de producción](design-details-production-order-posting.md).|  

 En relación con registros de cantidad, hay movimientos de liquidación de productos para vincular la entrada de existencias con la salida de existencias. Esto permite el motor de valoración desvíe los costes de las entradas a las salidas relacionadas, y viceversa. Para obtener más información, consulte [Detalles de diseño: Liquidación de productos](design-details-item-application.md).  

 Los movimientos de producto, los movimientos de valoración y los movimientos de liquidación de producto se crean como resultado del registro de una línea del diario de productos, ya sea indirectamente mediante el registro de una línea de pedido o directamente en la página Diario productos.  

 Las entradas de valores que se crean en el inventario físico se registran en intervalos regulares en la contabilidad para conciliar las dos contabilidades para efectos de control financiero. Para obtener más información, consulte [Detalles de diseño: Conciliación con contabilidad](design-details-reconciliation-with-the-general-ledger.md).  

 ![Flujo de entrada al reconciliar el inventario con C/G.](media/design_details_inventory_costing_1_entry_flow.png "Flujo de entrada al reconciliar el inventario con C/G")  

## <a name="example" />Ejemplo:

En el ejemplo siguiente se muestra cómo los movimientos de producto, los movimientos de valoración y los movimientos de liquidación de producto dan como resultado movimientos de contabilidad.  

 Registra un pedido de compra como recibido y facturado para 10 productos con un coste unitario directo de 7 DL y una tasa de costes generales de 1 DL. La fecha de registro es 01-01-20. Se crean los siguientes registros:  

### <a name="item-ledger-entries-1" />Movimientos contables de producto (1)

|Fecha reg.|Tipo movimiento|Importe coste (Real)|Cantidad|Nº mov.|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Compra|80,00|10|1|  

### <a name="value-entries-1" />Movimientos de valor (1)

|Fecha reg.|Tipo movimiento|Importe coste (Real)|Nº mov. producto|Nº mov.|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|Coste directo|70.00|1|1|  
|01-01-20|Coste indirecto|10.00|1|2|  

### <a name="item-application-entries-1" />Movimientos de liquidación de producto (1)

|Nº mov.|Nº movimiento contable de producto|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 A continuación, registre una venta de 10 unidades del producto con una fecha de registro de 15-01-20.  

### <a name="item-ledger-entries-2" />Movimientos contables de producto (2)

|Fecha reg.|Tipo movimiento|Importe coste (Real)|Cantidad|Nº mov.|  
|------------|----------|--------------------|--------|---------|  
|15-01-20|Venta|-80,00|-10|2|  

### <a name="value-entries-2" />Movimientos de valor (2)

|Fecha reg.|Tipo movimiento|Importe coste (Real)|Nº movimiento contable de producto|Nº mov.|  
|------------|----------|--------------------|---------------------|---------|  
|15-01-20|Coste directo|-80,00|2|3|  

### <a name="item-application-entries-2" />Movimientos de liquidación de producto (2)

|Nº mov.|Nº movimiento contable de producto|Nº mov. prod. entrada|Nº mov. prod. salida|Cantidad|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Al final del periodo contable se ejecuta el trabajo por lotes de **Registro variación inventario** en contabilidad para conciliar estas transacciones de inventario con la contabilidad.  

 Para obtener más información, consulte [Detalles de diseño: cuentas en la contabilidad](design-details-accounts-in-the-general-ledger.md).  

 En las tablas siguientes se muestra el resultado de conciliar las transacciones de inventario en este ejemplo con la contabilidad.  

### <a name="value-entries-3" />Movimientos de valor (3)

|Fecha reg.|Tipo movimiento|Importe coste (Real)|Coste regis. en contab.|Nº mov. producto|Nº mov.|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|Coste directo|70.00|70.00|1|1|  
|01-01-20|Coste indirecto|10.00|10.00|1|2|  
|15-01-20|Coste directo|-80,00|-80,00|2|3|  

### <a name="general-ledger-entries-3" />Movimientos de contabilidad (3)

|Fecha reg.|Cuenta|Nº cuenta (demostración En-US)|Importe|Nº mov.|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Cuenta de inventario]|2130|70.00|1|  
|01-01-20|[Cuenta de coste directo aplicado]|7291|-70,00|2|  
|01-01-20|[Cuenta de inventario]|2130|10.00|3|  
|01-01-07|[Cuenta liq. costes gen.]|7292|-10,00|4|  
|15-01-20|[Cuenta de inventario]|2130|-80,00|5|  
|15-01-20|[Cuenta de CV]|7290|80,00|6|  

> [!NOTE]  
> La fecha de registro de los movimientos de contabilidad es la misma que para los movimientos de valoración relacionados.  
> 
> El campo **Coste registro en contabilidad** de la tabla **Movimiento valor** está rellenado.  

 La relación entre los movimientos de valoración y los movimientos de contabilidad se almacena en la tabla **Relación movs. productos - C/G**  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3" />Movimientos de relación en C/G: tabla Relación movs. productos (3)

|Nº mov. contabilidad|Nº mov. valor|Nº asto. registro|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting" />Registro del ensamblado y de producción

La capacidad y los movimientos de recursos representan el tiempo registrado como consumido en producción o en ensamblado. Estos costes de proceso se registran como movimientos de valoración en la contabilidad junto con los costes de materiales relacionados en una estructura similar a la descrita para los movimientos de producto en este tema.  

Para obtener más información, consulte [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md).  

## <a name="see-also" />Consulte también

 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
 [Detalles de diseño: cuentas de contabilidad](design-details-accounts-in-the-general-ledger.md)  
 [Detalles de diseño: Componentes de coste](design-details-cost-components.md) [Gestión de costes de inventario](finance-manage-inventory-costs.md)  
 [Finanzas](finance.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
