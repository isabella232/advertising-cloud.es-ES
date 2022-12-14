---
title: Configuración de anuncios de vídeo universal
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios de vídeo universales.
feature: DSP Ads
source-git-commit: fa91f2c30841bde2b943dee31d373fec343bdc75
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Configuración de anuncios de vídeo universal

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]:** La URL de la etiqueta VAST.

**[!UICONTROL Title]:** Un título para el archivo que se encuentra en la variable [!UICONTROL Ads] ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la opción **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: Vídeo universal de 30 segundos&quot;).

**[!UICONTROL Show Controls]:** Dónde incluir controles de vídeo para el anuncio: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* o *[!UICONTROL None]* (predeterminado).

**[!UICONTROL Preserve Aspect Ratio]:** Si se deben conservar las proporciones de ancho y alto del vídeo (*[!UICONTROL Yes]*) o para ampliar el vídeo para ocupar el espacio disponible (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que introdujo como fuente de publicidad.

**[!UICONTROL Final VAST Tag]:** (Los anuncios que solo utilizan etiquetas VAST; solo lectura) La etiqueta VAST de terceros que ha introducido como fuente de publicidad con los [Macros de seguimiento de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Wmode]:** El modo de ventana: *[!UICONTROL window]*, *[!UICONTROL transparent]* o *[!UICONTROL opaque]*. Si esta configuración no es aplicable, déjela en blanco.

**[!UICONTROL Video Format]:** Formato del reproductor de publicidad para inventario potencial: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* o *[!UICONTROL VAST]*. La visibilidad siempre se mide para [!UICONTROL VPAID], pero [!UICONTROL VPAID & VAST] incluye un inventario que no permite la medición de la visibilidad. Tenga en cuenta esta distinción si las métricas de visibilidad son importantes para la campaña.

Uso *[!UICONTROL VAST]*, que no permite la medición de la visibilidad, cuando se segmenta por TV conectada o inventario que requiera estrictamente formato VAST únicamente (normalmente desde fuentes de suministro como Google Ad Manager, Appnexus, SpotX y Freewheel).

**[!UICONTROL Clock Number]**: (Utilizado únicamente en el Reino Unido; disponible solo para usuarios con permiso) Identificador único utilizado para garantizar que se emite el anuncio correcto. Si esta configuración no es aplicable, déjela en blanco.

### [!UICONTROL Pixel]

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se activará. Para este tipo de anuncio, utilice píxeles que se activen en la variable *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** La URL de la imagen en píxeles, en el formato adecuado para el [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** El nombre del píxel. Utilice un nombre que le ayude a identificar fácilmente el píxel.

**[!UICONTROL Pixel Provider]:** El proveedor de píxeles: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* o *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de publicidad](ad-about.md)
>* [Crear una sola publicidad](ad-create.md)
>* [Enumerar las ubicaciones asociadas a una publicidad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Especificaciones de la publicidad](ad-specs.md)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

