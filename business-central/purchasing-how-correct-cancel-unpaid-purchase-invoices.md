---
title: Modificar o cancelar facturas de compra sin abonar (contiene vídeo)
description: 'Explica cómo corregir, cancelar o deshacer una factura de compra registrada y crear automáticamente un abono de compra.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '138, 140, 146'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="correct-or-cancel-unpaid-purchase-invoices" />Corregir o cancelar facturas de compra sin abonar

Puede corregir o cancelar una factura de compra registrada. Esto es útil si se desea corregir un error de escritura o si desea cambiar la compra de forma anticipada en el proceso de pedido.

Si ya ha pagado productos en la factura de compra registrada, no puede corregirla o cancelarla desde la factura de compra registrada en sí. En su lugar, debe crear manualmente un abono de compra para revertir la compra, opcionalmente administrada con una orden de devolución de compra. Lo mismo se aplica si desea modificar una factura de compra registrada que se basó en recibos de compra combinados. Para obtener más información, vea [Procesar devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md).

En la página **Factura de compra registrada**, puede elegir el botón **Corregir** o **Cancelar**. Al corregir o cancelar una factura de compra registrada, el abono de compra de corrección se aplica a todos los movimientos contables y del inventario que se crearon cuando se registró la factura de compra inicial. De esta forma se invierte la factura de compra registrada en los registros financieros deja el abono de compra registrado de corrección para el seguimiento de auditoria. A continuación se describe el uso de **Corregir** y **Cancelar**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice" />Para corregir una factura de compra registrada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas compra** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la factura de compra registrada que desea corregir.  

    > [!NOTE]  
    >   Si se selecciona la casilla **Cancelado**, no puede corregir la factura de compra registrada porque ya se ha corregido o cancelado.
3. En la página **Factura de compra registrada**, elija **Corregir**.

    Una nueva factura de compra con la misma información se crea donde puede realizar la corrección. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md). El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.

    Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente.
4. Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.

## <a name="to-cancel-a-posted-purchase-invoice" />Para cancelar una factura de compra registrada

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico facturas compra** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la factura de compra registrada que desea cancelar.

    > [!NOTE]  
    >   Si se selecciona la casilla **Cancelado**, no puede cancelar la factura de compra registrada porque ya se ha cancelado o corregido.
3. En la página **Factura de compra registrada**, elija **Cancelar**.

    Un abono de compra se crea y se registra automáticamente para anular la factura de compra registrada inicialmente. El campo **Cancelado** en la factura de compra registrada inicial se cambia a **Sí**.
4. Elija **Mostrar abono correctivo** para ver el histórico de abonos de compra que anula la factura de compra registrada inicial.

### <a name="partial-invoice-posting-also-supported" />También se admite el registro parcial de facturas

Si la cancelación está relacionada con un registro parcial de la factura, la línea de pedido de compra original se actualiza para reflejar la cantidad facturada cancelada. Los campos **Cant. a facturar** y **Cant. facturada** en la línea de pedido de compra relacionada se restablecen a los valores previos del registro parcial.

## <a name="see-related-microsoft-trainingtrainingmodulesreceive-invoice-dynamics-d365-business-central" />Consultar la [formación de Microsoft](/training/modules/receive-invoice-dynamics-d365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
