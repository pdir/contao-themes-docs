#### Dokumentation - Mate Theme für Contao

---

# Farben und Schriften

Wenn das Theme erfolgreich installiert wurde, befinden sich die [SCSS](https://sass-lang.com/documentation/file.SASS_REFERENCE.html)-Dateien in der Dateiverwaltung unter dem Pfad **mate/sass**. Für individuelle Anpassungen nutzen Sie einfach die **custom.scss**, in der Sie sowohl SCSS oder auch normales CSS schreiben können, sowie die** \_custom\_variables.scss**.

In der \_custom\_variables.scss können Sie Farben und Schriften über Variabeln anpassen oder neue Variablen anlegen und diese in der custom.scss verwenden.

Wenn Sie lieber mit CSS-Dateien statt mit SCSS-Dateien arbeiten wollen, können Sie über **Themes - Stylesheets** einen neuen Stylesheet anlegen und ihn im **Layout** bei **Interne Stylesheets** einbinden. Das CSS wird anschließend automatisch nach dem CSS des Mate Theme geladen.

## Farbschemen

Das MATE Theme wird standardmäßig mit einem grünen Layout ausgeliefert. Es gibt die Möglichkeit das Theme auf ein dunkles \(dark\), blaues \(blue\) oder gelbes Layout \(yellow\) umzustellen. Bearbeiten Sie dafür die **\_custom\_variables.scss** und kommentieren Sie bei **Colour Schemes** die entsprechende Zeile ein \(die Schrägstriche entfernen\).

Wenn Sie weitere Anpassungen vornehmen wollen, können Sie die weiteren Variablen unter **MATE Theme Variables** und **MATE Theme Specific Variables** in der **\_custom\_variables.scss** nutzen. Kommentieren Sie die entsprechende Zeile aus, damit die Änderung aktiv wird.

## Erklärungen zu den Variablen

#### Schriften:

**$font1: **Haupt-Schriftart  
**$font2:** Überschriften für h1, News und Events  
**$font3: **Überschriften für h2, h3, h4, h5 und h6

#### Grundfarben:

**$mateColor1:** Hauptfarbe helle Abstufung  
**$mateColor2:** Hauptfarbe  
**$mateColor3:** Hauptfarbe dunkle Abstufung  
**$mateColor4:** Sekundärfarbe  
**$mateColor6:** Sekundärfarbe helle Abstufung  
**$mateColorWhite:** Weiß  
**$mateColorBlack:** Schwarz  
**$pageBackground:** Hintergrund der Webseite

**$primary-color: **Hauptfarbe \(standardmäßig $mateColor2\)  
**$secondary-color:** Sekundärfarbe \(standardmäßig $mateColor3\)

#### Textfarben:

**$primary-text-color:** alle Textfarben, die im Standard-Layout schwarz sind  
**$secondary-text-color:** alle Textfarben, die im Standard-Layout weiß sind

#### Boxen:

**$boxes-background:** Hintergrund der Boxen \(z. B. Contentbox, Teaserbox, News, Events, Login, Newsletter, etc.\)  
**$boxes-text-color:** Schriftfarbe der Boxen \(z. B. Contentbox, Teaserbox, News, Events, Login, Newsletter, etc.\)

---

#### Akkordion:

**$accordion-headline-background:** Hintergrund der Überschrift  
**$accordion-headline-color:** Schriftfarbe der Überschrift  
**$accordion-content-background:** Hintergrund des Inhalts  
**$accordion-content-color:** Schriftfarbe des Inhalts  
**$accordion-border-color:** Rahmenfarbe



