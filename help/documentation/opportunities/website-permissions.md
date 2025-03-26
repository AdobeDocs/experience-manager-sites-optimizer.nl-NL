---
title: Documentatie over opportunity-inhoud website
description: Meer informatie over de mogelijkheden voor websitemachtigingen en hoe u deze kunt gebruiken om de beveiliging van uw website te verbeteren.
badgeSecurityPosture: label="Beveiligingspositie" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Beveiligingspositie"
source-git-commit: c99bd0ab418c1eb0693f39ea16ee41f8a1263099
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Mogelijkheid voor webmachtigingen

![ de toestemmingenkans van de Website ](./assets/website-permissions/hero.png){align="center"}

De mogelijkheid om websitemachtigingen te gebruiken optimaliseert websitemachtigingen, die cruciaal zijn voor het onderhouden van een veilige en beheerbare AEM-omgeving. Met deze mogelijkheid kunt u de toegangsbesturingselementen verfijnen door te ruime machtigingen (zoals `jcr:all` voor algemene paden zoals `/` of `/content` ) te verwijderen en gebruikerstoegang uit te lijnen met het beginsel van de minste bevoegdheden. Door machtigingen te stroomlijnen en redundanties te elimineren, kunt u beveiligingsrisico&#39;s verkleinen, het onderhoud verbeteren en toekomstige fouten voorkomen. Neem actie door toestemmingen in de console van de Toestemmingen van de Veiligheid van AEM of uw codebewaarplaats te herzien en bij te werken, ervoor zorgen de dienstgebruikers slechts de toegang hebben zij werkelijk nodig.

## Automatische identificatie

![ auto-identificeer websitetoestemmingen ](./assets/website-permissions/auto-identify.png){align="center"}

De **eigenschap van de Toestemmingen van de Website** identificeert zich automatisch en maakt een lijst

* **Gebruiker** - de gebruikersrekening met de verdachte toestemming.
* **Weg** - de weg in AEM die door de toestemming wordt beïnvloed.
* **Toestemming** - de toestemming die verdacht is.
* **Uitgave** - wijst op het type van kwestie die de toestemming beïnvloeden.

## Automatisch voorstellen

![ automatisch-stelt websitekwetsbaarheden ](./assets/website-permissions/auto-suggest.png){align="center"} voor

De auto-suggestie verstrekt AI-Gegenereerde aanbevelingen op het **Voorgestelde toestemmingengebied**, toestaand u om het even welke gemarkeerde toestemmingen met veilige alternatieven te vervangen.

## Automatisch optimaliseren

[!BADGE  Ultimate ]{type=Positive tooltip="Ultimate"}

![ auto-optimaliseer websitetoestemmingen ](./assets/website-permissions/auto-optimize.png){align="center"}

Sites Optimizer Ultimate voegt de mogelijkheid toe om automatische optimalisatie te implementeren voor de gevonden kwetsbaarheden.

>[!BEGINTABS]

>[!TAB  stel optimalisering ] op

{{auto-optimize-deploy-optimization-slack}}

>[!TAB  Goedkeuring van het Verzoek ]

{{auto-optimize-request-approval}}

>[!ENDTABS]
