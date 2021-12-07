---
title: Al usar la variable [!DNL Last Event Service] Biblioteca JavaScript con [!DNL Web SDK]
description: Aprenda los pasos para evitar usar la variable [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising Cloud] implementación.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# Al usar la variable [!DNL Last Event Service] Biblioteca JavaScript con Adobe Experience Platform [!DNL Web SDK]

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

Si su organización utiliza el Adobe Analytics heredado `visitorAPI.js` biblioteca para la recopilación de datos, si lo desea, puede cambiar a mediante el [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) biblioteca (`alloy.js`), que le permite interactuar con los distintos servicios de Experience Cloud a través de la variable [!DNL Edge Network].

La variable [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] La biblioteca JavaScript, tal cual está, registra los eventos de visualizaciones y pulsaciones y los vincula a las conversiones asociadas con un ID suplementario (`SDID`). La variable [!DNL Web SDK] sin embargo, la biblioteca no proporciona un [!DNL stitch ID]. Para usar la variable [!DNL Web SDK] para [!DNL Analytics for Advertising Cloud], deberá modificar 1) el [!DNL Last Event Service] etiqueta que utilice en sus páginas web y 2) en su [!DNL Web SDK] `sendEvent` comandos en consecuencia.

## Paso 1: Edite su [!DNL Last Event Service] Etiqueta para generar un `[!DNL StitchID]`

En el [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] etiqueta que utilice en sus páginas web, agregue código para generar el `[!DNL StitchID]` usar el generador de ID aleatorio que está empaquetado en la biblioteca.

**Etiqueta heredada:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Nueva etiqueta:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Paso 2: Uso [!DNL Web SDK] para enviar la variable [!DNL StitchID] como datos XDM para [!DNL Analytics]

Inserte la siguiente propiedad dentro de su [!DNL Web SDK] `sendEvent` para enviar la variable [!DNL StitchID] a [!DNL Experience Edge] como [!DNL Experience Data Model] (XDM) para [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilizará el valor como un `SDID`.

**Propiedad que se va a añadir:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Ejemplo:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Código JavaScript para [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/javascript.md)

