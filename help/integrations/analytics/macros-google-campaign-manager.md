---
title: Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad
description: Descubra por qué y cómo añadir [!DNL Analytics for Advertising Cloud] macros a su [!DNL Google Campaign Manager 360] etiquetas de publicidad
feature: Integration with Adobe Analytics
exl-id: 05084a85-5890-4a82-b3eb-4520f44f9d66
source-git-commit: 7cb39998041d151ece7809adc8a2e872b922e5fc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Google Campaign Manager 360] Etiquetas de publicidad

*Anunciantes con solo integración Advertising Cloud-Adobe Analytics*

*Aplicable solo a Advertising Cloud DSP*

Si utiliza etiquetas de publicidad de [!DNL Google Campaign Manager 360] para sus publicidades de Advertising Cloud DSP, añada Analytics para los parámetros de Advertising Cloud a las URL de su página de aterrizaje mediante el [`%p` macro](https://support.google.com/campaignmanager/table/6096962). El registro de parámetros `s_kwcid` y `ef_id` parámetros de cadena de consulta en la dirección URL de la página de aterrizaje, lo que permite a Advertising Cloud enviar datos de clics sobre los anuncios a Adobe Analytics.

Usar macros para [!DNL Campaign Manager 360] anuncios en pantalla y en vídeo para los siguientes tipos de [!DNL Analytics for Advertising Cloud] implementaciones:

* **Los anunciantes con el [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Código JavaScript implementado en sus sitios web**: El código JavaScript ya registra la variable `s_kwcid` y `ef_id` parámetros de cadena de consulta. Sin embargo, el uso de macros amplía el seguimiento para incluir conversiones basadas en clics cuando no se admiten cookies de terceros. La práctica recomendada es agregar las macros de las secciones siguientes a las etiquetas de publicidad para capturar datos de pulsaciones adicionales que no se capturan a través del código JavaScript.

>[!NOTE]
>
>El código JavaScript es una solución para el rastreo de clics solamente mientras las cookies siguen disponibles. Una vez que se interrumpan las cookies, será necesario implementar las siguientes macros.

* **Anunciantes cuyos sitios web no utilicen la variable [!DNL Analytics for Advertising Cloud] Código JavaScript y, en su lugar, confían en [!DNL Analytics] reenvío del lado del servidor solo para datos de pulsaciones** (sin datos de visualización): Las siguientes macros son necesarias para informar sobre la actividad de clics en el sitio impulsada por los anuncios que compra a través de Advertising Cloud.

## Anexe las macros a su [!DNL Google Campaign Manager 360] Publicidades

Within [!DNL Google Campaign Manager 360], añada el siguiente parámetro a la dirección URL de la página de aterrizaje para cada uno de sus anuncios de vídeo y visualización: `%pamo=!;`

Puede especificar la dirección URL de la página de aterrizaje de varias formas. Las instrucciones para cada opción se incluyen en las siguientes subsecciones.

A continuación se muestra un ejemplo de la dirección URL de la página de aterrizaje con el sufijo .

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* Si la dirección URL de la página de aterrizaje incluye un símbolo hash (#), que no es común, coloque la variable `amo` antes del símbolo hash.
>* Si no se incluyen otros parámetros después de la variable `amo` y, a continuación, agregue un parámetro (por ejemplo, &amp;a=b) después de él. Ejemplo:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### Configuración del sufijo de dirección URL de la página de aterrizaje a nivel del anunciante

1. En el menú principal, haga clic en el [!UICONTROL Advertisers] pestaña .
1. Haga clic en el nombre del anunciante.
1. En el [!UICONTROL Landing page URL suffix] configuración, incluir `%pamo!;` en el [!UICONTROL URL suffix] campo .

![configuración a nivel del anunciante](/help/integrations/assets/macro-ggl360-advertiser.png)

### Configuración del sufijo de dirección URL de la página de aterrizaje de nivel de campaña

1. En el menú principal, haga clic en el [!UICONTROL Campaigns] pestaña .
1. Haga clic en el nombre de la campaña.
1. Haga clic [!UICONTROL Properties].
1. En el [!UICONTROL Landing page URL suffix] configuración, incluir `%pamo!;` en el [!UICONTROL URL suffix] campo .

![configuración de nivel de campaña](/help/integrations/assets/macro-ggl360-campaign.png)

### Configuración del sufijo de URL de la página de aterrizaje de nivel creativo

1. En el menú principal, haga clic en el [!UICONTROL Campaigns] pestaña .
1. Haga clic en el nombre de la campaña.
1. En el [!UICONTROL Views] seleccione [!UICONTROL Creatives].
1. Haga clic en el nombre del creativo.
1. En el [!UICONTROL Click tags] configuración, incluir `%pamo!;` en el [!UICONTROL Landing page] para la etiqueta de clic.

![ajustes de nivel creativo](/help/integrations/assets/macro-ggl360-creative.png)

## Cómo [!DNL Analytics for Advertising Cloud] Las macros se expanden en DSP

En DSP, al crear una publicidad que incluya la variable [!DNL Analytics for Advertising Cloud] parámetro (`amo`), el `ef_id` y `s_kwcid` las macros se añaden automáticamente a la URL de clic. La práctica recomendada es comprobar la etiqueta en DSP para asegurarse de que la variable `ef_id` y `s_kwcid` las macros están presentes.

El siguiente es un ejemplo de [!DNL Google Campaign Manager 360] [etiqueta ins](https://support.google.com/campaignmanager/answer/6080468) tal como aparece en DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Cuando un usuario hace clic en la publicidad, [!DNL Google Campaign Manager 360] seen `%pamo` en el sufijo URL e inserta dinámicamente el valor de la variable `amo` en la dirección URL.


>[!MORELIKETHIS]
>
>* [Información general sobre [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud ID que utiliza [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anexar [!DNL Analytics for Advertising Cloud] Macros a [!DNL Flashtalking] Etiquetas de publicidad](macros-flashtalking.md)

