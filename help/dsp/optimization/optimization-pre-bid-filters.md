---
title: Filtros de oferta previa de nivel de ubicación y cómo utilizarlos
description: Haga referencia a los filtros de oferta previos de nivel de ubicación disponibles y vea cómo utilizarlos.
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Filtros de oferta previa de nivel de ubicación y cómo utilizarlos

| Filtro de oferta previa | Descripción | Cuándo utilizar este filtro |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Establece un umbral de predicción mínimo para la probabilidad de que una subasta resulte en un clic. Por ejemplo, si establece el umbral en 0,1 %, no pujará en una subasta a menos que la probabilidad prevista de un clic sea buena o igual al 0,1 %.<br><br><b>Nota:</b>  Los filtros se aplican antes que los objetivos de optimización. Como resultado, los filtros muy estrictos pueden impedir el gasto. | Utilícelo cuando tenga un objetivo KPI mínimo para la tasa de clics (CTR) y no desee gastar su presupuesto cuando el CTR esté por debajo del umbral. Este filtro puede ser bastante restrictivo, por lo que es importante establecer objetivos realistas. Dependiendo de otras restricciones en la colocación, un objetivo de 0,03-0,07% es generalmente un buen punto de partida. Puede optimizarlo a nivel de sitio según sea necesario para ayudar a mejorar las métricas.<br><br>Si su objetivo es lograr un CTR mínimo y el mejor CPM posible, la configuración recomendada es combinar un  [!UICONTROL Click Through Rate] filtro con el objetivo de optimización &quot;[!UICONTROL Lowest CPM]&quot;. Si su objetivo es un CPM máximo sin ningún beneficio real para el logro excesivo y un CTR mínimo, entonces emparejar un filtro [!UICONTROL Click Through Rate] con el objetivo de optimización &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; puede ser más apropiado. |
| [!UICONTROL 100% Completion Rate] | Establece una tasa de finalización mínima necesaria que debe cumplirse antes de pujar por una impresión. | Utilice este filtro cuando el objetivo principal de la campaña sean las tasas de finalización. Factor en otros parámetros de segmentación, pero 65% es el porcentaje de inicio recomendado. |
| [!UICONTROL Player Size - Adobe] | Define el tamaño mínimo requerido del reproductor, utilizando los datos de Advertising Cloud DSP. Ofertará con una impresión cuando se alcance el umbral [!UICONTROL Player Size]. | Utilícelo para asegurarse de que está entregando en el inventario de reproductores de episodio completo utilizando los datos de DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Define el tamaño mínimo requerido del reproductor, utilizando datos de [!DNL Moat] o [!DNL Integral Ad Science] ([!DNL IAS]). Ofertará con una impresión cuando se alcance el umbral [!UICONTROL Player Size]. | Utilícelo para asegurarse de que está entregando en el inventario de reproductores de episodio completo mediante datos [!DNL Moat] o [!DNL IAS] de toda la plataforma.<br><br><b>Nota:</b> Utilice este filtro solo cuando la campaña esté configurada para usar  [!DNL Moat] o  [!DNL IAS] datos. |
| [!UICONTROL Viewability IAS] | Establece un porcentaje mínimo de visibilidad requerido, utilizando los datos históricos de [!DNL IAS]. Ofertará con una impresión cuando se cumpla el umbral especificado. | Este filtro funciona mejor a medida que se obtienen más datos mediante una integración [!DNL IAS] a nivel de campaña.<br><br>Cuando la campaña está configurada para utilizar  [!DNL IAS] datos, lo mejor es utilizar este filtro con el objetivo de optimización del paquete &quot;[!UICONTROL Lowest vCPM (IAS)]&quot;. Si la integración no está habilitada, utilice este filtro con el objetivo de optimización &quot;[!UICONTROL Lowest CPM]&quot;. |
| [!UICONTROL Viewability Moat] | Establece un porcentaje mínimo de visibilidad requerido, utilizando los datos históricos de [!DNL Moat]. Ofertará con una impresión cuando se cumpla el umbral especificado. | Este filtro funciona mejor a medida que se obtienen más datos mediante una integración [!DNL Moat] a nivel de campaña.<br><br>Cuando la campaña está configurada para utilizar  [!DNL Moat] datos, la mejor práctica es usar el objetivo de optimización de paquetes &quot;[!UICONTROL Lowest vCPM (Moat)]&quot;. Si la integración no está habilitada, utilice este filtro con el objetivo de optimización &quot;[!UICONTROL Lowest CPM]&quot;. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Define el porcentaje mínimo de visibilidad requerido, utilizando los números y las medidas de la visualización de Advertising Cloud DSP. Ofertará con una impresión cuando se cumpla el umbral especificado.<br><br><b>Notas:</b><ul><li>Si la configuración [!UICONTROL Viewability Sensitivity] de la campaña es &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, se usa el estándar de medición de la visibilidad [!DNL Media Rating Council] (MRC) para la campaña. Si la configuración [!UICONTROL Viewability Sensitivity] es &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, se usa el estándar de medición de la [!DNL GroupM] visibilidad para la campaña.</li><li>Las definiciones de medición de Adobes difieren de las definiciones de terceros, por lo que puede haber pequeñas discrepancias con los datos de terceros.</li></ul> | La práctica recomendada es hacer coincidir el objetivo de optimización y cualquier configuración de filtro de oferta previa con la configuración [!UICONTROL Viewability Sensitivity] de la campaña. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Cómo DSP las campañas](optimization-how-dsp-optimizes-campaigns.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Configuración de campaña](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)

