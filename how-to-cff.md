
<img width="1618" height="121" alt="grafik" src="https://github.com/user-attachments/assets/af9e33f3-7192-4c5c-a0f4-89ff57dc72ce" />

---

For those in a time crunch: use the ```CITATION.cff``` file generator: https://citation-file-format.github.io/cff-initializer-javascript/

---

A CFF file (Citation File Format) is a text file named ```CITATION.cff```, which is stored in the root directory of a GitHub repository. It contains **structured metadata about a project**, e.g.:

  * Authors
  * Title of the software or project
  * Version
  * Publication date
  * DOI (Digital Object Identifier)
  * Licence
  * Repository URL

The purpose is to provide others with **correct citation information for software or datasets**. 

GitHub automatically recognises a ```CITATION.cff``` file. If present, a **‘Cite this repository’ button** appears in the repository, allowing users to obtain a ready-made citation recommendation.

The file is **human- and machine-readable** and is based on **YAML** (a simple structure for configuration files).

Basic structure of a simple CFF file:


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

<details>
<summary>Table of Contents</summary>

[1. Creating a file](#1-creating-a-file)

[2. Using the YAML structure](#2-using-the-yaml-structure)

[3. Adding multiple authors](#3-adding-multiple-authors)

[4. Additional fields in a CFF file](#4-additional-fields-in-a-cff-file)

[5. Integration into a GitHub repository](#5-integration-into-a-github-repository)

[6. Example of a detailed CITATION.cff file](#6-example-of-a-detailed-citationcff-file)

[7. Common errors](7-common-errors)

[8. Useful tools for creating a CFF file](#8-useful-tools-for-creating-a-cff-file)

* [CFF Initiator](#cff-initiator)
* [YAML editors](#yaml-editors)
* [CFF validator](#cff-validator)

[9. Helpful links](#9-helpful-links)

</details>

---

## Step-by-step guide

### 1. Create a new file

**Via the command line (Git/Shell):**
  1. Open your GitHub repository.
  2. Create a new file in the root directory.
  3. The file name must be exactly: ```CITATION.cff```

**Via the GitHub web interface:**
  1. Open the repository on GitHub
  2. Create a new file in the root directory using the ‘Create new file’ button.
  3. Enter the file name: ```CITATION.cff```

<br>

>**Important!**
>  * **Note that the file name is case-sensitive.**
>  * **The file extension .cff is required.**

<br>

### 2. Using the YAML structure

CFF is based on YAML (YAML Ain’t Markup Language). A few simple rules apply:

   * Indentation is done using spaces, not tabs.
   * Lists are indented with a hyphen (-).
   * Keys and values are separated by a colon (:).

<br>

### 3. Adding multiple authors

Multiple authors are entered as a list.

Example:
```
authors:
  - family-names: Mustermann
    given-names: Max
  - family-names: Beispiel
    given-names: Anna
```
**Each new entry begins with a hyphen (-)**

<br>

### 4. Additional fields in a CFF file

In addition to the basic details, further metadata can be included. This **improves citability** and **scholarly traceability**.

Commonly used fields:
* ```doi:``` Digital Object Identifier of the publication.
* ```url:``` Project website or documentation.
* ```abstract:``` Brief description of the software or project.
* ```keywords:``` Keywords for thematic classification.
* ```preferred-citation:``` Allows for an alternative citation format, e.g. if a scientific article also exists.


Additional fields that may be relevant for larger research projects:
* ```affiliation:``` Specifies the institutional affiliation of an author.
* ```email:``` Contact details of the person responsible.
* ```references:``` References to related publications.

<br>

### 5. Integrating into a GitHub repository

**Via the command line (Git/Shell):**
* Place CITATION.cff in the root directory of the repository (if it is not already there).
* Commit the file

<br>

**Via the GitHub web interface:**
* Click **‘Commit changes...’** in the top right-hand corner; a small window will open
* In the **Commit message** field, briefly describe the change.
* Click **‘Commit changes...’** again to save the file to the repository.

**A “Cite this repository” section will then appear in the repository, allowing users to generate a citation recommendation.**

---

## 6. Example of a detailed CITATION.cff file:

```
cff-version: 1.2.0
message: ‘If you use this software, please cite it as described below.’
type: software
title: Sample data analysis software
version: 1.0.0
date-released: 2024-01-15
license: MIT
repository-code: https://github.com/username/testprojekt
url: https://github.com/username/testprojekt

authors:
  - family-names: Mustermann
    given-names: Max
    orcid: https://orcid.org/0000-0002-1825-0097
    max.mustermann@example.org
  - family-names: Placeholder
    given-names: Paula
    affiliation: University of Example City

keywords:
  - data analysis
  - research software
  - statistics

abstract: ‘This software supports the analysis and visualisation of scientific datasets.’

references:
  - type: article
    title: Sample article
    authors:
      - family-names: Mustermann
        given-names: Max
    year: 2023
```

<br>

---

### 7. Common errors

* **Incorrect indentation:** YAML is highly dependent on indentation. Example of an error:
```
authors:
- family-names: Mustermann
given-names: Max
```
Correct:
```
authors:
  - family-names: Mustermann
    given-names: Max
```

<br>

* **Using tabs:** YAML does not allow tabs, only spaces.

<br>

* **Invalid field names:** Field names must match the specifications exactly (e.g. ```family-names```, not ```lastname```).

<br>

* **Missing required fields:** The following are generally required as a minimum:
  * ```cff-version```
  * ```title```
  * ```message```
  * ```authors```

---

##  8. Useful tools for creating a CFF file

It is possible to write the code manually, but this is prone to errors. There are several tools available that simplify the process.

<br>

### CFF Initiator

The CFF Initiator is a web-based tool for creating CITATION.cff files.

Link: https://citation-file-format.github.io/cff-initializer-javascript/

Procedure:
  * Open the website.
  * Fill in the form fields (title, authors, version, etc.).
  * The tool automatically generates a valid CITATION.cff file.
  * Copy the generated text.
  * Save it to your CITATION.cff file in the repository.

<br>

### YAML editors

As CFF is based on YAML, editors with YAML support are useful. These offer syntax highlighting, indentation checking and, in some cases, YAML validation.

e.g.:
* Visual Studio Code
* Extension: YAML Extension (Red Hat)
* Notepad++
* Sublime Text

<br>

### CFF Validator

To identify errors in the structure, it is advisable to check the CFF file using a validator once it has been created. For example, https://citation-file-format.github.io/cffconvert/. This tool also allows you to generate alternative citation formats (e.g. BibTeX, APA).

---

### 9. Useful links

Official resources:
* CFF project page: https://citation-file-format.github.io/
* Format specification: https://github.com/citation-file-format/citation-file-format
* GitHub documentation on CITATION files: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files
