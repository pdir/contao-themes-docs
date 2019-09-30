# Theme anpassen

## Layouts

Unter Themes / Seitenlayouts finden Sie bereits vier verschiedene Layouts, die Sie einer Seite bei den Seiteneinstellungen unter Layout-Einstellungen zuweisen können.

* Einspaltiges Layout
* Zweispaltiges Layout mit rechter Spalte
* Zweispaltiges Layout mit linker Spalte
* Dreispaltiges Layout

## Header und Footer

Das Logo können Sie im Artikel **01_Logo** unter **Nature Theme Elemente / 01_Header** bearbeiten.

Die Inhalte des Footers können Sie in den Artikeln unter **Nature Theme Elemente / 02_Footer** bearbeiten.

![](../_images/nature-theme/einrichtung/nature_elemente_fuer_inserttag.png)

## Variablen

Wenn das Theme erfolgreich installiert wurde, befinden sich die [SCSS](https://sass-lang.com/documentation/file.SASS_REFERENCE.html)-Dateien in der Dateiverwaltung unter dem Pfad **naturetheme/scss**. Für individuelle Anpassungen nutzen Sie einfach die **custom.scss**, in der Sie sowohl SCSS oder auch normales CSS schreiben können, sowie die **\_custom\_colors.scss** und **\_custom\_variables.scss**.

In der **\_custom\_colors.scss** können Sie die Grundfarben des Themes verändern und ein anderes Farbschema auswählen. Wenn Sie eine Variable anpassen möchten, müssen Sie die Zeile auskommentieren (Schrägstriche entfernen).

In der **\_custom\_variables.scss** können Sie individuellere Anpassungen vornehmen, u. a. Schriften austauschen, die Schriftgrößen der Überschriften beeinflussen oder Farben von Elementen und Modulen anpassen. Wenn Sie eine Variable anpassen möchten, müssen Sie die Zeile auskommentieren (Schrägstriche entfernen).

Wenn Sie lieber mit CSS-Dateien statt mit SCSS-Dateien arbeiten wollen, können Sie über **Themes - Stylesheets** einen neuen Stylesheet anlegen und ihn im **Layout** bei **Interne Stylesheets** einbinden. Das CSS wird anschließend automatisch nach dem CSS des ODD Theme geladen.

### Farbschemen

Das Nature Theme wird standardmäßig mit einem hellen Layout und grüner Hauptfarbe ausgeliefert. Sie haben aber auch die Möglichkeit ein dunkles Farbschema auszuwählen.

Wenn Sie auf ein Layout umstellen wollen, kommentieren Sie in der **\_custom\_colors.scss** die entsprechende Zeile bei **Colour Schemes** aus \(Schrägstriche entfernen\). Gegebenenfalls müssen Sie die Seite mit Strg + F5 neuladen, damit die Änderung greift.

#### Variablen der \_custom\_colors.scss

| Variable | Bedeutung |
| ------------- | ------------- |
| $primary | Hauptfarbe |
| $text | Textfarbe |
| $link | Linkfarbe |
| $link-hover | Linkfarbe bei Hover |
| $background | Hintergrundfarbe der Seite |
| $boxes-background | Hintergrundfarbe von Boxen,<br><span style="font-size:12px;">Teaserboxen, Kontakt-Box, News-Boxen, Event-Boxen, Formularfelder, Breadcrumb etc.</span> |
| $boxes-color | Textfarbe von Boxen,<br><span style="font-size:12px;">Teaserboxen, Kontakt-Box, News-Boxen, Event-Boxen, Formularfelder, Breadcrumb etc.</span> |
| $info | Hintergrundfarbe für Info-Box,<br><span style="font-size:12px;">siehe Textelemente auf Demo-Seite</span> |
| $success | Hintergrundfarbe für Erfolgs-Box,<br><span style="font-size:12px;">siehe Textelemente auf Demo-Seite</span> |
| $warning | Hintergrundfarbe für Warnungs-Box,<br><span style="font-size:12px;">siehe Textelemente auf Demo-Seite</span> |
| $danger | Hintergrundfarbe für Achtung-Box,<br><span style="font-size:12px;">siehe Textelemente auf Demo-Seite</span> |

#### Variablen der \_custom\_variables.scss

In der **\_custom\_variables.scss** sind bereits diverse Variablen definiert um das Theme nach Ihren Vorstellungen anzupassen. Das Bulma Framework, auf dem das Theme basiert, bietet auch noch mehr Variablen an, die Sie definieren können. Diese finden Sie für folgende Elemente in der Bulma Dokumentation:

[Breadcrumb](https://bulma.io/documentation/components/breadcrumb/#variables)  
[Buttons](https://bulma.io/documentation/elements/button/#variables)  
[Footer](https://bulma.io/documentation/layout/footer/#variables)  
[Formulare](https://bulma.io/documentation/form/input/#variables)  
[Hauptnavigation](https://bulma.io/documentation/components/navbar/#variables)  
[Modaler Dialog](https://bulma.io/documentation/components/modal/#variables)  
[Pagination](https://bulma.io/documentation/components/pagination/#variables)  
[Unterseiten-Navigation](https://bulma.io/documentation/components/menu/#variables)  
[Tabellen](https://bulma.io/documentation/elements/table/#variables)  
[Tabs](https://bulma.io/documentation/components/tabs/#variables)  