---
uid: help-da-editor
title: Træk og slip-editor
description: Træk og slip-editor
author: SuperOffice RnD
so.date: 02.20.2023
keywords: marketing, editor, skabelonvariabler, fletfelter
so.topic: concept
language: da
---

# Træk og slip-editor

![Træk og slip-editor -screenshot][img1]

På trinet **Indhold** kan du redigere meddelelsens udseende og indhold.

* Du kan [indsætte tekst og billeder][1] (og andet indhold) i kolonnerne og rækkerne i meddelelsen.

* Du kan definere format/layout (f.eks. skrifttype og størrelse, farver og margener) på globalt plan (hele meddelelsen) eller efter enkelte afsnit.

* Du kan nemt trække og slippe indhold fra sidepanelet (menuer, knapper, SoMe-links, HTML-indhold og sidehoved- og sidefodsblokke).

SuperOffice Markedsføring leveres med flere [færdige meddelelsesskabeloner][9], og du kan nemt flytte indhold rundt, så meddelelsen får det ønskede udseende. Gem ofte brugt indhold som blokke for at spare tid.

> [!TIP]
> Vi anbefaler normalt en maksimal bredde på 600 pixel for udsendelser. Du kan også styre, hvordan udsendelsen ser ud på f.eks. smartphones ved at klikke på **Mobil** (![ikon][img4]) i menuen i nederste venstre hjørne. Se også [Tilpasse meddelelsen til visning på mobile enheder][3].

## Rediger kolonner og blokke/afsnit

Når du klikker på et afsnit (såsom kolonne, indholdsboks, række osv.), vises knapper med redigeringsindstillinger. Sidepanelet viser redigeringsindstillinger for det valgte afsnit.

Der vises en blå ramme rundt om det markerede element, så du altid ved, hvilken del af meddelelsen du redigerer.

Hvis du klikker på tekstindhold, vises en værktøjslinje til tekstredigering.

Den globale menu vises altid nederst til venstre i indholdsområdet.

## Redigere tekst og billeder

[Rediger tekst][5], [indsæt billeder][6] og tilføj andet indhold ved at klikke på et afsnit i meddelelsen. Brug værktøjslinjen til tekstredigering og sidepanelet til at redigere det valgte afsnit.

## Indsætte nyt indhold

I sidepanelet kan du trække og slippe elementer fra afsnittet **Indhold** til meddelelsen. Du kan også klikke på **+** over eller under en række for at indsætte en ny række.

## Flyt, kopier og slet indhold

Du kan markere et afsnit og bruge knapperne til at flytte (![ikon][img6]), kopiere (![ikon][img8]) og slette (![ikon][img7]) den.

## Rediger format and layout

Meddelelsens udseende og egenskaber (f.eks. skrifttype og -størrelse, farver og margener) kan defineres på globalt plan (hele meddelelsen) eller efter afsnit (som beskrevet ovenfor).

Hvis du vil redigere meddelelsen på globalt plan, skal du vælge **Brødtekst** (![ikon][img12]) i sidepanelet.

> [!TIP]
> Brug standardskrifttyper for bedst mulig læsbarhed uanset e-mailklient og webbrowser.

## Menuoversigt

Nedenfor er en oversigt over de forskellige funktioner i trinnet **Indhold**.

### Sidepanel

Sidepanelet indeholder følgende hovedafsnit:

[!include[Mailing - sections in the side panel](includes/mailing-side-panel.md)]

Se også [Tilføj indhold][1].

### Global menu

Fra den globale menu kan du få vist, fortryde eller gentage handlinger og se, hvordan meddelelsen ser ud på en computer eller mobil. Denne menu vises altid nederst til venstre i indholdsområdet.

| Ikon | Navn | Funktion |
|:-:|---|---|
| ![ikon][img11] | Fortryd/Gendan | Fortryder den sidste handling eller gendanner en fortrudt handling. |
| ![ikon][img2] | Forhåndsvisning | Åbner en forhåndsvisning af meddelelsen på en computer- eller mobilskærm. |
| ![ikon][img3],![ikon][img4] | Skift visning for pc- eller mobilenheder | Bruges til at se, hvordan det ser ud på en pc eller smartphone. |

### Genvejsmenu

Når du klikker på et afsnit i en meddelelse, får du adgang til forskellige funktioner for afsnittet.

| Ikon | Navn | Funktion |
|:-:|---|---|
| ![ikon][img5] | Tilføj række | Tilføjer en række under eller over det markerede afsnit. |
| ![ikon][img6] | Flyt | Klik og træk for at flytte afsnittet. |
| ![ikon][img7] | Slet | Sletter afsnittet. |
| ![ikon][img8] | Dupliker | Der oprettes en kopi af afsnittet. |
| ![ikon][img9] | Gem blok | Gemmer det markerede afsnit som en blok. Lader dig genbruge indhold på (f.eks. sidehoveder og sidefødder) på tværs af meddelelser. |

## <a id="variables" />Skabelonvariabler

For at give meddelelsen et mere personligt præg kan du bruge pladsholdere til at indsætte kundespecifikke oplysninger såsom kundens fornavn. På denne måde kan du skræddersy indholdet til hver enkelt kunde.

Disse pladsholdere kaldes **skabelonvariabler** i den gamle editor og flettefelter **i træk og** slip-editoren.

[!include[Note](includes/note-imported-recipients.md)]

Der findes flere slags fletfelter:

* Flettefelter, der er knyttet til kontakter. F.eks. **\[\[customer.name\]\]** indsætter personens fulde navn.
* Flettefelter, der er knyttet til firmaer. F.eks. **\[\[company.name\]\]** indsætter navnet på det firma, som personen tilhører.

### Eksempel

I stedet for denne tekst:

"Kære kunde. Vil du vide mere om, hvordan vores produkt kan hjælpe din virksomhed med at skaffe nye kunder? Ring venligst til os i SuperShop."

Du kan sende denne:

"Kære Jonas. Vil du vide mere om, hvordan vores produkt kan hjælpe Bilbutikken A/S med at skaffe nye kunder? Ring til Jesper Nielsen i SuperShop."

Teksten du skriver ser således ud:

"Kære **\[\[customer.firstname\]\]**. Vil du vide mere om, hvordan vores produkt kan hjælpe **\[\[company.name\]\]** med at skaffe nye kunder? Ring venligst til os **\[\[company.ourSalesContact.name\]\]** i SuperShop."

## To forskellige editorer

Bruger du den nye Træk og slip-editor eller den tidligere version af editoren?

I begyndelsen af 2021 tilføjede SuperOffice en ny meddelelseseditor ("Træk og slip-editoren") som erstatning for den gamle ("Editoren"). Meddelelseseditoren bruges, når der oprettes e-mailudsendelser og formularsvar. Den gamle meddelelseseditor vil stadig være tilgængelig til at redigere meddelelser og skabeloner, der er oprettet i den gamle version. Alle nye udsendelser og skabeloner vil bruge den nye meddelelseseditor.

### Editor (gammel)

![Editor (gammel) -screenshot][img13]

## Hvad vil du foretage dig nu?

* [Tilføj indhold][1]
* [Rediger indhold][5]
* [Medtage links, du vil spore][8]
* [Brug af fletfelter i meddelelser][7]
* [Indsæt billeder i meddelelsen][6]
* [Læs om den gamle editor][2]

<!-- Referenced links -->
[1]: add-content.md
[3]: customize-for-mobile.md
[5]: edit-paragraph.md
[6]: insert-images-in-message.md
[7]: add-merge-tag.md
[8]: ../tracked-links/learn/add-tracked-link-to-msg.md
[9]: work-with-messages-and-templates.md
[2]: https://help.superoffice.com/Documentation/Help/EN/CRM/UserHelp/index.htm#t=Mailing%2FHelptopics%2Foldeditor%2FStep_3__Content_-_Formatted_e-mail.htm

<!-- Referenced images -->
[img1]: ../../../media/loc/en/marketing/edit-template.png
[img2]: ../../../media/icons/marketing-and-forms/preview.png
[img3]: ../../../media/icons/marketing-and-forms/desktop.png
[img4]: ../../../media/icons/marketing-and-forms/mobile-2.png
[img5]: ../../../media/icons/marketing-and-forms/add-row.png
[img6]: ../../../media/icons/marketing-and-forms/move-2.png
[img7]: ../../../media/icons/marketing-and-forms/cancel.png
[img8]: ../../../media/icons/marketing-and-forms/copy.jpg
[img9]: ../../../media/icons/marketing-and-forms/save-block.png
[img11]: ../../../media/icons/marketing-and-forms/undo-redo.png
[img12]: ../../../media/icons/marketing-and-forms/side-panel-body-small.png
[img13]: ../../../media/loc/en/marketing/template-edit-overview-old.png