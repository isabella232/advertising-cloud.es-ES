---
title: Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Flashtalking] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising Cloud] macros a su [!DNL Flashtalking] etiquetas de publicidad
feature: Integration with Adobe Analytics
source-git-commit: 915eea83b2dd246f0f512981efca7ac481cf0c6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Flashtalking] Etiquetas de publicidad

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Aplicable solo a Advertising Cloud DSP*

Si utiliza etiquetas de publicidad de [!DNL Flashtalking] para sus publicidades de Advertising Cloud DSP, añada parámetros de Analytics para Advertising Cloud a las URL de sus páginas de aterrizaje. Los parámetros permiten a Advertising Cloud enviar datos de clics sobre las publicidades a Adobe Analytics.

Usar macros para [!DNL Flashtalking] anuncios en pantalla y en vídeo para los siguientes tipos de [!DNL Analytics for Advertising Cloud] implementaciones:

* **Los anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Código JavaScript implementado en sus sitios web**: Debería ver algunos datos de pulsaciones en Adobe Analytics de las publicidades que compra a través de Advertising Cloud, sin macros adicionales. Sin embargo, para capturar datos de pulsaciones en exploradores que no admiten cookies de terceros y que, por lo tanto, no se captura a través del código JavaScript, agregue las macros de las secciones siguientes a [!DNL Flashtalking] etiquetas de publicidad.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solamente mientras las cookies siguen disponibles. Una vez que Advertising Cloud interrumpa las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilicen la variable [!DNL Analytics for Advertising Cloud] Código JavaScript y, en su lugar, confían en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualización): Las siguientes macros son necesarias para informar sobre la actividad de clics en el sitio impulsada por anuncios que compra a través de Advertising Cloud.

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


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
