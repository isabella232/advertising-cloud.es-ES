---
title: Preguntas frecuentes sobre Campaign Management
description: Obtenga más información sobre la administración de campañas, incluido el periodo de latencia para los cambios y lo que sucede cuando realiza cambios en el presupuesto durante un vuelo.
feature: DSP Packages, DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Preguntas frecuentes sobre Campaign Management

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latencia de configuración de cambios

* Cuando cambia una ubicación o configuración de paquete, ¿cuándo tendrá efecto el cambio?

   Los cambios de configuración suelen tener efecto inmediatamente, pero pueden tardar hasta 12 horas.

   Si es el último día de la entrega, realice cambios temprano en el día para que DSP tiempo suficiente para recalibrar el paquete en función de los cambios. Por ejemplo, si se cambia de un ritmo uniforme a un ritmo de carga anticipada, DSP debe reevaluar cómo distribuirá el gasto durante el resto del vuelo. No hagas ese tipo de cambio si sólo te queda una hora para entregar el último día del vuelo.

## Actualizaciones presupuestarias intermedias

* Cuando realice un cambio en una ubicación, ¿cuánto DSP tarda en reasignar el presupuesto del paquete?

   La asignación del presupuesto se basa en el rendimiento de la ubicación, que se evalúa usando un promedio de 14 días. Los cambios en una ubicación solo producen cambios en la asignación presupuestaria cuando provocan cambios en el rendimiento durante el promedio de 14 días.

   Cuando se producen cambios de rendimiento, DSP reasigna el presupuesto del paquete entre las ubicaciones en consecuencia durante el siguiente ciclo de optimización del presupuesto, que se produce aproximadamente a la medianoche (00:00) en el huso horario de la campaña.

* ¿Cómo se reasigna el presupuesto cuando se elimina una colocación de un paquete y se agrega a otro paquete?

   El historial de gastos completo de una ubicación se adjunta a la ubicación y se mueve con ella de un paquete a otro.

   Cuando se elimina una ubicación de un paquete, el paquete ya no tiene ningún historial del gasto de la ubicación. El presupuesto del paquete se convertirá en (presupuesto del paquete - presupuesto de colocación eliminado)/intervalo de tiempo restante en vuelo. A continuación, el presupuesto del paquete se asigna a las ubicaciones que queden en el paquete.

   Del mismo modo, si agrega la misma ubicación a un paquete diferente, DSP tiene en cuenta el historial de gastos de la ubicación cuando asigna presupuesto para todas las ubicaciones en el nuevo paquete.

* ¿Cómo cambia el ritmo del paquete en el último día de un vuelo?

   En el último día de un vuelo, el día se acorta de 24 horas a 23 horas para que no se supere el presupuesto del paquete. Además, la estrategia de relleno de ritmo del paquete cambia automáticamente a[!UICONTROL Frontload],&quot; incluso si está configurado como &quot;[!UICONTROL even].&quot; Esto significa que el 65% del presupuesto diario debe entregarse antes de las 11:30 EST.

>[!MORELIKETHIS]
>
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md)

