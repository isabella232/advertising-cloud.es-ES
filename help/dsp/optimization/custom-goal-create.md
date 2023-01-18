---
title: Crear un objetivo personalizado
description: Crear un objetivo personalizado
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Crear un objetivo personalizado

Puede crear objetivos personalizados como *objetivos* en [!DNL Adobe Advertising Search].

Para crear un objetivo personalizado, la cuenta de DSP debe estar vinculada a un [!DNL Search] cuenta con el mismo ID de organización de Adobe Experience Cloud, desde el [!DNL Search] configuración del cliente. Si la cuenta de DSP no está vinculada a un [!DNL Search] póngase en contacto con su [!DNL Adobe] equipo de la cuenta.

>[!TIP]
>
>Consulte la [prácticas recomendadas para crear objetivos personalizados](custom-goal-best-practices.md) para obtener sugerencias sobre cómo configurar los objetivos personalizados.

1. Iniciar sesión [!DNL Adobe Advertising Search] at (empresas estadounidenses) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (empresas de todos los demás países) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Asegúrese de que las métricas que desea incluir en su objetivo se hayan rastreado, estén disponibles en el producto e incluyan un nombre para mostrar:
   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Busque la métrica y asegúrese de que **[!UICONTROL Show in UI and Reports]** está habilitado para la métrica.
   1. Si la métrica no tiene un valor en la variable **[!UICONTROL Display Name]** , haga clic en la celda, introduzca el nombre para mostrar y, a continuación, haga clic en **[!UICONTROL Apply].**
1. Cree el objetivo personalizado como un *objetivo*:
   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. En la barra de herramientas, haga clic en **[!UICONTROL Create objective].**
   1. Introduzca la configuración del objetivo:
      1. En el **[!UICONTROL Change Objective Name]** , introduzca el nombre del objetivo.

         El nombre del objetivo se mostrará en la variable [!UICONTROL Custom Goals] en la configuración del paquete de DSP.

      1. Asociar propiedades con el objetivo:

         >[!NOTE]
         >
         > Todas las propiedades de transacción rastreadas para el anunciante se enumeran de forma predeterminada en la [!UICONTROL Available Properties] lista.

         * Para importar un archivo CSV con propiedades y sus pesos, haga clic en **[!UICONTROL Import]** y busque el archivo que desea importar.

            Las propiedades importadas ya deben existir para el anunciante; los nombres no distinguen entre mayúsculas y minúsculas.

            Las propiedades importadas reemplazan a las propiedades existentes especificadas.

         * Para especificar manualmente la primera propiedad con el peso predeterminado (1), seleccione en una lista de todas las propiedades de transacción rastreadas para el anunciante.

         * Para añadir manualmente otra propiedad con el peso predeterminado (1), haga clic en **[!UICONTROL +]** .

            >[!TIP]
            >
            > Para buscar una propiedad en la lista, introduzca una cadena desde cualquier lugar dentro del nombre de la propiedad.

         * Para agregar manualmente varias propiedades, haga clic en **[!UICONTROL Add Multiple Properties].** Para cada propiedad que desee agregar, haga clic en el nombre de la propiedad en la [!UICONTROL Available Properties] y arrástrela al [!UICONTROL Added Properties] para abrir el Navegador. Cuando termine de agregar propiedades, haga clic en **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Para buscar una propiedad en la lista, introduzca una cadena desde cualquier lugar dentro del nombre de la propiedad en el campo de entrada.
            >* Para filtrar la lista y excluir las propiedades excluidas en los informes, seleccione la opción **[!UICONTROL Hide properties excluded from reports].**


         * (Cuando el objetivo contiene varias propiedades) Para cambiar el peso de una propiedad en relación con las otras propiedades del objetivo, introduzca valores en la variable **[!UICONTROL Weight]** campos.
      1. En la parte inferior de la configuración, haga clic en **[!UICONTROL Save]**.


Una vez creado un objetivo, puede asignarlo a un paquete de DSP como objetivo personalizado cuando el objetivo de optimización sea &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Para obtener un rendimiento óptimo, las métricas combinadas en el objetivo personalizado (objetivo) deben totalizar al menos diez conversiones al día. Cuando no lo hacen, lo mejor es agregar al objetivo eventos de soporte adicionales (propiedades de transacción), como páginas de producto o inicios de aplicación. Consulte [Prácticas recomendadas para crear un objetivo personalizado](custom-goal-best-practices.md) para las directrices.

>[!MORELIKETHIS]
>
>* [Acerca de los objetivos personalizados](custom-goal-about.md)
>* [Prácticas recomendadas para crear un objetivo personalizado](custom-goal-best-practices.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [Cómo DSP las campañas](optimization-how-dsp-optimizes-campaigns.md)

