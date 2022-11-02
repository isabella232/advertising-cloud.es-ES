---
title: Uso de Advertising Cloud ID para crear [!DNL Marketing Channels] Reglas
description: Obtenga información sobre cómo utilizar Advertising Cloud ID para crear reglas de procesamiento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: d136b1fe6f6fd3861d0850e07efe7c320da4a7cc
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Uso de Advertising Cloud ID para crear [!DNL Marketing Channels] Reglas de procesamiento

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Puede usar Advertising Cloud ID ([ID de AMO e ID de EF](../ids.md)) para configurar [!DNL Marketing Channels] reglas de procesamiento en Adobe Analytics. Use Advertising Cloud ID para reglas específicas de sus campañas de Advertising Cloud.

## El ID de AMO en las reglas de procesamiento

El ID de AMO es el código de seguimiento principal que se utiliza para informar de los datos de Advertising Cloud en [!DNL Analytics]. El ID de AMO es una concatenación de valores dinámicos administrados por Adobe para proporcionar informes granulares dentro de [!DNL Analytics]. Se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensión rVar (AMO ID). El ID de AMO se puede establecer en [!DNL Analytics] de dos maneras:

* Seguimiento de pulsaciones: Advertising Cloud establece la variable `s_kwcid` parámetro de cadena de consulta en un vínculo, y [!DNL Analytics] recoge el parámetro de la dirección URL de la página de aterrizaje cuando se produce una pulsación.
* Seguimiento de visualizaciones ([!DNL DSP] Solo): El servicio Último evento detecta una visualización en el servidor y envía el ID de AMO a [!DNL Analytics]. En este caso, la dirección URL no contiene un `s_kwcid` parámetro.

Los valores dinámicos dentro de ID de AMO indican el canal de marketing del que se realizó un seguimiento:

* El prefijo del ID de AMO se puede usar para identificar el canal de nivel superior dentro de [!DNL Marketing Channels].

* Las frases en caracteres del cuerpo del ID de AMO indican un tipo de campaña más específico.

* El sufijo &quot;vt&quot; está presente para [!DNL DSP] tráfico de visualización y se puede utilizar para crear clics y visualizaciones independientes [!DNL DSP] canales.

Se puede ignorar el resto del ID de AMO.

| AMO ID | Canal | Lógica de regla |
|--------|---------|--------------------|
| ¡AL! (prefijo) | [!UICONTROL Paid Search] | Comienza con |
| ¡AC! (prefijo) | [!UICONTROL DSP] | Comienza con |
| !g! (cuerpo) | [!UICONTROL Google Search] | Contiene |
| !s! (cuerpo) | [!UICONTROL Search Partner] | Contiene |
| !d! (cuerpo) | [!UICONTROL Display Network] | Contiene |
| !u! (cuerpo) | [!UICONTROL Smart Shopping Campaign] | Contiene |
| !ytv! (cuerpo) | [!UICONTROL YouTube Video Ad] | Contiene |
| !yts! (cuerpo) | [!UICONTROL YouTube Search Ad] | Contiene |
| !vp! (cuerpo) | [!UICONTROL Google Video Partners] | Contiene |
| !vt (sufijo) | [!UICONTROL DSP View-through] | Finaliza con |

### Ejemplos de reglas de procesamiento que utilizan el ID de AMO

La variable [!DNL Marketing Channels] regla de procesamiento para la variable [!UICONTROL Paid Search] el canal puede tener este aspecto:

![Ejemplo de [!UICONTROL Paid Search] regla](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La variable [!DNL Marketing Channels] regla de procesamiento para la variable [!UICONTROL YouTube Video Ads] el canal puede tener este aspecto:

![Ejemplo de [!UICONTROL YouTube Video Ads] regla](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Asegúrese de ejecutar las reglas en orden de especificidad. Si las dos reglas anteriores se ejecutan en orden, la variable [!DNL YouTube] el tráfico de anuncios de vídeo caería dentro de la categoría [!UICONTROL Paid Search] canal porque el ID de AMO empezaría por &quot;AL!&quot; y contiene &quot;!ytv!&quot;.

## El ID de EF en las reglas de procesamiento

El AMO EF ID (EF ID) es el segundo código de seguimiento utilizado en la variable [!DNL Analytics for Advertising Cloud] integración. Su principal propósito es rastrear y pasar [!DNL Analytics] datos de evento en Advertising Cloud. Cada vez que se produce una pulsación o una visualización, se genera un ID de EF único, aunque sea exactamente el mismo anuncio para el mismo visitante. El ID de EF no se usa en la variable [!DNL Analytics] interfaz de usuario de informes porque suele superar los 500 000 valores únicos por límite de variables en [!DNL Analytics], lo que hace que no se pueda utilizar para la creación de informes. Las métricas y los metadatos de Advertising Cloud no se aplican al ID de EF; solo se aplican al ID de AMO. La granularidad añadida del seguimiento es necesaria para la optimización de la campaña en Advertising Cloud, por lo que se necesitan ambos ID.

Aunque la dimensión de ID de EF no se utiliza directamente en [!DNL Analytics] informe, el ID de EF puede resultar útil para crear canales de marketing. El sufijo de ID de EF indica el canal (visualización o búsqueda) y si la visita fue impulsada por una pulsación o una visualización. El delimitador en el ID de EF es dos puntos, no el signo de exclamación en el ID de AMO.

| Sufijo de ID de EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Ejemplos de reglas de procesamiento que utilizan el ID de EF

#### Mostrar regla de pulsaciones

Cree un canal de marketing de visualización de pulsaciones capturando solo pulsaciones. Dado que el ID de AMO es el mismo tanto para clics como para visualizaciones, esta regla utiliza la variable de ID de EF y la variable `ef_id` parámetro de cadena de consulta.

A veces, las pulsaciones se rastrean a través de la dirección URL (la opción predeterminada). En otros casos, el seguimiento de las pulsaciones se realiza a través del servicio Último evento del lado del servidor y, por lo tanto, la dirección URL no contiene la variable `ef_id` parámetro. Por lo tanto, la regla comprueba las condiciones en las que la variable de ID de EF o la variable `ef_id` el parámetro de cadena de consulta termina con &quot;:d&quot;. Utilice el`Any`&quot; porque desea que esta regla se active para cualquiera de las condiciones.

![Ejemplo de regla de pulsación de visualización](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Mostrar regla de visualización

Para crear un canal de visualización de visualización, cree una regla en la que el ID de EF termine con &quot;:i&quot;. Como el visitante no hizo clic en la publicidad, el seguimiento de visualizaciones no incluye la variable `ef_id` o `s_kwcid` en la dirección URL, por lo que la regla solo requiere una condición.

![Ejemplo de regla de visualización](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Uso [!DNL Analytics Marketing Channels] con datos de Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Creación de informes con Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID que utiliza [!DNL Analytics]](/help/integrations/analytics/ids.md)

