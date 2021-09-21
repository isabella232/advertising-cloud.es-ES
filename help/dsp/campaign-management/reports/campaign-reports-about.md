---
title: Acerca de los informes en la plataforma
description: Obtenga información sobre los datos de informes incluidos en las vistas de administración de campañas.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Acerca de los informes en la plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Las vistas de administración de campañas incluyen datos completos de informes. Los informes disponibles le ayudan a identificar los paquetes y las ubicaciones que funcionan bien y aquellos que necesitan su atención. Los botones de acción rápida también le hacen más productivo.

## Lista Todas las campañas

La vista [!UICONTROL Campaigns] se abre a una lista de todas las campañas de la cuenta. La fila [!UICONTROL Subtotals] muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

![Lista de campañas](/help/dsp/assets/campaigns-list.png)

De forma predeterminada, cada fila de campaña incluye métricas de ritmo y envío. Las métricas de ritmo incluyen [!UICONTROL Gross Spend (Lifetime)], que incluye una medición del gasto real en el objetivo en comparación con el gasto objetivo esperado en todos los paquetes de la campaña, para que pueda identificar de un vistazo las campañas con bajo rendimiento. Si lo desea, puede [cambiar la vista de columna](column-view-change.md) o incluso [crear una vista de columna personalizada](column-view-create.md).

Puede [personalizar aún más las tablas de datos](campaign-data-views-about.md) de formas adicionales y [filtrar los datos visibles](campaign-data-filter.md).

Para ver una campaña con más detalle, haga clic en el nombre de la campaña.

## Informes de campaña única

Dentro de una campaña, puede filtrar los datos en función de la entidad de la campaña: [!UICONTROL Packages], [!UICONTROL Placements] y [!UICONTROL Ads]. Puede filtrar más [los datos visibles](campaign-data-filter.md) para incluir solo los paquetes, las ubicaciones o las publicidades que desee ver.

![Pestañas de entidad de Campaign](/help/dsp/assets/campaign-subtabs.png)

En cada ficha de entidad, cada fila incluye métricas de ritmo y envío de forma predeterminada, pero puede [cambiar la vista de columna](column-view-change.md) o incluso [crear una vista de columna personalizada](column-view-create.md) para aplicarla en todas las subpestañas de la campaña. Puede [personalizar aún más las tablas de datos](campaign-data-views-about.md) de formas adicionales. Cada tabla de datos incluye una fila [!UICONTROL Subtotals], que muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

Para cada campaña, también puede personalizar gráficos de tendencias de series temporales con tres métricas, que están disponibles en cada vista de entidad. De forma predeterminada, los datos de [!UICONTROL Net Spend], [!UICONTROL Impressions] y [!UICONTROL Net CPM] se incluyen en gráficos independientes (gráficos de listas de direcciones). Opcionalmente, puede cambiar las métricas.

![gráficos de tendencias independientes para tres métricas](/help/dsp/assets/trend-chart-separate.png)

Opcionalmente, también puede superponer las tres métricas para facilitar la detección de anomalías y áreas en las que mejorar la escala o el rendimiento.

![gráfico de tendencias con superposición](/help/dsp/assets/trend-chart.png)

Puede [personalizar los gráficos de tendencias](campaign-data-visualization-manage.md) por campaña, y las mismas métricas se mantienen en todos los gráficos de tendencias de la campaña.

### Inspector de ubicación

Para cada ubicación, puede [abrir una (vista de detalles [!UICONTROL Inspector])](placement-details-view.md), que incluye los siguientes datos en profundidad:

* **[!UICONTROL Sites]:** Todos los sitios en los que la ubicación ha tenido impresiones.

   La pestaña [!UICONTROL Sites] incluye funciones de búsqueda y filtro, las mismas opciones estándar y personalizadas de vista de columna que están disponibles en la página principal y un botón [!UICONTROL Exclude] en cada fila para que pueda excluir rápidamente un sitio de la ubicación.

* **[!UICONTROL Ads]:** Todas las publicidades de la ubicación.

   La pestaña [!UICONTROL Ads] incluye funciones de búsqueda y filtro, las mismas opciones estándar y personalizadas de vista de columna que están disponibles en la página principal y los botones de acción rápida en cada fila, como [!UICONTROL Pause] (para que pueda pausar rápidamente un anuncio).

* **[!UICONTROL Frequency]:** Datos de cada nivel de frecuencia de anuncio para la ubicación, incluidos:
   * el nivel de frecuencia de anuncio (como &quot;1&quot; para todas las instancias en las que los usuarios vieron un anuncio una vez)
   * el número único estimado de dispositivos, navegadores o personas (según el [!UICONTROL Cross Device Level] especificado para la ubicación) que recibieron impresiones en el nivel de frecuencia especificado
   * el número estimado de impresiones al nivel de frecuencia especificado
   * la frecuencia media estimada para el nivel de frecuencia especificado. Este valor es igual a (Impresiones estimadas)/(Únicas estimadas).

![inspector de ubicación](/help/dsp/assets/placement-inspector-sites.png)

Puede exportar los datos de las pestañas [!UICONTROL Sites], [!UICONTROL Ads] o [!UICONTROL Frequency] a la carpeta de descarga predeterminada del explorador como un informe en formato XLSM.

### Otros tipos de informes de nivel de campaña

Para otros desgloses de datos, vea [las páginas heredadas de informes de nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md) desde [!UICONTROL Campaigns Classic]. El informe heredado incluye secciones sobre datos [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] y [!UICONTROL Audience Performance].

>[!MORELIKETHIS]
>
>* [Ver los detalles de sitios, anuncios y frecuencia de una colocación](placement-details-view.md)
>* [Acerca de las vistas de datos de campaña](campaign-data-views-about.md)
>* [Crear una vista de columna personalizada](column-view-create.md)
>* [Cambiar la vista de columna](column-view-change.md)
>* [Administrar visualizaciones de datos](campaign-data-visualization-manage.md)
>* [Exportación de datos desde una vista de administración de campañas](campaign-export-data.md)
>* [Ver un informe detallado de una campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

