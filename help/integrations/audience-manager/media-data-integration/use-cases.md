---
title: Casos de uso
description: Obtenga información sobre casos de uso para compartir sus datos de medios de DSP publicitarios con Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Casos de uso para capturar datos de exposición de medios en Adobe Audience Manager

*Anunciantes con solo DSP publicitario*

*Anunciantes con Adobe de solo integración de Advertising-Adobe Audience Manager*

A continuación se indican algunas formas en las que puede beneficiarse de la captura de sus datos de exposición a los medios DSP publicidad <!-- ad impression data? --> en Audience Manager.

## Gestión de actualización y frecuencia

La captura de datos de impresión en Audience Manager permite mejorar la administración de la frecuencia al crear segmentos de usuarios que han sido expuestos a un anuncio o campaña en particular. Puede utilizar estos segmentos para la segmentación de anuncios si desea aumentar la frecuencia o para la supresión de anuncios si desea limitar la frecuencia.

Además, con Audience Manager [!DNL Segment Builder], puede aplicar [controles de actualización y frecuencia](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) a cualquiera [características basadas en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) que contienen señales procesables. Esto le permite, por ejemplo, limitar el número de veces que se muestra a un usuario un creativo en particular en una campaña de medios. Leer &quot;[Eliminación instantánea entre dispositivos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; para aprender a hacer esto.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Mensajería secuencial

Al capturar los datos de impresión, puede crear un segmento de usuarios que hayan estado expuestos a una campaña o publicidad y utilizar este segmento para la mensajería o supresión secuenciales. Por ejemplo, puede redirigirse a los usuarios que vieron elementos creativos `123` pero no hizo clic ni convirtió mostrándoles elementos creativos `456`.

Para ejecutar este ejemplo en Audience Manager, debe seguir estos pasos:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Cree un rasgo para capturar a los usuarios que vieron el creativo.

   Por ejemplo, para asignar un nombre al rasgo `Creative Trait 123`, utilice la siguiente regla de rasgos:

   `d_creative == 123 AND d_event == imp`

1. Cree una característica para capturar a los usuarios que hacen clic o convierten.

   Por ejemplo, para asignar un nombre a este rasgo `Click and Converter`, utilice la siguiente regla de rasgos:

   `d_event == click OR d_event=conv`

1. Cree un segmento llamado `Retarget Users` para rellenar con usuarios que vieron el elemento creativo `123` pero no hizo clic ni convirtió. Utilice la siguiente regla de rasgos:

   `Creative Trait 123 AND NOT Click and Converter`

1. Asignación del segmento `Retarget Users` a un destino y dirija los usuarios de destino con creative `456`.

## [!DNL Adobe Audience Analytics] y datos de exposición de campaña

Una vez que los datos de clics e impresiones de la campaña están disponibles en Audience Manager, puede crear rasgos y segmentos de usuarios que han estado expuestos a una campaña o táctica determinada o con los que han interactuado. Con un [[!DNL Audience Analytics] integración](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), los segmentos del Audience Manager se pueden sincronizar con [!DNL Analytics] para un análisis más detallado. Entre los posibles casos de uso se incluyen los siguientes:

* **Análisis de la interacción entre DSP y [!DNL Adobe Advertising Search] anuncios:** La [[!DNL Analytics for Advertising] integración](/help/integrations/analytics/overview.md) no proporciona perspectivas sobre la interacción entre DSP y [!DNL [!DNL Search]] porque ambos canales utilizan ID de AMO que siguen reglas de atribución de ID de AMO, para los que un clic de búsqueda anula una visualización. Al crear un segmento de exposición DSP en el Audience Manager, puede usar [!DNL Audience Analytics] para analizar la interacción entre DSP y [!DNL [!DNL Search]] anuncios en [!DNL Analytics].

* **Análisis de frecuencia:** Puede crear segmentos en el Audience Manager en función de cuántas veces se ha expuesto un usuario a un anuncio o campaña en particular. A continuación, puede analizar los diferentes segmentos de exposición en Analytics para ver cómo cambia el comportamiento del usuario en función del número de exposiciones DSP.

## [!DNL Audience Optimization Reports]

Puede aprovechar [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) para identificar posibles oportunidades de rendimiento para segmentos en sus campañas. Estos informes combinan datos de impresión, clics y conversiones de campañas con métricas de segmentos para informar optimizaciones centradas en segmentos y una combinación de canales eficaz.

### Tipos de informes de Audience Optimization relevantes

| Informe | Descripción |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Compara los segmentos asignados y no asignados por impresiones y tasas de conversión. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Informes]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Devolver datos sobre impresiones, tasas de pulsaciones y conversiones para una amplia gama de dimensiones publicitarias. |
| [[!UICONTROL Optimal Frequency] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Ayuda a descubrir el equilibrio óptimo entre el número de impresiones y conversiones servidas. Permite ajustar el número de impresiones que se mostrarán antes de comenzar a ver una disminución de los retornos. |
| [[!UICONTROL Unique User Reach] Informe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Un gráfico de burbujas con un tamaño de cada burbuja en proporción directa al número de usuarios únicos para la dimensión seleccionada. |

### Consideraciones

* If [!DNL Audience Optimization Reports] los usuarios tienen controles de acceso basados en roles (RBAC) y luego [!DNL Adobe Customer Care] debe configurar una asignación entre el ID del anunciante y el código de integración de la fuente de datos del Audience Manager de la organización. Los usuarios administradores pueden proporcionar derechos RBAC a distintos usuarios.

* Informes de conversión en [!DNL Audience Optimization Reports] requiere cierta configuración por parte del usuario final. Los usuarios deben rellenar los archivos de metadatos.

* [!DNL Audience Optimization Reports] no admite cambios en los metadatos de la campaña (como el nombre de la campaña o el nombre de la ubicación).

* Los clics en las publicidades de búsqueda se incluyen en [!DNL Audience Optimization Reports] solo cuando están correlacionados con impresiones. En otras palabras, los clics de búsqueda se tratan como conversiones después de las impresiones. Como resultado, es posible que muchos clics de búsqueda no se incluyan en [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Información general sobre el envío de datos de exposición DSP medios a Adobe Audience Manager](overview.md)
>* [Recopilar datos de clics e impresiones de campañas de publicidad DSP](collect.md)

