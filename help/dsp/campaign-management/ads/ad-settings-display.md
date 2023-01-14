---
title: Mostrar configuración de publicidad
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios en pantalla.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Mostrar configuración de publicidad

Los siguientes ajustes son para anuncios en pantalla estándar.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:** (Solo lectura) El tipo de anuncio que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad. Su valor predeterminado es *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la variable [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 300x250 Gamer&quot;).

**\[Fuente de publicidad\]**: (Solo lectura) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Solo anuncios de terceros) Indica que la publicidad es un anuncio tipo titular ampliable. La configuración de expansión relacionada determina qué inventario comprar, por lo que asegúrese de que refleja el comportamiento de la publicidad.

**[!UICONTROL Expansion Method]:** (Solo anuncios de banners ampliables de terceros) Si el banner se amplía *[!UICONTROL Click]* o *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Solo anuncios de banners ampliables de terceros) La dirección en la que se expande el anuncio: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* o *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Solo anuncios de banners ampliables de terceros) El proveedor certificado para el que está disponible la publicidad: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* o *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros. Cualquiera [timestamp] y [[timestamp]] se reemplazarán por valores reales.

**[!UICONTROL Final Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros, con los [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) insertado, si procede.

**[!UICONTROL Ad Size]:** Anchura y altura del anuncio. Debe ser [tamaño de anuncio estándar admitido](ad-specs.md). Puede introducir manualmente el tamaño de la publicidad antes de cargar la publicidad o introducir una [!UICONTROL Display Code]. Si no introduce el tamaño de la publicidad, las dimensiones de la publicidad cargada o de la etiqueta de publicidad se introducen automáticamente como de solo lectura. Tenga en cuenta que la publicidad de visualización no se guardará si las dimensiones no se encuentran dentro de la visualización estándar como tamaños (por ejemplo, 301x250 en lugar del tamaño de la publicidad de 300x250).

>[!IMPORTANT]
>
> El tamaño de anuncio declarado en los campos de ancho y alto coincidirá con las solicitudes de oferta entrantes. Puede experimentar problemas de envío si las dimensiones de la publicidad no coinciden con el tamaño de la publicidad declarado.

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
>* [Enumerar las ubicaciones asociadas a una publicidad](ad-list-placements.md)
>* [Especificaciones de la publicidad](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)

