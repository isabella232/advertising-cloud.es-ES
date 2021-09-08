---
title: Configuración de anuncios de TV conectados
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios de TV conectados.
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Configuración de anuncios de TV conectados

## [!UICONTROL Upload or Select Creative]

*Solo anuncios nuevos*

**[!UICONTROL Upload Audio]:** Para cargar un recurso sin procesar en DSP. Cuando seleccione esta opción, haga lo siguiente:

1. Haga clic en **[!UICONTROL Choose File]** y busque el archivo en su dispositivo o red.
1. Introduzca un título para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.
1. Haga clic **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Para seleccionar cualquier creativo cargado anteriormente con el formato correcto dentro de la cuenta.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Algunos tipos de anuncios) Para introducir una etiqueta VAST de terceros que contenga recursos creativos y rastreando píxeles:

1. Haga clic en ![flecha](/help/dsp/assets/compressed.png) junto a **[!UICONTROL Advanced: VAST Tag URL]**.
1. En el campo **[!UICONTROL URL]**, introduzca la URL de la etiqueta VAST.
1. Introduzca un **[!UICONTROL Title]** para el archivo, que se utilizará en la vista Anuncios y en los informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la tecla **[!UICONTROL Enter]**. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 30 segundos de CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Ancho de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height | Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

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

**[!UICONTROL Clock Number]**: (Utilizado únicamente en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel para que se active. Para este tipo de anuncio, utilice píxeles que se activen en *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un  *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles),  *[!UICONTROL HTML]* o  *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** URL de la imagen en píxeles, en el formato adecuado para el tipo de píxel especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* o  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

