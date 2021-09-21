---
title: Configuración de campaña
description: Consulte las descripciones de la configuración de campaña disponible.
feature: DSP Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# Configuración de campaña

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** El nombre de la campaña.

**[!UICONTROL Advertiser]:**  (Solo lectura para campañas existentes) El anunciante aplicable (marca). Seleccione un anunciante existente o cree uno nuevo.

**[!UICONTROL Advertiser URL]:** La página oficial del anunciante. Este campo acelera el proceso de aprobación de anuncios con socios de inventario.

**[!UICONTROL Timezone]:**  (Solo lectura para campañas existentes) Zona horaria para informes y ofertas.

**[!UICONTROL Customer PO]:**  (Opcional) Un pedido de compra del cliente para el pedido de inserción/pedido de compra.

**[Fechas] de campaña:** las fechas de inicio y finalización de la campaña.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Si se van a administrar los márgenes de la campaña:  *[!UICONTROL Yes]* o  *[!UICONTROL No]*  (predeterminado).

Al elegir *[!UICONTROL Yes],* especifique el tipo de margen y la cantidad:

* **[!UICONTROL Margin Type]:** El tipo de margen. No puede cambiar el tipo de margen una vez que habilite la administración de márgenes y guarde la campaña.

   * *[!UICONTROL Fixed]:*  (el valor predeterminado) permite a Advertising Cloud DSP calcular automáticamente y limitar el gasto en función de un porcentaje de margen fijo del  [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* permite administrar los márgenes hasta el nivel de ubicación especificando un independiente  [!UICONTROL Budget Reserve %] y  [!UICONTROL Gross Budget] para cada paquete y colocación en la campaña. Advertising Cloud DSP se optimiza en función de la eficacia financiera de cada ubicación, sin garantizar un margen específico. Utilice esto para pedidos de inserción que consten de varios artículos de línea para los que ha aceptado enviar una cantidad fija de unidades o tipos de unidades a una tasa fija.

* **[!UICONTROL Fixed Margin %]:** (Campañas con márgenes fijos únicamente) El marcado predeterminado para cada orden de inserción  <!-- impression? -->, como porcentaje. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de campaña neto.

* **[!UICONTROL Budget Reserve %]:** (campañas con márgenes fijos únicamente; (opcional) reserva un porcentaje especificado del  [!UICONTROL Gross Budget] como salvaguardia. Esta cantidad se deduce del [!UICONTROL Gross Budget] para definir el presupuesto de campaña neto.

**[!UICONTROL Gross Budget]:**  (Campañas solo con administración de márgenes) El presupuesto de la campaña bruta, antes de aplicar los ajustes marginales especificados.

Si lo desea, puede agregar un presupuesto bruto adicional diario, semanal o mensual:

1. Haga clic **[!UICONTROL Add an additional Gross Budget]**.

1. Introduzca el **[!UICONTROL Gross Budget]** y seleccione el intervalo presupuestario: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* o *[!UICONTROL Monthly]*.

El presupuesto neto total, que es el límite de gasto para la campaña, se calcula automáticamente en función de la configuración de margen y se indica por debajo de este valor.

**[!UICONTROL Budget]:**  (Campañas sin administración de márgenes) El presupuesto general de la campaña.

**[!UICONTROL Estimated Tax Withholding]:** Retiene un porcentaje del gasto total entre tarifas de publicidad, tarifas de servicio de publicidad y/o tarifas de datos a nivel de cuenta para impuestos locales o de país. Las tasas son estimaciones a efectos de presupuestación y ritmo, por lo que los tipos impositivos facturados pueden variar.

Para estimar los impuestos que deben retenerse:

1. Haga clic **[!UICONTROL Update rates here]**.

1. Especifique el **[!UICONTROL Estimated tax rate]** como porcentaje.

1. Active la casilla situada junto a cada tipo de tarifa para la que desea retener impuestos. Los tipos de tarifa incluyen:

   * *[!UICONTROL Include estimated tax - ads fee]:* se aplica a todos los gastos de medios de Advertising Cloud DSP, incluidos los impuestos sobre las tarifas de administración de campañas.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* se aplica a todo el gasto en Advertising Cloud DSP, excepto a los medios y los datos. Excluye los impuestos por las tarifas de administración de campañas

   * *[!UICONTROL Include estimated tax - data fee]:* se aplica a todos los datos gastados en Advertising Cloud DSP.

1. Haga clic **[!UICONTROL Submit]**.

>[!NOTE]
>
>* En los EE.UU., los estados pueden variar en la inclusión de tasas impositivas entre anuncios, servicio de publicidad y datos. En el caso de las organizaciones de otros países, se incluyen las tres categorías de impuestos para contabilizar el IVA.
>
>* También puede configurar estos valores en la configuración de tarifas de la cuenta.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (Solo lectura para las campañas existentes creadas desde el 22 de junio de 2020; no disponible para campañas creadas antes del 22 de junio de 2020) Nivel en el que Advertising Cloud se dirigirá a los anuncios y aplicará límites de frecuencia:  *El mismo dispositivo* para dirigirse a un dispositivo o a  ** personas para dirigirse a una persona en todos sus dispositivos conocidos.

**[!UICONTROL Device Graph]:**  (solo lectura para campañas existentes; campañas con targeting entre dispositivos basado en personas solamente) El gráfico de dispositivos que se usará para la segmentación entre dispositivos y la administración de frecuencia:

* *[!UICONTROL LiveRamp - U.S. only]:* Disponible para todos los anunciantes para la segmentación entre dispositivos a un CPM de 0,35 $ para impresiones que se entregan mediante el gráfico de  [!DNL LiveRamp] dispositivos (es decir, para dispositivos no encontrados dentro de los segmentos de audiencia de destino). Puede configurar la segmentación entre dispositivos en el nivel de ubicación.

   Esta opción también está disponible para todos los anunciantes, sin coste alguno, para la gestión de la frecuencia y la medición de la atribución.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Disponible solo para  [!DNL Device Co-op] participantes de Adobe Experience Cloud sin coste adicional.

>[!TIP]
>
>Si el anunciante también utiliza la atribución entre dispositivos, la práctica recomendada es utilizar la misma configuración de gráficos de dispositivos para la segmentación y la administración de frecuencias que las especificadas en la configuración de atribución entre dispositivos del anunciante. Si selecciona un gráfico de dispositivos diferente para esta campaña, pueden producirse discrepancias en los informes.

**[!UICONTROL Frequency Cap]:** (Opcional) El número de veces que un dispositivo o persona único (según el  [!UICONTROL Cross Device Level] especificado) será publicidad de la campaña. Las opciones incluyen *[!UICONTROL Unlimited]* o una cantidad específica por día, semana o mes.

>[!NOTE]
>
> Puede establecer límites de frecuencia en los niveles de campaña, paquete y ubicación. DSP respetará el límite de frecuencia más estricto de la jerarquía de campañas.

**[!UICONTROL Packages]:** Los  [](/help/dsp/campaign-management/packages/package-about.md) paquetes que se incluyen en la campaña. Seleccione los paquetes existentes o cree los paquetes que desee incluir. Si crea paquetes, consulte las descripciones sobre la [configuración del paquete](/help/dsp/campaign-management/packages/package-settings.md) para obtener más información.

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Las siguientes configuraciones solo habilitan capacidades de medición y creación de informes. La optimización del rendimiento solo se ejecuta en el nivel de paquete y ubicación.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** (opcional) permite la  [!DNL IAS] medición y la creación de informes de la visibilidad, el fraude, la seguridad de la marca y la verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Measure On]:** El inventario sobre el que se debe medir:  *[!UICONTROL Display and VPAID video inventory]* (el valor predeterminado) o  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >La visualización de vídeo solo se puede medir en el inventario VPAID.

* **[!UICONTROL IAS Account ID (AnID)]:** (Anunciantes con sus propias  [!DNL IAS] cuentas; (opcional) el ID de  [!DNL IAS] cuenta de la organización, que  [!DNL IAS] facturará directamente por su uso.

* **[!UICONTROL IAS Team ID]:** (Anunciantes con sus propias  [!DNL IAS] cuentas; (opcional) el ID de equipo de la  [!DNL IAS] cuenta de la organización, que  [!DNL IAS] facturará directamente por su uso.  <!-- verify -->

**[!UICONTROL MOAT]:** (Opcional) Permite la  [!DNL MOAT] medición y el sistema de informes de la visibilidad, el fraude, la seguridad de la marca y la verificación de audiencia. Se aplican tarifas adicionales.

#### Verificación de audiencia

**[!UICONTROL Nielsen]:** (Opcional) Habilita la  [!DNL Nielsen] medición y el sistema de informes de la verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo objetivo:  *[!UICONTROL Both]* (el valor predeterminado),  *[!UICONTROL Male]* o  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad al que se va a dirigir. Utilice los deslizadores izquierdo y derecho para reducir el intervalo según sea necesario.

* **[!UICONTROL Target Country]:**  (Opcional) Un país al que dirigirse. [!DNL Nielsen] medirá las impresiones servidas solo en los países admitidos.

**[!UICONTROL comScore vCE]:** (Opcional) Habilita la  [!DNL Comscore validated Campaign Essentials (vCE)] medición y el sistema de informes de la verificación de audiencia, utilizando la configuración especificada. Se aplican tarifas adicionales.

* **[!UICONTROL Target Gender]:** El sexo objetivo:  *[!UICONTROL Both]* (el valor predeterminado),  *[!UICONTROL Male]* o  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** El intervalo de edad al que se va a dirigir. Utilice los deslizadores izquierdo y derecho para reducir el intervalo según sea necesario.

* **[!UICONTROL Target Country]:**  (Opcional) Un país al que dirigirse. [!DNL Comscore] medirá las impresiones servidas solo en los países admitidos.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Permite la medición de origen y la creación de informes de la capacidad de visualización mediante la  [!DNL IAB Open Video Viewability (OpenVV)] tecnología, en función del nivel de sensibilidad especificado:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Acerca de la administración de campañas](campaign-about.md)
>* [Creación de una campaña](campaign-create.md)
>* [Editar una campaña](campaign-edit.md)

