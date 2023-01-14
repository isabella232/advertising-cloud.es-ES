---
title: Integraciones de publicidad de Adobe con Adobe Audience Manager
description: Obtenga información sobre las distintas formas en que la publicidad de Adobe puede intercambiar datos con Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 0f88235b-6f9c-4b97-9517-22e8c47e1846
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Integraciones de publicidad de Adobe con Adobe Audience Manager

Puede integrar Publicidad de Adobe con Audience Manager de las siguientes maneras.

## Sincronizar Audience Manager y otros [!DNL Adobe] Segmentos para segmentación de anuncios

[!DNL Search] y DSP pueden incorporar metadatos, datos de jerarquía y datos de audiencia únicos para todos los Audience Manager de un anunciante o de una agencia y otros [!DNL Adobe] audiencias. Esta conexión única solo está disponible para los especialistas en marketing que utilizan la publicidad de Adobe. Consulte &quot;[Importación de segmentos de Adobe Audience Manager para la segmentación de anuncios](/help/integrations/audience-manager/import-audiences.md).&quot;

### Usar Audience Manager y otros [!DNL Adobe] Segmentos para crear [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Anunciantes de inclusión con [!DNL Advertising Search] only*

Dentro de [!DNL [!DNL Search]], puede crear [!DNL Google Ads] Los clientes de Google hacen coincidir audiencias de ID de usuario usando segmentos de Audience Manager existentes que tengan [!UICONTROL Adobe Media Optimizer (HTTP)] y [!UICONTROL Adobe Media Optimizer Batch Destination] como destinos. ([!DNL Media Optimizer] es un nombre anterior para [!DNL [!DNL Search]].) Esto incluye los segmentos de Adobe Analytics que se publican en Adobe Experience Cloud y los segmentos que se crean en Adobe Experience Cloud mediante la [!DNL People core service]. Para obtener más información, consulte la ayuda del producto en [!DNL [!DNL Search]].

[Audiencias de coincidencia del cliente con ID de usuario](https://support.google.com/google-ads/answer/9199250) funcionan como las audiencias basadas en etiquetas de sitios web, pero se asigna un ID que no es de PII a miembros de audiencia únicos para obtener ventajas distintas con respecto a las audiencias estándar de coincidencia de clientes y las basadas en etiquetas de sitios web.

Para crear los ID de usuario necesarios, debe utilizar una etiqueta JavaScript de publicidad de Adobe <!-- with a user ID parameter -->en sus sitios web. Póngase en contacto con [!DNL [!DNL Search]] equipo de la cuenta para obtener más información.

![proceso de creación de segmentos](/help/integrations/assets/ad_search_user_id_pic.png)

Una vez que haya creado las audiencias, puede utilizarlas en [!DNL Google Ads] campañas como [objetivos o exclusiones a nivel de campaña o de grupo de anuncios](#audience-manager-targets).

### Usar Audience Manager y otros [!DNL Adobe] Segmentos para anuncios de destino o exclusión {#audience-manager-targets}

* (Anunciantes de inclusión con [!DNL) [!DNL Search]]) Puede utilizar cualquiera [!DNL Google Ads] audiencias que eran [creado mediante [!DNL Adobe] segmentos](#audience-manager-google-audiences) como objetivos o exclusiones a nivel de campaña o de grupo de anuncios en su [!DNL Google Ads] campañas.

* (Anunciantes con DSP) Puede utilizar su [!DNL Adobe] segmentos como objetivos para las ubicaciones de publicidades. Si lo desea, puede incluir los segmentos en audiencias reutilizables, que puede utilizar como destinos o exclusiones para varias ubicaciones.

* (Anunciantes con Advertising Creative) Puede utilizar su [!DNL Adobe] segmentos como objetivos para creativos específicos en sus experiencias publicitarias.

>[!NOTE]
>
>Para obtener más información sobre cómo crear audiencias en el Audience Manager y el Experience Cloud [!DNL Audience Library] interfaces y casos de uso comunes para diferentes tipos de audiencia, consulte &quot;[Opciones de creación de audiencias](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Envío de datos de exposición de medios DSP al Audience Manager

*Anunciantes con solo DSP*

DSP clientes con Adobe Audience Manager pueden capturar datos de campañas de publicidad mediante llamadas en píxeles al Audience Manager. A continuación, puede utilizar los datos de campaña para crear rasgos basados en reglas, que puede utilizar para definir nuevos segmentos a fin de habilitar varios casos de uso de DSP, como segmentación más avanzada, administración de frecuencias, análisis de marketing y perspectivas de informes.

Consulte &quot;[Información general sobre el envío de datos de exposición DSP medios a Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

## Obtener perspectivas más interesantes en la actividad del sitio con el Audience Analytics

Adobe Los clientes de publicidad con [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) puede enviar datos rastreados por la publicidad de Adobe y segmentos de Audience Manager a [!DNL Analytics] para obtener perspectivas enriquecidas sobre la actividad del sitio.

Para obtener más información, consulte &quot;[[!DNL Adobe][!DNL Audience Analytics] para clientes publicitarios de Adobe](/help/integrations/audience-manager/audience-analytics.md).&quot;
