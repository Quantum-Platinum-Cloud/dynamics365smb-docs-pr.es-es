---
title: 'Pagar a los proveedores mediante pagos electrónicos [ES]'
description: 'En Business Central, puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="pay-vendors-using-electronic-payments-in-the-spanish-version" />Pagar a los proveedores utilizando pagos electrónicos en la versión en español
En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede pagar a un proveedor mediante pagos electrónicos. Los pagos se exportarán a un archivo, que luego se transferirá al banco. Después, el banco transfiere los pagos de manera electrónica de su cuenta de banco a la cuenta de banco del beneficiario (proveedor).  

Este proceso es parecido al de los cheques automáticos.  

## <a name="to-pay-a-vendor-electronically" />Para pagar a un proveedor electrónicamente

1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.  
2. Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Tipo pago por banco**|Especifique un **Pago electrónico** para crear un movimiento de cheque correspondiente a ese importe.|  
    |**Tipo pago**|Especifique el tipo de pago para el pago de transferencia especial, si corresponde. Seleccione **En blanco** si no desea usar el tipo de pago de transferencia especial. Seleccione **01** para crear un pago especial para "artículos" en la línea del diario. Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.|  
    |**Código estadístico**|Especifique el código estadístico para el pago de transferencia especial, si corresponde. El código estadístico se tiene que usar conjuntamente con el tipo de pago. Seleccione **01** para crear un pago especial para "artículos" en la línea del diario. Seleccione **02** para crear un pago especial para "no artículos" en esta línea del diario.|  

## <a name="see-also" />Consulte también
[Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
