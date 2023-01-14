---
title: Configuración de anuncios de audio
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios de audio.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Configuración de anuncios de audio

## [!UICONTROL Insert Ad Tag]

*Solo anuncios nuevos*

**[!UICONTROL URL]**: La URL de la etiqueta VAST.

**[!UICONTROL Title]**: Un nombre para el archivo, que se utilizará en la variable [!UICONTROL Ads] ver e informes.

>[!TIP]
>
> Para comprobar la validez de una etiqueta VAST, péguela en un explorador y pulse la opción **[!UICONTROL Enter]** clave. Si la etiqueta es válida, verá un archivo XML que incluye `<VAST>` cerca de la parte superior.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad. Su valor predeterminado es *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: Audio de 30 segundos&quot;).

**[!UICONTROL Ad Duration]:** Longitud del archivo de audio. Se configura automáticamente como [!UICONTROL 15] o [!UICONTROL 30], según la unidad de publicidad seleccionada.

Este campo puede mostrarse o no, en función de los permisos de la cuenta.

**[!UICONTROL VAST Tag]:** (Anuncios que solo usan etiquetas VAST) Una dirección URL para una fuente de publicidad de terceros. Asegúrese de que la etiqueta VAST incluya solo archivos multimedia de audio.

**[!UICONTROL Final VAST Tag]:** (Los anuncios que utilizan únicamente etiquetas VAST) La dirección URL del origen de los anuncios de terceros con los [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Select Rate]:** (Usuarios con permiso solamente) Una tasa previamente negociada facturada a través del Adobe, o una de las tarifas que ha negociado y se facturará a través del proveedor. Para agregar una tasa, póngase en contacto con su [!DNL Adobe] equipo de la cuenta.

### Píxel

Todos los píxeles de seguimiento de eventos existentes para la ubicación se adjuntan automáticamente. Puede separar los píxeles existentes y crear nuevos píxeles según sea necesario, según sus necesidades de seguimiento para el anuncio individual.

Las siguientes opciones se aplican a cada píxel que cree o edite.

**[!UICONTROL Integration Event]:** Evento que déclencheur el píxel que se activará. Para este tipo de anuncio, utilice píxeles que se activen en la variable *[!UICONTROL Impression]* o *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Indica si el píxel es un *[!UICONTROL IMG UR]L* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.

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

