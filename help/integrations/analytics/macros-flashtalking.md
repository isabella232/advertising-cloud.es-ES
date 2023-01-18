---
title: Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising] macros a su [!DNL Flashtalking] etiquetas de publicidad
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad

*Anunciantes con Adobe de solo integración de Advertising-Adobe Analytics*

*Aplicable únicamente a los DSP publicitarios*

Si utiliza etiquetas de publicidad de [!DNL Flashtalking] para los anuncios de DSP, añada parámetros de Analytics para publicidad a las direcciones URL de las páginas de aterrizaje. El registro de parámetros `s_kwcid` y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite que Adobe Advertising envíe datos de clics sobre los anuncios a Adobe Analytics.

Usar macros para [!DNL Flashtalking] anuncios en pantalla y en vídeo para los siguientes tipos de [!DNL Analytics for Advertising] implementaciones:

* **Los anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising] Código JavaScript implementado en sus sitios web**: El código JavaScript ya registra la variable `s_kwcid` y `ef_id` parámetros de cadena de consulta. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es agregar las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de pulsaciones adicionales que no se capturan a través del código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solamente mientras las cookies siguen disponibles. Una vez que se interrumpan las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilicen la variable [!DNL Analytics for Advertising] Código JavaScript y, en su lugar, confían en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualización): Las siguientes macros son necesarias para informar sobre la actividad de clics en el sitio impulsada por los anuncios que compra a través de la publicidad de Adobe.

## Mostrar etiquetas de publicidad

Dentro de [!DNL Flashtalking] configuración de la etiqueta de publicidad, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[ftqs:[AdobeAMO]]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Etiquetas de anuncios de vídeo

Dentro de [!DNL Flashtalking] configuración de la etiqueta de publicidad, anexe la siguiente macro al final de la URL de pulsación en la `Clicktag` campo:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Ejemplo:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [ID de publicidad de Adobe utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

