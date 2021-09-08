---
title: Cómo DSP las campañas
description: Descubra cómo DSP optimiza los paquetes en sus campañas.
feature: Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Cómo DSP las campañas

Esta página describe cómo el motor de optimización de Advertising Cloud DSP, que utiliza [!DNL Adobe Sensei], optimiza los paquetes de sus campañas. Para obtener sugerencias y trucos sobre cómo optimizar manualmente sus campañas, póngase en contacto con el administrador de cuentas de Adobe. <!-- add link to trading playbook if we add it to help -->

Los objetivos de optimización de paquetes funcionan en dos niveles:

* Para cada paquete: DSP asigna el presupuesto a cada ubicación dentro del paquete en función del rendimiento de la ubicación con respecto al KPI seleccionado.

* Para cada colocación/subasta en el paquete: DSP calcula el valor de KPI económico en tiempo real para cada subasta por ubicación y luego utiliza este valor para determinar la oferta.

   >[!NOTE]
   >
   >El valor económico puede ponderarse en gran medida en función de lo bien que esté gastando una colocación. Si una ubicación está por detrás de su objetivo de gasto, entonces se le permitirá comprar subastas de menor calidad. Si una ubicación cumple fácilmente su objetivo de gasto, entonces se centrará en subastas de mayor calidad.

## Optimización de paquetes

DSP puede optimizar su envío de dos maneras fundamentales, con 20 variaciones disponibles para alinearlas con su objetivo de rendimiento específico. Puede elegir:

* Priorizar la tasa de rendimiento

* Priorice el equilibrio entre la eficiencia de los costos y la tasa de rendimiento

Consulte [Objetivos de optimización y cómo utilizarlos](optimization-goals.md) para determinar qué objetivo de optimización le ayudará a lograr sus KPI.

### Paquetes que dan prioridad a la tasa de rendimiento

Para los objetivos de optimización que dan prioridad a la tasa de rendimiento, DSP predice el rendimiento de cada subasta y siempre ofertas en la oferta máxima. Algunos ejemplos de objetivos de optimización aplicables son [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], etc.

Este modo de optimización funciona bien si:

* Ya conoce el nivel de CPM efectivo/aceptable (por ejemplo, un punto de referencia histórico).

* Si tiene problemas con la escala, está dispuesto a ajustar manualmente [!UICONTROL Max Bid] para cada ubicación.

* Estás priorizando la escala sobre la eficiencia.

#### Lógica de ritmo {#pacing-logic-performance}

* Si el gasto va a buen ritmo, las pujas se volverán más selectivas, de modo que solo pujarán en subastas que se prevea tengan altas tasas de rendimiento.

* Si el gasto está atrasado, las ofertas se volverán menos selectivas, de modo que pujarán en subastas que se prevea tengan tasas de rendimiento más bajas para alcanzar el objetivo de ritmo.

#### Borrado de precio/sombreado de oferta {#clearing-price-performance}

Después de ejecutar la lógica de ritmo, DSP ejecuta la oferta propuesta a través de un modelo de predicción de precios de compensación. Si la predicción indica que la oferta se puede reducir con una disminución mínima a la tasa de ganancia, entonces la oferta se reduce según la predicción.

### Paquetes que dan prioridad al equilibrio entre la eficiencia de los costos y la tasa de rendimiento

Para algunos objetivos de optimización, DSP predice el rendimiento de cada subasta y ajusta los precios de oferta automáticamente, sin exceder nunca el [!UICONTROL Max Bid] de una ubicación. Algunos ejemplos de objetivos de optimización aplicables son [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], etc.

#### Lógica de ritmo {#pacing-logic-balanced}

* Si el gasto va a buen ritmo, entonces DSP se vuelve más sensible a los precios, postulando cantidades más bajas para compensar la tasa de ganancia con el plan de ritmo.

* Si una métrica de rendimiento también se está equilibrando (todos los objetivos excepto [!UICONTROL Lowest CPM]), el KPI predicho se mezcla en la cantidad ofrecida. Por lo tanto, puja más por subastas que se predice que tendrán un mayor rendimiento sobre la base del &quot;coste por&quot;.

* Si el gasto está atrasado, entonces DSP se vuelve menos sensible a los precios y ofrece mayores cantidades, hasta [!UICONTROL Max Bid], para compensar la tasa de ganancias con el plan de ritmo.

#### Borrado de precio/sombreado de oferta {#clearing-price-balanced}

Después de ejecutar la lógica de ritmo, DSP ejecuta la oferta propuesta a través de un modelo de predicción de precios de compensación. Si la predicción indica que la oferta se puede reducir con una disminución mínima a la tasa de ganancia, entonces la oferta se reduce según la predicción.

## Optimización de ubicación

Los filtros de oferta previa de colocación son la manera más estricta de garantizar un rendimiento sólido. DSP utiliza filtros de oferta previa de forma estratégica en diferentes tipos de anuncios para lograr objetivos de rendimiento en todas las ubicaciones dentro de cada paquete. Puede utilizar filtros de oferta previa simultáneamente con la optimización a nivel de paquete o de forma independiente.

>[!NOTE]
>
>Los filtros de ofertas previas disponibles varían según el tipo de anuncio. Por ejemplo, para una colocación de visualización estándar, puede filtrar por tasa de pulsaciones y visibilidad, pero no por tasa de finalización.

Consulte [Filtros de oferta previa de nivel de ubicación y cómo utilizarlos](optimization-pre-bid-filters.md) para determinar qué filtro de oferta previa le ayudará a lograr sus KPI.

>[!MORELIKETHIS]
>
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Filtros de oferta previa de nivel de ubicación y cómo utilizarlos](optimization-pre-bid-filters.md)
>* [Resolución de problemas del rendimiento](/help/dsp/optimization/troubleshooting-performance.md)

