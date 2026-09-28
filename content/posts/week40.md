---
title: "WEEK 40"
date: 2026-09-27
draft: false
description: "An inspirational app for artists"
---

Stine Torndal · 3. semester, Datamatikeruddannelsen (EK Lyngby)

{{< lead >}}
An app to lend a helping hand to artists with art block and lack of inspiration.
{{< /lead >}}

---

## User Stories - ArtPrompt 

### User Story 1
* **Som** kunstner 
* **vil jeg** kunne hente tilfældige prompt-ord baseret på en valgt kategori, 
* **så** jeg kan få ny inspiration til mine tegninger.\
### User Story 2
* **Som** kunstner\ 
* **vil jeg** kunne hente en ny kategori, hvor min forrige valgte kategori er sorteret fra,
* **så** så jeg ikke får den samme kategori to gange i træk.
### User Story 3
* **Som** system 
* **vil jeg** sikre, at en ny brugers e-mail indeholder @ og et gyldigt domæne (fx .dk),
* **så** der kun gemmes korrekte email-adresser i databasen
### User Story 4
* **Som** system 
* **vil jeg** afvise adgangskoder, der er under 8 tegn eller mangler store bogstaver, tal og specialtegn,
* **så** så brugernes konti er bedre beskyttet mod uautoriseret adgang.
### User Story 5
* **Som** ny bruger
* **vil jeg** kunne oprette en konto med e-mail og adgangskode,
* **så** så min adgangskode gemmes sikkert i databasen i et krypteret/hashed format (BCrypt).
### User Story 6
* **Som** system
* **vil jeg** checke, om en e-mail allerede eksisterer i databasen før oprettelse,
* **så** der undgps duplikerede brugerprofiler
### User Story 7
* **Som** eksisterende bruger
* **vil jeg** kunne logge ind med min e-mail og adgangskode,
* **så** systemet kan bekræfte min identitet via BCrypt og give mig adgang.
### User Story 8
* **Som** eksisterende bruger
* **vil jeg** kunne gemme billeder fra billedprompt
* **så** jeg kan se en oversigt og et datostempel
### User Story 9
* **Som** eksisterende bruger
* **vil jeg** kunne oprette noter med ideer
* **så** jeg kan se en oversigt af mine ideer med dato
### User Story 10
* **Som** eksisterende bruger
* **vil jeg** kunne gemme noter mens jeg skriver dem
* **så** de er gemt, hvis computeren går ned