---
title: Crear una audiencia reutilizable
description: Aprenda a crear audiencias reutilizables compuestas por segmentos de audiencia y otras audiencias guardadas.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Crear una audiencia reutilizable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Puede guardar y administrar audiencias reutilizables, que son grupos de segmentos de audiencia e incluso otras audiencias guardadas, que puede utilizar como destinos o exclusiones para varias ubicaciones.

1. En el menú principal, haga clic en **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create]**.

1. Escriba un [!UICONTROL Audience Name].

1. (Opcional) Anule la selección de la opción a **[!UICONTROL Share with all advertisers in my account]**.

   Cuando comparte una audiencia, esta está disponible como destino o exclusión para todos los anunciantes de la cuenta. Sin embargo, los segmentos individuales de la audiencia solo están disponibles para los usuarios en los que se comparten los segmentos. Por ejemplo, si comparte una audiencia que contiene segmentos de Adobe Analytics con un anunciante que no está asignado al mismo [!DNL Analytics] , el segmento no se previsualizará en esa audiencia para ese anunciante. Solo los segmentos disponibles para ese anunciante obtendrán una vista previa en la audiencia.

1. Haga clic **[!UICONTROL Save]**.

1. Crear la audiencia:

   >[!NOTE]
   >
   >A medida que crea la audiencia, se detallan [datos de tamaño de audiencia](audience-about.md) se actualiza en el panel derecho

   * Para crear manualmente la lógica de segmentos, utilice segmentos disponibles en la variable [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]y [!UICONTROL Saved Audiences] pestañas](audience-settings.md), haga lo siguiente.

      * Para agregar el primer segmento, localice el segmento en el panel izquierdo y active la casilla de verificación situada junto al nombre del segmento.

      * Para agregar un segmento a un grupo de segmentos existente:

         1. Haga clic en el grupo de segmentos en el panel derecho.

         1. (Opcional) Cambie la lógica del grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.

            *[!UICONTROL Exclude All]* no está disponible para el primer grupo de segmentos. Para una audiencia que solo incluya exclusiones, cree esta audiencia como *[!UICONTROL Include Any]* y, a continuación, dentro de una ubicación, seleccione esa audiencia en el menú Audiencias excluidas .

         1. Busque el nuevo segmento en el panel izquierdo y seleccione la casilla de verificación situada junto al nombre del segmento.

            El grupo de segmentos se actualiza automáticamente con el nuevo segmento.
      * Para agregar un nuevo grupo de segmentos:

         1. Haga clic en **[!UICONTROL + New Group]** en el panel derecho.

         1. (Opcional) Cambie la lógica entre el grupo anterior y el nuevo a *[!UICONTROL And]* o *[!UICONTROL Or]*, según sea necesario.

         1. Busque los segmentos para el nuevo grupo en el panel izquierdo y seleccione las casillas de verificación situadas junto a los nombres de los segmentos.

         1. (Opcional) Cambie la lógica del grupo a *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* o *[!UICONTROL Exclude All]*, según sea necesario.
   * Para usar la lógica de segmentos de una audiencia existente:

      1. Copie la lógica de segmentos de la audiencia existente de cualquiera de las siguientes maneras:

         * En la vista Todas las audiencias , mantenga el cursor sobre la fila de audiencia y haga clic en **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * En la configuración de la audiencia existente, en la parte superior del panel lógico de segmento, haga clic en **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * En un editor de texto, cree manualmente la lógica del segmento utilizando ID de segmento alfanuméricos y [Sintaxis booleana](audience-segment-logic-syntax.md)y cópielo en el portapapeles.
      1. Haga clic en **[!UICONTROL paste in an audience rule to begin building]**, pegue la lógica de segmento existente en el campo de entrada y, a continuación, haga clic en **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Si la audiencia ya incluye lógica de segmento, pegar la nueva lógica de segmento sobrescribe la lógica existente.




1. Haga clic **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Acerca de la gestión de público](audience-about.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Sintaxis para la lógica del segmento de audiencia](audience-segment-logic-syntax.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
>* [Crear e implementar un segmento personalizado](custom-segment-create.md)
>* [Cree e implemente un [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)

