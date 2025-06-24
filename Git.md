## Allgemein

~ Navigieren zum Ordner
```bash
cd
```

~ Ordner Anzeigen
```bash
dir
```

~ Navigieren zum Ordner
```bash
cd
```

---
## Konfiguration

> [!NOTE] Git Identität
> Name und E-Mail in Ihrer Git-Konfiguration sind keine Logindaten. Diese Daten werden
einfach als Text in jeden Ihrer Commits eingetragen. Die GitHub Logindaten haben mit der
Git-Konfiguration nichts zu tun.

~ Konfiguration in Git Bash
```bash
git config --global user.name "Vorname Nachname"
git config --global user.email "name@beispiel.de"
```

~ Texteditor umändern
```bash
# Windows Notepad
git config --global core.editor "notepad"
# Visual Studio Code
git config --global core.editor "code --wait --new-window"
```

~ Config Anschauen
```bash
git config edit --global
```


---
## Project Starten

~ Lokal starten
```bash
git init
```

~ Remote Repository clonen
```bash
git clone <URL> <Zielordner>
```

~ via [GitHub](https://github.com/)
```bash
# In das Verzeichnis welchseln, in dem Sie Ihre Projekte sammeln
cd pfad/zu/meinem/fach

# Projekt "herunterladen"
git clone https://github.com/my-user-name/my-project.git "my_new_project"

# In das neue Projektverzeichnis welchseln und arbeiten
cd my_new_project
git status

# Remote URL ausgeben lassen (auch in .git/config zu finden)
git remote
```

___
## Status Push Pull

~ Git Status
```bash
git status
```

~ Änderungen
```bash
# Eine Datei zum Index hinzufügen
git add my_file.html

# Alle Änderungen hinzufügen
git add --all
git add -A
git add .

# Alle Änderungen wieder aus dem Index entfernen
git reset

# oder nur "index.html" und "main.css"
git reset my_file.html main.css
```

~ Commit
```bash
git commit -m "Eine kurze Beschreibung meiner Änderungen"
```

~ Änderungen holen ggf. mergen
```bash
git pull
```

~ Änderungen Hochladen bzw. "Veröffentlichen"
```bash
git push
```

~ Branch Erstellen
```bash
git switch -c "name"
```

~Visual Studio Code öffnen
```bash
code .
```

~ Aufgaben in der eigenen branch integrieren
```bash
git pull origin main
```

~Halbfertige Änderungen nicht in *commit history*
```bash
git stash --help
```
*stash* ist eine Art Zwischenablage in Git
```bash
git stash push -a -m "Zwischenstand vor dem pull"
git pull origin main
git stash pop
```
*-a steht für „all“ und bezieht auch untracked files in den Befehl mit ein. pop löscht den Eintrag
im stash sobald die Änderung erfolgreich auf den worktree angewandt wurde.*

___
## Wiederherstellen

~ Historie
```bash
git log
```

~ Wiederherstellen
```bash
git restore
```
* * für alle Dateien


