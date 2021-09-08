---
title: Advertising Cloud ID utilizados por [!DNL Analytics]
description: Advertising Cloud ID utilizados por [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising Cloud ID utilizados por [!DNL Analytics]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Aplicable a Advertising Cloud DSP y Advertising Cloud Search*

Advertising Cloud utiliza dos ID para el seguimiento del rendimiento en el sitio:  el EF ID y el AMO ID.

Cuando se produce una impresión de publicidad, Advertising Cloud crea los valores de AMO ID y EF ID y los almacena. Cuando un visitante que ha visto una publicidad entra en el sitio sin hacer clic en una publicidad, [!DNL Analytics] llama a estos valores desde Advertising Cloud a través del código JavaScript [!DNL Analytics for Advertising Cloud]. Para el tráfico de visualización, [!DNL Analytics] genera un ID suplementario (`SDID`), que se utiliza para unir el ID de EF y el ID de AMO en [!DNL Analytics]. Para el tráfico de pulsaciones, estos ID se incluyen en la dirección URL de la página de aterrizaje mediante los parámetros de cadena de consulta `s_kwcid` y `ef_id`.

Advertising Cloud distingue entre una entrada de pulsación o visualización del sitio web utilizando los siguientes criterios:

* Se captura una entrada de visualización cuando un usuario visita el sitio después de ver un anuncio pero no de hacer clic en él. [!DNL Analytics] registra una visualización si se cumplen dos condiciones:
   * El visitante no tiene pulsaciones para un anuncio [!DNL DSP] o [!DNL Search] durante el [clic en ventana retrospectiva](#lookback-a4adc).
   * El visitante ha visto al menos un [!DNL DSP] anuncio durante la [ventana de retrospectiva de impresión](#lookback-a4adc). La última impresión se pasa como visualización.
* Se captura una entrada de pulsación cuando el visitante de un sitio hace clic en un anuncio antes de entrar al sitio. [!DNL Analytics] captura una pulsación cuando se produce cualquiera de las siguientes condiciones:
   * La dirección URL incluye un ID de EF y un ID de AMO tal y como Advertising Cloud agrega a la dirección URL de la página de aterrizaje.
   * La dirección URL no contiene códigos de seguimiento, pero el código JavaScript de Advertising Cloud detecta un clic en los últimos dos minutos.

![Integración basada en  [!DNL Analytics] vistas de Advertising Cloud](/help/integrations/assets/a4adc-view-through-process.png)

*Figura 1: Integración basada en  [!DNL Analytics] vistas de Advertising Cloud*

![Advertising Cloud hace clic en la  [!DNL Analytics] integración basada en URL](/help/integrations/assets/a4adc-click-through-process.png)

*Figura 2: Advertising Cloud hace clic en la  [!DNL Analytics] integración basada en URL*

## Advertising Cloud EF ID

El ID de EF es un token único que Advertising Cloud utiliza para asociar la actividad con un clic en línea o una exposición a publicidad. El ID de EF se almacena en una dimensión [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o rVar (eVar reservado) (Advertising Cloud EF ID) y realiza un seguimiento de cada clic o exposición publicitarios a nivel individual de explorador o dispositivo. Los ID de EF actúan principalmente como claves para enviar [!DNL Analytics] datos a Advertising Cloud para la creación de informes y la optimización de las ofertas en Advertising Cloud.

### Formato de ID de EF

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

donde:

* &lt;>ID de visitante *de Advertising Cloud > es un ID único por visitante (por ejemplo, UhKVaAAABCkJ0mDt).* También se denomina *ID del internauta*.

* &lt;>timestamp *> es la hora con el formato AAAAMMDDHHMMSS (como 20190821192533 para el año 2019, Mes 08, Día 21, Hora 19:25:33).*

* &lt;>channel type *> es el tipo de canal responsable del clic o la exposición:*

   * `d` para hacer clic en un anuncio en pantalla DSP (mostrar pulsación)
   * `i` para obtener una impresión de un anuncio en pantalla DSP (visualización de visualización)
   * `s` para hacer clic en una publicidad de búsqueda (hacer clic en la búsqueda).

Ejemplo de `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una implementación [!DNL Analytics] fuerza el seguimiento de URL a minúsculas, Advertising Cloud no reconocerá el ID de EF. Esto afectará a las ofertas y los informes de Advertising Cloud, pero no afecta a los informes de Advertising Cloud en [!DNL Analytics].

### El Dimension de ID de EF en [!DNL Analytics]

En los informes [!DNL Analytics], puede encontrar los datos del ID de EF buscando la dimensión [!UICONTROL EF ID] y utilizando la métrica [!UICONTROL EF ID Instance].

`EF IDs` están sujetos al límite de 500.000 identificadores únicos en Analysis Workspace. Una vez que se alcanza el valor de 500.000, todos los nuevos códigos de seguimiento se incluyen en el título de un elemento de línea &quot;[!UICONTROL Low Traffic]&quot;. Debido a la posibilidad de que falte la fidelidad de los informes, `EF IDs` no se clasifican y no se deben usar para segmentos o informes en [!DNL Analytics].

## Advertising Cloud AMO ID

El ID de AMO rastrea cada combinación de publicidad única a un nivel menos granular y se utiliza para la clasificación de datos [!DNL Analytics] y la ingesta de métricas publicitarias (como impresiones, clics y costes) de Advertising Cloud. El ID de AMO se almacena en una [!DNL Analytics] [dimensión de eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o dimensión rVar (ID de AMO) y se utiliza exclusivamente para generar informes en [!DNL Analytics].

El ID de AMO también se denomina `s_kwcid`, que a veces se denomina &quot;calamar&quot;.

### Formato de ID de AMO para [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

donde:

* &lt;>El ID *de canal> puede ser:*

   * `AC` = Advertising Cloud DSP
   * `AL` para Advertising Cloud Search

* &lt;>ID de anuncio *> se utiliza como identificador único generado por Advertising Cloud para un anuncio.* Sirve como clave para traducir los metadatos de entidad de Advertising Cloud en dimensiones [!DNL Analytics] legibles.

* &lt;>ID de colocación *> es un identificador único generado por Advertising Cloud para una ubicación.* Sirve como clave para traducir los metadatos de entidad de Advertising Cloud en dimensiones [!DNL Analytics] legibles.

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

Los ID de AMO para [!DNL Search] siguen un formato distinto para cada motor de búsqueda. El formato de todos los motores de búsqueda comienza con lo siguiente:

```AL!{ef_userid}!{ef_sid}```

donde:

* `AL` es el ID de canal para el canal de búsqueda.
* `{ef_userid}` es el ID de usuario numérico único que Advertising Cloud asigna al anunciante.
* `{ef_sid}` es el ID numérico que Advertising Cloud utiliza para el motor de búsqueda especificado, como  `3` para  [!DNL Google Ads] o  `10` para  [!DNL Microsoft Advertising].

Los siguientes son los formatos de AMO ID completos para un par de motores de búsqueda. Para obtener los formatos de ID de AMO para otros motores de búsqueda, póngase en contacto con el administrador de cuentas de Adobe.

Formato de ID de AMO para [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

donde:

* `{creative}` es el ID numérico  [!DNL Google Ads] único del creativo.
* `{matchtype}` es el tipo de coincidencia de la palabra clave que activó la publicidad:  `e` para exacto,  `p` para frase o  `b` para amplio.
* `{placement}` es el nombre de dominio del sitio web en el que se hizo clic en el anuncio. Hay un valor disponible para los anuncios de campañas con objetivo de ubicación y para los anuncios de campañas con objetivo de palabra clave que se muestran en los sitios de contenido.
* `{network}` indica la red desde la que se produjo el clic:   `g` para la  [!DNL Google] búsqueda (solo para anuncios con objetivo de palabra clave),  `s` para un socio de búsqueda (solo para anuncios con objetivo de palabra clave) o  `d` para la Red de visualización (ya sea para anuncios con objetivo de palabra clave o con objetivo de ubicación).
* `{keyword}` es la palabra clave específica que activó la publicidad (en los sitios de búsqueda) o la palabra clave que mejor coincidió (en los sitios de contenido).

Formato de ID de AMO para [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

donde:

* `{AdId}` es el ID numérico  [!DNL Microsoft Advertising] único del creativo.
* `{OrderItemId}` es el ID  [!DNL Microsoft Advertising] numérico de la palabra clave.

### Dimension de AMO ID en [!DNL Analytics]

En los informes de Analytics, puede encontrar los datos del ID de AMO buscando la dimensión [!UICONTROL AMO ID] y utilizando la métrica [!UICONTROL AMO ID Instance]. La dimensión [!UICONTROL AMO ID] aloja todos los valores de ID de AMO capturados, mientras que la métrica [!UICONTROL AMO ID Instance] indica con qué frecuencia el sitio capturó un valor de ID de AMO. Por ejemplo, si se hizo clic en el mismo anuncio de búsqueda cuatro veces pero Analytics rastreó siete entradas del sitio, entonces [!UICONTROL AMO ID Instance] sería de siete (7) y [!UICONTROL Clicks] sería de cuatro (4).

Para cualquier informe o auditoría dentro de [!DNL Analytics], se recomienda utilizar el ID de AMO junto con su instancia correspondiente. Para obtener más información, consulte &quot;[Validación de datos para [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot; en &quot;Variaciones de datos previstas entre [!DNL Analytics] y Advertising Cloud&quot;.

## Acerca de las clasificaciones de Analytics

En [!DNL Analytics], una [clasificación](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) es un fragmento de metadatos para un código de seguimiento determinado, como Cuenta, Campaña o Anuncio. Advertising Cloud categoriza los datos sin procesar de Advertising Cloud mediante clasificaciones para que pueda mostrar los datos de diferentes maneras (por ejemplo, por tipo de anuncio o campaña) cuando genere informes. Las clasificaciones forman la base de los informes de Advertising Cloud en [!DNL Analytics] y se pueden usar con las métricas de AMO, como [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions] y [!UICONTROL AMO Clicks], así como con eventos en el sitio personalizados y estándar como [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] y [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Variaciones de datos previstas  [!DNL Analytics] entre Advertising Cloud y](data-variances.md)

