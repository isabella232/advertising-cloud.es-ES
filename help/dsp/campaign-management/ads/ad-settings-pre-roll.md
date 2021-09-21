---
title: Configuración de anuncio previo a la emisión
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios previos a la emisión.
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Configuración de anuncio previo a la emisión

## [!UICONTROL Upload or Select Creative]

*Solo anuncios nuevos*

**[!UICONTROL Transcode to]:** (Algunos usuarios, según los permisos; (opcional) los formatos que desea incluir en la etiqueta VAST cuando el editor tiene requisitos específicos de archivos creativos. Los formatos aceptados por la mayoría de los editores están seleccionados de forma predeterminada.

**[!UICONTROL Custom Transcode]:**  (solo usuarios beta; no disponible cuando está seleccionado Vídeo vertical ) Indica que el vídeo utiliza transcodificación personalizada. Si selecciona esta opción, especifique el formato de archivo, la velocidad de bits del vídeo, el zoom y las dimensiones para hasta tres versiones de transcodificación personalizadas.

**[!UICONTROL XTrader]:** (Algunos usuarios, según los permisos) Indica que el vídeo utiliza una o varias  [!DNL X_TRADER] fuentes.

**[!UICONTROL Upload Video]:** Para cargar un recurso sin procesar en DSP. Cuando seleccione esta opción, haga lo siguiente:

1. Haga clic en **[!UICONTROL Choose File]** y busque el archivo en su dispositivo o red.
1. Introduzca un título para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.
1. Haga clic **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** Para seleccionar cualquier creativo cargado anteriormente con el formato correcto dentro de la cuenta.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Algunos tipos de anuncios) Para introducir una etiqueta VAST de terceros que contenga recursos creativos y rastreando píxeles:

1. Haga clic en ![flecha](/help/dsp/assets/compressed.png) junto a **[!UICONTROL Advanced: VAST Tag URL]**.
1. En el campo **[!UICONTROL URL]**, introduzca la URL de la etiqueta VAST.
1. Introduzca un **[!UICONTROL Title]** para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la tecla **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 30 segundos de predesplazamiento&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:**  (Solo anuncios previos a la emisión estándar y omitidos) Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:**  (Solo anuncios previos a la emisión estándar y omitidos) La altura de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Ancho de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es lo mismo que el campo **[!UICONTROL Width]**.

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es lo mismo que el campo **[!UICONTROL Height]**.

**[!UICONTROL Show Controls]:** Dónde incluir controles de vídeo para el anuncio:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* o  *[!UICONTROL None]* (opción predeterminada).

**[!UICONTROL Preserve Aspect Ratio]:** Si se deben mantener las proporciones de ancho y alto del vídeo (*[!UICONTROL Yes]*) o si se debe estirar el vídeo para llenar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL Click URL]:**  (Solo anuncios servidos por Adobe) Dirección URL a la que llegará el espectador cuando haga clic en el anuncio.

**[!UICONTROL Final Click URL]:**  (solo anuncios de Adobe; solo lectura)  [!UICONTROL Click URL] con el seguimiento necesario de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) macrosserted, si corresponde.

**[!UICONTROL VAST Tag]:** (los anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (los anuncios que solo usan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como fuente de publicidad con el seguimiento de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) necesario macroniveado, si corresponde.

**[!UICONTROL Wmode]:**  (Solo pre-roll interactivo) El modo de ventana:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* o  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:**  (Solo pre-roll interactivo) El formato del reproductor de publicidad para inventario potencial:  *[!UICONTROL VPAID]* o  *[!UICONTROL VPAID & VAST]*. La visibilidad siempre se mide para VPAID, pero VPAID y VAST incluye un inventario que no permite la medición de la visibilidad. Tenga esto en cuenta si las métricas de visibilidad son importantes para la campaña.

**[!UICONTROL Clock Number]**: (Solo pre-roll interactivo; utilizado únicamente en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Companion]

*Solo anuncios DSP*

Si lo desea, puede adjuntar hasta tres banners adjuntos con un anuncio. La práctica recomendada es adjuntar banners complementarios siempre que sea posible.

>[!NOTE]
>
> No todos los editores permiten banners complementarios. Los editores que sí permiten banners complementarios no garantizan impresiones de banners complementarios.
> Es posible que los banners adjuntos de etiquetas de publicidad de terceros no siempre estén disponibles para la vista previa.

**\[Casilla de verificación\]:** incluye el banner complementario especificado con el anuncio. Cuando la casilla de verificación está desactivada, no se incluye el banner complementario.

**\[Tamaño del banner\]:** El tamaño del banner complementario:  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*, que es el tamaño de anuncio más común y recomendado para todos los anuncios;  *[!UICONTROL 300x60 (Small Banner)]*; o  *[!UICONTROL 728x90 (Leaderboard)]*, que es un tamaño de anuncio menos común.

**\[Origen\]:** Si está cargando su propio recurso de banner complementario o utilizando una etiqueta de terceros.

**Recurso:**  (solo activos sin procesar) El recurso del banner complementario. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**Etiqueta de anuncio]:[!UICONTROL ** (Los anuncios que usan etiquetas VAST solamente) Una URL a una fuente de banner complementario de terceros.

**[!UICONTROL Final Ad Tag]:** (Anuncios que solo utilizan etiquetas VAST) Dirección URL de un origen de banner complementario de terceros con el seguimiento necesario de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) macronizado, si corresponde.

### [!UICONTROL Overlays]

*Formatos interactivos interactivos de anuncio previo a la emisión y móviles y de toque para reproducción para anuncios DSP*

Las siguientes opciones se aplican a cada superposición que cree o edite.

**[!UICONTROL Asset]:**  (Solo recursos sin procesar) El recurso de imagen de superposición. El archivo debe estar en formato GIF, JPG o PNG de un solo fotograma y el tamaño máximo de la imagen debe ser inferior a 2 MB. Para cargar el recurso, haga clic en **[!UICONTROL Browse]**, busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

>[!TIP]
>
>Consulte las [Prácticas recomendadas para diseñar superposiciones](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  URL a la que llegará el espectador cuando haga clic en una superposición de su publicidad.

**[!UICONTROL X]:** Coordenada X para la superposición. Seleccione la posición de inicio de la superposición y, a continuación, introduzca el número de píxeles desde la posición de inicio (por ejemplo, 10 píxeles desde el centro). La práctica recomendada es utilizar *Desde el centro*, lo que evita que la superposición se mueva con diferentes tamaños de reproductor en los sitios del editor.

**[!UICONTROL Y]:** La coordenada Y para la superposición. Seleccione la posición inicial de la superposición y, a continuación, introduzca el número de píxeles desde la posición inicial (como 10 píxeles desde arriba). La práctica recomendada es especificar una coordenada *[!UICONTROL From Bottom]* o *[!UICONTROL From Top],* en función de la posición en la que desea que se muestre la superposición en el anuncio.

**[!UICONTROL Layer]:** La capa en la que aparecerá la superposición. El vídeo y cada superposición se encuentran en capas independientes.

* *[!UICONTROL 2 through 5]:* Delante del vídeo pero detrás de otras superposiciones.

* *[!UICONTROL 1]:* Delante del vídeo.

* *[!UICONTROL 0]:* en la misma capa que el vídeo. El vídeo se reducirá para ocupar el espacio restante. No recomendado para la preconfiguración interactiva.

* *[!UICONTROL -1]:* Detrás del vídeo.

* *[!UICONTROL -2 through -5]:* Detrás del vídeo pero delante de otras superposiciones.

* *[!UICONTROL Background]:* Detrás del vídeo y otras superposiciones. La superposición se escalará hasta el ancho y la altura completos del vídeo y no se conservará la relación de aspecto.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel para que se active. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un  *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles),  *[!UICONTROL HTML]* o  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La dirección URL de la imagen en píxeles, en el formato adecuado para el  [!UICONTROL Pixel Type] especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* o  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)
>* [Prácticas recomendadas para el diseño de superposiciones](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

