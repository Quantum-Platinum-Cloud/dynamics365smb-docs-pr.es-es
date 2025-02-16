---
title: Gestionar presupuestos de activos fijos
description: 'Puede configurar la información sobre inversiones, ventas/bajas y amortizaciones futuras de activos fijos como ayuda para preparar presupuestos y previsiones.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.search.form: '5610, 5611'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="manage-budgets-for-fixed-assets" />Gestionar presupuestos de los activos fijos

Puede configurar activos fijos presupuestados. Por ejemplo, esto le permite incluir adquisiciones y ventas anticipadas en los informes.  

Para preparar sus presupuestos de ingresos, presupuestos de cuentas de balance y el presupuesto de caja, necesitará información acerca de las inversiones futuras, ventas/bajas y amortización de activos fijos. Puede obtener esta información desde el informe **A/F - Proyección amort**. Antes de imprimir este informe, debe preparar el presupuesto.  

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset" />Para presupuestar el coste de un activo

Para preparar presupuestos, necesita configurar fiches de activos para los activos que quiera comprar en el futuro. Los activos fijos presupuestados se configuran como activos normales, pero deben configurarse para que no se registren en el libro mayor.

Al registrar el coste, introduzca el número de activos presupuestados en el campo **A/F N.º pptdo.** Esto provocará que se registre un coste con signo inverso en el activo presupuestado. Significa que el coste total del activo presupuestado es la diferencia entre el coste presupuestado y el real.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Elija la acción **Nuevo** para crear una nueva ficha del activo para el activo presupuestado.
3. Seleccione la casilla **Activo presupuestado** para evitar su registro en el libro mayor.
4. Rellene los campos restantes, asigne un libro de amortización y, a continuación, registre el primer coste con el activo presupuestado especificado en el campo **A/F N. º pptdo.** en la línea del diario. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset" />Para presupuestar la venta/baja de un activo fijo

Si desea vender activos en el periodo de presupuesto, puede especificar información acerca del precio y fecha de venta.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.
2. Seleccione el activo que desee dar de baja o vender y, a continuación, elija la acción **Libros amortización**.
3. En la página **Libros amortización A/F**, rellene los campos **Fecha prevista venta/baja** y **Ingresos previstos venta/baja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values" />Para ver valores venta/baja previstos

Para ver los valores venta/baja previstos y que se calculen las ganancias y pérdidas, puede usar el informe **Proyección de la amortización A/F**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Proyección de la amortización A/F**, y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-budget-depreciation" />Para presupuestar amortización

Puede usar el informe **A/F - Proyección amort.** para calcular la amortización futura. El informe muestra el valor neto y la amortización acumulada al principio del periodo seleccionado, los cambios durante el periodo y el valor neto y la amortización acumulada al final del periodo seleccionado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Valor proyectado de activo fijo** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario.
3. Para ver los valores totales de todos los activos, desactive la casilla **Imprimir por activo fijo**.
4. Deje en blanco la ficha desplegable **Activo** para incluir todos los activos. En el campo **Activo presupuestado**, puede especificar **No** para excluir los activos presupuestados o **Sí** para ver solo los activos presupuestados.
5. Elija el botón **Imprimir** o **Versión preliminar**.

## <a name="see-related-microsoft-trainingtrainingmodulesbudget-fixed-assets" />Consultar la [formación de Microsoft](/training/modules/budget-fixed-assets/) relacionada

## <a name="see-also" />Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
