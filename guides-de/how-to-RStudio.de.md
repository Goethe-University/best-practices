
<img width="1618" height="121" alt="grafik" src="https://github.com/user-attachments/assets/0664d9d0-6b07-4438-98c2-e27ee12656ce" />

---

Für die gemeinsame Arbeit an einem Projekt kann ein lokales RStudio-Projekt mit einem GitHub-Repository verbunden werden. Dadurch lassen sich Änderungen versionieren, austauschen und zwischen allen Beteiligten synchronisieren.

Für weitere Infos und Anwendungsmöglichkeiten, siehe auch https://happygitwithr.com/

---

### 1.	Öffnen des Projekts in RStudio, um Git zu aktivieren:

Tools > Version Control > Project Setup: Version control system: Git, mit OK bestätigen


<img width="751" height="406" alt="grafik" src="https://github.com/user-attachments/assets/e5b10c91-bdec-4016-ae12-7f2f09bb0f1a" />

<img width="769" height="686" alt="grafik" src="https://github.com/user-attachments/assets/0c0f3d20-40a2-4ecb-8a64-fa49f94ec908" /> 

RStudio fragt an der Stelle, ob automatisch ein Repository angelegt werden soll. Mit ‚Ja‘ bestätigen 

<img width="798" height="728" alt="grafik" src="https://github.com/user-attachments/assets/2caab214-dee2-4f4e-8d90-ee7591049dc6" />

 
**ACHTUNG: Anschließend ist ein Neustart von RStudio erforderlich (man wird auch gefragt, ob dieser direkt ausgeführt werden soll)
Nach dem Neustart erscheint im oberen rechten Fenster ein neuer Reiter „Git“**

---

### 2.	der erste Commit

Bevor das Projekt mit GitHub synchronisiert werden kann, muss ein erster Versionsstand in Git erstellt werden (1. Commit).

Git-Reiter öffnen, ‚Commit‘ anklicken, es öffnet sich ein neues Fenster.

<img width="797" height="365" alt="grafik" src="https://github.com/user-attachments/assets/ba4a852a-4e3a-41c3-8ce6-879d657bc64d" />
 
Hier eine aussagekräftige Beschreibung des Projektstands eingeben. Beim ersten Commit ist es oft was wie „Projekt initialisiert“, anschließend mit dem Button ‚Commit‘ bestätigen.

<img width="830" height="316" alt="grafik" src="https://github.com/user-attachments/assets/cfb0adb6-91fb-4240-80f3-1d089766dee5" />

**HINWEIS: Änderungen müssen vor dem Committen in den Dateien gespeichert werden!**

---

### 3.	Zu GitHub wechseln und ein leeres Repository anlegen:

Im eigenen Account zu ‚Repositories‘ gehen und oben rechts den Button ‚New‘ klicken und ein leeres Repo anlegen: Repository name eintragen und auf ‚create repository klicken (kein gitignore, kein README)

 <img width="783" height="766" alt="grafik" src="https://github.com/user-attachments/assets/2de2f942-d679-4924-b039-70656da6e0c7" />

 **HINWEIS: die Voreinstellung von Repos ist öffentlich. Die Sichtbarkeit kann in den Einstellungen jederzeit geändert werden.**


https-Adresse des Repos kopieren:

<img width="807" height="274" alt="grafik" src="https://github.com/user-attachments/assets/ac8464a8-1e65-430e-8c49-3721f38b1ed9" />
 
---

### 4.	In RStudio ein neues Terminal öffnen

(den Pfad prüfen, es sollte sich um den Projektordner handeln)

 <img width="939" height="524" alt="grafik" src="https://github.com/user-attachments/assets/7dbd5c3c-1d73-44f2-9b76-17d4ca752e4d" />

```
git remote add origin <https-Adresse>

```

Adresse ohne <> eingeben. 
Mit ``` git remote -v ``` kann geprüft werden, ob die Verbindung eingerichtet wurde. Als Ergebnis sollte folgendes zu sehen sein

```
origin https://github.com/... (fetch)
origin https://github.com/... (push)
```

Anschließend erfolgt der Push zu GitHub: 

```git push -u origin main```

Wenn GitHub an dieser Stelle nach Zugangsdaten fragt, diese eingeben.

Jetzt ist das lokale Git-Repository mit GitHub verbunden. Änderungen können nun über RStudio oder über Git-Befehle im Terminal versioniert und mit GitHub synchronisiert werden.
