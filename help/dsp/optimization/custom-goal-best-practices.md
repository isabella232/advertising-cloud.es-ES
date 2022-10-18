---
title: Prácticas recomendadas para crear un objetivo personalizado
description: Conozca las prácticas recomendadas para crear objetivos personalizados con el fin de definir los eventos de éxito.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: 7cb39998041d151ece7809adc8a2e872b922e5fc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Prácticas recomendadas para crear un objetivo personalizado

## Objetivos personalizados con una sola propiedad

Los siguientes ejemplos muestran cómo se pueden configurar los objetivos que se dirigen a una sola propiedad (métrica).

### Ejemplo de campaña con el[!UICONTROL Highest ROAS - Custom Goal]&quot; Objetivo de optimización

Si el objetivo de la campaña son los ingresos ([!UICONTROL Highest ROAS - Custom Goal]), entonces su objetivo personalizado (objetivo) incluirá el[!UICONTROL Revenue]&quot; propiedad con un peso de uno (1).

![ejemplo de objetivo personalizado ROAS con una sola propiedad](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de uno equivale a un valor de uno por cada $1 de ingresos de los que se realiza un seguimiento.
>
> Por ejemplo, una conversión de 250 dólares con una ponderación de uno se registra como 250 dólares. Si a la métrica de conversión se le asigna una ponderación de 0,5, entonces la conversión de 250 $ aparece como 125 $ en Advertising Cloud ( Conversión de 250 $ * 0,5 [!UICONTROL Property Weight] = $125).

### Ejemplo de campaña con el[!UICONTROL Lowest CPA - Custom Goal]&quot; Objetivo de optimización

Si el objetivo de la campaña es el costo más bajo por adquisición (CPA) y solo requiere un evento de éxito, debe incluir esa métrica (en el siguiente ejemplo, &quot;Envío de solicitud&quot;). La práctica recomendada es establecer el peso como uno (1).

![ejemplo de un objetivo personalizado de CPA con una sola propiedad](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] de uno equivale a un valor de uno para cada conversión de la que se realiza un seguimiento.
>
> Por ejemplo, si se realiza el seguimiento de 10 conversiones de envío de aplicación, se notifican 10 conversiones de envío de aplicación.  Si a la métrica de conversión se le asigna una ponderación de 0,5, entonces las 10 conversiones se informan como cinco (5) en Advertising Cloud (10 conversiones * 0.5 [!UICONTROL Property Weight] = 5).

## Objetivos personalizados con varias propiedades

Hay dos escenarios en los que se usarían varias propiedades en un objetivo personalizado:

* El objetivo de la campaña tiene varios eventos de éxito. Por ejemplo, puede que esté anunciando más de una acción en el sitio y que todos se atribuyan a su objetivo de CPA. El siguiente objetivo de ejemplo incluye tres propiedades independientes (Descarga de PDF, Contacto con nosotros y Registro por correo electrónico), cada una con un peso de uno (1), que indica a la variable [!DNL Adobe Sensei] que cada una de las propiedades tiene la misma importancia. Si incluye propiedades con diversos costes o importancia, puede ajustar sus pesos relativos en consecuencia.

   ![ejemplo de un objetivo personalizado con varias propiedades](/help/dsp/assets/custom-goal-multiple-properties.png)

* La propiedad única de su objetivo personalizado no está alcanzando el mínimo de 10 conversiones por día requerido para un rendimiento optimizado. Esto puede ocurrir debido al gasto diario mínimo en paquetes o a un número limitado de conversiones naturales. La adición de propiedades de compatibilidad adicionales al objetivo personalizado puede ayudarle a alcanzar el umbral de 10 conversiones por día. Diez eventos de soporte pueden ayudar a un paquete a alcanzar el umbral de 10/día, incluso cuando cada uno de sus pesos está por debajo de uno (1). Sin embargo, es posible que no necesite agregar muchos eventos.

   Cuando agregue propiedades de soporte a un objetivo personalizado, fíjese en ellas según su importancia relativa para el evento de éxito principal y tenga en cuenta la cantidad de puntos de datos. Esto permite que el algoritmo de Adobe Sensei equilibre varias propiedades y optimice hacia su objetivo.

   El siguiente objetivo de ejemplo incluye tres propiedades, cada una con un peso diferente: Envío de aplicación = 1, Inicio de aplicación = 0.1 y Página de aterrizaje del anunciante = 0.01. Esto significa que cada conversión de envío de aplicación tiene el mismo valor para su negocio que una media de 10 conversiones de inicio de aplicación y 100 conversiones de página de aterrizaje del anunciante.

   ![ejemplo de un objetivo personalizado con varias propiedades](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Si, en su lugar, ponderara las visitas a la página de aterrizaje de forma equitativa a los envíos de aplicaciones, la cantidad naturalmente mayor de visitas a la página de aterrizaje podría superar su objetivo y distorsionar las visitas a la página de aterrizaje.<!--reword-->

>[!MORELIKETHIS]
>
>* [Acerca de los objetivos personalizados](custom-goal-about.md)
>* [Crear un objetivo personalizado](custom-goal-create.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [Cómo DSP las campañas](optimization-how-dsp-optimizes-campaigns.md)

