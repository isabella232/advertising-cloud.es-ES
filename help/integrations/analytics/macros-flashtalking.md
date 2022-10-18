---
title: Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Flashtalking] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising Cloud] macros a su [!DNL Flashtalking] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: 7cb39998041d151ece7809adc8a2e872b922e5fc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Flashtalking] Etiquetas de publicidad

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Aplicable solo a Advertising Cloud DSP*

Si utiliza etiquetas de publicidad de [!DNL Flashtalking] para sus publicidades de Advertising Cloud DSP, añada parámetros de Analytics para Advertising Cloud a las URL de sus páginas de aterrizaje. El registro de parámetros `s_kwcid` y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite a Advertising Cloud enviar datos de clics sobre los anuncios a Adobe Analytics.

Usar macros para [!DNL Flashtalking] anuncios en pantalla y en vídeo para los siguientes tipos de [!DNL Analytics for Advertising Cloud] implementaciones:

* **Los anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Código JavaScript implementado en sus sitios web**: El código JavaScript ya registra la variable `s_kwcid` y `ef_id` parámetros de cadena de consulta. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es agregar las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de pulsaciones adicionales que no se capturan a través del código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solamente mientras las cookies siguen disponibles. Una vez que se interrumpan las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilicen la variable [!DNL Analytics for Advertising Cloud] Código JavaScript y, en su lugar, confían en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualización): Las siguientes macros son necesarias para informar sobre la actividad de clics en el sitio impulsada por los anuncios que compra a través de Advertising Cloud.

## Mostrar etiquetas de publicidad

Dentro de [!DNL Flashtalking] configuración de la etiqueta de publicidad, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[ftqs:[AdobeAMO]]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![Ejemplo de [!DNL Flashtalking] configuración de etiquetas de anuncio](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Etiquetas de anuncios de vídeo

Dentro de [!DNL Flashtalking] configuración de la etiqueta de publicidad, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![Ejemplo de [!DNL Flashtalking] configuración de etiquetas de anuncio](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID que utiliza [!DNL Analytics]](/help/integrations/analytics/ids.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
