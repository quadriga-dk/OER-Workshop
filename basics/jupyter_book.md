# Warum Jupyter Book?

## Proprietäre und freie Formate für die OER-Erstellung
Open Educational Resources sollten möglichst mit freier Software bearbeit- und nutzbar sowie möglichst in freien Standardformaten verfasst sein. Einfache Text-Dateien stellen hierfür eine besonders gute Lösung dar.

Auch wenn klassische Text-Dateien (`.txt`) durchaus genutzt werden können, so bieten sich <a href="https://de.wikipedia.org/wiki/Auszeichnungssprache" target="_blank" class="external-link">Auszeichnungssprachen</a> wie HTML (`.html`) oder <a href="https://daringfireball.net/projects/markdown/" target="_blank" class="external-link">Markdown (`.md`)</a> an, um die Inhalte strukturell und typographisch für das Lesen aufzubereiten. Die hier genannten Auszeichnungssprachen eignen sich besonders für ein Endprodukt, das im Browser – als Website – konsumiert werden soll.

Durch Software wie <a href="https://pandoc.org/index.html" target="_blank" class="external-link">Pandoc</a> können diese auf Text basierenden Formate auch in verschiede andere Dateiformate wie `.pdf` oder `.docx` transformiert werden.

## Vorteile von sog. _static site generators_ für die OER-Entwicklung
Klassisches Website-Hosting hat gewisse Mindestkosten, welche bei starker Nutzung stetig steigen. Dies gilt insbesondere für Seiten, welche pro Nutzer:innen-Zugriff Berechnungen auf Basis von Datenbanken durchführen müssen, um Inhalte zu präsentieren. Ist die dadurch gewonnene Individualisierbarkeit nicht nötig, so kann ein einfacheres Modell genutzt werden.

Ein sog. _static site generator_ (SSG) kompiliert Quelldateien (bspw. Markdown-Dateien) zu HTML-Dateien und strukturiert diese zusammen mit allen nötigen Dateien wie Bildern, `.css`- und `.js`-Dateien in eine Ordnerstruktur ein, welche dann sehr günstig (im Falle der Nutzung von bspw. GitHub Pages praktisch kostenlos) gehostet werden können. Klassische SSG überführen die Quelldateien in eine Website-Struktur, jedoch sind auch andere Ausgabeformate denkbar.

Die Kompilierung muss nicht für jede Nutzer:in sondern nur einmal, wenn die Quelldateien geändert wurden, durchgeführt werden.

## Das Juypter Ökosystem
In den letzten Jahren hat sich das <a href="https://jupyter.org" target="_blank" class="external-link">Jupyter-Projekt</a> als _das_ Ökosystem im Bereich Data Science und Machine Learning herauskristallisiert.

Dies liegt insbesondere an den sog. Jupyter Notebooks (`.ipynb`), welche es erlauben, Text (in Markdown formatiert) und ausführbaren Programmcode sowie Ergebnisse des Codes kombiniert zu präsentieren. Jupyter Notebooks sind Text-Dateien im Dateiformat JSON (`.json`). Die "Magie" entsteht, wenn ein spezieller Editor (bpsw. das gleichnamige Jupyter Notebook oder die mächtigere Entwicklungsumgebung Jupyter Lab oder auch Visual Studio Code) die `.ipynb`-Datei einliest und einen sogenannten Kernel startet. Ein Kernel ist ein Programm, welches Programmcode in einer Programmiersprache wie Python ausführen kann und die Berechnungsergebnisse so an den Editor übermittelt, dass dieser sie wieder in die `.ipynb`-Datei einbinden kann. Dadurch kann ein Schnipsel Programmcode (in Jupyter Notebooks spricht man auch von Zellen ('code cell')) ausgeführt und das Ergebnis direkt darunter angezeigt werden.

## Jupyter Book
Jupyter Book ist ein SSG, welcher ein Eingangs-Dateiformat nicht – wie normalerweise üblich – nur Markdown- und HTML-Dateien versteht, sondern auch nativ Jupyter Notebooks (`.ipynb`) ausführen und als Ergebnis in die Website-Kompilierung einbeziehen kann. Dadurch können Notebooks direkt genutzt und mit Markdown-Dateien kombiniert werden, um die Inhalte zu erstellen.

Zudem bietet Jupyter Book Funktionalitäten um die Inhalte von der Website aus in einer interaktiven Programmierumgebung wie Binder, Colab oder einem Jupyter Hub zu öffnen und mit den Inhalten direkt weiterzuarbeiten. Der Übergang von der lesenden zur bearbeitenden Nutzung ist also fließend.