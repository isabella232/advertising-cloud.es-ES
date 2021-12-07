---
title: Uso [!DNL Marketing Channels] con datos de Advertising Cloud
description: Obtenga información sobre cómo utilizar los datos de Advertising Cloud en [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Uso [!DNL Analytics Marketing Channels] con datos de Advertising Cloud

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Mediante el uso de Advertising Cloud y [!DNL Marketing Channels] , puede obtener información valiosa sobre cómo los medios digitales influyen en la actividad del sitio.

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

La siguiente ilustración muestra cómo Advertising Cloud y [!DNL Marketing Channels] realice un seguimiento de las visitas individuales que comprenden el recorrido de un visitante. Informes de Advertising Cloud en [!DNL Analytics] se limitan a la publicidad de búsqueda y visualización de pago que se transmite a través de Advertising Cloud, utilizando el ID de AMO. Sin embargo, [!DNL Marketing Channels] rastrea todos los canales configurados en la variable [!DNL Marketing Channels] Reglas de procesamiento.

![Cómo usar Advertising Cloud y [!DNL Marketing Channels] realizar un seguimiento de las visitas individuales en el recorrido de un visitante](/help/integrations/assets/a4adc-mc-sample-journey2.png)

En la primera visita, el usuario entró al sitio web a través de una campaña de correo electrónico, ejecutó diez vistas de página y luego se fue. En la segunda visita, el usuario entró al sitio mediante un anuncio en pantalla, ejecutó diez vistas de página y luego se marchó. En la tercera visita, el usuario ingresó al sitio a través de una búsqueda natural, ejecutó cinco vistas de página, ejecutó una conversión de 250 $ y la izquierda. Observe la diferencia en el seguimiento entre [!DNL Marketing Channels] y Advertising Cloud. El único canal que Advertising Cloud rastrea en este recorrido es [!UICONTROL Display]. Advertising Cloud realiza el seguimiento de [!UICONTROL Display] visita del canal y atribuye los datos de participación subsiguientes (como vistas de página) y las conversiones a la influencia de ese anuncio. [!DNL Marketing Channels], por otro lado, ofrece una vista completa de todos los canales.

Como el ID de AMO persiste a través del recorrido del visitante, puede utilizar los datos del ID de AMO para ver cómo Advertising Cloud influye en otros canales de marketing. ID de AMO [persiste durante 60 días de forma predeterminada](/help/integrations/analytics/overview.md), pero puede configurar la persistencia según sea necesario.

## Combinación de datos de canales de marketing y Advertising Cloud para analizar el rendimiento de los medios

Within [!DNL Analytics], puede combinar los datos de publicidad de pago persistentes de Advertising Cloud con el [!DNL Marketing Channels] datos completos de visitas para analizar mejor el rendimiento de los medios y así influir mejor en el recorrido del cliente.

El siguiente análisis utiliza los datos de Advertising Cloud para mostrar distintas versiones de cómo un anuncio en pantalla afecta a la conversión del sitio. Las tres columnas utilizan las mismas métricas de conversión, pero cada columna cuenta una historia diferente:

* La columna 1 observa los datos del ID de AMO que son persistentes en el recorrido del visitante. La columna 1 indica que 641 aplicaciones iniciadas estaban, en un momento dado, vinculadas a una publicidad de Advertising Cloud, ya sea a través de una visualización o un evento de pulsación. Esta vista no toma ninguna otra [!DNL Marketing Channels] atribución en consideración.

* En el [!DNL Marketing Channels] Sin embargo, el conjunto de datos 641 Aplicaciones iniciadas se atribuyen a otros canales de marketing. Las dos últimas columnas toman las 641 aplicaciones iniciadas y limitan los datos a la variable [!UICONTROL Display Click-Through] y [!UICONTROL Display View-Through] canales, que muestran las conversiones que se producen en un modelo de atribución de último contacto.

![ejemplo de cómo un anuncio en pantalla afecta a la conversión del sitio](/help/integrations/assets/a4adc-mc-display-impact.png)

Puede llevar este análisis un paso más allá. Puede desglosar aún más la fila de Advertising Cloud por canal de marketing para ver dónde se atribuyen las conversiones de Advertising Cloud al inicio de 641 aplicaciones. Ya sabe que cinco de esas conversiones se atribuyen a una pulsación en pantalla de último contacto y 19 a una visualización de último contacto. Esto sigue dejando 617 aplicaciones iniciadas atribuidas a otros canales de marketing. Puede arrastrar y soltar la dimensión Canal de último contacto en la parte superior del elemento de línea Advertising Cloud DSP para mostrar la atribución de canal para el resto de las aplicaciones iniciadas y mostrar el impacto multicanal del canal de visualización.

![cómo añadir la dimensión Canal de último contacto](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Ahora puede ver cómo se atribuyen los demás inicios de aplicaciones. El correo electrónico recibe crédito por 357 inicios de aplicaciones de último contacto para las que persistió un ID de AMO. Con este tipo de análisis, puede ver el impacto que tuvieron los anuncios en pantalla de Advertising Cloud en todos los canales. Con un solo conjunto de datos y modelo de atribución, este tipo de perspectiva no estaría disponible.

![ejemplo del impacto multicanal de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Puede mejorar aún más el análisis mediante un gráfico de pila configurado en &quot;Apilado al 100 %&quot; para mostrar los datos de tendencias a lo largo del tiempo. Esta visualización facilita el seguimiento de los canales de marketing de último contacto más afectados por las campañas de marketing de visualización.

![ejemplo del impacto multicanal de tendencias de los canales de visualización](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de Advertising Cloud ID para crear [!DNL Marketing Channels] Reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vídeo: Creación de informes con Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

