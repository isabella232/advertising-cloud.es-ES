---
title: Configuración de colocación
description: Consulte las descripciones de la configuración de ubicación disponible.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: 7bbeb3013ad7cd84bf3a25f5ebf8b16a82a6f591
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuración de colocación

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** El nombre de la ubicación.

>[!TIP]
>Utilice una convención de nombres que tenga sentido para su situación. Una convención de nomenclatura sugerida es &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** El estado de la ubicación: *[!UICONTROL Active]* (predeterminado) o *[!UICONTROL Paused]*.

>[!TIP]
>La práctica recomendada es poner en pausa la ubicación hasta que esté listo para iniciarla.

**[!UICONTROL Details]:** (Solo lectura) El tipo de anuncio aplicable, la cuenta que está creando o creando la ubicación y la campaña principal. Para ver más detalles, haga clic en **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Abre una lista de plantillas de colocación existentes. Para rellenar automáticamente la configuración de objetivos desde una plantilla:

1. Realice una de las siguientes acciones:

   * Para reutilizar todo el destino desde una plantilla, seleccione la casilla de verificación situada junto al nombre de la plantilla.

   * Para reutilizar tipos de objetivo individuales desde una plantilla, expanda el nombre de la plantilla y seleccione la casilla de verificación situada junto a los tipos de objetivo que desea reutilizar.

1. Haga clic **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Solo formatos de anuncio de vídeo) La duración o las especificaciones de anuncio que se utilizan para calcular la proyección de previsión a la derecha. Los campos varían según el tipo de anuncio.

**[!UICONTROL Placement tags]:** (Opcional) Palabras clave o apodos para ayudarle a localizar esta ubicación.

## Objetivos

**[!UICONTROL Package]:** (Opcional) Paquete al que se asigna la ubicación. Haga clic en ![Editar](/help/dsp/assets/edit.png) para seleccionar un paquete existente o crear un paquete nuevo. Cuando asigna la colocación a un paquete, la variable [!UICONTROL Goals] se actualiza con las fechas de vuelo, el objetivo de envío y el presupuesto del paquete.

**[!UICONTROL Flight Dates]:** La fecha de inicio y la fecha de finalización de la colocación. Los anuncios aprobados son aptos para ejecutarse durante el vuelo cuando la ubicación está activa y asignada a un paquete o campaña activo.

Las fechas del paquete (cuando corresponda) o la campaña se rellenan automáticamente de forma predeterminada.

>[!NOTE]
>
>* Las fechas de vuelo deben incluirse en las fechas de vuelo de la campaña y en las fechas de vuelo del paquete.


### Ubicaciones asignadas a paquetes con un ritmo de nivel de paquete

**[!UICONTROL Placement Funding]:** Cómo presupuestar la colocación:

* *[!UICONTROL Optimize based on performance]:* Controla el presupuesto en el nivel de paquete.
* *[!UICONTROL Set a fixed budget cap]:* Permite establecer un presupuesto de colocación diario, semanal, mensual o permanente. Introduzca un valor y la duración (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Placement Pre-bid Filters]:** Hasta cinco umbrales de KPI (como una métrica de visibilidad mínima o tasa de pulsaciones) que deben cumplirse para que se produzca la oferta. Puede usar filtros de oferta previa como tácticas de optimización, pero debe comprender que cada regla puede limitar las oportunidades en las que esta ubicación puede ofertar. Para añadir o editar filtros:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para agregar un filtro:
      1. Haga clic **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y, a continuación, introduzca un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Haga clic **[!UICONTROL Save]**.

Consulte las descripciones de cada filtro de oferta previa en &quot;[Filtros de oferta previa de nivel de ubicación y cómo utilizarlos](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Todas las demás ubicaciones

**[!UICONTROL Budget Goal]:** El límite presupuestario bruto y el intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Ubicaciones en campañas con solo administración de márgenes) El límite presupuestario bruto y el intervalo presupuestario (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  El objetivo de optimización del paquete. Consulte las descripciones de cada objetivo de optimización en &quot;[Objetivos de optimización y cómo utilizarlos](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** El objetivo, que se utiliza para rastrear el rendimiento.

>[!NOTE]
>
>Este campo es solo una referencia y no se utiliza para la toma de decisiones.

**[!UICONTROL Pace on]:** En qué ritmo se basará:

* **[!UICONTROL Budget goal]:** (Predeterminado) Esta opción proporciona tantas impresiones como sea posible dentro del presupuesto asignado.

* **[!UICONTROL Impressions]:** Esta opción envía impresiones hasta que se alcanza una cantidad especificada dentro de un intervalo especificado. Al seleccionar esta opción, especifique el número de impresiones y el intervalo: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* o *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** El máximo para pagar 1000 impresiones.

**[!UICONTROL Flight pacing]:** (Ubicaciones con un ritmo de nivel de ubicación solamente) Cómo colocar la entrega de publicidad:

* *[!UICONTROL Even]:* (El valor predeterminado) Realiza la entrega de manera uniforme a lo largo de cada vuelo, con un objetivo del 50% de la entrega en la primera mitad del vuelo.

* *[!UICONTROL Slightly Ahead]:* (El valor predeterminado) Acelera el envío para que se complete en un 55-65% a mitad de la duración del vuelo.

* *[!UICONTROL Frontload]:* Acelera el envío para que esté entre un 65 y un 75% completo a mitad del vuelo.

* *[!UICONTROL Aggressive Frontload]:* Acelera el envío para que esté entre un 75 y un 85% a mitad de camino.

**[!UICONTROL Intraday pacing]:** (Ubicaciones con un ritmo de nivel de ubicación solamente) Cómo rastrear la entrega de anuncios a lo largo de cada día dentro del vuelo:

* *[!UICONTROL Even]:* (El valor predeterminado) Escala la entrega según la disponibilidad del inventario. Por lo general, se entregan más anuncios por hora durante el día, cuando el volumen de la subasta es mayor, y se entregan menos anuncios por la mañana y por la noche.

* *[!UICONTROL ASAP]:* (el valor predeterminado) Acelera el envío al doble de la velocidad de *Even*.

   >[!CAUTION]
   >
   >Esta opción puede afectar negativamente al rendimiento. Utilícelo solo cuando priorice completamente el envío y gaste más que la optimización del rendimiento.

**[!UICONTROL Placement Pre-bid Filters]:** (Opcional) Se deben cumplir hasta cinco filtros para que se produzca la oferta. Puede utilizar filtros de oferta previa como tácticas de optimización, pero tenga en cuenta que cada regla puede limitar las oportunidades en las que esta ubicación puede ofertar. Para añadir o editar filtros:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para agregar un filtro:
      1. Haga clic **[!UICONTROL Add Filter]**.
      1. Junto a **[!UICONTROL Only bid if]**, seleccione una métrica y, a continuación, introduzca un valor.
   * Para quitar un filtro, haga clic en **[!UICONTROL X]** en la fila de filtro.
1. Haga clic **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Opcional) Ubicaciones específicas en las que se incluyen o excluyen publicidades en la colocación. Si no especifica ninguna ubicación, se segmentarán todas las ubicaciones.

>[!NOTE]
>
>Las ubicaciones de ciudad y DMA no están disponibles para las ubicaciones de Roku.

Para especificar ubicaciones:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para incluir o excluir un país, estado, ciudad, DMA, distrito legislativo federal o distrito legislativo estatal:
      1. Seleccione el tipo de ubicación en la columna izquierda.
      1. (Según sea necesario) Haga clic en una ubicación para expandirla.
      1. Junto a la ubicación, haga clic en *[!UICONTROL Include]* para incluirlo como objetivo o *[!UICONTROL Exclude]* para excluirlo como objetivo.
   * Para buscar un código postal e incluir o excluir todos los resultados seleccionados:
      1. Haga clic **[!UICONTROL Search Postal Code]**.
      1. Seleccione el país.
      1. Escriba el nombre de la ciudad y haga clic en ![Editar](/help/dsp/assets/search.png).
      1. Haga clic en el resultado de búsqueda correcto.
      1. Haga clic en *[!UICONTROL Include All]* para incluir todas las ubicaciones como objetivos o *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para introducir o pegar códigos postales e incluirlos o excluirlos todos:
      1. Haga clic **[!UICONTROL Paste Postal Code]**.
      1. Seleccione el país.
      1. Introduzca o pegue hasta 1000 códigos postales.
Incluya un código postal por línea o introduzca varios valores separados por comas o tabulaciones.
      1. Haga clic en *[!UICONTROL Include All]* para incluir todas las ubicaciones como objetivos o *[!UICONTROL Exclude All]* para excluir todas las ubicaciones como destinos.
   * Para quitar una ubicación de la variable [!UICONTROL Included] o [!UICONTROL Excluded] lista, haga clic en **[!UICONTROL X]** junto a la ubicación en la columna derecha.
1. Haga clic **[!UICONTROL Done]**.

>[!NOTE]
>
>* No todos los países tienen ubicaciones de estado, ciudad o código postal.
>* DMA (zona de mercado designada), Distritos Legislativos Federales y Distritos Legislativos Estatales sólo están disponibles para las ubicaciones de los Estados Unidos.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Fuentes de inventario que se incluirán o excluirán como objetivos. Para la mayoría de los tipos de ubicación, todos los tipos de inventario y todas las fuentes para cada tipo están incluidos de forma predeterminada. Para [!DNL Roku] ubicaciones, debe especificar el tipo de inventario y los orígenes. Puede elegir entre los siguientes tipos de inventario:

* [!UICONTROL Public]: (Todos los tipos de ubicación excepto Roku) Todo el inventario de intercambio abierto al que Advertising Cloud tiene acceso. Puede incluir y excluir el inventario público.

   Puede ver la lista por fuente o por fuente. Cuando ve la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una etiqueta característica seleccionada.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Sus ofertas privadas existentes (o las privadas existentes) [!DNL Roku] ofertas para [!DNL Roku] colocaciones) con editores que haya configurado en DSP. Puede incluir, pero no excluir, el inventario público.

   Puede buscar en la lista por palabra clave, clave, ID de oferta o etiqueta personalizada.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Todo [premium, no garantizado [!UICONTROL On Demand] inventario](/help/dsp/inventory/on-demand-inventory-about.md) (o [!UICONTROL On Demand] [!DNL] Ofertas de Roku para [!DNL Roku] ubicaciones) a las que se ha suscrito [!DNL DSP]. Puede incluir y excluir [!UICONTROL On Demand] inventario.

   Puede ver la lista por fuente o por fuente. Cuando ve la lista por fuente, puede buscar por nombre de fuente, clave de fuente o una región del editor, etiqueta de categoría o etiqueta característica seleccionada.

Para especificar el objetivo de inventario:

* Para excluir un tipo de inventario, desactive la casilla de verificación situada junto al nombre.
* Para dirigir un tipo de inventario:
   1. Active la casilla de verificación situada junto al nombre del tipo de inventario.
   1. (Opcional) Cambie las fuentes para incluir:
      1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] y [!UICONTROL On Demand] inventory) Haga clic en *[!UICONTROL *View by Source]** o **[!UICONTROL View by Feed]** para cambiar cómo se muestran las fuentes.
      1. (Cuando corresponda) Filtre el inventario según sea necesario.
      1. Especifique las fuentes que desea incluir y excluir:
         * Para incluir un [!UICONTROL Public] o [!UICONTROL On Demand] fuente, haga clic en **[!UICONTROL Include]** junto al nombre de origen.
         * Para incluir [!UICONTROL Private] fuentes:
            * Para incluir todo el inventario en una oferta, haga clic en **[!UICONTROL Include all]** junto al nombre de la oferta.
            * Para incluir un origen de inventario individual, expanda el nombre de la oferta y, a continuación, haga clic en la casilla de verificación situada junto al nombre del origen.
         * Para excluir un [!UICONTROL Public] o [!UICONTROL On ] fuente, haga clic en **[!UICONTROL Exclude]** junto al nombre de origen.
   1. (Opcional) Para descargar un archivo CSV con la información de objetivo en la ubicación Descargas del explorador, haga clic en **[!UICONTROL Save & Export]**.
   1. Haga clic **[!UICONTROL Save]**.

>[!TIP]
>
>Si se ha suscrito a [!UICONTROL On Demand] inventario, pero no puede localizar los editores ni las ofertas a los que dirigirse y, a continuación, comprobar el estado de las ofertas. Para obtener más información sobre los estados, consulte [Acerca de [!DNL On Demand] Inventario Premium](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Solo colocaciones de vídeo) Excluye el tráfico de salida.

Los anuncios salientes generalmente aparecen sobre el contenido como una ventana emergente o rellenados con contenido (en la experiencia nativa), en lugar de como anuncios de vídeo normales en un reproductor de vídeo.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Tipos de tráfico a destinatario. Las opciones incluyen **[!UICONTROL Websites]** y **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) La calidad de los sitios a los que dirigirse. Los neumáticos 1-3 son seguros para la marca y han sido evaluados y aprobados por el equipo de mapeo de DSP.

* *[!UICONTROL Tier 1]:* Sitios y aplicaciones Premium que son reconocibles a nivel nacional.
* *[!UICONTROL Tier 2]:* Se dirige al nivel 1, así como a sitios y aplicaciones de calidad que son menos conocidos que el nivel 1.
* *[!UICONTROL Tier 3]:* Segmenta los niveles 1-2, así como sitios y aplicaciones legítimos y seguros para la marca que se adaptan a una audiencia específica. Utilice el Nivel 3 para compras de alcance o segmentación de datos.
* *[!UICONTROL All Sites]:* Segmenta los niveles 1-3 y el nuevo inventario que no se ha seleccionado ni clasificado, que puede utilizar para su alcance.

>[!NOTE]
>
>El inventario es específico de las unidades de publicidad de la ubicación.

>[!TIP]
>
>Para las campañas de rendimiento, lo mejor es seleccionar *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Categorías de sitio dentro de los niveles de sitio seleccionados para incluir o excluir (pero no ambos) como objetivos. Elija entre las listas verticales del sitio que Advertising Cloud ha asignado en función del asunto del sitio:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique las categorías del sitio que se incluirán o excluirán:
   * Para incluir categorías de sitios:
      1. Haga clic **[!UICONTROL Include categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría a la que desea dirigirse.
   * Para excluir categorías de sitio:
      1. Haga clic **[!UICONTROL Exclude categories]**.
      1. Seleccione la casilla de verificación situada junto a cada categoría que desea excluir.
1. (Opcional) Para descargar un archivo CSV con la información de objetivo en la ubicación Descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Opcional; disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL Off]*) Sitios que se van a excluir. Puede buscar y seleccionar sitios, o bien introducir o pegar nombres de dominio:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Haga clic **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio o seleccione una categoría de sitio.
      1. En los resultados de la búsqueda, seleccione los sitios que desea excluir:
         * Para excluir un sitio individual, active la casilla de verificación situada junto a él.
         * (Cuando haya más de 50 resultados disponibles) Para excluir los primeros 50 resultados, haga clic en **[!UICONTROL Exclude these 50]**. Para excluir todos los resultados de búsqueda, haga clic en **[!UICONTROL Exclude these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. Haga clic **[!UICONTROL Paste]**.
      1. Introduzca uno o más nombres de dominio en líneas independientes.
      1. Haga clic **[!UICONTROL Exclude All]**.
1. Haga clic en **[!UICONTROL Done]** cuando hayas terminado.

>[!NOTE]
>
>* También se aplican las listas de sitios bloqueados a nivel de cuenta y de anunciante, además de Advertising Cloud DSP [lista de sitios bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md), que incluye los sitios considerados inseguros para los anuncios.
>* Las listas de sitios bloqueados siempre anulan las listas de sitios segmentados. Si una colocación excluye e incluye el mismo objetivo para una publicidad, se excluye el objetivo.


**[!UICONTROL Language]:** (Opcional) Un solo idioma de destino.

**[!UICONTROL Site List Preview]:** (Solo lectura) Todos los sitios dirigidos y bloqueados para la ubicación.

Si lo desea, puede exportar la lista de sitios bloqueados y con objetivo como archivo de valores separados por comas (CSV). Para exportar la lista, haga clic en **[!UICONTROL Export full site list]** y luego abra o guarde el archivo según el procedimiento normal del explorador.

**[!UICONTROL Allow unscreened sites]:** (Solo ubicaciones de visualización estándar) Habilita el envío de anuncios en sitios no auditados. Cuando la ubicación se dirige al inventario privado, esta opción puede entregar anuncios en sitios bloqueados.

**[!UICONTROL Paste list of targeted sites]:** Permite dirigirse solo a sitios específicos. Cuando activa esta opción, las demás opciones de segmentación del sitio se desactivan.

**[!UICONTROL Sites]:** (Disponible cuando **[!UICONTROL Paste list of targeted sites]** es *[!UICONTROL On]*) Sitios a los que dirigirse. Puede buscar y seleccionar sitios, o bien introducir o pegar nombres de dominio:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los sitios:
   * Para buscar un sitio:
      1. Haga clic **[!UICONTROL Search]**.
      1. Introduzca una palabra clave, seleccione un nivel de sitio o seleccione una categoría de sitio.
      1. En los resultados de la búsqueda, seleccione los sitios que desea incluir:
         * Para excluir un sitio individual, active la casilla de verificación situada junto a él.
         * (Cuando haya más de 50 resultados disponibles) Para incluir los primeros 50 resultados, haga clic en **[!UICONTROL Include these 50]**. Para incluir todos los resultados de búsqueda, haga clic en **[!UICONTROL Include these \<*NN *\>]**.
   * Para introducir nombres de dominio:
      1. click **[!UICONTROL Paste]**.
      1. Introduzca uno o más nombres de dominio en líneas independientes.
      1. Haga clic **[!UICONTROL Include All]**.
1. Haga clic **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Cualquier público objetivo para la ubicación, incluido [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todos los segmentos seleccionados y las audiencias guardadas. Puede seleccionar una audiencia existente, crear una nueva que pueda reutilizar más adelante o seleccionar segmentos de audiencia específicos:

* Para seleccionar una audiencia existente, haga clic en ![Select](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Included Audiences]y, a continuación, seleccione la audiencia.
* Para crear una audiencia nueva, haga clic en ![Select](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Included Audiences]y, a continuación, seleccione **[!UICONTROL + Create Audience]**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), comenzando con el paso 3.
* Para seleccionar segmentos de audiencia específicos, haga clic en **[!UICONTROL Select segments for this placement only]**. Seleccione la lógica del segmento; para obtener instrucciones, consulte el paso 6 de &quot;[Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md).&quot; Cuando haya terminado, haga clic en **Guardar**.

**[!UICONTROL Excluded Audiences]:** Cualquier audiencia que se excluya para la ubicación, incluidas las audiencias con [segmentos de terceros, segmentos de origen, segmentos de Adobe, segmentos personalizados y audiencias guardadas](/help/dsp/audiences/audience-settings.md). También se muestra el tamaño de audiencia deduplicada total y activa en todas las audiencias excluidas. Puede seleccionar una audiencia existente o crear una nueva que pueda reutilizar más adelante:

* Para seleccionar una audiencia existente, haga clic en ![Select](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Excluded Audiences]y, a continuación, seleccione la audiencia.
* Para crear una audiencia nueva, haga clic en ![Select](/help/dsp/assets/chevron-down.png) junto a [!UICONTROL Excluded Audiences]y, a continuación, seleccione **+ Crear audiencia**. Para obtener instrucciones, consulte [Crear una audiencia reutilizable](/help/dsp/audiences/reusable-audience-create.md), comenzando con el paso 3.

**[!UICONTROL Cross Device Targeting]:** (Disponible cuando selecciona al menos un segmento o audiencia y el [campaign está configurada para la segmentación entre dispositivos basada en personas](/help/dsp/campaign-management/campaigns/campaign-settings.md). Permite ampliar los objetivos a todos los dispositivos conocidos de una persona (según el gráfico de dispositivos especificado en la configuración de campañas), incluso a los dispositivos que no están en los segmentos especificados. Las tarifas pueden aplicarse según el gráfico especificado para la campaña. Actualmente, los datos de gráficos de dispositivos solo están disponibles en Norteamérica.

**[!UICONTROL Placement Cap]:** (Opcional) El número de veces que un dispositivo o una persona únicos (según el valor especificado) [!UICONTROL Cross Device Level] para la campaña) se servirán publicidades de la ubicación. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respetará el límite de frecuencia más estricto de la jerarquía de campañas.

**[!UICONTROL Secondary Cap]:** (Opcional; disponible al incluir un [!UICONTROL Placement Cap]) Una limitación adicional dentro de los límites del límite de colocación principal. Seleccione el número de impresiones y el período de tiempo (por ejemplo, 3 por 12 horas).

**[!UICONTROL Day Parting]:** (Opcional) Días específicos de la semana y hora del día en que se pueden ejecutar los anuncios. Para especificar intervalos de partición de días:
1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Seleccione la zona horaria correspondiente.
1. Especifique los intervalos:
   * Para seleccionar un intervalo preestablecido, haga clic en uno de los botones de intervalo. Las opciones incluyen *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* o *[!UICONTROL Prime]* (primetime).
   * Para seleccionar manualmente un intervalo, haga clic dentro de una celda y, opcionalmente, arrastre para seleccionarlo.
1. Haga clic **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Opcional; disponible para anunciantes configurados con [!DNL Comscore] y [!DNL Grapeshot] segmentos) Nombres o ID de segmentos específicos de [!DNL Comscore] y [!DNL Grapeshot] para incluir como objetivos. Se pueden aplicar tarifas adicionales para esta función. Para activar esta función y configurar segmentos de tema, póngase en contacto con su [!DNL Adobe] equipo de la cuenta.

Para especificar el objetivo de temas:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los segmentos a los que va a dirigirse:
   1. En la columna izquierda, seleccione el socio (*[!UICONTROL Comscore]* o *[!UICONTROL Grapeshot]*).
   1. En el campo de entrada, introduzca los nombres o ID de segmento.
1. (Opcional) Para descargar un archivo CSV con la información del tema en la ubicación Descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic **[!UICONTROL Save]**.

>[!TIP]
>
>* La segmentación por temas limita el inventario en el que la colocación puede ofertar, por lo que debe utilizar la segmentación por temas solo para un pequeño porcentaje de la compra general.
>
>* Configure cualquier objetivo negativo dentro del segmento en [!DNL Comscore] o [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Opcional) Información específica sobre dispositivos, incluidos tipos de dispositivos, fabricantes, sistemas operativos, navegadores y tipos de conectividad, para incluir y excluir como objetivos. Para especificar la segmentación de dispositivos:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los detalles del dispositivo que desea incluir y excluir:
   1. En la columna izquierda, seleccione la categoría .
   1. Especificar objetivo:
      * Para incluir un valor, haga clic en **[!UICONTROL Include]** junto al nombre del valor.
      * Para excluir un valor, haga clic en **[!UICONTROL Exclude]** junto al nombre del valor.
1. (Opcional) Para descargar un archivo CSV con la información de destino del dispositivo en la ubicación Descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Opcional) Proveedores específicos de servicios de Internet (ISP) para incluir o excluir (pero no ambos) como objetivos. Para especificar la segmentación del ISP:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Especifique los ISP que desea incluir o excluir:
   * Para incluir ISP:
      1. Haga clic **[!UICONTROL Include ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP a quien desee dirigirse.
   * Para excluir ISP:
      1. Haga clic **[!UICONTROL Exclude ISPs]**.
      1. (Opcional) Filtre la lista por palabra clave.
      1. Seleccione la casilla de verificación situada junto a cada ISP que desea excluir.
1. (Opcional) Para descargar un archivo CSV con la información de objetivo del ISP en la ubicación de descargas del explorador, haga clic en **[!UICONTROL Export]**.
1. Haga clic **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Tipos de [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]y [!DNL Peer39] filtros contextuales que se van a aplicar. Los valores predeterminados de nivel del anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de contexto de inventario que se van a bloquear de forma predeterminada. Pueden aplicarse tarifas adicionales.

* [!UICONTROL Peer 39]:

   * **Segmente sitios que:** (Opcional) Uno o más tipos de atributos de inventario a los que dirigirse de forma predeterminada. Pueden aplicarse tarifas adicionales.

* [!UICONTROL ComScore]:

   * **Bloquear sitios que:** (Opcional) Uno o más tipos de atributos de inventario que se van a bloquear de forma predeterminada. Pueden aplicarse tarifas adicionales.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Opcional) El grado de contenido adulto para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Pueden aplicarse tarifas adicionales.

   * **[!UICONTROL Alcohol Content]:** (Opcional) El grado de contenido de alcohol para el que se bloquean los anuncios de forma predeterminada: *[!UICONTROL Do Not Block]* (predeterminado), *[!UICONTROL Standard]* o *[!UICONTROL Strict]*. Pueden aplicarse tarifas adicionales.

**[!UICONTROL Pre-bid fraud blocking]:** Tipos de sitios para bloquear según tráfico fraudulento y actividades sospechosas medidas mediante [!DNL DoubleVerify], [!DNL Integral Ad Science]y [!DNL Peer39]. Los valores predeterminados de nivel del anunciante están seleccionados para nuevas ubicaciones, pero puede cambiar la configuración:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** De forma predeterminada, bloquea todo el tráfico no válido al 100 %, incluido el tráfico en dispositivos secuestrados, para nuevas ubicaciones. Pueden aplicarse tarifas adicionales.

   * **[!UICONTROL Also block sites with]:** (Opcional) Un nivel adicional de fraude y tráfico no válido que hará que los DSP bloqueen las publicidades de forma predeterminada:  *[!UICONTROL None]* (el valor predeterminado, que no bloquea el tráfico adicional), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* o *[!UICONTROL >25% Average Fraud/IVT levels]*. Pueden aplicarse tarifas adicionales.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Uno o más tipos de fraude que harán que los DSP bloqueen las publicidades de forma predeterminada: *[!UICONTROL Fraud]* (que bloquea todos los sitios con fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* y/o *[!UICONTROL Fraud: Zero Ads]*. Pueden aplicarse tarifas adicionales.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Opcional) Tipo de actividad sospechosa de un sitio web o aplicación que hará que los DSP bloqueen los anuncios de forma predeterminada: *[!UICONTROL None]* (el valor predeterminado, que no bloquea anuncios basados en actividades sospechosas), *[!UICONTROL Suspicious Activity - High Risk]* o *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Pueden aplicarse tarifas adicionales.

**[!UICONTROL Ads.txt filtering]:**

¿Qué nivel de [Ads.txt](https://iabtechlab.com/ads-txt-about/) filtrado pre-oferta para usar aprovechando la lista de vendedores digitales autorizados de cada editor. El valor predeterminado del nivel del anunciante se selecciona para las nuevas ubicaciones, pero puede cambiar la configuración:

* *[!UICONTROL Opt out of ads.txt (default)]*: Para comprar inventario de todos los vendedores.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Para priorizar la compra de inventario de vendedores y distribuidores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Para comprar inventario únicamente a vendedores y distribuidores directos autorizados de un dominio.
* *[!UICONTROL Ads.txt sellers only]*: Para comprar inventario únicamente a vendedores directos autorizados de un dominio.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Los anunciantes configurados con la variable [!UICONTROL DoubleVerify Authentic Brand Safety] opción) Habilita [!DNL DoubleVerify Authentic Brand Safety], que bloquea las impresiones posteriores a la oferta mediante las reglas de seguridad de marca personalizadas configuradas para el ID de segmento especificado. DSP factura a su cuenta por el uso del ID de segmento especificado en la configuración del anunciante.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] ubicaciones) Proveedores de seguimiento de terceros aprobados por [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]y [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Opcional) Píxeles de seguimiento de eventos de terceros que se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de evento:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, seleccione la casilla de verificación en la fila de píxeles.
   * Para crear un píxel nuevo:
      1. Haga clic **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Pixel name]:** El nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Pixel event fires on]:** Evento que déclencheur el píxel que se activará. Los eventos disponibles varían según el tipo de anuncio.
         * **[!UICONTROL Pixel type]:** Indica si el píxel es un *[!UICONTROL IMG URL]* (archivo de imagen de 1x1 píxeles), *[!UICONTROL HTML]* o *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Dirección URL de la imagen en píxeles.
      1. Haga clic **[!UICONTROL Create and attach]**.
   1. Haga clic **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Opcional) Píxeles de seguimiento de conversión que se adjuntarán de forma predeterminada a todos los anuncios nuevos de la ubicación. Para especificar píxeles de conversión:

1. Haga clic en ![Editar](/help/dsp/assets/edit.png).
1. Realice una de las siguientes acciones:
   * Para seleccionar un píxel existente, seleccione la casilla de verificación en la fila de píxeles.
   * Para crear un píxel nuevo:
      1. Haga clic **[!UICONTROL Create]**.
      1. Introduzca la siguiente información:
         * **[!UICONTROL Conversion pixel name]:** El nombre del píxel; la longitud máxima es de 500 caracteres. Utilice un nombre que le ayude a identificar fácilmente el píxel.
         * **[!UICONTROL Conversion category]:** Tipo de conversión.
         * **[!UICONTROL Impression conversion window]:** Número de días después de que se produzca una impresión publicitaria en la que la impresión se pueda atribuir a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Click conversion window]:** Número de días después de que se produzca un clic en un anuncio en el que el clic se pueda atribuir a una conversión. El valor predeterminado es de 30 días.
         * **[!UICONTROL Notes]:** (Opcional) Una descripción u otra información sobre el píxel.
      1. Haga clic **[!UICONTROL Create and attach]**.
      1. Implemente el píxel de conversión en las páginas web relevantes:
         1. En el menú principal, vaya a **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. En la fila de píxeles, haga clic en **[!UICONTROL edit]**.
         1. Copie los valores en la [!UICONTROL HTML Tag] y [!UICONTROL Flash Tag] , según sea necesario, para proporcionar al anunciante o al contacto del sitio web.

            Es posible que el departamento de TI u otro grupo del anunciante tenga que programar la implementación de etiquetas o que se le informe al respecto.
   1. Haga clic **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Opcional) Una tasa estática de terceros que se rastreará como un costo no facturable por 1000 impresiones. El valor predeterminado del nivel de paquete se aplica automáticamente a las nuevas ubicaciones, cuando corresponda, a menos que introduzca un valor diferente.

>[!NOTE]
>
>Las tasas facturables se reflejan en la [!UICONTROL Net CPM] métrica.

>[!MORELIKETHIS]
>
>* [Acerca de la administración de ubicaciones](placement-about.md)
>* [Crear una colocación](placement-create.md)
>* [Editar una colocación](placement-edit.md)
>* [Métodos abreviados del teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Preguntas frecuentes sobre Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

