---
title: Aspectos básicos de [!DNL Marketing Channels]
description: Información clave sobre [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] Los usuarios deben comprender.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Aspectos básicos de [!DNL Analytics Marketing Channels]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Esta página explica información clave sobre [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] Los usuarios deben comprender.

Para obtener documentación completa, consulte [!DNL Marketing Channels], consulte &quot;[Introducción con [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Información general sobre [!DNL Marketing Channels]

[!DNL Marketing Channels] son una función clave de Adobe Analytics. [!DNL Marketing Channels] los informes muestran cómo llegan los clientes al sitio web a través de la ventana de informes y cómo cada canal afecta a los ingresos o al comportamiento en el sitio.

Consideremos el siguiente ejemplo de recorrido entre visitas. Cada visita al sitio web se indica mediante el canal de marketing desde el que entró el visitante. La primera visita, también denominada Canal de primer toque, es Correo electrónico. La visualización en la visita dos es un canal participante y la búsqueda natural se considera el Canal de último toque. Si usa [!UICONTROL Last Touch Attribution] en [!UICONTROL Attribution IQ], la búsqueda natural recibiría el crédito completo por el evento de conversión de 250 dólares. Con el servicio de ID de Experience Cloud, puede unir estas visitas individuales para mostrar un recorrido por cada visitante.

![Ejemplo de recorrido de conversión entre visitas en los canales de marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

Usando [!UICONTROL Marketing Channels] Reglas de procesamiento, puede crear conjuntos de lógica para determinar los canales que dirigen el tráfico y para rastrear cada canal a medida que los usuarios llegan al sitio. Por ejemplo, la variable [!UICONTROL Email] canal se indicaría con un código de seguimiento único generado al hacer clic en el que, cuando Adobe Analytics lo registrara, clasificaría la visita como originaria de una campaña de marketing por correo electrónico.

## Reglas de procesamiento y configuración de los canales de marketing

Cada vez que un usuario llega a un sitio web, lo hace mediante una dirección URL en la que hizo clic o escribió directamente en la barra de direcciones. Cuando el usuario entra en el sitio web, [!DNL Analytics] rastrea la información que se puede utilizar para determinar el canal que condujo la visita.

A menudo, los especialistas en marketing añaden códigos de seguimiento de parámetros de cadena de consulta a las direcciones URL de canal para ayudar a realizar un seguimiento del impacto del canal en su sitio. Puede configurar [!DNL Marketing Channels] reglas de procesamiento para detectar parámetros y valores de seguimiento específicos y determinar el canal sin ningún seguimiento adicional. Por ejemplo, si todas las direcciones URL de campaña de correo electrónico siguen el formato `www.adobe.com?cid=email…` (donde la dirección URL contiene el parámetro y valor de la cadena de consulta `cid=email`), puede crear una regla para escuchar este código de seguimiento y agrupar la visita en la variable [!UICONTROL Email] canal.

Otros canales no tienen rutas URL rastreables y necesitan lógica adicional para la identificación. Por ejemplo, [!UICONTROL Earned Social], en el que un usuario hace clic en un vínculo que otro usuario compartió orgánicamente en una red social, es un canal importante para rastrear. Sin embargo, el especialista en marketing no tiene forma de anexar un código de seguimiento de parámetro de cadena de consulta a la dirección URL compartida. En este caso, puede crear una regla de procesamiento para detectar el dominio de referencia de las redes sociales de interés y la ausencia de códigos de seguimiento de pago para determinar el canal. Las visitas que cumplan estos requisitos se rastrearán como visitas sociales ganadas dentro del informe Canales de marketing .

Adobe recomienda trabajar con su equipo de análisis para crear un conjunto completo de [!DNL Marketing Channels] reglas de procesamiento para rastrear todos los canales relevantes para su negocio. Al hacerlo, puede crear potentes informes de atribución.

Para comprender cómo Advertising Cloud puede contribuir a las señales necesarias para crear canales de marketing personalizados, consulte &quot;[Uso de los ID de publicidad para crear [!DNL Marketing Channels] Reglas](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Uso de Advertising Cloud ID para crear [!DNL Marketing Channels] Reglas de procesamiento](mc-ids.md)
>* [Por qué los datos de canal pueden variar entre Advertising Cloud y [!DNL Marketing Channels]](mc-data-variances.md)
>* [Uso [!DNL Analytics Marketing Channels] con datos de Advertising Cloud](mc-ac-data.md)
>* [Vídeo: Creación de informes con Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

