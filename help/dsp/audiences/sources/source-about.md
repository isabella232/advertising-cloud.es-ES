---
title: Acerca de la activación de segmentos autenticados desde fuentes de audiencia
description: Obtenga información sobre la ingesta de segmentos de origen desde una plataforma de datos de clientes.
feature: DSP Audiences
source-git-commit: aac60e8fddce1db3d0101a617fca3af970043648
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Acerca de la activación de segmentos autenticados desde fuentes de audiencia

<!-- Doesn't specifically explain what you can do in our UI -->
*Función beta*

Advertising Cloud DSP puede introducir segmentos de origen compuestos por señales autenticadas creadas dentro de una plataforma de datos del cliente (CDP). Puede usar los segmentos incorporados como destinos para sus colocaciones.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP está integrado con la variable [el [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), que forma parte de Adobe Experience Platform.

En [!DNL Real-time CDP], *destinos* son conexiones a plataformas de datos externas que permiten una activación de datos sin problemas. Por ejemplo, puede utilizar destinos para activar las relaciones con los clientes conocidas (como direcciones de correo electrónico con hash) para la publicidad de destino en formatos digitales compatibles con DSP.

Para obtener más información sobre los destinos, consulte el Experience Platform [Guía de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), incluida una descripción general del producto, instrucciones para [creación de espacios de trabajo de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) y [creación de conexiones de destino](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)y [activación de datos en destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Flujo de trabajo para usar la integración DSP con [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Permita que los DSP traduzcan segmentos de datos de clientes a [!DNL LiveRamp RampIDs]](source-durable-id.md) que son reconocibles en un entorno bisible.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Crear una fuente de audiencia](source-create.md) para importar audiencias a su cuenta de DSP o a una cuenta de anunciante.

1. [Configure un [!DNL Real-Time CDP] conexión de destino en el Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).<!-- Verify URL once it's published. -->

Para obtener más asistencia, póngase en contacto con su [!DNL Adobe] equipo de la cuenta o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Activar segmentos autenticados de socios de ID duraderos](source-durable-id.md)
>* [Crear una fuente de audiencias para activar las audiencias de origen](source-create.md)
>* [Configuración de fuente de audiencia](source-settings.md)
>* [Conexión de Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Descripción general del catálogo de destinos](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)

