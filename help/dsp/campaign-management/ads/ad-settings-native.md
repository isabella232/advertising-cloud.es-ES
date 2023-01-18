---
title: Configuración de anuncios en pantalla nativos
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios en pantalla nativos.
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Configuración de anuncios en pantalla nativos

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El tipo de anuncio se usa de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 15 segundos nativos&quot;).

**[!UICONTROL Native Creative]:** Una imagen de 1200 x 627 para maximizar el envío en el inventario móvil. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Un título llamativo para atraer visitantes.

**[!UICONTROL Description]:** El cuerpo del anuncio. La longitud máxima es de 100 caracteres.

**[!UICONTROL Landing Page]:** Dirección URL a la que llega el visor cuando hace clic en el anuncio.

**[!UICONTROL Final Landing Page]:** La variable [!UICONTROL Landing Page] Dirección URL con la [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Sponsored By (Advertiser Name)]:** El anunciante del anuncio.

**[!UICONTROL Call to Action]:** (Opcional) El paso que desea que realicen los espectadores una vez que vean este anuncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Un logotipo de relación 1:1 que se incluirá con el anuncio para obtener más reconocimiento de marca. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

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
>* [DSP Macros](/help/dsp/campaign-management/macros.md)

