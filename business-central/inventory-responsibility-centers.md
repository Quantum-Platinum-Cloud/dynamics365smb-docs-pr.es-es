---
title: Trabajar con centros de responsabilidad
description: 'Un centro de responsabiliadad, como centro administrativo, ayuda a las empresas a configurar vistas específicas para cada usuario de los documentos de compra y de venta relacionados exclusivamente con cada centro.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 03/09/2023
ms.author: bholtorf
---
# <a name="work-with-responsibility-centers" />Trabajar con centros de responsabilidad

Los centros de responsabilidad proporcionan la capacidad de controlar los centros administrativos. Un centro de responsabilidad puede ser un centro de coste, de beneficios, de inversión o cualquier otro centro administrativo definido por la empresa. Entre los ejemplos de centros de responsabilidad se encuentran una oficina de ventas, un departamento de compras para varios almacenes y una oficina de planificación de una planta. Las empresas pueden, por ejemplo, configurar vistas específicas para cada usuario de los documentos de compra y de venta relacionados exclusivamente con un centro de responsabilidad determinado.  

El uso conjunto de varios almacenes y centros de responsabilidad ofrece la posibilidad de gestionar sus operaciones comerciales en formas flexibles y óptimas.

Con múltiples almacenes, las empresas pueden gestionar sus existencias en diversos almacenes utilizando una sola base de datos. Los elementos clave de este módulo son dos conceptos: almacenes y unidades de almacenamiento. Un almacén se define como el lugar donde se gestionan la ubicación física y las cantidades de los productos. El concepto es lo suficientemente amplio para incluir ubicaciones tales como plantas o instalaciones de producción, así como centros de distribución, almacenes, salas de exposiciones y vehículos de servicios. Una unidad de almacenamiento se define como un producto en un almacén específico y/o como variante. Al utilizar unidades de almacenamiento, las empresas con diversos almacenes pueden agregar información de reposición, direcciones y determinada información de registro financiero para el almacén. Como resultado, pueden reponer variantes de un mismo producto para cada almacén y productos para los almacenes, basándose en la información de reposición específica de cada uno.  

## <a name="to-set-up-a-responsibility-center" />Para configurar un centro de responsabilidad

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Centros de responsabilidad** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Si utiliza centros de responsabilidad para administrar la empresa, puede resultar útil tener un centro de responsabilidad predeterminado.
4. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Información empresa** y luego elija el enlace relacionado.
5. En el campo **Centro responsabilidades**, escriba un código de centro de responsabilidad.

Este código se utiliza en todos los documentos de compras, ventas o servicio en caso de que el usuario, el cliente o el proveedor no tengan un centro de responsabilidad predeterminado. Puede introducir otro centro de responsabilidad distinto al predeterminado en todos los documentos de ventas, compra o servicio.

> [!NOTE]  
> Cuando introduce un código de centro de responsabilidad en un documento, éste afecta a la dirección, dimensiones y precios que figuran en el documento.  

## <a name="to-assign-responsibility-centers-to-users" />Para asignar centros de responsabilidad a los usuarios

Puede establecer en la configuración de los usuarios que [!INCLUDE [prod_short](includes/prod_short.md)] recupere únicamente los documentos relevantes para sus áreas de trabajo concretas. Los usuarios suelen asociarse a un centro de responsabilidad y trabajan únicamente con los documentos relacionados con determinadas áreas de aplicación en dicho centro específico.  

Para configurarlo, debe asignar centros de responsabilidad a los usuarios en tres áreas funcionales básicas: Compras, Ventas y Gestión de servicios.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de usuario** y luego elija el enlace relacionado.  
2. En la página **Config. usuario**, seleccione el usuario al que desea asignar un centro de responsabilidad. Si el usuario no está incluido en la lista, deberá introducir un Id. de usuario en el campo **Id. usuario**.  
3. En el campo **Filtro centro de responsabilidad de ventas**, introduzca el centro de responsabilidad donde el usuario asumirá tareas relacionadas con ventas.  
4. En el campo **Filtro centro responsabilidad de compras**, introduzca el centro de responsabilidad donde el usuario asumirá tareas relacionadas con compras.  
5. En el campo **Filtro centro responsabilidad de servicio**, introduzca el centro de responsabilidad donde el usuario asumirá tareas relacionadas con gestión de servicios.  

> [!NOTE]  
> Los usuarios pueden ver solo los documentos publicados relacionados con su propio centro de responsabilidad. Sin embargo, pueden ver todas las entradas del libro mayor y navegar a otros documentos registrados desde las entradas del libro mayor.

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-responsibility-centers" />Consultar la [formación de Microsoft](/training/modules/set-up-responsibility-centers/) relacionada

## <a name="see-also" />Consulte también .

[Configurar inventario](inventory-setup-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definir una directiva de registro de facturas para usuarios](admin-setup-invoice-posting-policy.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
