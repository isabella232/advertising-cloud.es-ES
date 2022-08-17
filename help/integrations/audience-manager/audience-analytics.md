---
title: '"[!DNL Adobe][!DNL Audience Analytics] para clientes de Advertising Cloud"'
description: Aprenda a utilizar [!DNL Adobe][!DNL Audience Analytics] para casos de uso publicitario
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] para clientes de Advertising Cloud

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) es una integración entre Adobe Audience Manager y Adobe Analytics que permite a los clientes Audience Manager enviar segmentos a [!DNL Analytics] para obtener perspectivas enriquecidas sobre la actividad del sitio.

Los clientes de Advertising Cloud pueden beneficiarse del uso de [!DNL Audience Analytics]. La integración le permite:

* Envíe los datos de exposición de Advertising Cloud directamente a [!DNL Analytics] para determinar el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Determine los canales de marketing y los puntos de entrada del sitio a partir de los anuncios de exposición al canal superior.

* Capte la integración con [!DNL Analytics for Advertising Cloud] para incorporar segmentos demográficos de terceros de [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) con [!DNL Analytics for Advertising Cloud] para obtener más información sobre los perfiles de usuario.

   [!DNL Audience Marketplace] proporciona acceso a fuentes de datos de terceros con modelos de suscripción &quot;Activation&quot;, que permiten a los compradores enviar datos a un destino. Si los datos se utilizan en un [!DNL Analytics] destino, no se aplican las tarifas de activación.

* (Anunciantes con Advertising Cloud DSP) Agregue segmentos de exposición adicionales para obtener perspectivas holísticas sobre la administración de recorridos.

   Advertising Cloud DSP puede enviar datos de exposición al Audience Manager como señales procesables mediante la implementación de píxeles de seguimiento de impresión de Adobe Experience Platform o Audience Manager. Reenvío de los mismos datos a [!DNL Analytics] permite el análisis avanzado de datos. Consulte &quot;[Información general sobre la integración de datos de Advertising Cloud Media con Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot; para obtener más información.

Para obtener más información, consulte [!DNL Audience Analytics], incluidos sus requisitos previos y el flujo de trabajo, consulte &quot;[Información general del Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Ejemplos de uso [!DNL Audience Analytics] Datos con datos de Advertising Cloud

A continuación se muestran algunos ejemplos de cómo puede utilizar los datos combinados en [!DNL Analytics] [!DNL Analysis Workspace].

### Ver el impacto de la actividad del canal superior en la actividad descendente

Utilice segmentos de exposición del Audience Manager para ver el impacto de la actividad del sitio del canal superior en la actividad del sitio descendente. Incluya Advertising Cloud o ID de macros de terceros en los píxeles de seguimiento para realizar un seguimiento del impacto en un nivel detallado, desde el nivel de campaña hasta el nivel del sitio en el que se expuso al usuario.

Principales ventajas:

* Rastrear la exposición por tipo de canal/anuncio y usar [!DNL Audience Analytics] para determinar las tasas de entrada y superponerse a la siguiente fase del recorrido del cliente.

* Determine el impacto de la actividad del canal superior en la actividad del sitio descendente.

* Connect [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> y [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> para determinar un recorrido holístico del sitio.

A continuación se muestran algunos ejemplos de informes que se pueden crear en [!DNL Analysis Workspace].

![Ver el impacto de la actividad del canal superior en la actividad del sitio descendente](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Uso [!DNL Audience Analytics] Datos de segmentos de terceros para análisis de perfiles de usuario

Utilice segmentos de Audience Manager de terceros para obtener un análisis más completo de cómo interactúan los usuarios con el sitio. Puede utilizar la información para determinar nuevas audiencias de terceros para las que activar contenido, en función de cómo se comprometan los perfiles de segmentos de terceros con indicadores de rendimiento clave para los sitios de las campañas de contenido.

>[!TIP]
> Uso del Audience Manager `Audiences ID` y `Audiences Name` dimensiones [!DNL Analytics], como cualquier otra dimensión que [!DNL Analytics] recopila.

A continuación se muestran algunos ejemplos de informes que se pueden crear en [!DNL Analysis Workspace].

![Uso de segmentos de terceros para enriquecer el análisis de perfiles de usuario](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Integraciones de Advertising Cloud con Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

