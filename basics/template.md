# Template

Für die Nutzung im Workshop wurde ein <a href="https://quadriga-dk.github.io/OER-Workshop-Template" target="_blank" class="external-link">Template</a> (<a href="https://github.com/quadriga-dk/OER-Workshop-Template" target="_blank" class="external-link">GitHub</a>) entwickelt, das für den Start mit Jupyter Book genutzt werden kann. Dieses basiert auf dem <a href="https://quadriga-dk.github.io/Book_Template" target="_blank" class="external-link">QUADRIGA-Template</a> (<a href="https://github.com/quadriga-dk/Book_Template" target="_blank" class="external-link">GitHub</a>), wobei viele QUADRIGA-Spezifika entfernt wurden.

Für die Versionsverwaltung und gemeinsame Arbeit an den Inhalten nutzen wir Git und sowie die sog. Git Forge GitHub, welche nicht nur das Git-Repositorium speichert und die Zugriffsrechte darauf verwaltet, sondern auch ein Issue-System, ein CI/CD-System und einen Webhost bereitstellt.

Das Template beinhaltet verschiedene Ordner und Dateien, auf die in diesem Abschnitt eingegangen wird.

## Jupyter-Book-Dateien
Jupyter Book besteht aus zwei Konfigurationsdateien (`/_config.yml` und `/_toc.yml`), den zugehörigen inhaltstragenden Dateien (`.md`, `.ipynb`, Bilddateien, …) sowie den für die Website-Darstellung notwendigen `.css`- und `.js`-Dateien im Ordner `/_static`. Die Datei `/references.bib` wird für das Zitieren und Referenzieren von Literatur genutzt. 

Die inhaltstragenden Dateien sind in den Ordnern `/preamble` und `/epilog` für Text- sowie `/assets` für Bild-, und andere Dateien sortiert. Diese Sortierung wird nicht durch Jupyter Book vorgeschrieben, bietet sich aber für die bessere Übersichtlichkeit während des Erstellens der OER an. Wir empfehlen die Inhaltsdateien zu einem Kapitel in einem Ordner zu sammeln.

Die Einstiegsseite (im Template `/index.md`) sowie die Websitestruktur wird im Inhaltsverzeichnis `/_toc.yml` definiert. Dateien müssen im Inhaltsverzeichnis aufgeführt sein um in der Website, die durch Jupyter Book kompiliert wird, angezeigt zu werden.

Die Datei `/_config.yml` stellt die Konfiguration von Jupyter Book dar. Große Teile der Datei können direkt übernommen werden – auf die anzupassenden Teile wird im [nächsten Kapitel](/content/setup.md) eingegangen.

## Python-Dateien
Um Jupyter Book auf dem eigenen Computer zu nutzen muss dieses zuerst installiert werden. Dafür benötigen Sie Python – am besten in der Version, die in `/.python-version` angegeben ist – und müssen dann die in der Datei `/requirements.txt` angegebenen Pakete installieren.

Für den Workshop ist dies nicht notwendig. Wünschen Sie eine lokale installation, so funktioniert das mit den nachfolgenden Befehlen:

```bash
$ python3.13 -m venv .venv        # erstelle ein neues sog. virtual environment
$ source .venv/bin/activate       # aktiviere das environment
$ pip install -r requirements.txt # installiere die benötigten Python Pakete
```
Wollen Sie Jupyter Book dann nutzen, stellen Sie sicher, dass Sie im Wurzelordner Ihres Jupyter-Book-Projekts sind und, dass das passende 'virtual environment' aktiviert ist. Nutzen Sie dann die nachfolgenden Befehle:

```bash
# Kompiliert die Website und speichert das Ergebnis im Ordner /_build/html
$ jupyter book build .

# Bereinigt den Ordner _build um dann das Buch vollständig neu bauen zu können
# Muss nicht immer ausgeführt werden, kann jedoch bspw. Probleme mit dem Inhaltsverzeichnis lösen
$ jupyter book clean . --all
```

## Git-Dateien
Die Datei `/.gitignore` definiert, welche Dateien nicht in der Versionverwaltung geführt und versioniert werden sollen. Dies betrifft insbesondere den Jupyter-Book-Ergebnis-Ordner `/_build` sowie verschiedene Cache-Dateien die durch die Ausführung von Python-Code enstehen. Die Datei muss im Workshop nicht verändert werden.

Die gesamte Versionskontrolle findet im Ordner `/.git` statt, weshalb Inhalte dieses Ordners nie von Hand verändert werden sollten.

## GitHub-Dateien
Im Ordner `/.github` wird im Ordner `/.github/workflows` die sogenannte GitHub Action `deploy-book-python-only.yml` definiert. Diese führt beim Speichern von Änderungen auf GitHub (im sog. Branch `main`) verschiedene Befehle aus um das Jupyter Book zu kompilieren und das Ergebnis per GitHub Pages bereitzustellen. Die Inhalte der Datei müssen im Workshop nicht angepasst werden.

Die Datei `README.md` beinhaltet eine kurze Beschreibung der Inhalte des Repositoriums und wird auf GitHub prominent angezeigt.

## Zusätzliche Dateien

In der Datei `LICENSE.md` werden Informationen zur Nutzungslizenzen festgehalten.

Die Datei `CITATION.cff` definiert Metadaten für die Zitation des Git-Repositoriums. Sie wird von GitHub und von Zenodo genutzt um Zitierhinweise zu generieren.