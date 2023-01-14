---
title: Crear una fuente de audiencias para activar las audiencias de origen
description: Obtenga información sobre cómo crear una fuente para importar audiencias en su cuenta o en una cuenta de anunciante.
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Crear una fuente de audiencias para activar las audiencias de origen

*Función beta*

<!-- Will this remain for admin users/Adobe account teams only? -->

Cree un origen para importar audiencias a su cuenta de DSP o a una cuenta de anunciante. Actualmente, puede importar audiencias desde [el [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Después de crear un origen para la variable [!DNL Real-Time CDP], deberá activar su [!DNL Real-Time CDP] audiencias a través del Adobe Publicidad DSP destino dentro de [!DNL Real-Time CDP] para comenzar a importarlas. Consulte [los pasos del flujo de trabajo de activación](source-about.md#workflow-sources).

1. En el menú principal, haga clic en **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Haga clic [!UICONTROL Add Source].

1. En el [!UICONTROL Select a Type] , seleccione el tipo de origen.

   *[!UICONTROL RT-CDP]*: Este tipo de origen, para [el [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), es la única opción.

1. Especifique la variable [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* o *[!UICONTROL Account]*.

1. Escriba el resto [configuración de origen](source-settings.md).

   Guarde una copia del [!UICONTROL Source Key] que se genera. Necesitará el valor más tarde.

1. Haga clic **[!UICONTROL Save]**.

1. En el Experience Platform, cree una conexión de destino de Advertising DSP utilizando la variable [!UICONTROL Source Key] que se generó en la configuración de origen de DSP.

Para obtener instrucciones sobre la activación de la conexión de destino de DSP, la selección de segmentos y el acceso a los permisos de control, consulte &quot;[Conexión Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Configuración de fuente de audiencia](source-settings.md)
>* [Acerca de la activación de segmentos autenticados desde fuentes de audiencia](source-about.md)
>* [Activar segmentos autenticados de socios de ID duraderos](source-durable-id.md)<!-- title?-->
>* [Conexión Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)

