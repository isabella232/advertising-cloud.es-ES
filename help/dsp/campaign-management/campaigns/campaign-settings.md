---
title: Configuración de campaña
description: Consulte las descripciones de la configuración de campaña disponible.
feature: DSP Campaigns
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# Configuración de campaña

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** El nombre de la campaña.

**[!UICONTROL Advertiser]:** (Solo lectura para campañas existentes) El anunciante aplicable (marca). Seleccione un anunciante existente o cree uno nuevo.

**[!UICONTROL Advertiser URL]:** La página oficial del anunciante. Este campo acelera el proceso de aprobación de anuncios con socios de inventario.

**[!UICONTROL Timezone]:** (Solo lectura para campañas existentes) Zona horaria para informes y ofertas.

**[!UICONTROL Customer PO]:** (Opcional) Un pedido de compra del cliente para el pedido de inserción/pedido de compra.

**[Fechas de campaña]:** Las fechas de inicio y finalización de la campaña.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Si se van a administrar los márgenes de la campaña: *[!UICONTROL Yes]* o *[!UICONTROL No]* (predeterminado).

Al elegir *[!UICONTROL Yes],* especifique el tipo de margen y el importe:

* **[!UICONTROL Margin Type]:** Tipo de margen. No puede cambiar el tipo de margen una vez que habilite la administración de márgenes y guarde la campaña.

   * *[!UICONTROL Fixed]:* (el valor predeterminado) Permite DSP calcular automáticamente y limitar el gasto en función de un porcentaje de margen fijo del [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Permite administrar los márgenes hasta el nivel de ubicación especificando una [!UICONTROL Budget Reserve %] y [!UICONTROL Gross Budget] para cada paquete y colocación en la campaña. DSP optimiza en función de la eficiencia financiera de cada ubicación, sin garantizar un margen específico. Utilice esto para pedidos de inserción que consten de varios artículos de línea para los que ha aceptado enviar una cantidad fija de unidades o tipos de unidades a una tasa fija.

* **[!UICONTROL Fixed Margin %]:** (Campañas con márgenes fijos solamente) El marcado predeterminado para cada orden de inserción <!-- impression? -->, como porcentaje. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de la campaña neta.

* **[!UICONTROL Budget Reserve %]:** (Campañas con márgenes fijos únicamente; (opcional) Reserva un porcentaje especificado del [!UICONTROL Gross Budget] como salvaguardia. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de la campaña neta.

**[!UICONTROL Gross Budget]:** (Campañas solo con administración de márgenes) El presupuesto de la campaña bruta, antes de que se apliquen los ajustes marginales especificados.

Si lo desea, puede agregar un presupuesto bruto adicional diario, semanal o mensual:

1. Haga clic **[!UICONTROL Add an additional Gross Budget]**.

1. Introduzca la variable **[!UICONTROL Gross Budget]** y seleccione el intervalo presupuestario: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

El presupuesto neto total, que es el límite de gasto para la campaña, se calcula automáticamente en función de la configuración de margen y se indica por debajo de este valor.

**[!UICONTROL Budget]:** (Campañas sin administración de márgenes) El presupuesto general de la campaña.

**[!UICONTROL Estimated Tax Withholding]:** Retiene un porcentaje del gasto total entre las tarifas de publicidad, las tarifas de servicio de publicidad y/o las tarifas de datos a nivel de cuenta por impuestos locales o de país. Las tasas son estimaciones a efectos de presupuestación y ritmo, por lo que los tipos impositivos facturados pueden variar.

Para estimar los impuestos que deben retenerse:

1. Haga clic **[!UICONTROL Update rates here]**.

1. Especifique la variable **[!UICONTROL Estimated tax rate]**, como porcentaje.

1. Active la casilla situada junto a cada tipo de tarifa para la que desea retener impuestos. Los tipos de tarifa incluyen:

   * *[!UICONTROL Include estimated tax - ads fee]:* Se aplica a todo el gasto en medios de Advertising DSP, incluidos los impuestos sobre las tarifas de administración de campañas.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Se aplica a todo el gasto en DSP publicitarias, excepto a los medios y los datos. Excluye los impuestos por las tarifas de administración de campañas

   * *[!UICONTROL Include estimated tax - data fee]:* Se aplica a todos los datos gastados en DSP publicitarios.

1. Haga clic **[!UICONTROL Submit]**.

>[!NOTE]
>
>* En los EE.UU., los estados pueden variar en la inclusión de tasas impositivas entre anuncios, servicio de publicidad y datos. En el caso de las organizaciones de otros países, se incluyen las tres categorías de impuestos para contabilizar el IVA.
>
>* También puede configurar estos valores en la configuración de tarifas de la cuenta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (Solo lectura para campañas existentes creadas desde el 22 de junio de 2020; no disponible para campañas creadas antes del 22 de junio de 2020) El nivel en el que DSP los anuncios objetivo y aplicará límites de frecuencia: *El mismo dispositivo* para dirigirse a un dispositivo o *People* para dirigirse a una persona en todos sus dispositivos conocidos.

**[!UICONTROL Device Graph]:** (Solo lectura para campañas existentes; campañas con targeting entre dispositivos basado en personas solamente) El gráfico de dispositivos que se usará para la segmentación entre dispositivos y la administración de frecuencia:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible para todos los anunciantes para la segmentación entre dispositivos a $0,35 CPM para impresiones que se entregan mediante el uso de la variable [!DNL LiveRamp] gráfico de dispositivos (es decir, para dispositivos no encontrados dentro de los segmentos de audiencia de destino). Puede configurar la segmentación entre dispositivos en el nivel de ubicación.

   Esta opción también está disponible para todos los anunciantes, sin coste alguno, para la gestión de la frecuencia y la medición de la atribución.

**[!UICONTROL Frequency Cap]:** (Opcional) El número de veces que un dispositivo o una persona únicos (según el valor especificado) [!UICONTROL Cross Device Level]) se proporcionan como anuncios de la campaña. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respetará el límite de frecuencia más estricto de la jerarquía de campañas.

**[!UICONTROL Packages]:** La variable [paquetes](/help/dsp/campaign-management/packages/package-about.md) para incluir en la campaña. Seleccione los paquetes existentes o cree los paquetes que desee incluir. Si crea paquetes, consulte las descripciones sobre el [configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md) para obtener más información.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Las siguientes configuraciones solo habilitan capacidades de medición y creación de informes. La optimización del rendimiento solo se ejecuta en el nivel de paquete y ubicación.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (Opcional) Habilita [!DNL IAS] medición y generación de informes de la visibilidad, fraude, seguridad de marca y verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Measure On]:** Inventario sobre el que medir: *[!UICONTROL Display and VPAID video inventory]* (predeterminado) o *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >La visualización de vídeo solo se puede medir en el inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes con sus propios [!DNL IAS] cuentas; (opcional) el [!DNL IAS] ID de cuenta, que [!DNL IAS] facturará directamente por su uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes con sus propios [!DNL IAS] cuentas; (opcional) el ID de equipo de la organización [!DNL IAS] cuenta que [!DNL IAS] facturará directamente por su uso. <!-- verify -->

**[!UICONTROL MOAT]:** (Opcional) Habilita [!DNL MOAT] medición y generación de informes de visibilidad, fraude, seguridad de marca y verificación de audiencia. Se aplican tarifas adicionales.

#### Verificación de audiencia

**[!UICONTROL Nielsen]:** (Opcional) Habilita [!DNL Nielsen] medición e informes de la verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo objetivo: *[!UICONTROL Both]* (predeterminado), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad objetivo. Utilice los deslizadores izquierdo y derecho para reducir el intervalo según sea necesario.

* **[!UICONTROL Target Country]:** (Opcional) Un país al que dirigirse. [!DNL Nielsen] medirá las impresiones servidas solo en los países admitidos.

**[!UICONTROL comScore vCE]:** (Opcional) Habilita [!DNL Comscore validated Campaign Essentials (vCE)] medición e informes de la verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo objetivo: *[!UICONTROL Both]* (predeterminado), *[!UICONTROL Male]* o *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad objetivo. Utilice los deslizadores izquierdo y derecho para reducir el intervalo según sea necesario.

* **[!UICONTROL Target Country]:** (Opcional) Un país al que dirigirse. [!DNL Comscore] medirá las impresiones servidas solo en los países admitidos.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Permite la medición de origen y la creación de informes de la visibilidad mediante la variable [!DNL IAB Open Video Viewability (OpenVV)] en función del nivel de sensibilidad especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Acerca de Campaign Management](campaign-about.md)
>* [Creación de una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)

