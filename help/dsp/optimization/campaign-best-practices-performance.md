---
title: Prácticas recomendadas para configurar campañas de rendimiento
description: Conozca las prácticas recomendadas para configurar sus campañas centradas en el rendimiento, que incluyen ubicaciones optimizadas para la CPA más baja o el ROAS más alto.
feature: DSP Optimization, DSP Best Practices
exl-id: fc64680d-9d1c-4f74-a8b9-2e9b670c00eb
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# Prácticas recomendadas para configurar campañas de rendimiento

Advertising Cloud puede optimizar sus campañas centradas en el rendimiento para ubicaciones con el menor coste por adquisición (CPA) o el mayor retorno en gasto publicitario (ROAS).

Consulte las siguientes prácticas recomendadas para campañas de rendimiento:

* Paso 1: Definición de su objetivo
* Paso 2: Definición de la estrategia
* Paso 3: Creación de paquetes
* Paso 4: Creación de una estructura de colocación
* Paso 5: Uso de los recursos creativos adecuados

## Paso 1: Definición de su objetivo

Es importante entender si el objetivo de la campaña es lograr el ROAS más alto posible o el CPA más bajo posible. Para cada paquete de la campaña, especificará el objetivo en consecuencia como *[!UICONTROL Highest ROAS - Custom Goal]* o *[!UICONTROL Lowest CPA - Custom Goal]*.

![objetivo de optimización](/help/dsp/assets/optimization-goals.png)

También debe determinar los eventos de éxito que llevarán al objetivo general y crear objetivos personalizados en consecuencia. Para cada paquete, especificará un objetivo personalizado que se utilizará con el objetivo de optimización general para la optimización algorítmica y la creación de informes mediante [!DNL Adobe Sensei]. Para obtener más información sobre la creación de objetivos personalizados, consulte [Prácticas recomendadas para crear un objetivo personalizado](custom-goal-best-practices.md).

![objetivos personalizados](/help/dsp/assets/objective-goals.png)

## Paso 2: Definición de la estrategia

### Estrategias de prospección

Los paquetes de canal superior incluyen ubicaciones con objetivos muy amplios para llegar a nuevos consumidores.

#### Estrategias de colocación recomendadas para la prospección

* Busque nuevas audiencias que probablemente se conviertan con las siguientes tácticas:

   * Modelado similar desde una plataforma de administración de datos (DMP), como Adobe Audience Manager.
   * Segmentación basada en el comportamiento que utiliza datos de terceros.
   * Segmentación contextual.
   * Segmentación por sitio/categoría.

* Usar la segmentación de ejecución de red (RON): Es importante incluir una ejecución de la ubicación de red sin segmentación de audiencia y con una segmentación de inventario amplia. Esto permite que el algoritmo [!DNL Adobe Sensei] encuentre usuarios valiosos que puedan tener cookies más recientes que aún no se hayan clasificado en una audiencia.

### Estrategias de redireccionamiento

Los paquetes de canal más bajos incluyen ubicaciones dirigidas a usuarios que ya han estado en la página web del anunciante o para los que el anunciante tiene datos CRM.

#### Estrategias de colocación recomendadas para redireccionamiento

* Si el anunciante es un cliente de Adobe Analytics o Adobe Audience Manager, puede generar segmentos de origen (como visitantes de página de inicio, páginas de producto o usuarios que abandonan el carro de compras) y usarlos como destinos de ubicación en Advertising Cloud.

* Evite asignar demasiado presupuesto a una ubicación dirigida a audiencia. Como regla general, prevea $30 por 1.000 usuarios al mes.

## Paso 3: Creación de paquetes

La práctica recomendada es crear paquetes independientes para la prospección de canales superiores y para la reorientación de canales inferiores. La optimización se produce en el nivel de paquete, de modo que los datos de rendimiento de todas las ubicaciones dentro de un paquete se agrupan. Por lo tanto, agrupe las ubicaciones en paquetes con un rendimiento esperado similar.

![ejemplo de paquetes separados para la prospección y la reorientación](/help/dsp/assets/p-r.png)

Además, utilice la siguiente configuración.

### Objetivos y presupuesto

* **Rastreo y restricción:** para seleccionar un objetivo de optimización de CPA o ROAS, el paquete debe utilizar el ritmo a nivel de paquete. Esto garantiza que todas las ubicaciones dentro del paquete estén optimizadas para distribuir el gasto en función del rendimiento y la escala a los objetivos seleccionados.

* **Fechas de vuelo:**  (Paquetes de prospección) Si la campaña se ejecuta durante más de 25 días, utilice la  [!UICONTROL Activate Custom Flighting] función . En primer lugar, establezca un vuelo personalizado durante los primeros 10 días en aproximadamente el 75% del presupuesto diario necesario para reducir el gasto durante la *fase de aprendizaje*. Luego establezca un segundo vuelo personalizado para el resto del presupuesto.

   Por ejemplo, si tiene 100 000 $ que gastar en 30 días, establezca el presupuesto para el Vuelo 1 (Días 1-10) en 25 000 $ (75% x 100 000 $/30 días = 2 500 $ por día). Utilice el presupuesto restante de 75.000 dólares para el vuelo 2 (días 11 a 30).

* **Presupuesto:** DSP siempre intentará asignar el 100% del presupuesto del paquete de forma uniforme entre todas las ubicaciones de un paquete. Si una colocación tiene un gasto bajo o ningún gasto, recomendamos limitar el presupuesto para permitir que una mayor parte del presupuesto se asigne a ubicaciones con escala. Espere entre 24 y 48 horas para que los cambios en el presupuesto se calibren.

* **Objetivos de optimización:** utilice uno de los dos objetivos de optimización del rendimiento  *[!UICONTROL Highest ROAS]* o  *[!UICONTROL Lowest CPA]*, según el objetivo del paquete. Estos objetivos optimizan automáticamente el paquete hacia las ubicaciones de ROAS más altas o CPA más bajas, respectivamente.

* **Objetivos personalizados:**
   * Si un nuevo paquete tiene el mismo objetivo que un paquete existente, puede opcionalmente vincular el paquete existente para que el algoritmo pueda utilizar los datos de aprendizaje automático existentes.
   * Introduzca el [!UICONTROL Target CPA] o [!UICONTROL Target ROAS] apropiado.

* **Estrategia de relleno de ritmo:** seleccione esta opción  *[!UICONTROL Even]* para maximizar sus objetivos de rendimiento con un ritmo uniforme a lo largo de toda la fecha de vuelo.

   Utilice el ritmo *[!UICONTROL FrontLoad]* y *[!UICONTROL Aggressive Front Load]* solo cuando priorice completamente el envío y la optimización del rendimiento, ya que estas estrategias pueden afectar negativamente a los KPI de rendimiento deseados.

## Paso 4: Creación de una estructura de colocación

Menos es más. Si puede configurar menos de seis ubicaciones por paquete, el presupuesto disponible puede cambiar de forma dinámica a las ubicaciones de mejor rendimiento con mayor facilidad.

Además, asegúrese de añadir cada ubicación a un paquete con un tipo de objetivo de paquete *[!UICONTROL Prospecting]* o *[!UICONTROL Retargeting]*, según corresponda.

A continuación se indican los ajustes de ubicación recomendados para las campañas de rendimiento.

### Objetivos

Configurará la optimización de CPA o ROAS en el nivel de paquete (consulte Paso 3: Crear paquetes), pero puede agregar configuraciones de nivel de ubicación adicionales.

* **Oferta máxima:**
   * Para la prospección de ubicaciones, utilice una oferta máxima baja (5 dólares).
   * Para volver a destinar las ubicaciones, utilice una oferta máxima alta (12 dólares).

* **Filtros de oferta previa:** minimice o, idealmente, evite establecer filtros de oferta previa agresivos, que impiden que la colocación alcance una escala. Entre las prácticas recomendadas se incluyen las siguientes:

   * Utilice un (1) filtro de oferta previa por ubicación. Varios filtros previos a la oferta requerirán que se cumplan ambos, lo que reduce la escala.

   * Considere la posibilidad de establecer filtros de oferta previos menos estrictos en los casos en que se aplique un objetivo adicional (como audiencia, ubicación geográfica y segmentación de sitios).

Consulte las descripciones de cuándo utilizar cada filtro de oferta previa en [Filtros de oferta previa de nivel de ubicación y cómo utilizarlos](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventario

Para maximizar la escala, utilice el inventario [!UICONTROL Public] (Open Exchange) y [!UICONTROL On Demand].

### Segmentación de sitios

* **[!UICONTROL Traffic Type]**:  [!UICONTROL Websites] only
* **[!UICONTROL Site Tier]**:  [!UICONTROL All sites]

### Segmentación de audiencia

* **[!UICONTROL Included Audiences]:**
   * Para la prospección de ubicaciones, agrupe categorías de audiencia similares y tamaños de audiencia similares en una ubicación. A continuación, según el rendimiento, realice una de las siguientes acciones:
      * Elimine las audiencias de bajo rendimiento de las ubicaciones existentes.
      * Mueva las audiencias de mayor rendimiento a una ubicación diferente para controlar mejor los presupuestos.
   * Para volver a destinar las ubicaciones, lo ideal es incluir un segmento de audiencia por ubicación para controlar fácilmente las ofertas y el presupuesto.

>[!NOTE]
>
>Los anuncios funcionarán mejor si solo se puede acceder a un usuario mediante una ubicación. Una superposición significativa de usuarios entre ubicaciones puede provocar competencia, lo que produce un ciclo de ofertas que aumentan continuamente, lo que aumenta el coste por usuario. Por lo tanto, si incluye varias audiencias, asegúrese de que no estén formadas por usuarios o miembros de audiencia superpuestos.
>
> Puede evitar la superposición de audiencias creando sus audiencias en niveles para poder suprimir los niveles más altos e inclusivos de las ubicaciones según sea necesario.

* **[!UICONTROL Frequency Capping]:**
   * Para la prospección de colocaciones, utilice límites de frecuencia ajustados (una impresión por día).
   * Para volver a destinar las ubicaciones, establezca el límite de ubicación principal en 6-10 impresiones por día y el límite secundario en una impresión por hora.

* **[!UICONTROL Device Targeting]**:
   * Incluir [!UICONTROL Computer], [!UICONTROL Mobile] y [!UICONTROL Tablet].
   * No establezca objetivos [!UICONTROL Firefox] y [!UICONTROL Safari] debido a las limitaciones de segmentación y medición. Póngase en contacto con el administrador de cuentas de Adobe para obtener más información sobre la compatibilidad con [!DNL Adobe] para [!DNL Safari ITP].
   * Si segmenta el tráfico web móvil, deshabilite todos los exploradores móviles excepto [!UICONTROL Chrome] y [!UICONTROL Edge].

### Seguridad de la marca y calidad de los medios

El uso de filtros contextuales, bloqueos de fraude antes de la oferta y/o filtros [!UICONTROL Ads.txt] limitarán la escala de las ubicaciones, pero utilícelos si es necesario.

## Paso 5: Uso de los recursos creativos adecuados

* La práctica recomendada es incluir tantos tamaños de publicidad únicos como sea posible para maximizar el alcance. La plantilla de visualización universal permite cargar cualquier tamaño de anuncio de visualización estándar.
* Asegúrese de que todas las ubicaciones contengan *al menos* todos los tamaños de anuncios de visualización principales (300x250, 728x90, 160x600, 300x600, 320x50 y 300x50).
* Actualice los elementos creativos con frecuencia para evitar la fatiga creativa.

>[!MORELIKETHIS]
>
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Cómo DSP las campañas](optimization-how-dsp-optimizes-campaigns.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Filtros de oferta previa de nivel de ubicación y cómo utilizarlos](optimization-pre-bid-filters.md)
>* [Lista de comprobación de Campaign Launch](/help/dsp/campaign-management/campaign-launch-checklist.md)

