---
title: Activar segmentos autenticados de socios de ID duraderos
description: Obtenga información sobre la activación de audiencias autenticadas mediante una solución de ID duradera.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Activar segmentos autenticados de socios de ID duraderos

*Función beta*

Para activar audiencias autenticadas a través de una solución de ID duradera dentro de Advertising DSP, los segmentos deben traducirse a [!DNL RampIDs], que son reconocibles en un entorno bisible. Esto se puede lograr mediante:

* Aprovechamiento de la integración DSP con [!DNL Adobe Real-Time Customer Data Profile (CDP)] y [!DNL Adobe-LiveRamp Retrieval API].

* Envío manual de segmentos autenticados a DSP desde el [!DNL LiveRamp] [!DNL Connect] tablero.

## Tareas

1. Para cualquiera de las opciones, póngase en contacto con `adcloud-support@adobe.com` para habilitar la siguiente configuración en DSP, que le permitirá dirigirse a segmentos autenticados en DSP campañas una vez [se han completado todos los pasos del flujo de trabajo de activación](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] configuración de campaña antes de compartir segmentos de [!DNL Real-Time CDP].

   1. El nivel de cuenta &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Usuarios que comparten manualmente segmentos autenticados desde [!DNL LiveRamp]) Complete los siguientes pasos en la sección [!DNL LiveRamp] [!DNL Connect] tablero:

   1. Activar el mosaico de destino **[!DNL AAC API 1P Onboarding]**.

   1. Establezca [!DNL Identifier Settings] a **[!DNL Ramp ID]** solo.

      ![Configuración de identificador](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Opcional) Si todavía desea recibir identificadores basados en cookies, cree un segundo [!DNL AAC API 1P Onboarding] mosaico de destino con &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; y &quot;[!DNL AAID]&quot; seleccionado.

## Prácticas recomendadas para pruebas y validación de datos

* **Target [!DNL RampID]Segmentos basados en cookies y segmentos basados en cookies en campañas independientes.**

   * La configuración de campaña permite priorizar solo un identificador.

   * Actualmente, [!DNL RampIDs] no se pueden recuperar durante los eventos en el sitio. Esto significa que algunos objetivos personalizados, como la CPA más baja y el ROAS, no están disponibles con el uso de segmentos autenticados. Utilice segmentos basados en cookies solo si tiene un KPI de rendimiento restrictivo.

* **Cree una ubicación en ambas [!DNL RampID] y campañas basadas en cookies.**

   * Segmente los segmentos compartidos desde [!DNL LiveRamp] mediante el proceso de activación de segmentos estándar.

   * Póngase en contacto con el equipo de soporte técnico de Advertising de Adobe para validar la distribución de datos adecuada.

Para obtener más información sobre la integración de DSP con [!DNL LiveRamp], póngase en contacto con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de la activación de segmentos autenticados desde fuentes de audiencia](source-about.md)
>* [Crear una fuente de audiencias para activar las audiencias de origen](source-create.md)
>* [Configuración de fuente de audiencia](source-settings.md)
>* [Adobe Publicidad DSP conexión](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)

