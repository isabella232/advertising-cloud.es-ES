---
title: Configuración de anuncios de TV conectados
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios de TV conectados.
feature: DSP Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Configuración de anuncios de TV conectados

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: La URL de la etiqueta VAST.

**[!UICONTROL Title]**: Un nombre para el archivo, que se utilizará en la vista Anuncios y en los informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la opción **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 30 segundos de CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Height | Ad Unit Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

**[!UICONTROL Player X]:** Coordenada X para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Y]:** Coordenada Y para la unidad de publicidad. Mantenga la configuración predeterminada.

**[!UICONTROL Player Width]:** Ancho de toda la unidad publicitaria. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es igual que la variable **[!UICONTROL Width]** campo .

**[!UICONTROL Player Height]:** Altura de toda la unidad de publicidad. Esta opción puede bloquearse en función del tipo de unidad de publicidad seleccionada.

Es igual que la variable **[!UICONTROL Height]** campo .

**[!UICONTROL Show Controls]:** Dónde incluir controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se deben mantener las proporciones de ancho y alto del vídeo (*[!UICONTROL Yes]*) o para ampliar el vídeo para ocupar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como fuente de publicidad con los [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Clock Number]**: (Utilizado únicamente en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se activará. Para este tipo de anuncio, utilice píxeles que se activen en la variable *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Dirección URL de la imagen de píxel, en el formato adecuado para el tipo de píxel especificado.

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una sola publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones de la publicidad](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)

