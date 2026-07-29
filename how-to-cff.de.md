<img width="1618" height="121" alt="grafik" src="https://github.com/user-attachments/assets/b44f5d1b-1e94-411f-b66c-e7f58c02f897" />


---

Wer es ganz eilig hat: hier ein ```CITATION.cff```-Generator: https://citation-file-format.github.io/cff-initializer-javascript/

---

Eine CFF-Datei (Citation File Format) ist eine Textdatei mit dem Namen ```CITATION.cff```, die im Hauptverzeichnis eines GitHub-Repositories abgelegt wird. Sie enthält **strukturierte Metadaten zu einem Projekt**, z. B.:

  * Autorinnen und Autoren
  * Titel der Software oder des Projekts
  * Version
  * Veröffentlichungsdatum
  * DOI (Digital Object Identifier)
  * Lizenz
  * URL des Repositories

Der Zweck besteht darin, anderen Personen eine **korrekte Zitierweise für Software oder Datensätze** bereitzustellen. GitHub erkennt eine ```CITATION.cff``` automatisch. Wenn sie vorhanden ist, erscheint im Repository eine **Schaltfläche „Cite this repository“**, über die Nutzer eine fertige Zitierempfehlung erhalten.

Die Datei ist **menschen- und maschinenlesbar** und basiert auf **YAML** (eine einfache Struktur für Konfigurationsdateien).

Grundstruktur einer einfachen CFF-Datei:

```
cff-version: 1.2.0
title: Beispielprojekt
message: "If you use this software, please cite it as below."
authors:
  - family-names: Mustermann
    given-names: Max
version: 1.0.0
date-released: 2024-01-15
```
---

## Inhaltsverzeichnis

[1. Datei anlegen](#1-datei-anlegen)

[2. YAML-Struktur verwenden](#2-yaml-struktur-verwenden)

[3. Mehrere Autoren hinzufügen](#3-mehrere-autoren-hinzufügen)

[4. Zusätzliche Felder in einer CFF-Datei](#4-zusätzliche-felder-in-einer-cff-datei)

[5. Integration in ein GitHub-Repository](#5-integration-in-ein-github-repository)

[6. Beispiel für eine ausführliche CITATION.cff-Datei](#6-beispiel-für-eine-ausführliche-citationcff-datei)

[7. Häufige Fehler](7-häufige-fehler)

[8. Nützliche Tools zum Erstellen einer CFF-Datei](#8-nützliche-tools-zum-erstellen-einer-cff-datei)

* [CFF-Initiator](#cff-initiator)
* [YAML-Editoren](#yaml-editoren)
* [CFF-Validator](#cff-validator)

[9. Hilfreiche Links](#9-hilfreiche-links)


---

## Schritt-für-Schritt-Anleitung

### 1. Datei anlegen

**Über die Kommandozeile (Git/Shell):**
  1. Öffnen Sie Ihr GitHub-Repository.
  2. Legen Sie im Hauptverzeichnis (Root) eine neue Datei an.
  3. Der Dateiname muss exakt lauten: ```CITATION.cff```

**Über das GitHub-Webinterface:**
  1. Repository auf GitHub öffnen
  2. im Hauptverzeichnis (Root) über den Button "Create new file" eine neue Datei erstellen.
  3. Dateinamen eingeben: ```CITATION.cff```

<br>

>**Wichtig!**
>  * **Groß- und Kleinschreibung beachten.**
>  * **Die Dateiendung .cff ist erforderlich.**

<br>

### 2. YAML-Struktur verwenden

CFF basiert auf YAML (YAML Ain’t Markup Language). Dabei gelten einige einfache Regeln:

   * Einrückungen erfolgen mit Leerzeichen, nicht mit Tabs.
   * Listen werden mit - eingeleitet.
   * Schlüssel und Werte werden mit : getrennt.

<br>

### 3. Mehrere Autoren hinzufügen

Mehrere Autorinnen oder Autoren werden als Liste eingetragen.

Beispiel:
```
authors:
  - family-names: Mustermann
    given-names: Max
  - family-names: Beispiel
    given-names: Anna
```
**Jeder neue Eintrag beginnt mit -**

<br>

### 4. Zusätzliche Felder in einer CFF-Datei

Neben den grundlegenden Angaben können weitere Metadaten ergänzt werden. Diese **verbessern die Zitierfähigkeit** und die **wissenschaftliche Nachvollziehbarkeit**.

Häufig verwendete Felder:
* ```doi:``` Digital Object Identifier der Veröffentlichung.
* ```url:``` Projektwebseite oder Dokumentation.
* ```abstract:``` Kurzbeschreibung der Software oder des Projekts.
* ```keywords:``` Schlagwörter zur thematischen Einordnung.
* ```preferred-citation:``` Ermöglicht eine alternative Zitierform, z. B. wenn zusätzlich ein wissenschaftlicher Artikel existiert.

<br>

Zusätzliche Felder, können bei größeren Forschungsprojekten relevant sein:
* ```affiliation:``` Gibt die institutionelle Zugehörigkeit einer Autorin oder eines Autors an.
* ```email:``` Kontaktadresse der verantwortlichen Person.
* ```references:``` Verweise auf verwandte Publikationen.

<br>

### 5. Integration in ein GitHub-Repository

**Über die Kommandozeile (Git/Shell):**
* Legen Sie CITATION.cff im Root-Verzeichnis des Repositories ab (falls sie nicht schon dort liegt).
* Committen Sie die Datei

<br>

**Über das GitHub-Webinterface:**
* Klicken Sie oben rechts auf **"Commit changes..."**, es öffnet sich ein kleines Fenster
* Im Feld **Commit message** beschreiben Sie kurz die Änderung.
* Durch erneutes klicken auf **"Commit changes..."** wird die Datei im repository gespeichert.

**Im Repository erscheint anschließend ein Bereich „Cite this repository“, über den Nutzer eine Zitierempfehlung generieren können.**

---
## 6. Beispiel für eine ausführliche CITATION.cff-Datei:
```
cff-version: 1.2.0
message: "If you use this software, please cite it as described below."
type: software
title: Beispielsoftware zur Datenanalyse
version: 1.0.0
date-released: 2024-01-15
license: MIT
repository-code: https://github.com/username/beispielprojekt
url: https://github.com/username/beispielprojekt

authors:
  - family-names: Mustermann
    given-names: Max
    orcid: https://orcid.org/0000-0002-1825-0097
    max.mustermann@example.org
  - family-names: Platzhalter
    given-names: Paula
    affiliation: Universität Beispielstadt

keywords:
  - data analysis
  - research software
  - statistics

abstract: "Diese Software unterstützt die Analyse und Visualisierung wissenschaftlicher Datensätze."

references:
  - type: article
    title: Beispielartikel
    authors:
      - family-names: Mustermann
        given-names: Max
    year: 2023
```


---
### 7. Häufige Fehler

* **Falsche Einrückung:** YAML ist stark einrückungsabhängig. Beispiel für einen Fehler:
```
authors:
- family-names: Mustermann
given-names: Max
```
Richtig:
```
authors:
  - family-names: Mustermann
    given-names: Max
```

<br>

* **Verwenden von Tabs:** YAML erlaubt keine Tabs, nur Leerzeichen.

<br>

* **Ungültige Feldnamen:** Die Feldnamen müssen exakt den Spezifikationen entsprechen (z. B. ```family-names```, nicht ```lastname```).

<br>

* **Fehlende Pflichtfelder:** Mindestens notwendig sind in der Regel
  * ```cff-version```
  * ```title```
  * ```message```
  * ```authors```

---

##  8. Nützliche Tools zum Erstellen einer CFF-Datei

Das manuelle Schreiben ist möglich, aber fehleranfällig. Es gibt mehrere Tools, die den Prozess vereinfachen.

<br>

### CFF-Initiator

Der CFF-Initiator ist ein webbasiertes Tool zur Erstellung von CITATION.cff-Dateien.

Link: https://citation-file-format.github.io/cff-initializer-javascript/

Vorgehensweise:
  * Öffnen Sie die Webseite.
  * Füllen Sie die Formularfelder aus (Titel, Autoren, Version usw.).
  * Das Tool erzeugt automatisch eine gültige CITATION.cff.
  * Kopieren Sie den generierten Text.
  * Speichern Sie ihn in Ihrer Datei CITATION.cff im Repository.

<br>

### YAML-Editoren

Da CFF auf YAML basiert, sind Editoren mit YAML-Unterstützung hilfreich. Diese bieten Syntaxhervorhebung, Einrückungskontrolle und teilweise auch Validierung von YAML.

z.B.:
* Visual Studio Code
* Erweiterung: YAML Extension (Red Hat)
* Notepad++
* Sublime Text

<br>

### CFF-Validator

Um Fehler in der Struktur zu erkennen empfiehlt sich nach dem Erstellen der cff-Datei diese mit Hilfe eines Validators zu prüfen. Z.B. https://citation-file-format.github.io/cffconvert/. Hier besteht auch die Möglichkeit, alternative Zitierformate zu erzeugen (z.B. BibTex, APA).

<br>

---

### 9. Hilfreiche Links

Offizielle Ressourcen:
* CFF-Projektseite: https://citation-file-format.github.io/
* Spezifikation des Formats: https://github.com/citation-file-format/citation-file-format
* GitHub-Dokumentation zu CITATION-Dateien: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files





     
