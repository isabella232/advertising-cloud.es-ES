---
title: Sintaxis para la lógica del segmento de audiencia
description: Haga referencia a la sintaxis que puede utilizar para definir la lógica de los segmentos de audiencia.
feature: Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Sintaxis para la lógica del segmento de audiencia

Al crear audiencias reutilizables, puede definir manualmente la lógica del segmento mediante ID de segmento alfanuméricos y la siguiente sintaxis:

* () para indicar un grupo
* `||` para  [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; para [!DNL AND]
* ! para [!DNL NOT] (excluir)

>[!NOTE]
>
>* Todos los grupos de segmentos especificados se incluyen a menos que estén precedidos de ! (que los excluye).


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
>* [Acerca de la gestión de público](audience-about.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)

