---
title: Extensión de pagos y conciliaciones (DK)
description: Esta extensión facilita la exportación de archivos con formato predefinido para cumplir con los requisitos del banco para envíos electrónicos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, bank, formats'
ms.date: 06/24/2021
ms.author: bholtorf
---

# <a name="the-payments-and-reconciliations-dk-extension" />Extensión de pagos y conciliaciones (DK)

Realice pagos rápidos y sin errores exportando archivos formateados específicamente para intercambios con su proveedor o banco. Estos archivos aceleran los procesos de pago y conciliación, y eliminan los errores que pueden ocurrir al ingresar manualmente la información en un sitio web de un banco.  

Esta extensión admite los formatos de archivo para varios bancos de Dinamarca. Cuando exporta información de pago a un archivo, la extensión empaqueta los datos en el formato que su banco requiere. Por ejemplo, algunos de los formatos son Bankdata-V3, BEC, SDC y FIK, que utilizan muchos bancos diferentes, y algunos que son más especializados para ciertos bancos, por ejemplo, Danske Bank y Nordea. La extensión también incluye algunos formatos para importar y conciliar extractos bancarios.  

> [!Note]
> Para utilizar la extensión, es necesario conocer el formato que el banco o proveedor requiere. Algunos bancos o proveedores ofrecen esta información en las páginas web; sin embargo, es posible que deba contactar con su servicio de atención al cliente para obtener la información.  

## <a name="supported-bank-formats" />Formatos bancarios compatibles
Esta extensión puede liquidar los formatos de archivo siguiente para archivos de pagos:  

* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CSV  

## <a name="to-set-up-the-extension" />Para configurar la extensión

Existen algunos pasos a seguir para empezar.  

* Permitir exportaciones de datos de pagos. Para ayudar a proteger sus datos, no se mostrarán.  
* Configurar compra y pagos de manera que no requieran números de documentos externos en las facturas. Si es necesario, puede utilizar el número de referencia para hacer referencia a una factura específica.  
* Especificar la forma de pago de cada proveedor. Las formas de pago definen cómo se pagan las facturas de los proveedores. Por ejemplo, depósito bancario, efectivo, cheque o cuenta.  
* Especifique el tipo de formato que utiliza para cada uno de sus bancos. Por ejemplo, NORDEA, DANSKEBANK, SDC, etc.  

Además, debe asignar a los proveedores a un **Grupo contable negocio** y un **Grupo contable proveedor** nacional. La configuración de país/región para el proveedor debe ser Dinamarca (DK). Para obtener más información, consulte [Configurar los grupos contables](finance-posting-groups.md).  

### <a name="to-allow-includeprodshortincludesprodshortmd-to-export-payment-data" />Para permitir que [!INCLUDE[prod_short](includes/prod_short.md)] realice exportaciones de datos de pagos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de pagos** y luego elija el enlace relacionado.  
2. En la página **Editar diario de pagos**, seleccione el proceso **Banco**.  
3. Seleccione la casilla de verificación **Permitir exportación de pagos**.  

### <a name="to-specify-a-payment-method-for-a-vendor" />Para especificar una forma de pago de un proveedor

La siguiente tabla muestra las combinaciones de formas de pago FIK y GIRO que [!INCLUDE[prod_short](includes/prod_short.md)] admite.

|Combinación|Tipo 01 | Tipo 04 | Tipo 71 | Tipo 73 |
|----|--------|---------|---------|---------|
|¿Número de cuenta de Giro o Número acreedor de FIK? | Número de cuenta de Giro | Número de cuenta de Giro | N.º acreedor de FIK | N.º acreedor de FIK|
|¿Se permiten los mensajes al destinatario? | Sí |No |No | Sí |
|¿Contiene el número de referencia de pago? | No | Sí, 16 dígitos. | Sí, 15 dígitos. | No|

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proveedores** y luego elija el enlace relacionado.  
2. Abra la ficha, amplíe la pestaña **Pagos**, en el campo **Forma pago** seleccione la forma de pago.  
3. Según de la opción que seleccione, debe rellenar otros campos. Consulte la tabla anterior para obtener una descripción de las combinaciones.  

### <a name="to-specify-the-format-to-use-for-a-bank-account" />Para especificar el formato que debe utilizar en un banco

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el enlace relacionado.  
2. Abra la ficha del banco.  
3. En el campo **Formato de exportación de pagos**, seleccione el formato del archivo de exportación.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices" />Elección de la información de pago de FIK o Giro para facturas de proveedores

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.
2. Seleccione el proveedor. Recuerde, debe ser un proveedor danés con una dirección en Dinamarca.
3. Cree una factura. Los campos **Forma pago** y **Número de proveedor** se rellenan según los valores de la ficha de proveedor. Puede cambiarlo si lo desea.
4. En el campo **Referencia de pago**, introduzca el número de 15 dígitos de la factura del proveedor.  

    > [!Tip]
    > Tiene que agregar solo los 11 últimos dígitos del número. [!INCLUDE[prod_short](includes/prod_short.md)] añadirá cuatro ceros al comienzo del número.  

5. Registrar la factura.

## <a name="to-use-the-extension-to-export-payment-data" />Para utilizar la extensión para exportar datos de pago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.  
2. Seleccione la acción **Proponer diarios de pagos a proveedores**.  

    > [!Tip]
    > Si desea exportar únicamente pagos específicos, utilice las opciones para filtrar los datos.  

3. Si es necesario, puede agregar filtros para exportar únicamente pagos específicos.  
4. En el campo **Tipo pago por banco**, elija **Pago electrónico**.  
5. Seleccione la acción **Exportar**.  

## <a name="see-also" />Consulte también .

[Personalizar Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
