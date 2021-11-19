---
title: Advertising Cloud ID que utiliza [!DNL Analytics]
description: Advertising Cloud ID que utiliza [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 1ba45d789c4ad365166df829ac74e0200cdc8851
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 0%

---

# Advertising Cloud ID que utiliza [!DNL Analytics]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Aplicable a Advertising Cloud DSP y Advertising Cloud Search*

Advertising Cloud utiliza dos ID para el seguimiento del rendimiento en el sitio: el *EF ID* y *AMO ID*.

Cuando se produce una impresión de publicidad, Advertising Cloud crea los valores de AMO ID y EF ID y los almacena. Cuando un visitante que ha visto una publicidad entra en el sitio sin hacer clic en una publicidad, [!DNL Analytics] llama a estos valores desde Advertising Cloud a través de la función [!DNL Analytics for Advertising Cloud] Código JavaScript. Para el tráfico de visualización, [!DNL Analytics] genera un ID suplementario (`SDID`), que se utiliza para unir el ID de EF y el ID de AMO a [!DNL Analytics]. Para el tráfico de pulsaciones, estos ID se incluyen en la dirección URL de la página de aterrizaje mediante la variable `s_kwcid` y `ef_id` parámetros de cadena de consulta.

Advertising Cloud distingue entre una entrada de pulsación o visualización del sitio web utilizando los siguientes criterios:

* Se captura una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio pero no de hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:
   * El visitante no tiene pulsaciones para un [!DNL DSP] o [!DNL Search] durante el [haga clic en ventana retrospectiva](#lookback-a4adc).
   * El visitante ha visto al menos una [!DNL DSP] durante el [ventana retrospectiva de impresión](#lookback-a4adc). La última impresión se pasa como visualización.
* Se captura una entrada de pulsación cuando el visitante de un sitio hace clic en un anuncio antes de entrar al sitio. [!DNL Analytics] captura una pulsación cuando se produce cualquiera de las siguientes condiciones:
   * La dirección URL incluye un ID de EF y un ID de AMO tal y como Advertising Cloud agrega a la dirección URL de la página de aterrizaje.
   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de Advertising Cloud detecta un clic en los últimos dos minutos.

![Basado en vistas de Advertising Cloud [!DNL Analytics] integración](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Basado en vistas de Advertising Cloud [!DNL Analytics] integración*

![Advertising Cloud hace clic en basado en URL [!DNL Analytics] integración](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Advertising Cloud hace clic en basado en URL [!DNL Analytics] integración*

## Advertising Cloud EF ID

El ID de EF es un token único que Advertising Cloud utiliza para asociar la actividad con un clic en línea o una exposición a publicidad. El ID de EF se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o la dimensión rVar (eVar reservado) (Advertising Cloud EF ID) y rastrea cada clic o exposición del anuncio a nivel de dispositivo o navegador individual. Los ID de EF actúan principalmente como claves para enviar [!DNL Analytics] datos en Advertising Cloud para informes y optimización de ofertas en Advertising Cloud.

### Formato de ID de EF

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

donde:

* &lt;*ID de visitante de Advertising Cloud*> es un ID único por visitante (como UhKVaAAABCkJ0mDt). También se denomina *ID de surfer*.

* &lt;*timestamp*> es la hora con el formato AAAAMMDDHHMMSS (por ejemplo, 20190821192533 para el año 2019, Mes 08, Día 21, Hora 19):25:33).

* &lt;*tipo de canal*> es el tipo de canal responsable del clic o la exposición:

   * `d` para hacer clic en un anuncio en pantalla DSP (mostrar pulsación)
   * `i` para obtener una impresión de un anuncio en pantalla DSP (visualización de visualización)
   * `s` para hacer clic en una publicidad de búsqueda (hacer clic en la búsqueda).

Ejemplo `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una [!DNL Analytics] la implementación fuerza el seguimiento de URL a minúsculas y, a continuación, Advertising Cloud no reconocerá el ID de EF. Esto afectará a las ofertas y los informes de Advertising Cloud, pero no afecta a los informes de Advertising Cloud en [!DNL Analytics].

### El Dimension de ID de EF en [!DNL Analytics]

En [!DNL Analytics] para encontrar los datos de ID de EF, busque la variable [!UICONTROL EF ID] dimensión y uso de [!UICONTROL EF ID Instance] métrica.

`EF IDs` están sujetos al límite de 500.000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500.000, todos los nuevos códigos de seguimiento se incluyen en el título del elemento de una línea &quot;[!UICONTROL Low Traffic].&quot; Debido a la posibilidad de que falte fidelidad a los informes, la variable `EF IDs` no están clasificadas y no debe utilizarlas para segmentos ni para generar informes en [!DNL Analytics].

## Advertising Cloud AMO ID

El ID de AMO rastrea cada combinación de anuncios única a un nivel menos granular y se utiliza para [!DNL Analytics] clasificación de datos e ingesta de métricas publicitarias (como impresiones, clics y costes) de Advertising Cloud. El ID de AMO se almacena en un [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensión rVar (AMO ID) y se utiliza exclusivamente para generar informes en [!DNL Analytics].

El ID de AMO también se denomina `s_kwcid`, que a veces se denomina &quot;el calamar&quot;.

### Formato de ID de AMO para [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

donde:

* &lt;*ID de canal*> puede ser:

   * `AC` = Advertising Cloud DSP
   * `AL` para Advertising Cloud Search

* &lt;*ID de anuncio*> se utiliza como identificador único generado por Advertising Cloud para un anuncio. Sirve como clave para traducir los metadatos de entidad de Advertising Cloud en legibles [!DNL Analytics] dimensiones.

* &lt;*ID de colocación*> es un identificador único generado por Advertising Cloud para una ubicación. Sirve como clave para traducir los metadatos de entidad de Advertising Cloud en legibles [!DNL Analytics] dimensiones.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

Ejemplo de ID de AMO: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### Formato de ID de AMO para [!DNL Search]

ID de AMO para [!DNL Search] siga un formato distinto para cada motor de búsqueda. El formato de todos los motores de búsqueda comienza con lo siguiente:

```AL!{ef_userid}!{ef_sid}```

donde:

* `AL` es el ID de canal para el canal de búsqueda.
* `{ef_userid}` es el ID de usuario numérico único que Advertising Cloud asigna al anunciante.
* `{ef_sid}` es el ID numérico que Advertising Cloud utiliza para el motor de búsqueda especificado, como `3` para [!DNL Google Ads] o `10` para [!DNL Microsoft Advertising].

Los siguientes son los formatos de AMO ID completos para un par de motores de búsqueda. Para obtener formatos de AMO ID para otros motores de búsqueda, póngase en contacto con su [!DNL Adobe] administrador de cuentas.

Formato de ID de AMO para [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

donde:

* `{creative}` es la variable [!DNL Google Ads] ID numérica única para el creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó la publicidad: `e` para exacto, `p` para frase, o `b` en general.
* `{placement}` es el nombre de dominio del sitio web en el que se hizo clic en el anuncio. Hay un valor disponible para los anuncios de campañas con objetivo de ubicación y para los anuncios de campañas con objetivo de palabra clave que se muestran en los sitios de contenido.
* `{network}` indica la red desde la que se produjo el clic:  `g` para [!DNL Google] buscar (solo para anuncios con objetivo de palabra clave), `s` para un socio de búsqueda (solo para anuncios con objetivo de palabra clave), o `d` para la red de visualización (para anuncios dirigidos a palabras clave o a ubicaciones).
* `{keyword}` es la palabra clave específica que activó la publicidad (en los sitios de búsqueda) o la palabra clave que mejor coincidió (en los sitios de contenido).

Formato de ID de AMO para [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

donde:

* `{AdId}` es la variable [!DNL Microsoft Advertising] ID numérica única para el creativo.
* `{OrderItemId}` es la variable [!DNL Microsoft Advertising] ID numérica de la palabra clave.

### Dimension de AMO ID en [!DNL Analytics]

En los informes de Analytics, puede encontrar los datos del ID de AMO buscando la variable [!UICONTROL AMO ID] dimensión y uso de [!UICONTROL AMO ID Instance] métrica. La variable [!UICONTROL AMO ID] contiene todos los valores de ID de AMO capturados, mientras que la dimensión [!UICONTROL AMO ID Instance] indica la frecuencia con la que el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic en el mismo anuncio de búsqueda cuatro veces pero Analytics rastreó siete entradas del sitio, entonces [!UICONTROL AMO ID Instance] sería de siete (7) y [!UICONTROL Clicks] sería de cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics], se recomienda utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud&quot;.

## Acerca de las clasificaciones de Analytics

En [!DNL Analytics], [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Advertising Cloud categoriza los datos sin procesar de Advertising Cloud mediante clasificaciones para que pueda mostrar los datos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) cuando genere informes. Las clasificaciones forman la base de los informes de Advertising Cloud en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]y [!UICONTROL AMO Clicks], así como con eventos personalizados y estándar en el sitio como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud](data-variances.md)

