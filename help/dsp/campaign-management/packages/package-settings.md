---
title: Configuración de paquetes
description: Consulte las descripciones de la configuración de paquetes disponible.
feature: DSP Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 4a699912468cd89efec0c1da9fdb6302ca93a3b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuración de paquetes

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** El nombre del paquete. La longitud máxima es de 60 caracteres.

**[!UICONTROL Description]:** (Opcional) Descripción del paquete.

**[!UICONTROL 3rd Party Billed Fees]:** (Opcional) Una tarifa estática de terceros que se rastreará como un coste no facturable:

>[!NOTE]
>
>Las tasas facturables se reflejan en la [!UICONTROL Net CPM] métrica.
* **[!UICONTROL CPM]:** El coste por 1000 impresiones (CPM).

* **[!UICONTROL CPM Description]:** Descripción de la tarifa CPM.

Puede anular la configuración de nivel de paquete en la variable [nivel de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Sólo lectura para paquetes existentes) A qué nivel colocar y limitar las colocaciones en el paquete:

* **[!UICONTROL Package level pacing]:** Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas como *grupo*. Esta estrategia garantiza que todas las ubicaciones dentro de un paquete determinado se optimizan de forma integral, distribuyendo el gasto en función del rendimiento y la escala a indicadores clave de rendimiento (KPI) seleccionados.

* **[!UICONTROL Placement level pacing]:**  Esta estrategia de ritmo funciona mediante el ritmo y el límite de todas las ubicaciones incluidas *individual*. La mejor práctica es utilizar esta estrategia solo para ejecutar ofertas de mercado privadas garantizadas.

**[!UICONTROL Flight Dates]:** La fecha de inicio y la fecha de finalización del paquete.

Para, opcionalmente, crear vuelos de ritmo no uniforme para el paquete, seleccione *[!UICONTROL *Activate Custom Flighting]** y configurar los vuelos personalizados en el [!UICONTROL Flighting] a continuación. Una vez que habilite el envío personalizado y guarde el paquete, no podrá deshabilitar el envío personalizado.

>[!NOTE]
>
>* Las fechas de vuelo deben incluirse en las fechas de vuelo de la campaña. Además, las fechas de vuelo de todas las ubicaciones asignadas a este paquete deben incluirse en estas fechas.
> * No se puede editar la fecha de inicio del paquete cuando se activa el vuelo personalizado.


**[!UICONTROL Budget]:** (Paquetes con un ritmo solo de nivel de paquete) El límite presupuestario bruto y el intervalo presupuestario.

Para los paquetes con delimitación personalizada, el intervalo presupuestario siempre es *[!UICONTROL All time]*. Para los paquetes sin un vuelo personalizado, especifique el intervalo de presupuesto: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Paquetes con ritmo a nivel de paquete y administración dinámica de márgenes solamente) El límite presupuestario bruto para la duración del paquete.

**[!UICONTROL Optimization Goal]:** (Paquetes solo con ritmo de nivel de paquete) El objetivo de optimización para el paquete. Consulte las descripciones de cada objetivo de optimización en [Objetivos de optimización y cómo utilizarlos](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Paquetes solo con objetivos de optimización personalizados) La variable [objetivo personalizado](/help/dsp/optimization/custom-goal-about.md) para el paquete. Para obtener más información sobre las prácticas recomendadas para objetivos personalizados y campañas que los utilizan, consulte  [Prácticas recomendadas para crear un objetivo personalizado](/help/dsp/optimization/custom-goal-best-practices.md) y [Prácticas recomendadas para configurar campañas de rendimiento](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** (Paquetes solo con objetivos de optimización personalizados) El propósito del paquete. Esta configuración ayuda a determinar cómo optimizar el paquete:

* *[!UICONTROL Prospecting]:* Los paquetes de prospección se centran en adquirir nuevos clientes.

* *[!UICONTROL Retargeting]:* Los paquetes de redireccionamiento se centran en volver a exponer a visitantes o clientes anteriores.

* *[!UICONTROL Other]:* Todos los demás propósitos.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Paquetes solo con objetivos de optimización personalizados) Otro paquete cuyos datos históricos se utilizan como entrada para optimizar el paquete.

**[!UICONTROL Target]:** (Paquetes solo con ritmo de nivel de paquete) El objetivo, que se utiliza para rastrear el rendimiento.

>[!NOTE]
>
>Este campo es solo una referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Frequency Cap]:** (Paquetes con un ritmo de nivel de paquete solamente) El número de veces que un dispositivo o una persona únicos (según el valor especificado [!UICONTROL Cross Device Level]) se pueden servir anuncios del paquete. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
>* Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respeta el límite de frecuencia más estricto de la jerarquía de campañas.
>* La práctica recomendada es establecer límites de frecuencia tanto para la prospección como para la reorientación a nivel de paquete.
> * Los límites de frecuencia más altos dan como resultado un mayor gasto e impresiones, pero un menor alcance. Los límites de frecuencia más bajos dan como resultado menos gasto e impresiones, pero mayor alcance.


**[!UICONTROL Pace on]:** (Paquetes solo con ritmo a nivel de paquete) En qué ritmo se basa:

* *[!UICONTROL Budget]:* (Predeterminado) Esta opción proporciona tantas impresiones como sea posible dentro del presupuesto del paquete asignado.

* *[!UICONTROL Impressions]:* Esta opción envía impresiones hasta que se alcanza una cantidad especificada dentro de un intervalo especificado. Al seleccionar esta opción, especifique el número de impresiones y el intervalo: *Todo el tiempo,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Pacing Fill Strategy]:** (Paquetes solo con ritmo de nivel de paquete) Cómo rastrear la entrega de anuncios:

* *[!UICONTROL Even]:* Realiza la entrega de manera uniforme a lo largo de cada vuelo, con un objetivo del 50% de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (El valor predeterminado) Acelera el envío para que se complete en un 55-65% a mitad de la duración del vuelo.

<!-- replaced with ASAP -->
* *[!UICONTROL Frontload]:* Acelera el envío para que esté entre un 65% y un 75% completo a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera el envío para que esté entre un 75 y un 85% a mitad del vuelo.

## [!UICONTROL Flighting]

(Paquetes con un ritmo a nivel de paquete y con &quot;[!UICONTROL Activate Custom Flighting]&quot; activado) Períodos de vuelo personalizados dentro del [!UICONTROL Flight Dates] especificado en [!UICONTROL Goals & Budget] para obtener más información.

Para cada vuelo, introduzca la fecha de inicio, la fecha de finalización y el número de impresiones objetivo. Para añadir otro vuelo, haga clic en **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de paquetes](package-about.md)
>* [Creación de un paquete](package-create.md)
>* [Editar un paquete](package-edit.md)
>* [Adjuntar una colocación a un paquete](package-attach-placement.md)
>* [Preguntas frecuentes sobre la administración de campañas](/help/dsp/campaign-management/campaign-management-faq.md)

