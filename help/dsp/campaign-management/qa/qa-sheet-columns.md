---
title: Columnas de hojas de cálculo descargadas o cargadas
description: Haga referencia a las columnas en las hojas de cálculo de control de calidad de Excel descargadas y cargadas.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---

# Columnas de hojas de cálculo descargadas o cargadas

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> En una hoja de cálculo descargada, todas las columnas editables aparecen resaltadas en azul.

| Sección | Columna | Descripción | ¿Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | ID numérico de la colocación. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Nombre de la ubicación. | Sí |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Cualquier etiqueta aplicada para los informes. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Vínculo para abrir la ubicación en el modo de edición. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | El estado de la ubicación: *[!UICONTROL active]* o *[!UICONTROL inactive]*. | Sí |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | El tipo de ubicación. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Nombre del paquete principal, cuando corresponda. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | La fecha de inicio de la colocación. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | La fecha de finalización de la colocación. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Si la parrilla de programación es *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<br><b>Nota:</b> Para comprobar la programación real de parrilla de programación, abra la configuración de colocación en DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | El presupuesto de colocación, si hay uno. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | El intervalo presupuestario: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Sí |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | El objetivo del paquete. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | El valor objetivo del objetivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indica si la ubicación avanza hacia el *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | La oferta máxima para la ubicación. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | La estrategia de ritmo de vuelo para la ubicación: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | La estrategia de ritmo intradía para la ubicación: *[!UICONTROL Even]* o *[!UICONTROL ASAP]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Cualquier criterio de filtro previo a la oferta que se deba aplicar. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Si las reglas de oferta (obsoletas) son *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Límite de frecuencia principal para la colocación durante el periodo especificado [!UICONTROL Frequency Cap Interval]. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalo para el límite de frecuencia principal: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Límite de frecuencia secundario para la colocación durante el período especificado [!UICONTROL Secondary Frequency Cap Interval] | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | El tipo de intervalo para el límite de frecuencia secundario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. El número aplicable de semanas, días, horas o minutos se indica mediante la variable [!UICONTROL Secondary Frequency Cap Interval Value]. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | El número de semanas, días, horas o minutos para los que la variable [!UICONTROL Secondary Frequency Cap] se aplica. Por ejemplo, si el límite secundario es de tres impresiones por seis horas, el valor aquí sería <b>6&lt;/>. | Sí |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | El número de ubicaciones geográficas objetivo, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Las ubicaciones geográficas de destino, separadas por punto y coma, o *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | El número de ubicaciones geográficas excluidas o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Las ubicaciones geográficas excluidas, separadas por punto y coma, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | El número de ofertas de inventario público objetivo, si se especifica alguno, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | El número de ofertas de inventario público excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | El número de ofertas de inventario privado de destino, si se especifica alguno, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | El número de ofertas de inventario privado excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | El número de destinatarios [!UICONTROL On-Demand Inventory] ofertas, si se especifican, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | El número de ofertas de inventario bajo demanda excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | El tipo de tráfico de destino: *[!UICONTROL Website]* y/o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Indica si la opción Segmentación de inventario para excluir el tráfico saliente es &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* o *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Los anuncios salientes generalmente aparecen sobre el contenido como una ventana emergente o rellenados con contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La calidad de los sitios objetivo: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* o *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | El número de categorías de sitios de destino, si las hay, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | El número de categorías de sitio excluidas, si las hay, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Los sitios excluidos, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Idiomas del sitio de destino. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Solo las ubicaciones de visualización estándar) Si se permite o no la entrega de anuncios en sitios que no son auditados: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Cuando la ubicación se dirige al inventario privado, esta opción puede entregar anuncios en sitios bloqueados. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | El número de sitios de destino, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Las audiencias de destino, si las hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Las audiencias excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Si o no [!DNL Comscore] los segmentos demográficos están habilitados para la ubicación (y otras ubicaciones en la campaña): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Esta función solo se puede habilitar para campañas para las que la variable [!DNL Audience Verification] está activada para [!DNL Nielsen] y/o [!DNL Comscore].  Supone tasas adicionales. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Indica si ampliar o no la segmentación de anuncios entre dispositivos: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. La segmentación entre dispositivos amplía la segmentación en todos los dispositivos conocidos de una persona, según el gráfico de dispositivos especificado en la configuración de la campaña. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Se ha incluido # | El número de códigos de temas de destino, si se especifican, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | El número de códigos de tema excluidos, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | El número de destinos de dispositivo de destino, si se especifica alguno, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | El número de destinos de dispositivo excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | El número de proveedores de ISP de destino, si se especifica alguno, o *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | El número de proveedores de ISP excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | El número de filtros de seguridad de la marca aplicados, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | El número de filtros de bloqueo de fraude preoferta aplicados, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | El número de filtros de visualización de oferta previos aplicados, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Indica si el bloque de seguridad del sitio está habilitado o no: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | El número de píxeles de seguimiento de eventos de terceros adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | El número de píxeles de seguimiento de conversión adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Una tasa estática de terceros que se rastreará como un coste no facturable por 1000 impresiones, si corresponde. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | El número de anuncios adjuntos a la ubicación, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Los nombres de los anuncios adjuntos a la ubicación, si los hay, o *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Acerca de la corrección de la configuración de colocación de una campaña utilizando hojas de cálculo](qa-about.md)
>* [Descargar la configuración de colocación de una campaña](qa-sheet-download.md)
>* [Cargar la configuración de colocación de una campaña](qa-sheet-upload.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

