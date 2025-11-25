---
title: Preflight instellen
description: Leer hoe u de Preflight-extensie instelt voor AEM Sites Optimizer.
source-git-commit: 2f4ef1c6f44d602bfe365a52eb692fe7faa7f05f
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Preflight instellen

Voor identificatie van de AEM Sites Optimizer Preflight-opportuniteit moet de extensie Preflight zijn ingesteld. U kunt deze instellen in de Universal Editor, in documentvoorvertoning of in de AEM Cloud Service, zodat u Preflight-controles op uw pagina&#39;s kunt uitvoeren voordat deze worden gepubliceerd.

## Gebruikerstoegang inschakelen

Om de Preflight uitbreiding te gebruiken, zorg ervoor dat uw gebruiker aan minstens één van de volgende het productprofielen van AEM Sites Optimizer in [&#x200B; Adobe Admin Console &#x200B;](https://adminconsole.adobe.com) wordt toegewezen:

* AEM Sites Optimizer - Gebruiker automatisch voorstellen
* AEM Sites Optimizer - Gebruiker automatisch optimaliseren

## De extensie Preflight inschakelen

>[!BEGINTABS]

>[!TAB  Universele Redacteur ]

Voer de volgende stappen uit om Preflight in de Universal Editor in te stellen:

1. Open **Extension Manager** bij:
   [&#x200B; https://experience.adobe.com/#/@org/aem/extension-manager/universal-editor](https://experience.adobe.com/#/@org/aem/extension-manager/universal-editor)
1. Bepaal de plaats van **Preflight Uitbreiding van AEM Sites Optimizer** en leg een verzoek voor om het toe te laten.
1. Het **team van Adobe AEM** overzichten en laat de uitbreiding voor uw organisatie toe.
1. Nadat de uitbreiding wordt toegelaten, open een pagina in **Universele Redacteur**, bijvoorbeeld:
   `https://author-p12345-e123456.adobeaemcloud.com/ui#/@org/aem/universal-editor/canvas/author-p12345-e123456.adobeaemcloud.com/content/en/example/home.html`
1. De **Preflight Uitbreiding** verschijnt in **zijspoor**.
1. Selecteer de **Uitbreiding Preflight** van de zijspoor om a **Preflight Controle** van de huidige pagina te beginnen.

>[!TAB  op document-Gebaseerde creatie ]

Voer de volgende stappen uit om Preflight in te stellen voor ontwerpen op basis van document:

1. Voeg de volgende configuratie toe aan `/tools/sidekick/config.json` in de GitHub-opslagplaats van uw Edge Delivery Services-project:

   ```json
   {
     "plugins": [
       {
         "id": "preflight",
         "titleI18n": {
           "en": "Preflight"
         },
         "environments": ["preview"],
         "event": "preflight"
       }
     ]
   }
   ```

1. Maak een nieuw bestand `/tools/sidekick/aem-sites-optimizer-preflight.js` en voeg de volgende inhoud toe:

   ```javascript
   (function () {
     let isAEMSitesOptimizerPreflightAppLoaded = false;
     function loadAEMSitesOptimizerPreflightApp() {
       const script = document.createElement('script');
       script.src = 'https://experience.adobe.com/solutions/OneAdobe-aem-sites-optimizer-preflight-mfe/static-assets/resources/sidekick/client.js?source=plugin';
       script.onload = function () {
         isAEMSitesOptimizerPreflightAppLoaded = true;
       };
       script.onerror = function () {
         console.error('Error loading AEMSitesOptimizerPreflightApp.');
       };
       document.head.appendChild(script);
     }
   
     function handlePluginButtonClick() {
       if (!isAEMSitesOptimizerPreflightAppLoaded) {
         loadAEMSitesOptimizerPreflightApp();
       }
     }
   
     // Sidekick V1 extension support
     const sidekick = document.querySelector('helix-sidekick');
     if (sidekick) {
       sidekick.addEventListener('custom:preflight', handlePluginButtonClick);
     } else {
       document.addEventListener('sidekick-ready', () => {
         document.querySelector('helix-sidekick')
           .addEventListener('custom:preflight', handlePluginButtonClick);
       }, { once: true });
     }
   
     // Sidekick V2 extension support
     const sidekickV2 = document.querySelector('aem-sidekick');
     if (sidekickV2) {
       sidekickV2.addEventListener('custom:preflight', handlePluginButtonClick);
     } else {
       document.addEventListener('sidekick-ready', () => {
         document.querySelector('aem-sidekick')
           .addEventListener('custom:preflight', handlePluginButtonClick);
       }, { once: true });
     }
   }());
   ```

1. Werk de functie `loadLazy()` in `/scripts/scripts.js` bij om het Preflight-script te importeren voor voorbeeld-URL&#39;s:

   ```javascript
   if (window.location.href.includes('.aem.page')) {
      import('../tools/sidekick/aem-sites-optimizer-preflight.js');
   }
   ```

1. Open de voorproef URL (`*.aem.page`) van de pagina die u wilt controleren.
1. In **Sidekick**, klik **Preflight** knoop om de controle voor de huidige pagina te beginnen.

>[!TAB  de Redacteur van de Pagina van AEM Sites ]

Als u Preflight wilt gebruiken in de AEM Sites Page Editor, kunt u een bladwijzer maken in uw webbrowser. Voer de volgende stappen uit:

1. Toon uw **Bar van Referenties** in uw browser van het Web:

   * Pers **Ctrl+Shift+B** (Vensters) of **Cmd+Shift+B** (Mac).

1. Maak een nieuwe bladwijzer in uw browser:

   * Klik met de rechtermuisknop op de bladwijzerbalk en selecteer **Nieuwe pagina** of **Bladwijzer toevoegen** .
   * Op het **Adres (URL)** gebied, kleef de volgende code:

   ```javascript
   javascript:(function(){const script=document.createElement('script');script.src='https://experience.adobe.com/solutions/OneAdobe-aem-sites-optimizer-preflight-mfe/static-assets/resources/sidekick/client.js?source=bookmarklet&target-source=aem-cloud-service';document.head.appendChild(script);})();
   ```

1. Noem de referentie **Preflight** (of om het even welke naam u verkiest).
1. Open voorproef URL (`*.aem.page`) van de pagina die u in de **Redacteur van de Pagina van AEM Sites** wilt controleren.
1. Klik **Preflight** referentie in uw bar van Bladwijzers om de controle voor de huidige pagina te beginnen.

>[!ENDTABS]

## Aanbevolen procedures

Houd rekening met de volgende richtlijnen wanneer u Preflight-controles uitvoert:

* Voer altijd controles op **het opvoeren of voorproef pagina&#39;s** alvorens aan productie te publiceren in werking.
* Prioriseer het oplossen van **high-impact kwesties** zoals gebroken verbindingen, ontbrekende markeringen H1, of onveilige verbindingen.
* Zorg ervoor dat **de authentificatie** voor beschermde het opvoeren milieu&#39;s alvorens controles wordt toegelaten in werking te stellen.
* Herzie en pas **aanbevelingen van de meta markering** toe om prestaties SEO te verbeteren.
