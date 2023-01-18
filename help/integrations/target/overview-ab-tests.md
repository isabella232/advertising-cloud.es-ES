---
title: Configuración de pruebas A/B para publicidad de Adobe en Adobe Target
description: Obtenga información sobre cómo configurar una prueba A/B en [!DNL Target] para su DSP y [!DNL Search] anuncios.
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Configuración de pruebas A/B en Adobe Target para DSP publicitarios y [!DNL Advertising Search] Publicidades

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Anunciantes con solo DSP publicitario*

Adobe Advertising y Adobe Target facilitan aún más a los especialistas en marketing la entrega de una experiencia personalizada y conectada a través de medios de pago y mensajería en el sitio. Al compartir señales entre los productos, puede:

* Reduzca las tasas de visitas en el sitio vinculando la exposición de publicidad de los clientes desde DSP campañas a sus experiencias en el sitio.

* Establezca pruebas A/B reflejando las experiencias en el sitio con mensajes publicitarios que utilizan datos de exposición de Adobe Audience Manager y audiencias de Target con las que se hace clic para alimentar.

* Mida el impacto de la mensajería unificada en un alza objetivo in situ con visualizaciones sencillas en Adobe Analytics para [!DNL Target].

Consulte las siguientes secciones para conocer los requisitos previos y para obtener instrucciones sobre cómo configurar el seguimiento de clics y visualizaciones, implementar el uso compartido de señales entre DSP y [!DNL Target] y configurar una actividad de prueba A/B, y [!DNL Analytics] Analysis Workspace para ver los datos de prueba.

Si tiene más preguntas, póngase en contacto con adcloud_support@adobe.com.

## Requisitos previos

Este caso de uso requiere los siguientes productos e integraciones:

* [!DNL Target]

* [[!DNL Analytics] para publicidad](/help/integrations/analytics/overview.md) integración<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] para [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integración

* Audience Manager (requerido solo para pruebas de visualización)

## Paso 1: Configuración del marco de pulsaciones {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Marco de pulsaciones](/help/integrations/assets/target-ct-framework.png)

Cuando agrega DSP macros a una URL de pulsación (la URL que se muestra cuando un usuario hace clic en un anuncio y llega a la página de aterrizaje), DSP captura automáticamente la clave de colocación incluyendo ```${TM_PLACEMENT_ID}``` en la URL de pulsación. Esta macro captura la clave de colocación alfanumérica y no la ID de colocación numérica.

![Dirección URL de pulsación anexada a la dirección URL de la página de aterrizaje](/help/integrations/assets/target-ct-url.jpg)

### (Solo DSP) Agregar macros DSP a las direcciones URL de pulsación

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

En Flash que habla o Google Campaign Manager 360, actualice manualmente la URL de pulsación de cada anuncio para incluir las macros necesarias para capturar las variables de AMO ID. Las variables de ID de AMO se utilizan para enviar datos de clics a Adobe Analytics y para compartir claves de colocación para la prueba A/B. Consulte las siguientes páginas para obtener instrucciones:

* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Flashtalking] Etiquetas de publicidad](/help/integrations/analytics/macros-flashtalking.md)

* [Anexar [!DNL Analytics for Advertising] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad](/help/integrations/analytics/macros-google-campaign-manager.md)

Póngase en contacto con el equipo de su cuenta de DSP y con el Grupo de soluciones de publicidad (aac-advertising-solutions-group@adobe.com) para recuperar la clave de ubicación necesaria y finalizar la configuración, y para asegurarse de que cada URL de pulsación se rellene con la clave de ubicación.

## Paso 2: Configuración del marco de visualización mediante el Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Marco de visualización](/help/integrations/assets/targetr-vt-framework.png)

Al agregar un píxel de evento de impresión de Audience Manager en la configuración de ubicación y etiquetas de publicidad, puede crear un segmento de prueba para obtener más oportunidades de pruebas de visualización.

1. Implemente un píxel de evento de impresión de Audience Manager en las etiquetas de publicidad y en la configuración de ubicación de DSP.

   Para obtener instrucciones, consulte &quot;[Recopilación de datos de exposición de medios de campañas de DSP publicitarias](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Asegúrese de agregar [DSP macros](/help/dsp/campaign-management/macros.md) para capturar todos los datos que desea que el píxel del evento de impresión devuelva, incluido `${TM_PLACEMENT_ID_NUM}` para el ID de colocación numérica.

   >[!NOTE]
   >
   >Las direcciones URL de rastreo de clics incluyen la variable `${TM_PLACEMENT_ID}` macro para la clave de colocación alfanumérica, en lugar de `${TM_PLACEMENT_ID_NUM}` para el ID de colocación numérica.

1. Configure un segmento de Audience Manager a partir de los datos de impresión de DSP:

   1. Vaya a **Audience Manager** > **Datos de audiencia** > **Señales** y, a continuación, seleccione **Buscar** en la parte superior izquierda.

   1. Introduzca la variable **Clave** y **Valor** para la señal que determina a qué nivel se agrupan los usuarios del segmento. Utilice un [clave admitida](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) con un valor que corresponde a una macro que agregó al píxel del evento de impresión del Audience Manager.

      Por ejemplo, para agrupar usuarios para una ubicación en particular, use el `d_placement` clave. Para el valor, utilice un ID de colocación numérica real (como 2501853 en la captura de pantalla anterior) capturado por la macro de DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Si el campo Recuento total muestra recuentos de usuarios para el par clave-valor, lo que indica que el píxel se colocó correctamente y que los datos fluyen, puede continuar con el siguiente paso.
   ![Señales de búsqueda](/help/integrations/assets/target-am-signals.png)

1. [Crear un rasgo basado en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) para la creación de segmentos en Audience Manager.

   1. Asigne un nombre a la característica para que se pueda identificar fácilmente dentro de las actividades de prueba. Almacene el rasgo en la carpeta que prefiera.

   1. En el **Fuente de datos** menú desplegable, seleccione **Ad Cloud**.

   1. En el Generador de expresiones, agregue ```d_event``` en el campo Clave y ```imp``` en el **Valor** campo, seleccione **Agregar regla** y, a continuación, guarde el rasgo.

   ![Captura de pantalla de un rasgo basado en reglas](/help/integrations/assets/target-am-trait.png)

1. Configure un segmento de prueba en Audience Manager:

   1. En la parte superior de la página, vaya a **Datos de audiencia** > **Rasgos** y busque el nombre completo de la característica. Seleccione la casilla de verificación situada junto al nombre del rasgo y haga clic en **Crear segmento**.

   1. Asigne un nombre al segmento, seleccione `Ad Cloud` como el **Fuente de datos** y, a continuación, guarde el segmento.

      El Audience Manager divide automáticamente el segmento en un grupo de control que recibe la experiencia de página de aterrizaje estándar y un grupo de prueba que recibió una experiencia personalizada en el sitio.
   ![Captura de pantalla de un segmento de prueba](/help/integrations/assets/target-am-segment.png)

## Paso 3: Configurar una actividad &quot;Prueba A/B&quot; en Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

Las siguientes instrucciones destacan la información relativa al caso de uso DSP. Para obtener instrucciones completas, consulte &quot;[Crear una prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html.&quot;

1. [Iniciar sesión en Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. En el **Actividades** lista, haga clic en **Crear actividad** > **Prueba A/B**.

   ![Crear una actividad de prueba A/B](/help/integrations/assets/target-create-ab.png)

1. En el **Introducir URL de actividad*** , introduzca la dirección URL de la página de aterrizaje para la prueba.

   ![Introduzca el campo URL de la actividad](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Puede usar varias direcciones URL para probar la entrada al sitio de visualización. Para obtener más información, consulte &quot;[Actividad de varias páginas](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Puede identificar fácilmente las entradas principales por dirección URL de la página creando una [Informe de entrada al sitio](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) en Analytics.

1. En el **Objetivo** , introduzca la métrica de éxito de la prueba.

   >[!NOTE]
   >
   >Asegúrese de que [!DNL Analytics] está habilitado como origen de datos en [!DNL Target]y que se ha seleccionado el grupo de informes correcto.

1. Configure las variables **Prioridad** a `High` o `999` para evitar conflictos cuando los usuarios del segmento de prueba reciben una experiencia en el sitio incorrecta.

1. Within **Configuración de informes**, seleccione **Nombre de la empresa** y **Grupo de informes** conectado a su cuenta de DSP.

   Para obtener más sugerencias para la creación de informes, consulte &quot;[Prácticas recomendadas y resolución de problemas de la creación de informes](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. En el **Intervalo de fechas** , introduzca las fechas de inicio y finalización adecuadas para la prueba.

1. Agregue audiencias a la actividad:

   1. Elija la [segmento que creó anteriormente en Audience Manager para probar las audiencias de visualización](#view-through-framework).

      ![Añadir audiencias a la actividad](/help/integrations/assets/target-create-ab-audiences.png)

   1. Select **Páginas del sitio** > **Página de aterrizaje** > **Consulta** e introduzca la clave de colocación de DSP en la **Valor** para utilizar los parámetros de cadena de consulta de Target para audiencias de pulsación.

      ![Captura de pantalla de una audiencia de clic de destino](/help/integrations/assets/target-click-audience.jpg)

1. Para la variable **Método de asignación de tráfico**, seleccione **Manual (predeterminado)** y dividir la audiencia 50/50.

1. Guarde la actividad.

1. Uso [!DNL Target] [Compositor de experiencias visuales](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) para realizar cambios de diseño en la plantilla de página de aterrizaje de la prueba A/B.

   * Experiencia A: No edite porque es la experiencia de página de aterrizaje predeterminada/de control sin personalización.

   * Experiencia B: Utilice la variable [!DNL Target] interfaz de usuario para personalizar la plantilla de página de aterrizaje en función de los recursos incluidos en la prueba (como titulares, copia, colocación de botones y elementos creativos).
   >[!NOTE]
   >
   >Por ejemplo, casos de uso de pruebas creativas para pruebas creativas, póngase en contacto con el equipo de la cuenta.

## Paso 4: Configure su [!DNL Analytics for Target] Analysis Workspace en [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) es una integración entre soluciones que permite a los anunciantes crear [!DNL Target] actividades basadas en [!DNL Analytics] métricas de conversión y segmentos de audiencia y luego medir los resultados usando [!DNL Analytics] como fuente de informes. Todos los informes y la segmentación de esa actividad se basan en [!DNL Analytics] recopilación de datos.

Para obtener más información, consulte [!DNL Analytics for Target], incluido un vínculo a las instrucciones de implementación, consulte &quot;[Adobe Analytics como fuente de informes para Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configure el [!DNL Analytics for Target] Panel

En Analysis Workspace, configure la variable [!DNL Analytics for Target panel] para analizar su [!DNL Target] actividades y experiencias. Tenga en cuenta los siguientes puntos importantes e información sobre sus informes.

#### Métricas

* Cree un panel en el espacio de trabajo específico de la campaña, el paquete o la ubicación de publicidad de Adobe para la que se ejecutó la prueba. Utilice visualizaciones de resumen para mostrar métricas de publicidad de Adobe en el mismo informe que el rendimiento de la prueba de Target.

* Priorice el uso de métricas en el sitio (como visitas y conversiones) para medir el rendimiento.

* Comprenda que las métricas de medios agregadas de la Publicidad de Adobe (como impresiones, clics y costes) no se pueden comparar con las métricas de Target.

#### Dimension

Las siguientes dimensiones pertenecen a [!DNL Analytics for Target]:

* **Actividades de Target**: Nombre de la prueba A/B

* **Experiencias de Target**: Nombres de las experiencias de página de aterrizaje utilizadas en la actividad

* **Actividad de Target** > **Experiencia**: El nombre de la actividad y de la experiencia en la misma fila

### Resolución de problemas de Analytics para [!DNL Target] Datos

En Analysis Workspace, si observa que los datos de actividades y experiencias son mínimos o no se rellenan, haga lo siguiente:

* Compruebe que se utiliza el mismo ID de datos suplementarios (SDID) tanto para Target como para Analytics. Puede verificar los valores del SDID utilizando la variable [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) en la página de aterrizaje a la que la campaña dirige a los usuarios.

[Valores de ID de datos adicionales (SDID) en Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* En la misma página de aterrizaje, compruebe que a) el nombre de host mostrado en Adobe Debugger en Soluciones > Target coincide con b) el servidor de seguimiento mostrado en [!DNL Target] para la actividad (en Objetivos y configuración > Configuración de informes).

   [!DNL Analytics For Target] requiere un [!DNL Analytics] servidor de seguimiento que se enviará en llamadas desde [!DNL Target] a [!DNL Modstats] servidor de recopilación de datos para Analytics.&lt;!— solo &quot;¿a Analytics?&quot;>

[Valor de nombre de host en Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valor del servidor de seguimiento en Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Lectura adicional

* [Integración de Target con Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html): explica cómo configurar informes de Target en Analysis Workspace.
* [Información general sobre la prueba A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Describe las actividades de prueba A/B, que se pueden usar con anuncios DSP.
* [Experiencias y ofertas](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explica [!DNL Target] herramientas para determinar el contenido en el sitio al que se exponen DSP usuarios de prueba.
* [Señales, rasgos y segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) : Define algunas de las herramientas de Audience Manager que pueden ayudar con DSP pruebas de visualización.
* [Descripción general de Analytics for Advertising](/help/integrations/analytics/overview.md) : presenta Analytics for Advertising, que le permite hacer un seguimiento de las interacciones de clics y visualizaciones del sitio en las instancias de Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
