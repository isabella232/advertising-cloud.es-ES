---
title: Columnas de hojas de cálculo descargadas o cargadas
description: Haga referencia a las columnas en las hojas de cálculo de control de calidad de Excel descargadas y cargadas.
feature: Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: fcd55f882f56c9eacd82d554d30364400b99555c
workflow-type: tm+mt
source-wordcount: '734'
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
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Indica si la parrilla de programación es *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<br><b>Nota:</b> Para comprobar la programación real de partición de día, abra la configuración de colocación en  [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | El presupuesto de colocación, si hay uno. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | El intervalo presupuestario: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* o *[!UICONTROL All Time]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | El objetivo del paquete. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | El valor objetivo del objetivo. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Indica si la ubicación se acerca hacia *[!UICONTROL Budget]* o *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | La oferta máxima para la ubicación. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Pacing Fill Strategy] | La estrategia de relleno de ritmo para la ubicación: *[!UICONTROL evenly]*, *[!UICONTROL frontload]* o *[!UICONTROL aggressive frontload]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Cualquier criterio de filtro previo a la oferta que se deba aplicar. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Si las reglas de oferta (obsoletas) son *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Límite de frecuencia principal para la colocación durante el [!UICONTROL Frequency Cap Interval] especificado. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Intervalo para el límite de frecuencia principal: *[!UICONTROL Day]*, *[!UICONTROL Week]* o *[!UICONTROL Month]*. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Límite de frecuencia secundario para la colocación durante el [!UICONTROL Secondary Frequency Cap Interval] especificado | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | El tipo de intervalo para el límite de frecuencia secundario: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* o *[!UICONTROL Minute]*. El número correspondiente de semanas, días, horas o minutos se indica mediante el [!UICONTROL Secondary Frequency Cap Interval Value]. | Sí |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Número de semanas, días, horas o minutos para los que se aplica el [!UICONTROL Secondary Frequency Cap]. Por ejemplo, si el límite secundario es de tres impresiones por seis horas, el valor aquí sería <b>6&lt;/>. | Sí |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | El número de ubicaciones geográficas objetivo, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Las ubicaciones geográficas de destino, separadas por punto y coma o *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | El número de ubicaciones geográficas excluidas o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | Las ubicaciones geográficas excluidas, separadas por punto y coma o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | El número de ofertas de inventario público de destino, si se especifica alguna, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | El número de ofertas de inventario público excluidas, si las hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | El número de ofertas de inventario privado de destino, si se especifica alguna, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | El número de ofertas de inventario privado excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | El número de [!UICONTROL On-Demand Inventory] ofertas de destino, si se especifica alguna, *[!UICONTROL All]* o *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | El número de ofertas de inventario bajo demanda excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | El tipo de tráfico de destino: *[!UICONTROL Website]* y/o *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Indica si la opción Segmentación de inventario para excluir el tráfico saliente es &lt;i[!UICONTROL >ON]* o *[!UICONTROL OFF]*.<br>Los anuncios salientes generalmente aparecen sobre el contenido como una ventana emergente o rellenados con contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | La calidad de los sitios objetivo: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* o *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | El número de categorías de sitio de destino, si las hay, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | El número de categorías de sitio excluidas, si las hay, o *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Los sitios excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Idiomas del sitio de destino. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | Si se permite o no la entrega de anuncios en sitios no auditados: *[!UICONTROL ON]* o *[!UICONTROL OFF]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | El número de sitios de destino, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Las audiencias de destino, si las hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | Las audiencias excluidas, si se especifica alguna, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Indica si los segmentos demográficos de [!DNL Comscore] están habilitados para la ubicación (y otras ubicaciones en la campaña): *[!UICONTROL ON]* o *[!UICONTROL OFF]*. Esta función solo se puede habilitar para campañas para las que la función [!DNL Audience Verification] esté habilitada para [!DNL Nielson] y/o [!DNL Comscore].  Supone tasas adicionales. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Indica si ampliar o no la segmentación de anuncios entre dispositivos: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the Cross Device Targeting setting is enabled for the placement : *ON* or *OFF*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings.--> | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Se ha incluido # | El número de códigos de tema de destino, si se especifica alguno, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | El número de códigos de tema excluidos, si se especifican, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | El número de destinos de dispositivo de destino, si se especifica alguno, o *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | El número de destinos de dispositivo excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | El número de proveedores ISP de destino, si se especifica alguno, o *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | El número de proveedores de ISP excluidos, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | El número de filtros de seguridad de marca aplicados, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | El número de filtros de bloqueo de fraude preoferta aplicados, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | El número de filtros de visualización de oferta previa aplicados, si se especifica alguno, o *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Indica si el bloque de seguridad del sitio está habilitado o no: *[!UICONTROL ON]* o *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | El número de píxeles de seguimiento de eventos de terceros adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | El número de píxeles de seguimiento de conversión adjuntos a la ubicación o *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Una tasa estática de terceros que se rastreará como un coste no facturable por cada mil impresiones, si corresponde. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | El número de anuncios adjuntos a la ubicación, si los hay, o *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | Los nombres de los anuncios adjuntos a la ubicación, si los hay, o *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Acerca de la corrección de la configuración de colocación de una campaña utilizando hojas de cálculo](qa-about.md)
>* [Descargar la configuración de colocación de una campaña](qa-sheet-download.md)
>* [Cargar la configuración de colocación de una campaña](qa-sheet-upload.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

