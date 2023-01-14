---
title: Variaciones de datos previstas entre [!DNL Analytics] y publicidad de Adobe
description: Variaciones de datos previstas entre [!DNL Analytics] y publicidad de Adobe
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# Variaciones de datos previstas entre [!DNL Analytics] y publicidad de Adobe

*Anunciantes con Adobe de solo integración de Advertising-Adobe Analytics*

Los anunciantes con el [!DNL Analytics for Advertising] <!-- (A4AdC) --> la integración rastrea la publicidad de pago a través de Adobe Advertising y Adobe Analytics. Al rastrear medios, campañas y canales a través de varios sistemas, los mismos conjuntos de datos de diferentes sistemas rara vez coinciden por completo. En este documento se explica cómo debe esperar que los datos de los medios que se trafican a través de la publicidad de Adobe se comparen con los datos de los diferentes sistemas en los que se realiza un seguimiento de los medios dentro de [!DNL Analytics].

>[!NOTE]
>
>Este documento se centra en Adobe Advertising and Analytics, pero muchos de los puntos clave también se pueden transferir a otras soluciones de seguimiento.

## Diferencias de atribución en informes similares

### Modelos de atribución y Windows de retrospectiva potencialmente diferentes

La variable [!DNL Analytics for Advertising] la integración utiliza dos variables (eVars o rVars \[eVars reservadas]\) para capturar la variable [EF ID y AMO ID](ids.md). Estas variables se configuran con una sola ventana retrospectiva (el tiempo dentro del cual se atribuyen las pulsaciones y las visualizaciones) y con un modelo de atribución. A menos que se especifique lo contrario, las variables están configuradas para que coincidan con el modelo predeterminado de retrospectiva de clics a nivel del anunciante y con el modelo de atribución en Publicidad de Adobe.

Sin embargo, las ventanas retrospectivas y los modelos de atribución se pueden configurar tanto en Analytics (a través de las eVars) como en Publicidad de Adobe. Además, en la publicidad de Adobe, el modelo de atribución es configurable no solo a nivel del anunciante (para la optimización de la oferta), sino también dentro de informes y vistas de datos individuales (solo para fines de informes). Por ejemplo, es posible que una organización prefiera utilizar el modelo de atribución de distribución par para la optimización, pero use la atribución de último contacto para los informes de Advertising DSP o [!DNL Advertising Search]. Al cambiar los modelos de atribución, se cambia el número de conversiones atribuidas.

Si se modifica una ventana retrospectiva de informes o un modelo de atribución en un producto y no en el otro, los mismos informes de cada sistema mostrarán datos diferentes:

* **Ejemplo de discrepancias causadas por diferentes ventanas retroactivas:**

   Supongamos que la publicidad de Adobe tiene una ventana retrospectiva de clics de 60 días y [!DNL Analytics] tiene una ventana retrospectiva de 30 días. Y supongamos que un usuario llega al sitio a través de un anuncio de Adobe rastreado por publicidad, se marcha y luego vuelve el día 45 y se convierte. La publicidad de Adobe atribuirá la conversión a la visita inicial porque la conversión se produjo dentro de la ventana retrospectiva de 60 días. [!DNL Analytics]sin embargo, no se puede atribuir la conversión a la visita inicial porque la conversión se produjo después de que caducara la ventana retrospectiva de 30 días. En este ejemplo, la publicidad de Adobe informaría de un número mayor de conversiones que [!DNL Analytics] lo haría.

   ![Ejemplo de una conversión atribuida en publicidad de Adobe pero no en [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Ejemplo de discrepancias causadas por diferentes modelos de atribución:**

   Supongamos que un usuario interactúa con tres anuncios publicitarios de Adobe diferentes antes de la conversión, con los ingresos como tipo de conversión. Si un informe Publicidad de Adobe utiliza un modelo de distribución uniforme para la atribución, entonces atribuirá los ingresos de manera uniforme en todos los anuncios. If [!DNL Analytics] no obstante, utiliza el modelo de atribución de último contacto y, a continuación, atribuirá los ingresos al último anuncio. En el siguiente ejemplo, la publicidad de Adobe atribuye un valor de 10 USD de los 30 USD de ingresos capturados a cada uno de los tres anuncios, mientras que [!DNL Analytics] atribuye todos los 30 USD de ingresos al último anuncio visto por el usuario. Al comparar informes de publicidad de Adobe y [!DNL Analytics], puede esperar ver el impacto de la diferencia en la atribución.

   ![Diferentes ingresos atribuidos a la publicidad de Adobe y [!DNL Analytics] basado en diferentes modelos de atribución](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>La práctica recomendada es utilizar las mismas ventanas de retrospectiva y el mismo modelo de atribución tanto en la Publicidad de Adobe como [!DNL Analytics]. Trabaje con su [!DNL Adobe] equipo de la cuenta según sea necesario para identificar la configuración actual y mantener las configuraciones sincronizadas.

Estos mismos conceptos se aplican a cualquier otro canal similar que utilice diferentes ventanas retroactivas o modelos de atribución.

#### Distintas ventanas de búsqueda para el seguimiento de visualizaciones {#impression-lookback}

En la Publicidad de Adobe, la atribución se basa en clics e impresiones, y puede configurar diferentes ventanas retrospectivas para clics y para impresiones. En [!DNL Analytics]sin embargo, la atribución se basa en pulsaciones y visualizaciones, y no tiene la opción de establecer distintas ventanas de atribución para pulsaciones y visualizaciones; para cada inicio en la visita inicial al sitio. Puede producirse una impresión el mismo día o varios días antes de que se produzca una visualización, lo que puede afectar al lugar en el que se inicie la ventana de atribución en cada sistema.

Normalmente, la mayoría de las conversiones de visualización se producen lo suficientemente rápido como para que ambos sistemas atribuyan crédito. Sin embargo, algunas conversiones pueden ocurrir fuera de la ventana de retrospectiva de Adobe Advertising , pero dentro de la ventana [!DNL Analytics] ventana retrospectiva; estas conversiones se atribuyen a la visualización en [!DNL Analytics] pero no a la impresión en Adobe Publicidad.

En el siguiente ejemplo, supongamos que un visitante recibió un anuncio el día 1, realizó una visita de visualización (es decir, visitó la página de aterrizaje del anuncio sin hacer clic previamente en el anuncio) el día 2 y lo convirtió el día 45. En este caso, Adobe Advertising rastrearía al usuario desde los Días 1 a 14 (usando una retrospectiva de 14 días), [!DNL Analytics] rastrearía al usuario desde los días 2 a 61 (usando una retrospectiva de 60 días), y la conversión en el día 45 se atribuiría al anuncio dentro de [!DNL Analytics] pero no dentro de la publicidad de Adobe.

![Ejemplo de conversión de visualización atribuida en [!DNL Analytics] pero no la publicidad de Adobe](/help/integrations/assets/a4adc-viewthrough-example.png)

Otra causa de discrepancias es que, en Publicidad de Adobe, puede asignar conversiones de visualización a un *ponderación de visualización* que es relativo al peso atribuido a una conversión basada en clics. El peso de visualización predeterminado es del 40 %, lo que significa que una conversión de visualización se cuenta como el 40 % del valor de una conversión basada en clics. [!DNL Analytics] no proporciona esta ponderación de las conversiones de visualización. Por lo tanto, por ejemplo, un pedido de ingresos de 100 USD capturado en [!DNL Analytics] se descontará a 40 USD en publicidad de Adobe si utiliza el peso de visualización predeterminado, una diferencia de 60 USD.

Tenga en cuenta estas diferencias al comparar las conversiones de visualización entre la publicidad de Adobe y [!DNL Analytics] informes.

#### Modelos de atribución disponibles

| Atribución de publicidad de Adobe | [!DNL Analytics] Atribución | Asignación de eVar/eVar |
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
>Para la asignación lineal, [!DNL Analytics] atribuye eventos de éxito de forma equitativa a través de todos los valores de eVar dentro de una sola visita, por lo que debe utilizar una asignación lineal con una caducidad de eVar de &quot;Visita&quot;. Sin embargo, para la publicidad, el uso de la atribución lineal conduce a una asignación que no es realmente lineal y a informes menos que ideales. Por ejemplo, si un visitante interactúa con tres publicidades antes de realizar la conversión en tres visitas separadas, solo la publicidad que se haya visto en la última visita se atribuirá a la conversión, no a los tres anuncios.
>
>Además, si se cambia la asignación de conversión a &quot;Lineal&quot; o de &quot;Lineal&quot;, los datos históricos no se mostrarán, lo que puede provocar una exposición incorrecta de los datos en los informes. Por ejemplo, la asignación lineal puede dividir los ingresos entre un número de valores de eVar diferentes. Si cambia la asignación a &quot;Más reciente&quot;, entonces el 100 % de esos ingresos se asocia con el valor único más reciente. Esta asociación puede llevar a conclusiones incorrectas.
>
>Para evitar confusiones, [!DNL Analytics] hace que los datos históricos no estén disponibles en la interfaz de informes. Puede ver los datos del historial si vuelve a cambiar el eVar a la configuración de asignación inicial, aunque no debería cambiar la configuración de asignación de eVar simplemente para acceder a los datos del historial. Adobe recomienda usar un eVar nuevo cuando desee aplicar una nueva configuración de asignación para los datos que ya se están registrando, en lugar de cambiar la configuración de asignación para un eVar que ya tiene una cantidad significativa de datos históricos.

Consulte una lista de [!DNL Analytics] modelos de atribución y sus definiciones en [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Si ha iniciado sesión [!DNL Search], puede encontrar una lista de modelos de atribución en
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Atribución de fecha de evento en publicidad de Adobe

En Publicidad de Adobe, puede notificar los datos de conversión por la fecha de clic/evento asociada (la fecha del evento de clic o impresión) o por la fecha de transacción (la fecha de conversión). El concepto de informe de fechas de clic/evento no existe en [!DNL Analytics]; todas las conversiones rastreadas en [!DNL Analytics] se registran por fecha de transacción. Como resultado, se puede informar de la misma conversión con fechas diferentes en Publicidad de Adobe y [!DNL Analytics]. Por ejemplo, supongamos que un usuario hace clic en un anuncio el 1 de enero y lo convierte el 5 de enero. Si visualiza los datos de conversión por fecha de evento en Publicidad de Adobe, la conversión se registrará en el informe el 1 de enero, cuando se produjo el clic. En [!DNL Analytics], la misma conversión se registraría el 5 de enero.

![Ejemplo de conversión atribuida a fechas diferentes](/help/integrations/assets/a4adc-conversions-based-on.png)

## Atribución en [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] creación de informes](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) le permite configurar reglas para identificar diferentes canales de marketing en función de distintos aspectos de la información de visitas. Puede realizar un seguimiento de los canales de seguimiento de anuncios de Adobe ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]y [!UICONTROL Paid Search]) como [!DNL Marketing Channels] usando la variable `ef_id` parámetro de cadena de consulta para identificar el canal. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Sin embargo, aunque el [!DNL Marketing Channels] Los informes pueden rastrear canales publicitarios de Adobe; es posible que los datos no coincidan con los informes de publicidad de Adobe por varios motivos. Consulte las secciones siguientes para obtener más información.

>[!NOTE]
>
> Los siguientes conceptos principales también se aplican a cualquier seguimiento multicanal que incluya campañas que no se rastrean en la publicidad de Adobe, como la [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (también conocido como el Dimension &quot;Código de seguimiento&quot; o &quot;eVar 0&quot;) y seguimiento de eVar personalizado.

### Modelos de atribución potencialmente diferentes en [!DNL Marketing Channels]

Más [!DNL Marketing Channels] los informes se configuran con [!UICONTROL Last Touch] atribución, para la cual el último canal de marketing detectado se asigna al 100% del valor de conversión. Uso de diferentes modelos de atribución para la variable [!DNL Marketing Channels] los informes y los informes de publicidad de Adobe llevarán a discrepancias en las conversiones atribuidas.

### Una ventana retrospectiva potencialmente diferente en [!DNL Marketing Channels]

La ventana retrospectiva de [!DNL Marketing Channels] se puede personalizar. En Publicidad de Adobe, la ventana de retrospectiva de clics es configurable, aunque una ventana fija de 60 días es común. Si los dos productos utilizan ventanas retrospectivas diferentes, puede esperarse discrepancias en los datos.

### Atribución de canal diferente en [!DNL Marketing Channels]

Los informes publicitarios de Adobe capturan solo los medios pagados que son objeto de tráfico mediante la publicidad de Adobe (búsqueda de pago para [!DNL Advertising Search] anuncios y mostrar para anuncios DSP), mientras que [!DNL Marketing Channels] los informes pueden rastrear todos los canales digitales. Esto puede provocar una discrepancia en el canal para el que se atribuye una conversión.

Por ejemplo, la búsqueda de pago y los canales de búsqueda natural suelen tener una relación simbiótica, en la que cada canal ayuda al otro. La variable [!DNL Marketing Channels] atribuirá algunas conversiones a la búsqueda natural que la publicidad de Adobe no hará porque no rastrea la búsqueda natural.

Considere también un cliente que ve un anuncio en pantalla, hace clic en un anuncio de búsqueda de pago, hace clic dentro de un mensaje de correo electrónico y, a continuación, realiza un pedido de 30 USD. Incluso si la publicidad de Adobe y [!DNL Marketing Channels] ambos utilizan el modelo de atribución de último contacto; la conversión seguiría atribuyéndose de forma diferente a cada uno. La publicidad de Adobe no tiene acceso al [!UICONTROL Email] , por lo que acreditaría la búsqueda de pago para la conversión. [!DNL Marketing Channels], sin embargo, tiene acceso a los tres canales, por lo que se acreditaría [!UICONTROL Email] para la conversión.

![Ejemplo de atribución de conversión diferente en Adobe de publicidad [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Para obtener más información sobre por qué las métricas pueden variar, consulte &quot;[Por qué los datos de canal pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Diferencias de datos en Adobe Analytics [!DNL Paid Search Detection]

La variable [heredado [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) en [!DNL Analytics] permite a las empresas [definir reglas para rastrear el tráfico de búsqueda orgánica y de pago](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) para motores de búsqueda especificados. La variable [!DNL Paid Search Detection] las reglas utilizan una cadena de consulta y el dominio de referencia para identificar el tráfico de búsqueda natural y de pago. La variable [!DNL Paid Search Detection] los informes forman parte del grupo más grande de [Métodos de búsqueda](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) , que caducan cuando se produce un evento especificado (como un cierre de compra del carro de compras) o cuando finaliza la visita.

A continuación se muestra la interfaz para crear una [!DNL Paid Search Detection] conjunto de reglas:

![Ejemplo de una regla de detección de búsqueda de pago establecida en [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

El resultado [!DNL Paid Search Detection] los informes incluyen [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]y [!UICONTROL Natural Search Keywords] informes.

Tenga en cuenta las dos limitaciones siguientes con los datos en [!DNL Paid Search Detection] informes:

* La variable [!UICONTROL Paid Search Keywords] y [!UICONTROL Natural Search Keywords] los informes muestran las consultas de búsqueda identificadas por las direcciones URL de referencia, no las palabras clave en las que los usuarios ofrecen. Adobe Publicidad y [!DNL Analytics] los informes muestran las palabras clave reales, por lo que no espere que se alineen con la variable [!DNL Paid Search Detection] informes de palabra clave.

* Cuando la variable [!DNL Paid Search Detection] se creó originalmente, la consulta de búsqueda de origen (la cadena de caracteres que el usuario introdujo en la barra de búsqueda en el motor de búsqueda) estaba más disponible para los anunciantes a través de la dirección URL de referencia. En la actualidad, los motores de búsqueda ocultan en gran medida la consulta de búsqueda y la variable [!DNL Paid Search Detection] los informes de palabra clave tienen un valor limitado, ya que la mayoría de los datos de consulta caen dentro del estado &quot;sin especificar&quot;.

   con [!DNL Analytics for Advertising], los anunciantes aún pueden rastrear palabras clave pagas en [!DNL Analytics]. El dominio de referencia informa al motor de informes sobre el motor de búsqueda que dirigió el tráfico. Dado que la información de cuenta específica del anunciante no está vinculada al dominio de referencia, todo el tráfico se enumera en el motor de búsqueda. Los anunciantes con varias cuentas en el mismo motor de búsqueda deben hacer referencia a la Publicidad de Adobe o [!DNL Analytics] informes para informes específicos de cuenta.

### Por qué configurar [!DNL Paid Search Detection]?

La variable [!DNL Paid Search Detection] los informes permiten identificar el tráfico de búsqueda natural en la variable [[!DNL Analytics Marketing Channels] informes](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). La separación del tráfico de búsqueda de pago y el tráfico de búsqueda natural es una buena manera de comprender el valor que la búsqueda natural aporta al ecosistema de marketing completo.

## Validación de datos de pulsaciones para [!DNL Analytics for Advertising] {#data-validation}

Para su integración, debe validar los datos de pulsaciones para asegurarse de que todas las páginas del sitio rastrean correctamente las pulsaciones.

En [!DNL Analytics], una de las formas más sencillas de validar [!DNL Analytics for Advertising] El seguimiento de es para comparar los clics con las instancias mediante la métrica calculada &quot;Clics en instancias de AMO ID&quot;, que se calcula de la siguiente manera:

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] representa el número de veces que los AMO ID (`s_kwcid` ) se rastrean en el sitio. Cada vez que se hace clic en un anuncio, se llama a `s_kwcid` se agrega a la dirección URL de la página de aterrizaje. El número de [!UICONTROL AMO ID Instances], por lo tanto, es análogo al número de clics y se puede validar con respecto a los clics de publicidad reales. Normalmente, vemos una tasa de coincidencia del 80 % para [!DNL Search] y una tasa de coincidencia del 30 % para [!DNL DSP] tráfico (cuando se filtra para incluir solo pulsaciones) [!UICONTROL AMO ID Instances]). La diferencia en las expectativas entre la búsqueda y la visualización se puede explicar por el comportamiento del tráfico esperado. La búsqueda captura la intención y, como tal, los usuarios normalmente tienen la intención de hacer clic en los resultados de búsqueda de su consulta. Sin embargo, es más probable que los usuarios que ven una publicidad de vídeo en pantalla o en línea hagan clic en la publicidad de forma involuntaria y luego reboten del sitio o abandonen la nueva ventana que se carga antes de que se rastree la actividad de la página.

En los informes Publicidad de Adobe, puede comparar los clics con las instancias que utilizan la variable[!UICONTROL ef_id_instances]&quot; en lugar de [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Aunque se espera una tasa de coincidencia alta entre el ID de AMO y el ID de EF, no se espera una paridad del 100 % porque el ID de AMO y el ID de EF rastrean fundamentalmente datos diferentes, y esta diferencia puede provocar ligeras diferencias en el total [!UICONTROL AMO ID Instances] y [!UICONTROL EF ID Instances]. Si el total [!UICONTROL AMO ID Instances] en [!DNL Analytics] difieren de [!UICONTROL EF ID Instances] sin embargo, en la publicidad de Adobe en más del 1 %, póngase en contacto con su [!DNL Adobe] equipo de la cuenta para obtener ayuda.

Para obtener más información sobre el ID de AMO y el ID de EF, consulte [ID de publicidad de Adobe utilizados por Analytics](ids.md).

A continuación se muestra un ejemplo de un espacio de trabajo para rastrear clics en instancias.

![Ejemplo de un espacio de trabajo para rastrear clics en instancias](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Comparación de conjuntos de datos en [!DNL Analytics for Advertising] Comparación con la publicidad de Adobe

La variable [AMO ID](ids.md) (parámetro de cadena de consulta s_kwcid) se utiliza para generar informes en [!DNL Analytics]y [EF ID](ids.md) se utiliza para generar informes en Adobe Advertising. Como son valores distintos, es posible que un valor se dañe o no se añada a la página de aterrizaje.

Por ejemplo, supongamos que tenemos la siguiente página de aterrizaje:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

donde el ID de EF es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id`.&quot;

Si se produce un redireccionamiento del lado del sitio, la dirección URL podría terminar así:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

donde el ID de EF es &quot;`test_ef_id`&quot; y el ID de AMO es &quot;`test_amo_id#redirectAnchorTag`.&quot;

En este ejemplo, la adición de la etiqueta delimitadora agrega caracteres inesperados al ID de AMO, lo que da como resultado un valor que Analytics no reconoce. Este ID de AMO no se clasificaría y las conversiones asociadas a él caerían en &quot;[!UICONTROL unspecified]&quot; o &quot;[!UICONTROL none]&quot; [!DNL Analytics] informes.

Afortunadamente, mientras que problemas como este son comunes, normalmente no resultan en un alto porcentaje de discrepancia. Sin embargo, si observa una gran discrepancia entre los ID de AMO en [!DNL Analytics] e ID de EF en la publicidad de Adobe, póngase en contacto con su [!DNL Adobe] equipo de la cuenta para obtener ayuda.

## Otras consideraciones de métricas

### La diferencia entre clics y visitas {#clicks-vs-visits}

Parecen análogos, pero los clics y las visitas representan datos diferentes:

* **Haga clic en:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Visita:** [!DNL Analytics] define un [visita](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) como una serie de vistas de página por un usuario, que finalizan según uno de varios criterios, como 30 minutos de inactividad.

Por definición, un clic puede llevar a varias visitas.

Consideremos el siguiente ejemplo: Tanto el usuario 1 como el usuario 2 acceden a un sitio haciendo clic en un anuncio publicitario de Adobe. El usuario 1 ve cuatro páginas y luego sale del día, por lo que el clic inicial resulta en una visita. El usuario 2 ve dos páginas, deja un almuerzo de 45 minutos, regresa, ve dos páginas más y luego se marcha; en este caso, el clic inicial resulta en dos visitas.

![Ejemplo de la diferencia entre clics y visitas](/help/integrations/assets/a4adc-visits-example.png)

### Diferencia entre clics y pulsaciones

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Los clics y las pulsaciones son dos métricas diferentes:

* **Haga clic en:** [!DNL DSP] o el motor de búsqueda registra un clic cuando un visitante hace clic en un anuncio del sitio web de un publicador.

* **Pulsaciones:** [!DNL Analytics] registra una pulsación cuando el visitante aterriza en el sitio web de destino, la página de aterrizaje se carga y la variable [!DNL Analytics] solicitud en la parte inferior de la página envía los datos a [!DNL Analytics].

Los clics y las pulsaciones pueden variar considerablemente debido a los clics en publicidad accidentales. Hemos observado que la mayoría de los clics en anuncios en pantalla son clics accidentales y que estos visitantes accidentales pulsan el botón Atrás antes de que se cargue la página de aterrizaje, por lo que [!DNL Analytics] no se puede registrar una pulsación. Esto es especialmente cierto en el caso de los anuncios en los que es más probable que se produzca un clic accidental, como anuncios para móviles, anuncios de vídeo y anuncios que llenan la pantalla y deben cerrarse para que el usuario pueda ver la página.

Los sitios cargados en dispositivos móviles también tienen menos probabilidades de provocar pulsaciones debido a un ancho de banda menor o a la potencia de procesamiento disponible, lo que hace que las páginas de aterrizaje tarden más en cargarse. No es inusual que entre el 50 y el 70 % de los clics no produzcan pulsaciones. En entornos móviles, la diferencia puede llegar a ser del 90 % debido a la combinación de un explorador más lento y a la mayor probabilidad de que el usuario haga clic accidentalmente en la publicidad mientras se desplaza por la página o intenta cerrarla.

Los datos de clics también se pueden registrar en entornos que no pueden registrar pulsaciones con los mecanismos de seguimiento actuales (como clics que entran o salen de una aplicación móvil) o para los que el anunciante implementó solo un método de seguimiento (por ejemplo, con el método de visualización de JavaScript, los navegadores que bloquean cookies de terceros rastrearán clics, pero no pulsaciones). Un motivo clave por el que Adobe recomienda implementar tanto el rastreo de direcciones URL de clic como los enfoques de seguimiento JavaScript de visualización es maximizar la cobertura de las pulsaciones a las que se puede realizar un seguimiento.

### Uso de métricas de tráfico publicitario de Adobe para Dimension publicitarios que no son de Adobe

La publicidad de Adobe proporciona a Analytics [métricas de tráfico específicas de publicidad y las dimensiones relacionadas de DSP y [!DNL [!DNL Search]]](advertising-metrics-in-analytics.md). Las métricas proporcionadas por la publicidad de Adobe solo se aplican a las dimensiones de publicidad de Adobe especificadas y los datos no están disponibles para otras dimensiones en [!DNL Analytics].

Por ejemplo, si ve la variable [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] métricas por cuenta, que es una dimensión Publicidad de Adobe, entonces verá el total [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] por cuenta.

![Ejemplo de métricas de publicidad de Adobe en un informe que utiliza una dimensión de publicidad de Adobe](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Sin embargo, si ve la variable [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] métricas por una dimensión en la página (como Página), para la cual la publicidad de Adobe no proporciona datos, y luego la variable [!UICONTROL AMO Clicks] y [!UICONTROL AMO Cost] para cada página será cero (0).

![Ejemplo de métricas de publicidad de Adobe en un informe que utiliza una dimensión no admitida](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Uso [!UICONTROL AMO ID Instances] como sustituto de clics con Dimension publicitarios que no sean de Adobe

Como no puede usar [!UICONTROL AMO Clicks] con las dimensiones en el sitio, es posible que desee encontrar un equivalente a los clics. Puede que esté tentado de usar Visitas como sustituto, pero no son la mejor opción porque cada visitante puede tener múltiples visitas. (Consulte[La diferencia entre clics y visitas](#clicks-vs-visits).&quot; En su lugar, se recomienda utilizar [!UICONTROL AMO ID Instances], que es el número de veces que se captura el ID de AMO. While [!UICONTROL AMO ID Instances] no coincidirá [!UICONTROL AMO Clicks] exactamente, son la mejor opción para medir el tráfico de clics en el sitio. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising]](#data-validation).&quot;

![Ejemplo de [!UICONTROL AMO ID Instances] en lugar de [!UICONTROL AMO Clicks] para una dimensión no admitida](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising]](overview.md)
>* [ID de publicidad de Adobe utilizados por [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Métricas de publicidad de Adobe en Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Datos en publicidad de Adobe](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Por qué los datos pueden variar entre la publicidad de Adobe y [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

