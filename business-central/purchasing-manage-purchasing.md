---
title: Descripción general de las tareas para gestionar las compras
description: 'Describe las tareas para administrar sus procesos de compra o aprovisionamiento, incluido el modo en que funcionan las facturas de compra y los pedidos de compra.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="purchasing" />Compra

Cree una factura o un pedido de compra para registrar el coste de las compras y para realizar el seguimiento de los pagos. Si necesita controlar un inventario, las facturas de compra también se utilizan para actualizar dinámicamente los niveles de inventario para que pueda minimizar sus costes de inventario y proporcionar un mejor servicio al cliente. Los costes de compra, incluidos los gastos del servicio, y los valores de inventario resultantes del registro de las facturas de compra contribuyen a las cifras de ganancias y otros KPI financieros en el área de trabajo.

Debe usar pedidos de compra si el proceso de compra requiere que registre recibos parciales de una cantidad del pedido, por ejemplo, porque el proveedor no disponía de la cantidad total. Si vende productos que se entregan directamente desde el proveedor al cliente, como envío directo, deberá usar también pedidos de compras. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, los pedidos de compra funcionan de la misma forma que las facturas de compra.

Puede crear facturas automáticamente mediante el servicio OCR (reconocimiento óptico de caracteres) para convertir facturas PDF de sus proveedores en documentos electrónicos, que se convierten en facturas de compra mediante un flujo de trabajo. Para usar esta funcionalidad, primero debe registrarse en el servicio OCR y, a continuación, realizar algunas configuraciones. Para obtener más información, vea [Documentos entrantes](across-income-documents.md).

Los productos pueden ser productos de inventario y servicios. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

Para todos los procesos de compra, puede introducir un flujo de trabajo de aprobación, por ejemplo, para requerir que el administrador de contabilidad apruebe las compras grandes. Para obtener más información, vea [Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.

| Para | Vea |
| --- | --- |
| Cree una factura de compra para registrar el contrato con un proveedor para comprar productos según términos de entrega y pago determinados. |[Registrar compras](purchasing-how-record-purchases.md) |
|Cree una oferta de compra para reflejar una solicitud de oferta del proveedor, que puede convertir posteriormente en un pedido de compra.|[Solicitar presupuestos](purchasing-how-request-quotes.md)|
| Crear una factura de compra para todas las líneas en una factura de venta o las seleccionadas. |[Comprar productos para una venta](purchasing-how-purchase-products-sale.md) |
|Conozca lo que sucede cuando se registran documentos de compra.|[Registrar compras](ui-post-purchases.md)|
| Realice una acción en una factura de compra registrada sin abonar para crear automáticamente un abono y para cancelar la factura de compra o regenerarla para poder hacer correcciones. |[Corregir o cancelar facturas de venta sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Cree un abono de compra para revertir una factura de compra registrada específica para reflejar qué productos se están devolviendo al proveedor y qué importe de pago se cobrará. |[Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-register-new-vendors.md) |
|Prepárese a facturar varios albaranes del mismo proveedor una vez combinándolos en una factura.|[Agrupar albaranes en una factura única](purchasing-how-to-combine-receipts.md)|
|Convertir, por ejemplo, facturas electrónicas de sus proveedores a facturas de compra en Business Central.|[Recibir y convertir documentos electrónicos](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Aprenda cómo [!INCLUDE[prod_short](includes/prod_short.md)] calcula cuando se debe solicitar un producto para recibirlo en una fecha determinada.|[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)|
|Resolver la confusión cuando existen dos o más registros para el mismo proveedor.|[Combinar registros duplicados](sales-how-merge-duplicate-records.md)|
|Administrar el compromiso a un proveedor para comprar grandes cantidades entregadas en varios envíos a lo largo del tiempo.|[Trabajar con pedidos abiertos de compra](sales-how-to-create-blanket-sales-orders.md)|

## <a name="external-document-numbers" />Números de documento externo

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-microsoft-trainingtrainingpathspurchase-items-services-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/paths/purchase-items-services-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Configurar compras](purchasing-setup-purchasing.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Administrar pagos](payables-manage-payables.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
