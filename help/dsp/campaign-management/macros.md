---
title: Macros de Advertising Cloud DSP
description: Haga referencia a las macros disponibles para el seguimiento general y para rastrear los clics en anuncios en pantalla de terceros.
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: b3fc18cf84713adcff5a4208db537b03904cfa08
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Macros de Advertising Cloud DSP

Una macro es un comando corto o abreviatura para una instrucción y normalmente sigue el formato `${MACRO_NAME}`. Las macros incluidas en el código creativo o en las URL de pulsación se expanden en una cadena de código más larga que el servidor de publicidad pueda comprender. El servidor de publicidad de Advertising Cloud DSP ejecuta macros cuando se publica o se hace clic en el anuncio.

Las macros del servidor de publicidad son útiles para pasar información importante a DSP o a servidores de publicidad de terceros. Las macros se utilizan habitualmente durante el tráfico de metadatos o código creativo personalizado o de terceros (como píxeles de terceros).

Puede insertar manualmente una macro en cualquier lugar, como en una etiqueta VAST, en cualquier URL o en un DSP o en un píxel de evento de terceros. Sin embargo, cada cliente DSP y socio tiene un formato de etiqueta de publicidad diferente, y las macros deben insertarse en diferentes puntos de la etiqueta en consecuencia. Cada vez que trabaje con un cliente o socio nuevo, pídale documentación sobre dónde insertar las macros en sus etiquetas de publicidad que DSP los traficantes.

## Macros de seguimiento generales

Utilice macros de seguimiento generales en todos los tipos de anuncios y etiquetas para devolver datos específicos, según sea necesario.

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | El ID de cuenta. | integer |
| `${TM_AD_ID}` | La clave de anuncio (adKey). | string |
| `${TM_AD_ID_NUM}` | El ID de anuncio. | integer |
| `${TM_ADVERTISER_ID}` | El ID del anunciante. | integer |
| `${TM_CAMPAIGN_ID}` | La clave de campaña. | string |
| `${TM_CAMPAIGN_ID_NUM}` | El ID de campaña. | integer |
| ` ${TM_CLICK_URL}` | La dirección URL de redireccionamiento, que permite a los servidores de publicidad rastrear y contar clics de publicidad. Cuando se presenta la publicidad, si el usuario hace clic en ella, la macro se activa y el clic se registra y se cuenta para los informes. | string |
| ` ${TM_CLICK_URL_URLENC}` | La dirección URL de redireccionamiento codificada, que permite a los servidores de publicidad rastrear y contar clics de publicidad. Cuando se presenta la publicidad, si el usuario hace clic en ella, la macro se activa y el clic se registra y se cuenta para los informes. No utilice esta macro a menos que esté creando publicidades de terceros y que el proveedor requiera codificación de URL. | string |
| `${TM_FEED_ID}` | La clave para la colocación de contenido (feedKey). | string |
| `${TM_FEED_ID_NUM}` | ID de la ubicación del contenido. | integer |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | La clave del sitio para la ubicación. Requerido para [!DNL AppsFlyer] rastreadores de clics para anuncios de instalación de aplicaciones móviles.<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | La clave de colocación (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | El ID de colocación. | integer |
| `${TM_RANDOM}` | Cachebuster: un número aleatorio entre 1 y 100000. | long |
| `${TM_SESSION_ID}` | El ID de la sesión, que corresponde a una sola recuperación de la etiqueta de publicidad. | string |
| `${TM_SITE_DOMAIN_URLENC}` | El subdominio de página analizado desde la dirección URL en la solicitud de oferta; Con codificación de dirección URL. No es compatible con los anuncios en banners y clics para reproducir. | string |
| ` ${TM_SITE_NAME}` | El nombre del sitio para la ubicación. | string |
| `${TM_SITE_URL_URLENC}` | La URL pasada en la solicitud de oferta; Con codificación de dirección URL. No es compatible con los anuncios en banners y clics para reproducir. | string |
| `${TM_SITE_ID_NUM}` | ID del sitio para la ubicación. | integer |
| `${TM_TIMESTAMP}` | Marca de tiempo Unix que indica el número de segundos transcurridos desde la medianoche (00:00 UTC) el 1 de enero de 1970. | long |
| ` ${TM_VIDEO_DURATION}` | Duración del vídeo del anuncio en segundos. | integer |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros específicas del dispositivo móvil

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) El ID de plataforma, que corresponde al sistema operativo del dispositivo:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` cuando la plataforma no es ninguna de las anteriores</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) El nombre del modelo de dispositivo, con codificación URL. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) El entorno en el que se publicó el anuncio:<ul><li>`a` = aplicación móvil</li><li>`b` = sitio web móvil</li></ul> | cadena (`a` o `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) El ID de plataforma, que corresponde al sistema operativo del dispositivo:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` cuando la plataforma no es ninguna de las anteriores</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) El tipo de dispositivo en el que se vio el anuncio:<ul><li>`TAB` = tableta</li><li>`PHN` = mobile</li><li>`computer` = equipo</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Indica si el usuario ha excluido o no el seguimiento de anuncios:<ul><li>`1` (Indicador DNT = 1) = el usuario ha excluido el seguimiento de anuncios</li><li>`0` (Indicador DNT = 0) = el usuario ha elegido el seguimiento de anuncios</li></ul> | integer (`0` o `1`) |
| `${TM_BUNDLE}` | La variable [!DNL iOS] o [!DNL Android] ID del paquete de la tienda de aplicaciones. Ejemplos: com.zynga.www2.free o id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indica si el ofertante determina que la solicitud de oferta procede del origen de la Unión Europea y requiere la aplicación del RGPD:<ul><li>`1` = El RGPD debe aplicarse</li><li>`0` = El RGPD no debe aplicarse</li></ul>`gdpr_consent=${GDPR_CONSENT}` es el valor de consentimiento pasado del socio de suministro en la solicitud de oferta entrante:<ul><li>En la mayoría de los casos, se trata de una cadena de consentimiento con codificación base64url o daisybit (por ejemplo: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = sin consentimiento</li><li>`1` = consentimiento</li></ul> | daisybit o integer |

{style=&quot;table-layout:auto&quot;}

## Haga clic en Macros para anuncios en pantalla de terceros

Para rastrear con precisión los clics de los anuncios que utilizan etiquetas de visualización de terceros, DSP requiere una macro de clic en pantalla. Solo se requiere una versión de la macro; la macro correspondiente depende del tipo de etiqueta.

| Macro | Descripción de reemplazo | Tipo |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | Dirección URL de redireccionamiento que permite a los servidores de publicidad rastrear y contar los clics de publicidad en la plataforma. | string |
| `${TM_CLICK_URL_URLENC}` | Dirección URL de redireccionamiento que permite a los servidores de publicidad que requieren codificación de dirección URL rastrear y contar los clics de publicidad en la plataforma. | string |

{style=&quot;table-layout:auto&quot;}

DSP inserta automáticamente las macros de clics de visualización en una etiqueta de visualización de terceros al:

* Exportación de etiquetas de publicidad desde un socio de servidor de publicidad de Advertising Cloud <!-- [Needs PM confirmation.] -->
* Carga masiva [!DNL Flashtalking] o [!DNL Google DoubleClick for Advertisers] etiquetas de publicidad directamente en DSP

Si falta una macro de clic al crear un anuncio en pantalla, DSP muestra un mensaje de advertencia en el que se le pide que inserte manualmente la macro de clic en pantalla adecuada en el área correcta de la etiqueta.

## Solución de problemas con los errores de macro

Cuando agregue macros al código, asegúrese de utilizar la sintaxis exacta de la macro. Al validar las macros, DSP comprueba que la macro coincida exactamente con una de las macros válidas.

Los errores se generan si faltan caracteres desde el principio o el final del nombre de la macro. Por ejemplo, verá un mensaje de error si:

* Se olvidan uno o más de los caracteres al principio del nombre de la macro, como `${`. Si no se incluye la sintaxis completa, la entrada no se reconoce como una macro válida.
* La macro no termina con un conjunto válido de caracteres, como `}`.

>[!MORELIKETHIS]
>
>* [Configuración de anuncios de audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Configuración de anuncios de TV conectados](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Mostrar configuración de publicidad](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Configuración de publicidad móvil](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Configuración de anuncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Configuración de anuncio previo a la emisión](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Configuración de anuncios de vídeo universal](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

