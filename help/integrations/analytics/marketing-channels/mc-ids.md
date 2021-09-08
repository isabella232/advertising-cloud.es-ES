---
title: 'Uso de Advertising Cloud ID para crear reglas [!DNL Marketing Channels] '
description: Aprenda a utilizar Advertising Cloud ID para crear reglas de procesamiento para [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Uso de Advertising Cloud ID para crear [!DNL Marketing Channels] reglas de procesamiento

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Puede utilizar Advertising Cloud ID ([AMO ID y EF ID](../ids.md)) para configurar las reglas de procesamiento en Adobe Analytics. [!DNL Marketing Channels] Use Advertising Cloud ID para reglas específicas de sus campañas de Advertising Cloud.

## El ID de AMO en las reglas de procesamiento

El ID de AMO es el código de seguimiento principal que se utiliza para informar de los datos de Advertising Cloud en [!DNL Analytics]. El ID de AMO es una concatenación de valores dinámicos administrados por Adobe para proporcionar informes granulares en [!DNL Analytics]. Se almacena en una dimensión [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (ID de AMO). El ID de AMO se puede establecer en [!DNL Analytics] de dos maneras:

* Seguimiento de pulsaciones: Advertising Cloud establece el parámetro de cadena de consulta `s_kwcid` en un vínculo y [!DNL Analytics] recoge el parámetro de la dirección URL de la página de aterrizaje cuando se produce una pulsación.
* Seguimiento de visualizaciones ([!DNL DSP] solamente): El servicio Último evento detecta una visualización en el servidor y envía el ID de AMO a [!DNL Analytics]. En este caso, la dirección URL no contiene un parámetro `s_kwcid`.

Los valores dinámicos dentro de ID de AMO indican el canal de marketing del que se realizó un seguimiento:

* El prefijo del ID de AMO se puede usar para identificar el canal de nivel superior dentro de [!DNL Marketing Channels].

* Las frases en caracteres del cuerpo del ID de AMO indican un tipo de campaña más específico.

* El sufijo &quot;vt&quot; está presente para el tráfico de visualización [!DNL DSP] y se puede utilizar para crear canales de pulsaciones y visualizaciones independientes [!DNL DSP].

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

La regla de procesamiento [!DNL Marketing Channels] para el canal [!UICONTROL Paid Search] puede tener este aspecto:

![Ejemplo de  [!UICONTROL Paid Search] regla](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La regla de procesamiento [!DNL Marketing Channels] para el canal [!UICONTROL YouTube Video Ads] puede tener este aspecto:

![Ejemplo de  [!UICONTROL YouTube Video Ads] regla](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Asegúrese de ejecutar las reglas en orden de especificidad. Si las dos reglas anteriores se ejecutan en orden, el tráfico de anuncios de vídeo [!DNL YouTube] caería en el canal [!UICONTROL Paid Search] porque el ID de AMO empezaría por &quot;AL!&quot; y contiene &quot;!ytv!&quot;.

## El ID de EF en las reglas de procesamiento

El AMO EF ID (EF ID) es el segundo código de seguimiento utilizado en la integración [!DNL Analytics for Advertising Cloud]. Su principal propósito es rastrear y pasar [!DNL Analytics] datos de evento a Advertising Cloud. Cada vez que se produce una pulsación o una visualización, se genera un ID de EF único, aunque sea exactamente el mismo anuncio para el mismo visitante. El ID de EF no se utiliza en la interfaz de usuario de informes [!DNL Analytics] porque suele superar los 500.000 valores únicos por límite de variables en [!DNL Analytics], por lo que no se puede utilizar para los informes. Las métricas y los metadatos de Advertising Cloud no se aplican al ID de EF; solo se aplican al ID de AMO. La granularidad añadida del seguimiento es necesaria para la optimización de la campaña en Advertising Cloud, por lo que se necesitan ambos ID.

Aunque la dimensión de ID de EF no se utiliza directamente en los informes [!DNL Analytics] , el ID de EF puede resultar útil para crear canales de marketing. El sufijo de ID de EF indica el canal (visualización o búsqueda) y si la visita fue impulsada por una pulsación o una visualización. El delimitador en el ID de EF es dos puntos, no el signo de exclamación en el ID de AMO.

| Sufijo de ID de EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Ejemplos de reglas de procesamiento que utilizan el ID de EF

#### Mostrar regla de pulsaciones

Cree un canal de marketing de visualización de pulsaciones capturando solo pulsaciones. Dado que el ID de AMO es el mismo tanto para clics como para visualizaciones, esta regla utiliza la variable de ID de EF y el parámetro de cadena de consulta `ef_id`.

A veces, las pulsaciones se rastrean a través de la dirección URL (la opción predeterminada). En otros casos, el seguimiento de las pulsaciones se realiza a través del servicio Último evento del lado del servidor y, por lo tanto, la dirección URL no contiene el parámetro `ef_id`. Por lo tanto, la regla comprueba las condiciones en las que la variable de ID de EF o el parámetro de cadena de consulta `ef_id` terminan con &quot;:d&quot;. Utilice el operador &quot;`Any`&quot; porque desea que esta regla se active para cualquiera de las condiciones.

![Ejemplo de regla de pulsación de visualización](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Mostrar regla de visualización

Para crear un canal de visualización de visualización, cree una regla en la que el ID de EF termine con &quot;:i&quot;. Dado que el visitante no hizo clic en la publicidad, el seguimiento de visualización no incluye los valores `ef_id` o `s_kwcid` en la dirección URL. Por lo tanto, solo se necesita una condición.

![Ejemplo de regla de visualización](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Uso de datos de Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Creación de informes con Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud ID que utiliza [!DNL Analytics]](/help/integrations/analytics/ids.md)

