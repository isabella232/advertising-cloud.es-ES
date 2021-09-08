---
title: Configuración de anuncios nativos
description: Consulte las descripciones de la configuración de publicidad disponible para los anuncios nativos.
feature: Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Configuración de anuncios nativos

## [!UICONTROL Upload or Select Creative]

*Solo anuncios en vídeo nuevos (pero no en pantalla)*

**[!UICONTROL Upload Audio]:** Para cargar un recurso sin procesar en DSP. Cuando seleccione esta opción, haga lo siguiente:

1. Haga clic en **[!UICONTROL Choose File]** y busque el archivo en su dispositivo o red.
1. Introduzca un título para el archivo, que se utilizará en la vista [!UICONTROL Ads] y en los informes.
1. Haga clic **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** Para seleccionar cualquier creativo cargado anteriormente con el formato correcto dentro de la cuenta.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Solo lectura) El tipo de publicidad que está creando, que corresponde al tipo de ubicación al que se puede adjuntar la publicidad.

**[!UICONTROL Ad Name]:** El nombre del anuncio. El tipo de anuncio (mostrar nativo) o el título del vídeo (formatos de vídeo) se usan de forma predeterminada, pero puede cambiar el nombre.

>[!TIP]
>
> Utilice un nombre que sea fácil de encontrar cuando adjunte la publicidad a una ubicación, en la vista [!UICONTROL Ads] y en los informes. Por ejemplo, describa el tipo de unidad y algunos atributos clave (como Vista previa de productos de vacaciones: 15 segundos nativos&quot;).

**[!UICONTROL Native Creative]:** Una imagen de 1200 x 627 para maximizar el envío en el inventario móvil. En el caso de los anuncios de vídeo, esta será la imagen que se mostrará antes de que se reproduzca el vídeo nativo. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Un título llamativo que atraerá a los espectadores.

**[!UICONTROL Description]:** Para los anuncios en vídeo, este es un breve resumen del anuncio. En el caso de los anuncios en pantalla, este es el cuerpo de la publicidad. La longitud máxima es de 100 caracteres.

**[!UICONTROL Landing Page]:** Dirección URL a la que llegará el espectador cuando haga clic en el anuncio.

**[!UICONTROL Final Landing Page]:** La  [!UICONTROL Landing Page] dirección URL con el seguimiento de  [Advertising Cloud DSP ](/help/dsp/campaign-management/macros.md) necesario macronivdado, si corresponde.

**[!UICONTROL Sponsored By (Advertiser Name)]:** El anunciante del anuncio.

**[!UICONTROL Call to Action]:**  (Opcional) El paso que desea que realicen los espectadores una vez que vean este anuncio.

**[!UICONTROL Advertiser Logo]:** (Opcional) Un logotipo de proporción 1:1 que se incluirá en la publicidad para obtener más reconocimiento de marca. Haga clic en **[!UICONTROL Browse]** y busque el archivo en su dispositivo o red y, a continuación, haga clic en **[!UICONTROL Upload]**.

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
>* [Macros de Advertising Cloud DSP](/help/dsp/campaign-management/macros.md)

