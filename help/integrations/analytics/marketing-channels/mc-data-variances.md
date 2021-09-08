---
title: Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]
description: Descubra por qué los datos de canal rastreados por el ID de AMO pueden variar de los datos de canal rastreados por [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Una pregunta común de los usuarios que aprenden sobre la integración de los conjuntos de datos de Advertising Cloud y [!DNL Marketing Channels] es &quot;¿Qué causa la variación en los datos entre el ID de AMO y [!DNL Marketing Channels]?&quot; O, a veces, &quot;¿Por qué se rompen los datos? Necesito que todas las métricas coincidan en los informes&quot;. Afortunadamente, las discrepancias no indican que los datos estén &quot;rotos&quot;, y se esperan discrepancias e incluso se desean. Veamos por qué la integración se diseñó de esta manera.

Los dos conjuntos de datos tienen diferentes casos de uso principales:

* [!DNL Marketing Channels]: El caso de uso principal de  [!DNL Marketing Channels] es comparar los datos de varios canales con un modelo de atribución común. Los analistas pueden utilizar la dimensión [!UICONTROL Marketing Channel] para obtener una mayor información sobre cómo los canales interactúan entre sí. Esta perspectiva puede ayudar a impulsar las decisiones de macronivel sobre cómo invertir en cada canal y puede generar perspectivas sobre cómo los visitantes de cada canal interactúan con el sitio web.

   Por lo tanto, la dimensión [!DNL Analytics] [!UICONTROL Marketing Channel] está configurada para capturar y rastrear todos los canales. [!DNL Marketing Channels] también se puede configurar para capturar visualizaciones y pulsaciones de Advertising Cloud DSP, y lo hace en relación con los demás canales de marketing.

* Advertising Cloud AMO ID: El caso de uso principal de los datos de ID de AMO de Advertising Cloud es el de alimentar los algoritmos avanzados de ofertas con tecnología [!DNL Adobe Sensei] de Advertising Cloud. Los algoritmos toman automáticamente miles de decisiones de oferta de micronivel diarias para maximizar el gasto publicitario y lograr los objetivos de la [!DNL DSP] campaña o del portafolio [!DNL Search]. Cuantos más datos de conversión puedan conectar los algoritmos con las campañas, mejor podrán tomar estas decisiones de oferta.

   Para recopilar estos datos, la integración [!DNL Analytics for Advertising Cloud] pasa los ID de AMO sin procesar que pueden traducirse como códigos de seguimiento de pulsaciones y visualizaciones en la dimensión de AMO ID de Adobe Analytics, que se almacena como variable personalizada (eVar) o como variable reservada (rVar). Las pulsaciones para otros canales no están configuradas en la dimensión de ID de AMO, por lo que la dimensión de ID de AMO no puede rastrear la entrada desde estos otros canales. El resultado es que el ID de AMO persiste a través de [!DNL Marketing Channes]l puntos de entrada.

Para obtener más información sobre posibles variaciones de datos entre los datos rastreados por Advertising Cloud y los datos [!DNL Analytics] rastreados, consulte &quot;[Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Variaciones de datos previstas  [!DNL Analytics] entre Advertising Cloud y](/help/integrations/analytics/data-variances.md)
>* [Aspectos básicos de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Uso de Advertising Cloud ID para  [!DNL Marketing Channels] crear reglas de procesamiento](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Uso de datos de Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Creación de informes con Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

