---
title: Configuración de anuncios de Mobile
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios móviles.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Configuración de publicidad móvil

## [!UICONTROL Insert Ad Tag]

*Solo formatos de anuncios de vídeo móvil nuevos*

**[!UICONTROL URL]** o **[!UICONTROL Ad Tag]**: Etiqueta de publicidad VAST de terceros o etiqueta de publicidad que contiene recursos creativos y seguimiento de píxeles

**[!UICONTROL Ad Title]** o **[!UICONTROL Title]**: Un nombre para la publicidad que se usa en la [!UICONTROL Ads] ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la opción **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Publicidades para pantallas móviles

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 300x250 Gamer&quot;).

**\[Fuente de publicidad\]**: (Solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** La URL del recurso creativo de terceros. Cualquiera [timestamp] y [[timestamp]] se reemplazarán por valores reales.

**[!UICONTROL Final Display Code]:** La dirección URL del recurso creativo de terceros, con los [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

### [!UICONTROL Basic]: Anuncios de vídeo

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista Anuncios y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 30 segundos de predesplazamiento del teléfono&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es igual que la variable **[!UICONTROL Width]** campo .

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es igual que la variable **[!UICONTROL Height]** campo .

**[!UICONTROL Show Controls]:** Dónde incluir controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se deben mantener las proporciones de ancho y alto del vídeo (*[!UICONTROL Yes]*) o para ampliar el vídeo para ocupar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Algunos tipos de anuncios) El número de segundos que se tarda en retrasar el aspecto del botón de cierre.

**[!UICONTROL VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como recurso creativo.

**[!UICONTROL Final VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como recurso creativo con el [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Wmode]:** (Algunos tipos de anuncios) El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se activará. Para este tipo de anuncio, utilice píxeles que se activen en la variable *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen en píxeles, en el formato adecuado para el [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* o *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Obsoleto

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una sola publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones de la publicidad](ad-specs.md)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

