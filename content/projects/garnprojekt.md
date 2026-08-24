---
title: "Garn-projekt"
date: 2026-08-20
draft: false
description: "App til brug for alle os, der har lidt for mange garnrester"
---

Stine & Katarina · 3. semester, Datamatikeruddannelsen (EK Lyngby)

{{< lead >}}
En app designet til at hjælpe strikke- og hækleentusiaster med at holde styr på og udnytte garnrester.
{{< /lead >}}

## Teknologier

{{< badge >}}Java 21{{< /badge >}}
{{< badge >}}PostgreSQL{{< /badge >}}
{{< badge >}}Docker{{< /badge >}}

---

{{< button href="https://github.com/stinetorndal/portfolio_DAT3_2026" target="_blank" >}}
Se projektet på GitHub
{{< /button >}}

## User Story 1: Søgning

> **Som** nørkler  
> **vil jeg** kunne filtrere opskrifter ud fra mine garnrester (garntype, strikkefasthed, pindestørrelse og mængde)  
> **for at** jeg hurtigt kan finde projekter, der matcher det garn, jeg allerede har liggende.

**Scenario: Matchende opskrifter**
* **Givet** at brugeren har angivet gyldig garntype, strikkefasthed, pindestørrelse og mængde
* **Når** brugeren udfører søgningen
* **Da** viser systemet en liste over matchende opskrifter

**Scenario: Ingen opskrifter matcher kriterierne**
* **Givet** at brugeren har angivet en kombination af parametre, som ingen opskrifter opfylder
* **Når** brugeren udfører søgningen
* **Da** informerer app’en om, at der ikke blev fundet nogen match
* **Og** systemet foreslår at ændre på søgekriterierne / filtrene

---

## User Story 2: Gratis / betalte opskrifter

> **Som** bruger  
> **vil jeg** kunne vælge mellem gratis opskrifter og betalingsopskrifter samt filtrere på pris  
> **for at** vælge om jeg vil hente en opskrift med det samme eller købe en opskrift.

**Scenario: Visning og sortering af betalings- og gratis opskrifter**
* **Givet** at brugeren ser en liste over søgeresultater
* **Når** brugeren vælger at filtrere på "Kun gratis opskrifter"
* **Da** opdaterer systemet visningen til kun at indeholde opskrifter uden købskrav

**Scenario: Valg af betalingsopskrift**
* **Givet** at brugeren vælger en opskrift, der er markeret som betalingsopskrift
* **Når** brugeren klikker på opskriften
* **Da** sendes brugeren videre til den side, hvor opskriften hostes

---

## User Story 3: Garnmængde og opskriftsmatch

> **Som** hækler/strikker  
> **vil jeg** kunne se et præcist overblik over opskriftens garnmængde sammenholdt med mine filtrerede oplysninger  
> **for at** være sikker på, at mit restgarn rækker, inden jeg går i gang.

**Scenario: Visning af opskriftsdetaljer**
* **Givet** at brugeren åbner en specifik opskrift fra søgeresultaterne
* **Når** opskriften indlæses
* **Da** viser systemet en komplet oversigt over anbefalet garntype, pindestørrelse, strikkefasthed og det nøjagtige garnforbrug i gram eller meter
* **Og** app’en fremhæver, hvordan brugerens indtastede restgarn matcher opskriftens krav