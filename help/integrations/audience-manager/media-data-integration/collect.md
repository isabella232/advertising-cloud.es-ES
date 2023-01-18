---
title: Recopilar datos de clics e impresiones de campañas de publicidad DSP
description: Aprenda a capturar impresiones basadas en cookies y eventos de clics de anuncios DSP anuncios mediante píxeles de Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Recopilación de datos de exposición de medios de campañas de DSP publicitarias

*Anunciantes con solo DSP publicitario*

*Anunciantes con Adobe de solo integración de Advertising-Adobe Audience Manager*

En este documento se explica cómo etiquetar anuncios publicitarios DSP anuncios para capturar impresiones basadas en cookies y eventos de clics mediante píxeles de Audience Manager, así como las tareas adicionales necesarias para utilizar los datos.

Los píxeles de evento no capturan eventos que se producen en entornos sin cookies, como aplicaciones móviles y TV conectada (CTV).

## Paso 1: Configuración de una fuente de datos en el Audience Manager {#set-up-data-source}

En el Audience Manager, cree un [fuente de datos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) para los datos de impresión y clic de DSP. Incluir el ID de fuente de datos [en cada etiqueta de evento](#implement-dsp-pixels) de modo que todos los eventos rastreados se atribuyan al origen de datos.

>[!NOTE]
> Es posible recopilar todos los datos de impresión y clics para campañas publicitarias que se ejecuten en varios DSP dentro de una única fuente de datos.

## Paso 2: Implementar la impresión y los píxeles de eventos de clic en las páginas web {#implement-dsp-pixels}

Los anunciantes pueden crear e implementar etiquetas de evento para sus propias marcas. Si es necesario, póngase en contacto con su asesor de Adobe Audience Manager o con su [!DNL Adobe] administrador de cuentas para obtener asistencia.

>[!NOTE]
>
>Si su organización utiliza [!DNL Analytics] , es posible que no necesite el rastreo de clics del Audience Manager. Adobe Analytics captura las señales de clic y las puede enviar al Audience Manager a través de [reenvío del lado del servidor](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Sintaxis de píxeles

Los píxeles de evento deben incluir los siguientes parámetros.

**Píxeles de seguimiento de impresión:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

**Píxeles de rastreo de clics:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

con [parámetros adicionales opcionales](#parameters) con el prefijo `&`

Donde:

* `[Audience Manager customer domain]` es el nombre de dominio al que se envían eventos de impresión o clic [!DNL Adobe].

* `[source id]` es el ID de la variable [fuente de datos](#set-up-data-source) en el que realizará un seguimiento de los datos de DSP impresión y clics.

* `[redirect URL]` es la dirección URL de redireccionamiento con codificación doble. Si utiliza una herramienta de codificación en línea, como www.urlencoder.org, ejecute la cadena a través del codificador y vuelva a codificar el resultado.

* `${TM_CAMPAIGN_ID_NUM}` es el ID numérico de campaña de DSP. Si desea codificar de forma rígida un ID de campaña individual en lugar de usar la macro de DSP, busque el ID en la configuración de la campaña.

* Cada [parameter](#key-value-pairs) tiene el prefijo `&` y tiene el formato `d_parameter=parameter_id`, donde `parameter` se reemplaza por el par clave-valor para el nuevo campo. Ejemplo: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parámetros como pares de clave-valor {#parameters}

**Formato:**  `d_parameter=parameter_id`

    donde:
    
    * el parámetro lleva el prefijo &quot;&amp;`
    
    * `parámetro` se reemplaza por el par clave-valor para el nuevo campo
    
    Ejemplo: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}`

Ambos tipos de píxeles pueden contener parámetros adicionales como *pares clave-valor* para recopilar características o proporcionar metadatos de campaña (como un nombre de ubicación o un nombre de campaña) para otros informes. Un par clave-valor consta de dos elementos relacionados: a *key*, que es una constante que define el conjunto de datos y un *value*, que es una variable que pertenece al conjunto.

En el par clave-valor, la variable de valor puede ser un ID codificado o un *macro*, que es una pequeña unidad de código independiente que se sustituye dinámicamente por los valores correspondientes cuando se carga la etiqueta de publicidad para el seguimiento de usuarios y campañas. Para los parámetros relacionados con la campaña, puede utilizar [DSP macros](/help/dsp/campaign-management/macros.md) en lugar de macros de Audience Manager para enviar atributos de campaña junto con los datos de impresión o clic correspondientes al Audience Manager, utilizando un solo píxel en todos los anuncios. Las DSP macros que inserte en los píxeles del evento deben ser valores adecuados para los pares clave-valor que incluya dentro de los píxeles. Por ejemplo, para la variable `d_placement` , utilice la macro DSP `${TM_PLACEMENT_ID_NUM}` como valor para capturar las ID de colocación generadas por la macro Publicidad de Adobe.

Para obtener una lista de macros compatibles con el Audience Manager para los píxeles de eventos de impresión, consulte &quot;[Captura de los datos de impresión de campaña a través de Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Para obtener una lista de macros compatibles con el Audience Manager para los píxeles de eventos de clic, consulte &quot;[Captura de los datos de campaña por clic a través de Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* La práctica recomendada es incluir la campaña, la ubicación, el elemento creativo (publicidad) y los ID de sitio para poder usar los atributos de campaña para crear características de Audience Manager.
>* Para crear informes de Audience Optimization, se necesitan parámetros adicionales.
>* En los pares clave-valor, reemplace los valores por los correspondientes [DSP macros](/help/dsp/campaign-management/macros.md) de este modo, puede utilizar un solo píxel en todos los anuncios de todas las campañas. Por ejemplo, cambie `d_campaign=[%campaignID%]`a `d_campaign=${TM_CAMPAIGN_ID_NUM}` para capturar los ID de campaña generados por la macro Publicidad de Adobe .
>* Si es necesario, puede crear sus propios parámetros con valores codificados. Ejemplo: `d_DSP=AdCloud`


Ejemplo de píxel de evento de impresión:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Dónde añadir los píxeles

#### Píxel de seguimiento de impresión

Adjunte un píxel de seguimiento de eventos de impresión a todos los anuncios de su [!DNL DSP] campañas. Puede hacerlo en cualquiera de los siguientes lugares:

* En el nivel de ubicación, que aplica el píxel de forma predeterminada a todos los anuncios de la ubicación. En la sección Seguimiento de la configuración de ubicación, agregue el píxel en la variable [[!UICONTROL Event pixels] field](/help/dsp/campaign-management/placements/placement-settings.md).

* En el nivel de anuncio, que anula los píxeles de evento de nivel de ubicación. En la configuración de publicidad, [crear un píxel de evento en la variable [!UICONTROL Pixel] ficha](/help/dsp/campaign-management/ads/ad-edit.md).

* (Para anuncios en un servidor de publicidad de terceros) En el nivel de publicidad dentro del servidor de publicidad.

#### Píxel de rastreo de clics

Dentro del servidor de publicidad, inserte el píxel del evento de clic (con la URL codificada anexada) donde normalmente inserte la URL de pulsación de la publicidad.

## Paso 3: Tareas posteriores a la implementación

Una vez implementadas las etiquetas de evento, los datos fluirán a los servidores de recopilación de datos del Audience Manager. Complete las siguientes tareas antes de poder utilizar los datos en los informes.

### Cree un [!DNL Amazon S3] Cubo y fuente de datos

Una vez que los datos se encuentran en los servidores de Audience Manager, debe crear una [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) y, a continuación, una fuente de datos, a la que se enviarán todos los datos de píxeles. Póngase en contacto con su asesor de Audience Manager o [Servicio de atención al cliente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) si necesita asistencia técnica.

### Crear rasgos y segmentos de Audience Manager

Los datos del evento fluirán a Audience Manager como [señales no utilizadas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Crear manualmente [características basadas en reglas](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) a partir de los datos introducidos y, a continuación, cree [segmentos](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) con estos rasgos, antes de poder usar los datos en los informes.

Ejemplo de característica que rellena datos de nivel de usuario para usuarios expuestos a un creativo específico en DSP:

1. Identifique el evento como `d_event = imp`.
1. Identifique el ID creativo dentro de la campaña de DSP y luego asígnelo como `d_creative=[Creative ID]`.

![Pantalla de creación de características](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
>* [Información general sobre el envío de datos de exposición DSP medios a Adobe Audience Manager](overview.md)
>* [Casos de uso](use-cases.md)

