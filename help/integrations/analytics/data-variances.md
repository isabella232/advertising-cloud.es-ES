---
title: Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud
description: Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Los anunciantes con la integración [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> rastrean la publicidad de pago a través de Advertising Cloud y Adobe Analytics. Al rastrear medios, campañas y canales a través de varios sistemas, los mismos conjuntos de datos de diferentes sistemas rara vez coinciden por completo. En este documento se explica cómo debe esperar que los datos de los medios que se trafican a través de Advertising Cloud se comparen con los datos de los diferentes sistemas en los que se realiza un seguimiento del contenido en [!DNL Analytics].

>[!NOTE]
>
>Este documento se centra en Advertising Cloud y Analytics, pero muchos de los puntos clave también se pueden transferir a otras soluciones de seguimiento.

## Diferencias de atribución en informes similares

### Modelos de atribución y Windows de retrospectiva potencialmente diferentes

La integración [!DNL Analytics for Advertising Cloud] utiliza dos variables (eVars o rVars \[eVars reservadas]\) para capturar el [EF ID y el AMO ID](ids.md). Estas variables se configuran con una sola ventana retrospectiva (el tiempo dentro del cual se atribuyen las pulsaciones y las visualizaciones) y con un modelo de atribución. A menos que se especifique lo contrario, las variables están configuradas para que coincidan con la ventana de retrospectiva de clics predeterminada a nivel del anunciante y con el modelo de atribución en Advertising Cloud.

Sin embargo, las ventanas retrospectivas y los modelos de atribución se pueden configurar tanto en Analytics (a través de las eVars) como en Advertising Cloud. Además, en Advertising Cloud, el modelo de atribución se puede configurar no solo en el nivel del anunciante (para la optimización de la oferta), sino también dentro de vistas de datos e informes individuales (solo para fines de informes). Por ejemplo, una organización puede preferir utilizar el modelo de atribución de distribución par para la optimización, pero utilizar la atribución de último contacto para los informes en Advertising Cloud DSP o [!DNL Search]. Al cambiar los modelos de atribución, se cambia el número de conversiones atribuidas.

Si se modifica una ventana retrospectiva de informes o un modelo de atribución en un producto y no en el otro, los mismos informes de cada sistema mostrarán datos diferentes:

* **Ejemplo de discrepancias causadas por diferentes ventanas retroactivas:**

   Supongamos que Advertising Cloud tiene una ventana retrospectiva de clics de 60 días y [!DNL Analytics] tiene una ventana retrospectiva de 30 días. Y supongamos que un usuario llega al sitio a través de un anuncio rastreado por Advertising Cloud, lo abandona y luego vuelve el día 45 y se convierte. Advertising Cloud atribuirá la conversión a la visita inicial porque la conversión se produjo dentro de la ventana retrospectiva de 60 días. [!DNL Analytics]sin embargo, no se puede atribuir la conversión a la visita inicial porque la conversión se produjo después de que caducara la ventana retrospectiva de 30 días. En este ejemplo, Advertising Cloud informaría de un número mayor de conversiones que [!DNL Analytics].

   ![Ejemplo de conversión atribuida en Advertising Cloud pero no  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Ejemplo de discrepancias causadas por diferentes modelos de atribución:**

   Supongamos que un usuario interactúa con tres publicidades Advertising Cloud diferentes antes de la conversión, con los ingresos como tipo de conversión. Si un informe de Advertising Cloud utiliza un modelo de distribución uniforme para la atribución, entonces atribuirá los ingresos de manera uniforme en todos los anuncios. Sin embargo, si [!DNL Analytics] utiliza el modelo de atribución de último contacto, atribuirá los ingresos al último anuncio. En el siguiente ejemplo, Advertising Cloud atribuye 10 USD de los 30 USD de ingresos capturados a cada uno de los tres anuncios, mientras que [!DNL Analytics] atribuye los 30 USD de ingresos al último anuncio que vio el usuario. Al comparar informes de Advertising Cloud y [!DNL Analytics], se puede esperar ver el impacto de la diferencia en la atribución.

   ![Diferentes ingresos atribuidos a Advertising Cloud y  [!DNL Analytics] basados en diferentes modelos de atribución](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La práctica recomendada es utilizar las mismas ventanas de retrospectiva y modelo de atribución tanto en Advertising Cloud como [!DNL Analytics]. Póngase en contacto con el administrador de cuentas de Adobe según sea necesario para identificar la configuración actual y mantener las configuraciones sincronizadas.

Estos mismos conceptos se aplican a cualquier otro canal similar que utilice diferentes ventanas retroactivas o modelos de atribución.

#### Distintas ventanas de búsqueda para el seguimiento de visualizaciones {#impression-lookback}

En Advertising Cloud, la atribución se basa en clics e impresiones, y puede configurar distintas ventanas retroactivas para clics e impresiones. Sin embargo, en [!DNL Analytics], la atribución se basa en pulsaciones y visualizaciones, y no tiene la opción de establecer diferentes ventanas de atribución para pulsaciones y visualizaciones; para cada inicio en la visita inicial al sitio. Puede producirse una impresión el mismo día o varios días antes de que se produzca una visualización, lo que puede afectar al lugar en el que se inicie la ventana de atribución en cada sistema.

Normalmente, la mayoría de las conversiones de visualización se producen lo suficientemente rápido como para que ambos sistemas atribuyan crédito. Sin embargo, algunas conversiones pueden ocurrir fuera de la ventana de retrospectiva de impresión de Advertising Cloud, pero dentro de la ventana de retrospectiva [!DNL Analytics]; estas conversiones se atribuyen a la visualización en [!DNL Analytics] pero no a la impresión en Advertising Cloud.

En el siguiente ejemplo, supongamos que un visitante recibió un anuncio el día 1, realizó una visita de visualización (es decir, visitó la página de aterrizaje del anuncio sin hacer clic previamente en el anuncio) el día 2 y lo convirtió el día 45. En este caso, Advertising Cloud realizaría un seguimiento del usuario desde los Días 1-14 (usando una retrospectiva de 14 días), [!DNL Analytics] seguiría al usuario desde los Días 2-61 (usando una retrospectiva de 60 días) y la conversión en el Día 45 se atribuiría al anuncio dentro de [!DNL Analytics] pero no dentro de Advertising Cloud.

![Ejemplo de conversión de visualización atribuida en  [!DNL Analytics] pero no en Advertising Cloud](/help/integrations/assets/a4adc-viewthrough-example.png)

Otra causa de discrepancias es que, en Advertising Cloud, puede asignar conversiones de visualización de *ponderación de visualización* personalizada que sea relativa al peso atribuido a una conversión basada en clics. El peso de visualización predeterminado es del 40 %, lo que significa que una conversión de visualización se cuenta como el 40 % del valor de una conversión basada en clics. [!DNL Analytics] no proporciona esta ponderación de las conversiones de visualización. Por lo tanto, por ejemplo, un pedido de ingresos de 100 USD capturado en [!DNL Analytics] se descontará a 40 USD en Advertising Cloud si utiliza el peso de visualización predeterminado, una diferencia de 60 USD.

Tenga en cuenta estas diferencias al comparar las conversiones de visualización entre los informes de Advertising Cloud y [!DNL Analytics].

#### Modelos de atribución disponibles

| Atribución de Advertising Cloud | [!DNL Analytics] Atribución | Asignación de eVar/eVar |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n.a | n.a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>No usar* |
| [!UICONTROL Weight Last Event More] | n.a | n.a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n.a |
| n.a | [!UICONTROL J-Shaped] | n.a |
| n.a | [!UICONTROL Inverse-J] | n.a |
| n.a | [!UICONTROL Custom] | n.a |
| n.a | [!UICONTROL Participation] | n.a |
| n.a | [!UICONTROL Algorithmic] | n.a |

>[!NOTE]
>
>Para la asignación lineal, [!DNL Analytics] atribuye los eventos de éxito de forma equitativa a través de todos los valores de eVar dentro de una sola visita, por lo que debe utilizar la asignación lineal con una caducidad de eVar de &quot;Visita&quot;. Sin embargo, para la publicidad, el uso de la atribución lineal conduce a una asignación que no es realmente lineal y a informes menos que ideales. Por ejemplo, si un visitante interactúa con tres publicidades antes de realizar la conversión en tres visitas separadas, solo la publicidad que se haya visto en la última visita se atribuirá a la conversión, no a los tres anuncios.
>
>Además, si se cambia la asignación de conversión a &quot;Lineal&quot; o de &quot;Lineal&quot;, los datos históricos no se mostrarán, lo que puede provocar una exposición incorrecta de los datos en los informes. Por ejemplo, la asignación lineal puede dividir los ingresos entre un número de valores de eVar diferentes. Si cambia la asignación a &quot;Más reciente&quot;, entonces el 100 % de esos ingresos se asocia con el valor único más reciente. Esta asociación puede llevar a conclusiones incorrectas.
>
>Para evitar confusiones, [!DNL Analytics] impide que los datos históricos estén disponibles en la interfaz de informes. Puede ver los datos del historial si vuelve a cambiar el eVar a la configuración de asignación inicial, aunque no debería cambiar la configuración de asignación de eVar simplemente para acceder a los datos del historial. Adobe recomienda usar un eVar nuevo cuando desee aplicar una nueva configuración de asignación para los datos que ya se están registrando, en lugar de cambiar la configuración de asignación para un eVar que ya tiene una cantidad significativa de datos históricos.

Consulte la lista de modelos de atribución [!DNL Analytics] y sus definiciones en [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Si ha iniciado sesión en Advertising Cloud, puede encontrar una lista de modelos de atribución en
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Atribución de fecha de evento en Advertising Cloud

En Advertising Cloud, puede notificar los datos de conversión por la fecha de clic/evento asociada (la fecha del evento de clic o impresión) o por la fecha de transacción (la fecha de conversión). El concepto de informe de fechas de clic/evento no existe en [!DNL Analytics]; todas las conversiones rastreadas en [!DNL Analytics] se registran por fecha de transacción. Como resultado, se puede informar de la misma conversión con fechas diferentes en Advertising Cloud y [!DNL Analytics]. Por ejemplo, supongamos que un usuario hace clic en un anuncio el 1 de enero y lo convierte el 5 de enero. Si está viendo los datos de conversión por fecha de evento en Advertising Cloud, la conversión se registrará en el informe el 1 de enero, cuando se produjo el clic. En [!DNL Analytics], la misma conversión se registraría el 5 de enero.

![Ejemplo de conversión atribuida a fechas diferentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Atribución en [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] Los informes de ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)  le permiten configurar reglas para identificar diferentes canales de marketing en función de distintos aspectos de la información de visitas. Puede rastrear los canales rastreados por Advertising Cloud ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] y [!UICONTROL Paid Search]) como [!DNL Marketing Channels] usando el parámetro de cadena de consulta `ef_id` para identificar el canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Sin embargo, aunque los  [!DNL Marketing Channels] informes pueden rastrear canales de Advertising Cloud, es posible que los datos no coincidan con los informes de Advertising Cloud por varios motivos. Consulte las secciones siguientes para obtener más información.

>[!NOTE]
>
> Los siguientes conceptos principales también se aplican a cualquier seguimiento de varios canales que incluya campañas que no se rastrean en Advertising Cloud, como la variable [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (también conocida como el Dimension &quot;Código de seguimiento&quot; o &quot;eVar 0&quot;) y el seguimiento de eVar personalizado.

### Modelos de atribución potencialmente diferentes en [!DNL Marketing Channels]

La mayoría de los informes [!DNL Marketing Channels] se configuran con atribución [!UICONTROL Last Touch], para los que el último canal de marketing detectado se asigna al 100% del valor de conversión. El uso de diferentes modelos de atribución para los informes [!DNL Marketing Channels] y los informes de Advertising Cloud dará lugar a discrepancias en las conversiones atribuidas.

### Una ventana retrospectiva potencialmente diferente en [!DNL Marketing Channels]

La ventana retrospectiva de [!DNL Marketing Channels] se puede personalizar. En Advertising Cloud, la ventana de retrospectiva de clics es configurable, aunque es común una ventana fija de 60 días. Si los dos productos utilizan ventanas retrospectivas diferentes, puede esperarse discrepancias en los datos.

### Atribución de canal diferente en [!DNL Marketing Channels]

Los informes de Advertising Cloud capturan solo los medios de pago que se trafican a través de Advertising Cloud (búsqueda de pago de anuncios de Advertising Cloud Search y visualización de anuncios de Advertising Cloud DSP), mientras que los informes [!DNL Marketing Channels] pueden rastrear todos los canales digitales. Esto puede provocar una discrepancia en el canal para el que se atribuye una conversión.

Por ejemplo, la búsqueda de pago y los canales de búsqueda natural suelen tener una relación simbiótica, en la que cada canal ayuda al otro. El informe [!DNL Marketing Channels] atribuirá algunas conversiones a la búsqueda natural que Advertising Cloud no usará porque no rastrea la búsqueda natural.

Considere también un cliente que ve un anuncio en pantalla, hace clic en un anuncio de búsqueda de pago, hace clic dentro de un mensaje de correo electrónico y, a continuación, realiza un pedido de 30 USD. Aunque tanto Advertising Cloud como [!DNL Marketing Channels] utilicen el modelo de atribución de último contacto, la conversión se seguirá atribuyendo de forma diferente a cada uno. Advertising Cloud no tiene acceso al canal [!UICONTROL Email], por lo que acreditaría la búsqueda de pago para la conversión. [!DNL Marketing Channels], sin embargo, tiene acceso a los tres canales, por lo que se  [!UICONTROL Email] atribuiría el crédito por la conversión.

![Ejemplo de atribución de conversión diferente en Advertising Cloud frente a  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Para obtener más información sobre por qué las métricas pueden variar, consulte &quot;[Por qué los datos de canal pueden variar entre Advertising Cloud y  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;.

## Diferencias de datos en Adobe Analytics [!DNL Paid Search Detection]

La función [heredada [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) de [!DNL Analytics] permite a las empresas [definir reglas para rastrear el tráfico de búsqueda orgánica y de pago](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) para los motores de búsqueda especificados. Las reglas [!DNL Paid Search Detection] utilizan una cadena de consulta y el dominio de referencia para identificar el tráfico de búsqueda natural y de pago. Los informes [!DNL Paid Search Detection] forman parte del grupo más grande de informes [Métodos de localización](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html), que caducan cuando se produce un evento especificado (como un cierre de compra del carro de compras) o cuando finaliza la visita.

La siguiente es la interfaz para crear un conjunto de reglas [!DNL Paid Search Detection]:

![Ejemplo de una regla de detección de búsqueda de pago establecida en  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Los informes [!DNL Paid Search Detection] resultantes incluyen los informes [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] y [!UICONTROL Natural Search Keywords].

Tenga en cuenta las dos limitaciones siguientes con los datos en los informes [!DNL Paid Search Detection]:

* Los informes [!UICONTROL Paid Search Keywords] y [!UICONTROL Natural Search Keywords] muestran las consultas de búsqueda identificadas por las direcciones URL de referencia, no las palabras clave en las que los usuarios ofertan. Los informes de Advertising Cloud y [!DNL Analytics] muestran las palabras clave reales, por lo que no espere que estén alineadas con los informes de palabras clave [!DNL Paid Search Detection].

* Cuando se creó originalmente la función [!DNL Paid Search Detection], la consulta de búsqueda de origen (la cadena de caracteres que el usuario introdujo en la barra de búsqueda en el motor de búsqueda) estaba más fácilmente disponible para los anunciantes a través de la dirección URL de referencia. En la actualidad, los motores de búsqueda confunden en gran medida la consulta de búsqueda y los informes de palabra clave [!DNL Paid Search Detection] tienen un valor limitado, ya que la mayoría de los datos de consulta caen dentro del estado &quot;sin especificar&quot;.

   Con [!DNL Analytics for Advertising Cloud], los anunciantes aún pueden rastrear palabras clave pagas en [!DNL Analytics]. El dominio de referencia informa al motor de informes sobre el motor de búsqueda que dirigió el tráfico. Dado que la información de cuenta específica del anunciante no está vinculada al dominio de referencia, todo el tráfico se enumera en el motor de búsqueda. Los anunciantes con varias cuentas en el mismo motor de búsqueda deben hacer referencia a los informes de Advertising Cloud o [!DNL Analytics] para los informes específicos de la cuenta.

### ¿Por qué configurar [!DNL Paid Search Detection]?

Los informes [!DNL Paid Search Detection] permiten identificar el tráfico de búsqueda natural en los [[!DNL Analytics Marketing Channels] informes](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html). La separación del tráfico de búsqueda de pago y el tráfico de búsqueda natural es una buena manera de comprender el valor que la búsqueda natural aporta al ecosistema de marketing completo.

## Validación de datos de pulsaciones para [!DNL Analytics for Advertising Cloud] {#data-validation}

Para su integración, debe validar los datos de pulsaciones para asegurarse de que todas las páginas del sitio rastrean correctamente las pulsaciones.

En [!DNL Analytics], una de las formas más sencillas de validar el seguimiento de [!DNL Analytics for Advertising Cloud] es comparar los clics con las instancias mediante la métrica calculada &quot;Clics en instancias de AMO ID&quot;, que se calcula de la siguiente manera:

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] representa el número de veces que se rastrean los ID de AMO (parámetros `s_kwcid` ) en el sitio. Cada vez que se hace clic en un anuncio, se agrega un parámetro `s_kwcid` a la dirección URL de la página de aterrizaje. Por lo tanto, el número de [!UICONTROL AMO ID Instances] es análogo al número de clics y se puede validar frente a los clics de publicidad reales. Normalmente, vemos una tasa de coincidencia del 80 % para [!DNL Search] y una tasa de coincidencia del 30 % para el tráfico [!DNL DSP] (cuando se filtra para incluir solo las pulsaciones [!UICONTROL AMO ID Instances]). La diferencia en las expectativas entre la búsqueda y la visualización se puede explicar por el comportamiento del tráfico esperado. La búsqueda captura la intención y, como tal, los usuarios normalmente tienen la intención de hacer clic en los resultados de búsqueda de su consulta. Sin embargo, es más probable que los usuarios que ven una publicidad de vídeo en pantalla o en línea hagan clic en la publicidad de forma involuntaria y luego reboten del sitio o abandonen la nueva ventana que se carga antes de que se rastree la actividad de la página.

En los informes de Advertising Cloud, también puede comparar los clics con las instancias utilizando la métrica &quot;[!UICONTROL ef_id_instances]&quot; en lugar de [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Aunque se espera una tasa de coincidencia alta entre el ID de AMO y el ID de EF, no se espera una paridad del 100 % porque el ID de AMO y el ID de EF rastrean fundamentalmente datos diferentes, y esta diferencia puede provocar ligeras diferencias en el total [!UICONTROL AMO ID Instances] y [!UICONTROL EF ID Instances]. Sin embargo, si el total [!UICONTROL AMO ID Instances] en [!DNL Analytics] difiere de [!UICONTROL EF ID Instances] en Advertising Cloud en más del 1%, póngase en contacto con el administrador de cuentas de Adobe para obtener ayuda.

Para obtener más información sobre el AMO ID y el EF ID, consulte [Advertising Cloud IDs used by Analytics](ids.md).

A continuación se muestra un ejemplo de un espacio de trabajo para rastrear clics en instancias.

![Ejemplo de un espacio de trabajo para rastrear clics en instancias](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Comparación de conjuntos de datos en [!DNL Analytics for Advertising Cloud] frente a en Advertising Cloud

El [AMO ID](ids.md) (parámetro de cadena de consulta s_kwcid) se utiliza para los informes en [!DNL Analytics] y el [EF ID](ids.md) se utiliza para los informes en Advertising Cloud. Como son valores distintos, es posible que un valor se dañe o no se añada a la página de aterrizaje.

Por ejemplo, supongamos que tenemos la siguiente página de aterrizaje:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

donde el ID de EF es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id`&quot;.

Si se produce un redireccionamiento del lado del sitio, la dirección URL podría terminar así:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

donde el ID de EF es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id#redirectAnchorTag`&quot;.

En este ejemplo, la adición de la etiqueta delimitadora agrega caracteres inesperados al ID de AMO, lo que da como resultado un valor que Analytics no reconoce. Este ID de AMO no se clasificaría y las conversiones asociadas a él caerían dentro de &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; en los informes [!DNL Analytics].

Afortunadamente, mientras que problemas como este son comunes, normalmente no resultan en un alto porcentaje de discrepancia. Sin embargo, si observa una gran discrepancia entre los ID de AMO en [!DNL Analytics] y los ID de EF en Advertising Cloud, póngase en contacto con el administrador de cuentas de Adobe para obtener ayuda.

## Otras consideraciones de métricas

### La diferencia entre clics y visitas {#clicks-vs-visits}

Parecen análogos, pero los clics y las visitas representan datos diferentes:

* **Haga clic en:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Visita:** [!DNL Analytics] define una  [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) visitas una serie de vistas de página por un usuario, que finalizan según uno de varios criterios, como 30 minutos de inactividad.

Por definición, un clic puede llevar a varias visitas.

Consideremos el siguiente ejemplo: Tanto el usuario 1 como el usuario 2 acceden a un sitio haciendo clic en una publicidad para Advertising Cloud. El usuario 1 ve cuatro páginas y luego sale del día, por lo que el clic inicial resulta en una visita. El usuario 2 ve dos páginas, deja un almuerzo de 45 minutos, regresa, ve dos páginas más y luego se marcha; en este caso, el clic inicial resulta en dos visitas.

![Ejemplo de la diferencia entre clics y visitas](/help/integrations/assets/a4adc-visits-example.png)

### Diferencia entre clics y pulsaciones

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Los clics y las pulsaciones son dos métricas diferentes:

* **Haga clic en:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Pulsaciones:** [!DNL Analytics] registra una pulsación cuando el visitante aterriza en el sitio web de destino, la página de aterrizaje se carga y la  [!DNL Analytics] solicitud situada en la parte inferior de la página envía los datos a  [!DNL Analytics].

Los clics y las pulsaciones pueden variar considerablemente debido a los clics en publicidad accidentales. Hemos observado que la mayoría de los clics en anuncios en pantalla son clics accidentales y que estos visitantes accidentales pulsan el botón Atrás antes de que se cargue la página de aterrizaje, por lo que [!DNL Analytics] no puede registrar una pulsación. Esto es especialmente cierto en el caso de los anuncios en los que es más probable que se produzca un clic accidental, como anuncios para móviles, anuncios de vídeo y anuncios que llenan la pantalla y deben cerrarse para que el usuario pueda ver la página.

Los sitios cargados en dispositivos móviles también tienen menos probabilidades de provocar pulsaciones debido a un ancho de banda menor o a la potencia de procesamiento disponible, lo que hace que las páginas de aterrizaje tarden más en cargarse. No es inusual que entre el 50 y el 70 % de los clics no produzcan pulsaciones. En entornos móviles, la diferencia puede llegar a ser del 90 % debido a la combinación de un explorador más lento y a la mayor probabilidad de que el usuario haga clic accidentalmente en la publicidad mientras se desplaza por la página o intenta cerrarla.

Los datos de clics también se pueden registrar en entornos que no pueden registrar pulsaciones con los mecanismos de seguimiento actuales (como clics que entran o salen de una aplicación móvil) o para los que el anunciante implementó solo un método de seguimiento (por ejemplo, con el método de visualización de JavaScript, los navegadores que bloquean cookies de terceros rastrearán clics, pero no pulsaciones). Un motivo clave por el que Adobe recomienda implementar tanto el rastreo de direcciones URL de clic como los enfoques de seguimiento JavaScript de visualización es maximizar la cobertura de las pulsaciones a las que se puede realizar un seguimiento.

### Uso de métricas de tráfico de Advertising Cloud para Dimension que no son de Advertising Cloud

Advertising Cloud proporciona a Analytics [métricas de tráfico específicas de publicidad y las dimensiones relacionadas de DSP y Búsqueda](advertising-cloud-metrics-in-analytics.md). Las métricas proporcionadas por Advertising Cloud solo se aplican a las dimensiones de Advertising Cloud especificadas y los datos no están disponibles para otras dimensiones en [!DNL Analytics].

Por ejemplo, si ve las métricas [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] por cuenta, que es una dimensión de Advertising Cloud, verá el total [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] por cuenta.

![Ejemplo de métricas de Advertising Cloud en un informe que utiliza una dimensión de Advertising Cloud](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Sin embargo, si ve las métricas [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] por una dimensión en la página (como Página), para la cual Advertising Cloud no proporciona datos, entonces las métricas [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] de cada página serán de cero (0).

![Ejemplo de métricas de Advertising Cloud en un informe que utiliza una dimensión no admitida](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Uso de [!UICONTROL AMO ID Instances] como sustituto de clics con Dimension que no son de Advertising Cloud

Como no puede usar [!UICONTROL AMO Clicks] con dimensiones en el sitio, es posible que desee encontrar un equivalente a los clics. Puede que esté tentado de usar Visitas como sustituto, pero no son la mejor opción porque cada visitante puede tener múltiples visitas. (Consulte &quot;[La diferencia entre clics y visitas](#clicks-vs-visits).&quot; En su lugar, recomendamos utilizar [!UICONTROL AMO ID Instances], que es el número de veces que se captura el ID de AMO. Aunque [!UICONTROL AMO ID Instances] no coincidirá exactamente con [!UICONTROL AMO Clicks], son la mejor opción para medir el tráfico de clics en el sitio. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising Cloud]](#data-validation)&quot;.

![Ejemplo de  [!UICONTROL AMO ID Instances] en lugar de  [!UICONTROL AMO Clicks] para una dimensión no admitida](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID que utiliza [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Métricas de Advertising Cloud en Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Por qué los datos pueden variar entre Advertising Cloud y [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

