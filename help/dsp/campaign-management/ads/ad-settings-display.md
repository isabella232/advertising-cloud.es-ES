---
title: Mostrar configuración de publicidad
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios en pantalla.
feature: Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Mostrar configuración de publicidad

Los siguientes ajustes son para anuncios en pantalla estándar. También puede ofrecer anuncios de vídeo de clic para reproducir para mostrar, pero no se recomienda hacerlo, ya que no hay muchos editores que los admitan.

## [!UICONTROL Ad Options]

### Básico

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad. Su valor predeterminado es *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El título del recurso se utiliza de forma predeterminada, pero puede cambiarlo.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 300x250 Gamer&quot;).

**\[Fuente de publicidad\]**: Si Advertising Cloud DSP está sirviendo el anuncio (*[!UICONTROL Adobe served]*) o está utilizando un servidor de publicidad de terceros (*[!UICONTROL 3rd party]*).

**[!UICONTROL This is an expandable Banner]:** (Solo anuncios de terceros) Indica que la publicidad es un anuncio tipo titular ampliable. La configuración de expansión relacionada determina qué inventario comprar, por lo que asegúrese de que refleja el comportamiento de la publicidad.

**[!UICONTROL Expansion Method]:** (Solo anuncios de banner ampliables de terceros) Indica si el banner se expande sobre  *[!UICONTROL Click]* o  *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:**  (Solo anuncios de banner ampliables de terceros) Dirección en la que se expande el anuncio:  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]* o  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:**  (Solo anuncios de banners ampliables de terceros) El proveedor certificado para el que está disponible la publicidad:  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]* o  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:**  (Solo anuncios de terceros) La URL del recurso creativo de terceros. Cualquier parámetro [timestamp] y [[timestamp]] se reemplazará por valores reales.

**[!UICONTROL Final Display Code]:** (Solo anuncios de terceros) La URL del recurso creativo de terceros, con el seguimiento de  [Advertising Cloud DSP necesario ](/help/dsp/campaign-management/macros.md) macronizado, si corresponde.

**[!UICONTROL Creative type]:**  (Solo anuncios de Adobe) Si el recurso es un  *[!UICONTROL Image]* recurso o un  *[!UICONTROL HTML5]* recurso.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:**  (solo anuncios publicados en Adobe) Archivo de imagen o recurso HTML5 comprimido que se va a cargar, según el tipo de creativo. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]** o **[!UICONTROL Upload Image]**.

**[!UICONTROL Ad Size]:** Ancho y alto del anuncio. Debe ser un [tamaño de anuncio estándar admitido](/help/dsp/assets/ad-specs.pdf). Puede introducir manualmente el tamaño de la publicidad antes de cargarla o introducir un [!UICONTROL Display Code]. Si no introduce el tamaño de la publicidad, las dimensiones de la publicidad cargada o de la etiqueta de publicidad se introducen automáticamente como de solo lectura. Tenga en cuenta que la publicidad de visualización no se guardará si las dimensiones no se encuentran dentro de la visualización estándar como tamaños (por ejemplo, 301x250 en lugar del tamaño de la publicidad de 300x250).

>[!IMPORTANT]
>
> El tamaño de anuncio declarado en los campos de ancho y alto coincidirá con las solicitudes de oferta entrantes. Puede experimentar problemas de envío si las dimensiones de la publicidad no coinciden con el tamaño de la publicidad declarado.

**[!UICONTROL Click URL]:**  (Solo anuncios servidos por Adobe) Dirección URL a la que llegará el espectador cuando haga clic en el anuncio.

**[!UICONTROL Final Click URL]:**  (solo anuncios de Adobe; solo lectura)  [!UICONTROL Click URL] con el seguimiento necesario de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) macrosserted, si corresponde.

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
>* [Enumerar las ubicaciones asociadas a una publicidad](ad-list-placements.md)
>* [Tipos de anuncios disponibles](ad-types.md)
>* [Especificaciones de la publicidad](/help/dsp/assets/ad-specs.pdf)
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

