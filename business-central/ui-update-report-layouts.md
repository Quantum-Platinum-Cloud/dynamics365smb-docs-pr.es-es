---
title: Actualizar los diseños de informe personalizados
description: 'Aprenda a actualizar un diseño de informe personalizado que se utiliza en un informe cuando hay cambios de diseño en el conjunto de datos del informe, por ejemplo.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9652, 9650'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="legacy-update-custom-report-layouts" />(Versión heredada) Actualizar los diseños de informe personalizados

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

De vez en cuando es posible que necesite actualizar un diseño de informe personalizado que se use en un informe. Esto es necesario cuando ha habido un cambio de diseño en el conjunto de datos del informe, por ejemplo, si se elimina un campo que se utiliza en el diseño. Si un diseño de informe requiere actualización, recibirá un mensaje de error cuando intente obtener una vista previa del informe, o al imprimirlo o guardarlo.  

Para actualizar automáticamente el diseño de un informe a partir del mensaje de error que aparece al ejecutar un informe, seleccionando el botón **Sí** en el mensaje de error. O, antes de ejecutar los informes, puede actualizar determinados diseños de informe o todos los diseños de informe personalizados que podrían verse afectados por los cambios del conjunto de datos.  

También tiene la opción de probar actualizaciones sin aplicar los cambios necesarios en los diseños de informe personalizados. Así puede ver qué cambios se aplicarán en el diseño de informe a e identificar posibles problemas en el proceso. Desde los resultados de la prueba puede abrir diseños de informe personalizados directamente para modificarlos y solucionar problemas. Se recomienda que pruebe el diseño de informe antes de aplicar las actualizaciones.  

No todos los cambios de conjunto de datos de informe se pueden actualizar automáticamente en sus diseños de informe. Algunos cambios requerirán que se modifique manualmente el diseño del informe. Para obtener más información, vea [Limitaciones de actualización con la venta o baja del informe personalizados](ui-update-report-layouts.md#UpdateLimitations).  

## <a name="to-update-one-or-more-custom-report-layouts" />Para actualizar una o varias plantillas de informe personalizado

1.  Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección de diseño de informes** y luego elija el enlace relacionado.  

2.  En la página **Selección de diseño de informes**, si desea actualizar un informe específico, seleccione el diseño de lista y, después, seleccione la acción **Actualizar diseño**. O, si desea actualizar todos los diseños de informe personalizados para la empresa, seleccione la acción **Actualizar todos los diseños**.  

Si no se producen errores, las actualizaciones se aplican a los diseños de informe. Si se producen errores, aparece un mensaje que contiene errores. A continuación tendrá que modificar el diseño de informe personalizado para corregir el error. Para obtener más información, vea [Corrección de errores](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates" />Para probar actualizaciones de diseños de informe personalizados

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección de diseño de informes** y luego elija el enlace relacionado.  

2.  En la página **Selección de diseño de informes**, seleccione la acción **Probar actualizaciones de diseño**.  

 Los cambios en los diseños de informe se prueban pero no se aplican a los diseños de informe reales. Una página **Registro de actualización de diseño de informe** aparece, la cual proporciona el estado de actualizaciones potenciales para cada diseño de informe. Si hay errores en un diseño de informe, puede acceder al diseño de informe directamente para modificar el mensaje para solucionar errores. Para obtener más información, vea [Corrección de errores](ui-update-report-layouts.md#FixErrors).  

## <a name="a-nameupdatelimitationsa-limitations-of-the-custom-report-layout-update" /><a name="UpdateLimitations"></a> Limitaciones de la actualización de diseños de informe personalizados
 Existen varios tipos de cambios que la actualización automática puede aplicar a los diseños de informe personalizados, por ejemplo, un campo que se utiliza en el diseño se ha eliminado del conjunto de datos del informe. Sin embargo, la actualización automática no puede administrar los siguientes cambios en un conjunto de datos de informe.  

1.  Campos, etiquetas o elementos de datos borrados.  

2.  Nombres de campos duplicados en el diseño de informe después haber cambiado el nombre de un campo en el conjunto de datos. Esto debe tratarse como error de diseño.  

3.  Actualizar casos cuando hay varias iteraciones de un diseño de informe que causa varias acciones de cambio de nombre en los mismos campos, etiquetas o elementos de datos.  

 Si el proceso de actualización detecta cualquiera de estos problemas, la actualización no puede aplicarse. Tendrá que solucionar los problemas manualmente, por ejemplo modificando el diseño de informe en Word o programáticamente con codeunits de actualización.  

## <a name="a-namefixerrorsa-fixing-errors" /><a name="FixErrors"></a> Corrección de errores
 Si sigue recibiendo un mensaje de error al actualizar o probar actualizaciones de diseño de informe, es muy probable que tenga que modificar el diseño del informe para corregir el problema. Consulte el mensaje de error para determinar la causa del problema.  

 El problema más habitual se produce cuando un campo que se utiliza en el diseño se elimina del conjunto de datos del informe. En este caso, verá una línea en el mensaje de error que indica que se ha eliminado un producto. Para corregir este problema, tendrá que modificar el diseño y eliminar el campo en cuestión.  

 Para obtener más información, vea [Crear y modificar un diseño de informe personalizado](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Después de modificar el diseño, pruebe a actualizar el diseño de nuevo.  

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también
 [Gestión de diseños de informe](ui-manage-report-layouts.md)  
 [Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
