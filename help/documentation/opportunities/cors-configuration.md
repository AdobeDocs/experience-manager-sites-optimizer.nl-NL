---
title: Documentatie over de configuratiemogelijkheid van CORS
description: Leer over de de configuratiekans van CORS en om kwetsbaarheid van de plaatsveiligheid te identificeren en te bevestigen.
badgeSecurityPosture: label="Beveiligingspositie" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Beveiligingspositie"
source-git-commit: cb64a34b758de8f5dcea298014ddd0ba79a24c17
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# Mogelijkheid voor CORS-configuratie

![ de configuratiekans van CORS ](./assets/cors-configuration/hero.png){align="center"}

Het correct configureren van het delen van bronnen van oorsprong (CORS) is essentieel voor het beveiligen van webtoepassingen tegen ongeoorloofde gegevenstoegang. Wanneer de header `Access-Control-Allow-Origin` is ingesteld op `*` , kan elk domein reacties aanvragen en ontvangen, waarbij gevoelige informatie mogelijk aan aanvallers wordt getoond. Deze functionaliteit biedt een kans om de beveiliging te versterken door een gecontroleerde lijst van gewenste personen van vertrouwde domeinen te implementeren of CORS uit te schakelen wanneer dit niet vereist is. Door een veilige installatie van CORS te garanderen, helpt u persoonlijke inhoud te beschermen en zorgt u voor naadloze toegang voor geautoriseerde gebruikers.

## Automatische identificatie

![ auto-identificeer de configuratiekans van CORS ](./assets/cors-configuration/auto-identify.png){align="center"}

Met Automatisch identificeren kunt u uw website scannen op onjuiste CORS-configuraties en URL&#39;s detecteren die mogelijk zijn voor onbevoegde toegang. Deze URL&#39;s worden in de bovenste tabel weergegeven, samen met de volgende details:

* **prefix van de Pagina** - de URL wegprefix die aan misconfiguration CORS kwetsbaar is.
* **Voorbeeld van de Pagina** - een voorbeeld URL die aan onbevoegde toegang vatbaar is.

## Automatisch voorstellen

![ auto-stelt de configuratiekans van CORS voor ](./assets/cors-configuration/auto-suggest.png){align="center"}

De auto-voorstellen verstrekt van **dossiers van de code van de Toepassing** en hun **Lijnen** om worden herzien die laks beleid van CORS kunnen plaatsen.


## Automatisch optimaliseren

[!BADGE  Ultimate ]{type=Positive tooltip="Ultimate"}

>[!BEGINTABS]

>[!TAB  stel optimalisering ] op

{{auto-optimize-deploy-optimization-slack}}

>[!TAB  Goedkeuring van het Verzoek ]

{{auto-optimize-request-approval}}

>[!ENDTABS]
