---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: Acerca de las listas de sitios bloqueados a nivel de cuenta y de anunciante
description: Acerca de las listas de sitios bloqueados a nivel de cuenta y de anunciante
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Acerca de las listas de sitios bloqueados a nivel de cuenta y de anunciante

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
Puede editar la lista de sitios bloqueados que se usa para toda la cuenta de Advertising Cloud y las listas adicionales para anunciantes individuales en la cuenta.

Las listas de sitios bloqueados definen conjuntos de objetivos que se excluirán de las ubicaciones. Cada lista puede constar de dominios de sitio web de nivel superior y de cualquier nivel <!--- verify --> de subdominios (como ejemplo.com, my.example.com o my.new.example.com) y nombres de aplicaciones móviles (como ???)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

Las listas de nivel del anunciante anulan las listas de nivel de cuenta.

>[!NOTE]
>
>* Las listas de sitios bloqueados a nivel de cuenta y de anunciante se aplican además de Advertising Cloud DSP [lista de sitios bloqueados globalmente](/help/dsp/introduction/features/brand-safety-media-quality.md), que incluyen sitios considerados inseguros para los anuncios.
>* Los usuarios también pueden agregar sitios de destino a cualquier ubicación.
>* Las listas de sitios bloqueados siempre anulan las listas de sitios segmentados. Si una colocación excluye e incluye el mismo objetivo para una publicidad, se excluye el objetivo. <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
