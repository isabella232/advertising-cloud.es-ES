---
title: Acerca de los informes en la plataforma
description: Obtenga información sobre los datos de informes incluidos en las vistas de administración de campañas.
feature: DSP Campaign Data Views
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Acerca de los informes en la plataforma

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Las vistas de administración de campañas incluyen datos completos de informes. Los informes disponibles le ayudan a identificar los paquetes y las ubicaciones que funcionan bien y aquellos que necesitan su atención. Los botones de acción rápida también le hacen más productivo.

## Vista de todas las campañas

La variable [!UICONTROL Campaigns] la vista se abre a un conjunto de gráficos de datos de rendimiento y a una lista de todas las campañas de la cuenta.

### Vista de gráfico {#chart-view}

Puede [personalizar gráficos de tendencias de series temporales](campaign-data-visualization-manage.md) en todas las campañas utilizando tres métricas. De forma predeterminada, los datos de [!UICONTROL Net Spend], [!UICONTROL Impressions]y [!UICONTROL Net CPM] se incluyen en gráficos separados (gráficos de mosaico). Opcionalmente, puede cambiar las métricas. Para habilitar los datos por hora en los gráficos de tendencias de series temporales, cambie la selección de fechas a un solo día ([!UICONTROL Today], [!UICONTROL Yesterday]o un día específico).

![gráficos de tendencias independientes para tres métricas](/help/dsp/assets/trend-chart-separate.png)

Opcionalmente, también puede superponer las tres métricas para facilitar la detección de anomalías y áreas en las que mejorar la escala o el rendimiento.

![gráfico de tendencias con superposición](/help/dsp/assets/trend-chart.png)

### Vista de tabla

![Lista de campañas](/help/dsp/assets/campaigns-list.png)

De forma predeterminada, cada fila de campaña incluye métricas de ritmo y envío. Las métricas de ritmo incluyen [!UICONTROL Gross Spend (Lifetime)], que incluye una medición del gasto real en el objetivo en comparación con el gasto previsto en el objetivo en todos los paquetes de la campaña, para que pueda identificar de un vistazo las campañas con bajo rendimiento. Opcionalmente, puede [cambiar la vista de columna](column-view-change.md) o [crear una vista de columna personalizada](column-view-create.md).

Puede [personalizar las tablas de datos](campaign-data-views-about.md) de formas adicionales y [filtrar los datos visibles](campaign-data-filter.md).

Para ver una campaña con más detalle, haga clic en el nombre de la campaña.

## Informes de campaña única {#single-campaign-reporting}

Dentro de una campaña, puede filtrar los datos en función de la entidad de la campaña: [!UICONTROL Packages], [!UICONTROL Placements]y [!UICONTROL Ads]. Puede [filtrar los datos visibles](campaign-data-filter.md) para incluir solo los paquetes, las ubicaciones o las publicidades que desee ver.

![Pestañas de entidad de Campaign](/help/dsp/assets/campaign-subtabs.png)

### Vista de gráfico

Para cada campaña, puede [personalizar gráficos de tendencias de series temporales](campaign-data-visualization-manage.md) con tres métricas, que están disponibles en cada vista de entidad. Las mismas métricas se mantienen en todos los gráficos de tendencias de la campaña.

Consulte la [Sección &quot;Vista de gráfico&quot; sobre métricas entre campañas](#chart-view) para obtener más información.

### Vista de tabla

En cada pestaña de entidad, cada fila incluye métricas de ritmo y envío de forma predeterminada, pero puede [cambiar la vista de columna](column-view-change.md) o [crear una vista de columna personalizada](column-view-create.md) para aplicar a todas las subpestañas de la campaña. Puede [personalizar las tablas de datos](campaign-data-views-about.md) de formas adicionales. Cada tabla de datos incluye un [!UICONTROL Subtotals] , que muestra la suma o el valor promedio de cada métrica en todas las filas visibles.

### Colocación [!UICONTROL Inspector] {#placement-inspector}

Para cada ubicación, puede [abrir una (vista de detalles) [!UICONTROL Inspector])](placement-details-view.md), que incluye los siguientes datos detallados:

* **[!UICONTROL Sites]:** Todos los sitios en los que la ubicación ha tenido impresiones.

   La variable [!UICONTROL Sites] incluye las funciones de búsqueda y filtro, las mismas opciones de vista de columna estándar y personalizadas que están disponibles en la página principal y una [!UICONTROL Exclude] en cada fila para poder excluir rápidamente un sitio de la ubicación.

* **[!UICONTROL Ads]:** Todas las publicidades de la ubicación.

   La variable [!UICONTROL Ads] La pestaña incluye funciones de búsqueda y filtro, las mismas opciones estándar y personalizadas de vista de columna que están disponibles en la página principal y los botones de acción rápida en cada fila, como [!UICONTROL Pause] (para poder pausar rápidamente una publicidad).

* **[!UICONTROL Frequency]:** Datos de cada nivel de frecuencia de anuncio para la ubicación, incluidos:
   * el nivel de frecuencia de anuncio (como &quot;1&quot; para todas las instancias en las que los usuarios vieron un anuncio una vez)
   * la cantidad única estimada de dispositivos, navegadores o personas (en función del [!UICONTROL Cross Device Level] para la campaña) que recibieron impresiones en el nivel de frecuencia especificado
   * el número estimado de impresiones al nivel de frecuencia especificado
   * la frecuencia media estimada para el nivel de frecuencia especificado. Este valor es igual a (Impresiones estimadas)/(Únicas estimadas).

* **[!UICONTROL Inventory]:** Información sobre todas las ofertas segmentadas por la ubicación.

   La variable [!UICONTROL Inventory] permite una solución rápida de problemas al mostrar estadísticas de rendimiento, como [!UICONTROL Auctions], [!UICONTROL Bids]y [!UICONTROL Win Rate]. La pestaña incluye funciones de búsqueda y filtro, las mismas opciones estándar y personalizadas de vista de columna que están disponibles en la página principal y los botones de acción rápida en cada fila, incluidas [!UICONTROL Edit], [!UICONTROL View Report]y [[!UICONTROL Auction Insights] para obtener más información sobre la resolución de problemas](/help/dsp/inventory/private-deal-auction-insights.md).

#### Solución de problemas del inventario

| Problema | Posible causa | Acciones que hay que emprender |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | El editor no ha empezado a enviar solicitudes de oferta. | Póngase en contacto con el editor para activar la oferta. |
|  | La operación se configuró incorrectamente, por ejemplo, introduciendo un ID de oferta externa incorrecto. | Confirme los detalles del acuerdo y edite el acuerdo. |
| [!UICONTROL Auctions but no Bids] | El objetivo de ubicación no coincide con las solicitudes de oferta entrantes para la oferta. <br><br> Por ejemplo, una ubicación podría estar dirigiéndose a una ubicación geográfica que no sea elegible para la oferta. | Edite los objetivos de ubicación según sea necesario para evitar discrepancias de objetivos. |
|  | La ubicación no tiene un anuncio activo con el tipo de medio requerido para la oferta. | Cree y adjunte una publicidad con el tipo de medio correcto a la ubicación. |
|  | La colocación no tiene presupuesto adecuado. | Aumente el presupuesto de colocación para permitir pujas en solicitudes entrantes. |
|  | Las fechas de vuelo de colocación no se superponen con las fechas de entrega de impresiones para el acuerdo. | Edite las fechas de vuelo de la ubicación según sea necesario. |
| [!UICONTROL Low Win Rate] | La oferta máxima de la ubicación (mínimo o fijo) es inferior al mínimo requerido por la oferta. | Aumente el [!UICONTROL Max Bid] según sea necesario. |
|  | La colocación utiliza filtros de oferta previos a la oferta que limitan la oferta. | Reduzca los umbrales de los filtros de oferta previa para permitir más ofertas. |
|  | La segmentación de audiencia para la colocación es demasiado restrictiva. | Compruebe si los destinatarios de audiencia especificados tienen suficientes usuarios activos y expanda la audiencia si es posible. |

![inspector de ubicación](/help/dsp/assets/placement-inspector.png)

Puede exportar los datos en la variable [!UICONTROL Sites], [!UICONTROL Ads]o [!UICONTROL Frequency] a la carpeta de descarga predeterminada del explorador como un informe en formato XLSM.

### Otros tipos de informes de nivel de campaña

Para ver otros desgloses de datos, consulte [las páginas de informes de nivel de campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md). La variable <!--legacy --> informe incluye secciones sobre [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]y [!UICONTROL Audience Performance] datos.

>[!MORELIKETHIS]
>
>* [Ver los detalles de sitios, anuncios y frecuencia de una colocación](placement-details-view.md)
>* [Acerca de las vistas de datos de campaña](campaign-data-views-about.md)
>* [Crear una vista de columna personalizada](column-view-create.md)
>* [Cambiar la vista de columna](column-view-change.md)
>* [Administrar visualizaciones de datos](campaign-data-visualization-manage.md)
>* [Exportación de datos desde una vista de Campaign Management](campaign-export-data.md)
>* [Ver un informe detallado de una campaña](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

