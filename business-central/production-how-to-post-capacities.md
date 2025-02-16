---
title: Registrar capacidades
description: Registra las capacidades consumidas que no están asignadas a la orden de producción en el diario de capacidad y visualiza las capacidades registradas en la página de asientos del libro mayor de capacidad.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5832, 99000802, 99000820'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="post-capacities" />Registrar capacidades

En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción. Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.  

## <a name="to-post-capacities" />Para registrar capacidades

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de capacidad**, y luego elija el enlace relacionado.  
2. Rellene los campos **Fecha registro** y **Nº documento**.  
3. En el campo **Tipo**, introduzca el tipo de capacidad, ya sea **Centro máquina** o **Centro trabajo**, que esté registrando.  
4. En el campo **N.º**, introduzca el número del centro de trabajo o del centro de máquina.  
5. Introduzca los datos correspondientes en el resto de los campos, como **Hora inicial**, **Hora final**, **Cantidad** y **Rechazo**.  
6. Para registrar la factura, elija la acción **Registrar**.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-work-center-ledger-entries" />Para consultar los movimientos de centros de trabajo

En las páginas **Ficha de centro de trabajo** y **Ficha de centro de máquina**, puede ver las capacidades registradas como resultado de órdenes de producción terminadas.    
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Centros de trabajo** y luego elija el enlace relacionado.  
2. Abra la ficha relevante **Centro trabajo** de lista, y seleccione la acción **Movimientos de capacidad**.  

    La página **Movs. capacidad** muestra los movimientos registrados desde el centro de trabajo en la orden en que fueron registrados.   

## <a name="see-also" />Consulte también

[Fabricación](production-manage-manufacturing.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
