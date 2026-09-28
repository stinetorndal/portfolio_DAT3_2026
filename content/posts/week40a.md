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

# User Stories og Acceptkriterier - Artprompt

## User Story 1
**Som** kunstner  
**vil jeg** kunne hente tilfældige prompt-ord baseret på en valgt kategori,  
**så** jeg kan få ny inspiration til mine tegninger.

### Acceptance Criteria 1.1
- **Given** at en gyldig kategori vælges (f.eks. `CREATURES`).
- **When** der anmodes om et prompt-ord for denne kategori.
- **Then** får brugeren en liste med kategorier at vælge imellem.

### Acceptance Criteria 1.2
- **Given** at en ugyldig kategori sendes med forespørgslen.
- **When** anmodningen behandles.
- **Then** kaster systemet en fejl, og fejlen logges. 

---

## User Story 2
**Som** kunstner  
**vil jeg** kunne hente en ny kategori, hvor min forrige valgte kategori er sorteret fra,  
**så** jeg ikke får den samme kategori to gange i træk.

### Acceptance Criteria 2.1
- **Given** at brugeren senest har haft kategorien `MOOD`.
- **When** der anmodes om en ny tilfældig kategori med parametret for forrige kategori (`MOOD`).
- **Then** får brugeren en ny kategori-liste, hvor `MOOD` ikke indgår.

---

## User Story 3
**Som** system  
**vil jeg** sikre, at en ny brugers e-mail indeholder `@` og et gyldigt domæne (fx `.dk`),  
**så** der kun gemmes korrekte email-adresser i databasen.

### Acceptance Criteria 3.1
- **Given** en e-mailstreng med korrekt format (f.eks. `test@example.dk`).
- **When** e-mailen valideres af applikationen.
- **Then** accepteres e-mailen.

### Acceptance Criteria 3.2
- **Given** en e-mailstreng uden `@` eller uden et gyldigt domæne (f.eks. `testexample`).
- **When** e-mailen valideres ved brugeroprettelse.
- **Then** kastes en fejl, fejlen logges i systemes log. 

---

## User Story 4
**Som** system  
**vil jeg** afvise adgangskoder, der er under 8 tegn eller mangler store bogstaver, tal og specialtegn,  
**så** brugernes konti er bedre beskyttet mod uautoriseret adgang.

### Acceptance Criteria 4.1
- **Given** en adgangskode, der opfylder alle kravene (f.eks. mindst 8 tegn, 1 stort bogstav, 1 tal, 1 specialtegn: `Qwerty26!`).
- **When** adgangskoden valideres.
- **Then** godkendes koden.

### Acceptance Criteria 4.2
- **Given** en adgangskode, der bryder ét eller flere krav (f.eks. for kort eller mangler specialtegn: `qwerty`).
- **When** adgangskoden valideres ved brugeroprettelse.
- **Then** kastes en fejl, fejlen logges i systemes log og oprettelse afbrydes

---

## User Story 5
**Som** ny bruger  
**vil jeg** kunne oprette en konto med e-mail og adgangskode,  
**så** min adgangskode gemmes sikkert i databasen i et krypteret/hashed format.

### Acceptance Criteria 5.1
- **Given** en unik e-mail og en stærk adgangskode.
- **When** brugeren er oprettet.
- **Then** oprettes brugeren i databasen, og adgangskoden gemmes som en krypteret streng.

---

## User Story 6
**Som** system  
**vil jeg** checke, om en e-mail allerede eksisterer i databasen før oprettelse,  
**så** der undgås duplikerede brugerprofiler.

### Acceptance Criteria 6.1
- **Given** at en bruger med e-mailen `eksisterer@mail.dk` allerede findes i databasen.
- **When** der gøres forsøg på at oprette en ny bruger med samme e-mail.
- **Then** kastes en fejl, den logges og bruger oprettes ikke

---

## User Story 7
**Som** eksisterende bruger  
**vil jeg** kunne logge ind med min e-mail og adgangskode,  
**så** systemet kan bekræfte min identitet og give mig adgang.

### Acceptance Criteria 7.1
- **Given** der er en oprettet bruger i databasen.
- **When** der sendes korrekte login-oplysninger.
- **Then** bekræftes koden, og systemet logger brugeren ind.

### Acceptance Criteria 7.2
- **Given** forkert adgangskode eller uregistreret e-mail.
- **When** login forsøges.
- **Then** afvises anmodningen ved at kaste en fejl der registeres i systemets log.

---

## User Story 8
**Som** eksisterende bruger  
**vil jeg** kunne gemme billeder fra billedprompt,  
**så** jeg kan se en oversigt og et datostempel.

### Acceptance Criteria 8.1
- **Given** en oprettet bruger og en URL til et billede.
- **When** brugeren vil gemme billedet
- **Then** gemmes billedet url og dato i databasen, så det er knyttet til brugeren profil

---

## User Story 9
**Som** eksisterende bruger  
**vil jeg** kunne oprette noter med ideer,  
**så** jeg kan se en oversigt af mine ideer med dato.

### Acceptance Criteria 9.1
- **Given** en oprettet bruger og noget notetekst.
- **When** noten oprettes af brugeren
- **Then** gemmes noten med relation til brugeren samt et automatisk genereret datostempel.

---

## User Story 10
**Som** eksisterende bruger  
**vil jeg** kunne gemme noter mens jeg skriver dem,  
**så** de er gemt, hvis computeren går ned.

### Acceptance Criteria 10.1
- **Given** en eksisterende note i databasen med et unikt id.
- **When** der sendes en opdatering af teksten 
- **Then** opdateres den eksisterende note i databasen med den nye tekst