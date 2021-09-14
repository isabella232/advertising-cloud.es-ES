---
title: Macros de Advertising Cloud DSP
description: Haga referencia a las macros disponibles para el seguimiento general y para rastrear los clics en anuncios en pantalla de terceros.
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: e0166dbad4fec41fdc64a65cb3a8ac97496c681f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Macros de Advertising Cloud DSP

Una macro es un comando corto o una taquigrafía para una instrucción y generalmente sigue el formato `${MACRO_NAME}`. El servidor de publicidad de Advertising Cloud DSP ejecuta macros cuando se publica o se hace clic en el anuncio.

Las macros se utilizan habitualmente durante el tráfico de metadatos o código creativo personalizado o de terceros (como píxeles de terceros).

## Macros de seguimiento generales

Utilice macros de seguimiento generales en todos los tipos de anuncios y etiquetas para devolver datos específicos, según sea necesario.

| Macro | Descripción |
| --------------- | ---------------------- |
| `${USER_ID}` | Identificador de usuario para todos los tipos de dispositivos. |
| `${TM_RANDOM}` | Cachebuster: un número aleatorio comprendido entre 1 y 100000 |
| `${TM_PLACEMENT_ID_NUM}` | El ID de ubicación |
| `${TM_SITE_URL_URLENC}` | La URL pasada en la solicitud de oferta; URL codificada |
| `${TM_SITE_DOMAIN_URLENC}` | El subdominio de página analizado desde la dirección URL en la solicitud de oferta; URL codificada |

{style=&quot;table-layout:auto&quot;}

## Haga clic en Macros para anuncios en pantalla de terceros

Para rastrear con precisión los clics de los anuncios que utilizan etiquetas de visualización de terceros, DSP requiere una macro de clic en pantalla. Solo se requiere una versión de la macro; la macro correspondiente depende del tipo de etiqueta.

| Macro | Descripción |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | Dirección URL de redireccionamiento que permite a los servidores de publicidad rastrear y contar los clics de publicidad en la plataforma |
| `${TM_CLICK_URL_URLENC}` | Dirección URL de redireccionamiento que permite a los servidores de publicidad que requieren codificación de dirección URL rastrear y contar los clics de publicidad en la plataforma |

{style=&quot;table-layout:auto&quot;}

DSP inserta automáticamente las macros de clic en pantalla en una etiqueta de visualización cuando:

* Exportar etiquetas de publicidad de un socio de servidor de publicidad de Advertising Cloud <!-- [Needs PM confirmation.] -->
* Etiquetas de anuncios de carga masiva [!DNL Flashtalking] o [!DNL Google DoubleClick for Advertisers] directamente en DSP

Si falta una macro de clic al crear un anuncio en pantalla, DSP muestra un mensaje de advertencia en el que se le pide que inserte manualmente la macro de clic en pantalla adecuada en el área correcta de la etiqueta.

>[!MORELIKETHIS]
>
>* [Configuración de anuncios de audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configuración de anuncios de TV conectados](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Mostrar configuración de publicidad](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configuración de publicidad móvil](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configuración de anuncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configuración de anuncio previo a la emisión](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

