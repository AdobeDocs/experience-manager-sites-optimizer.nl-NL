---
title: Documentatie over kwetsbaarheden van website
description: Leer meer over de kwetsbaarheden van de website en hoe u deze kunt gebruiken om de beveiliging van uw website te verhogen.
badgeSecurityPosture: label="Beveiligingspositie" type="Caution" url="../../opportunity-types/security-posture.md" tooltip="Beveiligingspositie"
source-git-commit: ab2d75b1d986d83e3303e29a25d2babd1598394a
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---


# Onmogelijkheid voor website

![ de kwetsbaarheidskans van de Website ](./assets/website-vulnerabilities/hero.png){align="center"}

De kans op websitekwetsbaarheden identificeert beveiligingskwetsbaarheden in de bibliotheken van derden die door uw toepassingscode worden gebruikt. Deze kwetsbaarheden kunnen worden misbruikt door een kwaadwillige aanvaller, die het risico vergroot en de beveiligingspositie van uw website vermindert.

De kans op websitekwetsbaarheden toont een overzicht boven aan de pagina, met inbegrip van het volgende:

* **Gevonden kwesties** - het aantal gevonden kwetsbaarheden, die door het veiligheidsrisico worden gecategoriseerd zij (laag, middelgroot, hoog) vertegenwoordigen.
* **Geaggregeerd veiligheidsrisico** - het algemene veiligheidsrisico aan uw website die op de kwetsbaarheid wordt gebaseerd die door de kans wordt gevonden.

## Automatische identificatie

![ auto-identificeer websitekwetsbaarheden ](./assets/website-vulnerabilities/auto-identify.png){align="center"}

De **eigenschap van de Kans van de Kwetsbaarheid van de Kwetsbaarheid van de Website** identificeert zich automatisch en maakt een lijst van kwetsbaarheid die in derdebibliotheken wordt gevonden die door uw toepassingscode worden gebruikt. Hierin worden de volgende details gegeven:

* **Bibliotheek** - de derdebibliotheek die de kwetsbaarheid bevat. Een enkele bibliotheek kan meerdere kwetsbaarheden hebben.
* **Huidige Versie** - de versie van de bibliotheek momenteel in gebruik.
* **Geadviseerde Versie** - de gesuggereerde versie die de kwetsbaarheid oplost.
* **Score** - de strengheidsclassificatie van de kwetsbaarheid, ook samengevat bij de bovenkant van de pagina.
* **Vulnerability** - het kwetsbaarheidsherkenningsteken, een korte beschrijving, en een verbinding aan het Nationale Gegevensbestand van de Vulnerability (NVD) voor meer details. U opent de NVD-koppeling door op de id of de koppeling naast de beschrijving te klikken.

## Automatisch voorstellen

![ automatisch-stelt websitekwetsbaarheden ](./assets/website-vulnerabilities/auto-suggest.png){align="center"} voor

De auto-suggestie verstrekt AI-Gegenereerde suggesties voor de **Geadviseerde versie** van kwetsbare bibliotheek u zou moeten bevorderen aan. Elke ingang heeft a **Score** die op zijn algemene strengheid wijst, die aan de meest kritieke kwetsbaarheid helpt voorrang geven.

>[!BEGINTABS]

>[!TAB  de details van de Vulnerability ]

Elke kwetsbaarheid bevat een verbinding aan de gedetailleerde informatie in het [ Nationale Gegevensbestand van de Vulnerability (NVD) ](https://nvd.nist.gov/). Als u klikt op de kwetsbaarheidsidentificatie of het koppelingsitem rechts van de beschrijving, gaat u naar de NVD-pagina voor die kwetsbaarheid.

>[!TAB  negeer ingangen ]

U kunt items in de lijst met kwetsbaarheden negeren. Het selecteren van **negeert pictogram** verwijdert de ingang uit de lijst. De genegeerde ingangen kunnen van het **Genegeerde** lusje bij de bovenkant van de opportuniteitspagina opnieuw worden aangehaald.<!---right now it does not seem to be implemented, but the page description mentions this functionality-->

>[!ENDTABS]


## Auto-optimaliseer [!BADGE  Ultimate ]{type=Positive tooltip="Ultimate"}

![ automatisch-optimaliseer website kwetsbaarheid ](./assets/website-vulnerabilities/auto-optimize.png){align="center"}

Sites Optimizer Ultimate voegt de mogelijkheid toe om automatische optimalisatie te implementeren voor de gevonden kwetsbaarheden.

>[!BEGINTABS]

>[!TAB  stel optimalisering ] op

{{auto-optimize-deploy-optimization-slack}}

>[!TAB  Goedkeuring van het Verzoek ]

{{auto-optimize-request-approval}}

>[!ENDTABS]