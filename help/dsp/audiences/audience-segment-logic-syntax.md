---
title: Sintaxis para la lógica del segmento de audiencia
description: Haga referencia a la sintaxis que puede utilizar para definir la lógica de los segmentos de audiencia.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: efd04189de975f8f075dec7851a3a06d2d647ded
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Sintaxis para la lógica del segmento de audiencia

Al crear audiencias reutilizables, puede definir manualmente la lógica del segmento mediante ID de segmento alfanuméricos (claves) y la siguiente sintaxis:

* () para indicar un grupo
* `||` para [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; para [!DNL AND]
* ! para [!DNL NOT] (excluir)

>[!NOTE]
>
>* Todos los grupos de segmentos especificados se incluyen a menos que estén precedidos de ! (que los excluye).
>* Puede [buscar el ID de segmento de una audiencia](reusable-audience-clipboard.md) from [!UICONTROL Audiences] > [!UICONTROL All audiences].


Por ejemplo, la siguiente lógica:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (en inglés normal)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>En la configuración de ubicación, puede usar audiencias guardadas como audiencias para segmentar explícitamente o como audiencias independientes para excluir de la segmentación. Asegúrese de que la lógica del segmento refleje el propósito para el que va a utilizar la audiencia.

>[!MORELIKETHIS]
>
>* [Copiar la clave de segmento para una audiencia reutilizable en el portapapeles](reusable-audience-clipboard.md)
>* [Acerca de la gestión de público](audience-about.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)

