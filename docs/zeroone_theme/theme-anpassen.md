# Theme anpassen

## Header und Footer

Die Inhalte des Headers können Sie in den Artikeln unter **Elemente** > **01 Header** bearbeiten.

Die Inhalte des Footers können Sie in den Artikeln unter **Elemente** > **03 Footer** bearbeiten.

![Header und Footer Inhalte anpassen](../_images/zeroone-theme/einrichtung/header_footer_artikel.png)

## Styling anpassen

Wenn das Theme erfolgreich installiert wurde, befinden sich die SCSS-Dateien in der Dateiverwaltung unter dem Pfad 
**zeroOne/scss**. Für individuelle Anpassungen nutzen Sie einfach die **custom.scss**, in der Sie sowohl SCSS als auch 
normales CSS schreiben können, und die **_custom_variables.scss**.

In der **_custom_variables.scss** können Sie die Farben und die Schriftart des Themes verändern und ein anderes 
Farbschema auswählen. Wenn Sie eine Variable anpassen möchten, müssen Sie die Zeile auskommentieren 
(Schrägstriche entfernen).

Wenn Sie lieber mit CSS-Dateien statt mit SCSS-Dateien arbeiten wollen, können Sie über Themes - Stylesheets einen 
neuen Stylesheet anlegen und ihn im Layout bei Interne Stylesheets einbinden. Das CSS wird anschließend automatisch 
nach dem CSS des Theme geladen.

### Farbschemen

Das 0.1 Theme wird standardmäßig mit einem hellen Layout in orangenen/gelben Farben ausgeliefert. Sie haben aber die
Möglichkeit andere Farbschemen zu aktivieren:

* Helles Farbschema - Orange/Gelb (DAY)
* Helles Farbschema - Grün/Blau (EARTH)
* Helles Farbschema - Rot/Blau (NIGHT)

Wenn Sie auf ein Layout umstellen wollen, kommentieren Sie in der **\_custom\_variables.scss** die entsprechende Zeile 
bei **Colour Schemes** aus (Schrägstriche entfernen). Gegebenenfalls müssen Sie die Seite mit Strg + F5 neuladen, 
damit die Änderung greift.

Beispiel um das EARTH Farbschema zu aktivieren:

```
@import '/colour_schemes/earth';
//@import '/colour_schemes/night';
```

#### Dark Mode

Bei vielen Geräten haben Sie die Möglichkeit den Dark Mode bzw. Dunkelmodus zu aktivieren, der die Benutzeroberfläche 
in einen dunklen Hintergrund und den Text zur besseren Lesbarkeit in eine hellere Farbe ändert. Wenn Sie den Dark Mode 
aktivieren wird im 0.1 Theme automatisch zu einem dunkleren Farbschema geändert, egal welches Farbschema Sie gerade 
aktiv haben. Dies hat den Vorteil, dass nachts Ihre Augen weniger belastet werden und es besteht eine geringe Chance, 
dass die Akkulaufzeit damit verbessert werden kann.

In der **_custom_variables.scss** können Sie den Dark Mode auch deaktivieren, indem Sie die entsprechende Zeile 
einkommentieren (zwei Schrägstriche an den Anfang der Zeile).

```
//@import '/colour_schemes/dark_mode';
```

#### Anpassung der Bilder an des Farbschema

Die Bilder von News, Events und dem Parallax-Element werden farblich automatisch an das Farbschema angepasst. Außerdem 
können Sie einem Bild-Element die Klasse **css-filter** mitgeben um das Bild entsprechend dem Theme farblich anzupassen.

Sie können dies in der **_custom_variables.scss** deaktivieren, in dem Sie die folgende Zeile einkommentieren 
(zwei Schrägstriche an den Anfang der Zeile).

Bis auf den Internet Explorer funktioniert dies in allen Browsern.

```
//@import '/colour_schemes/adjust_images';
```

#### Variablen

Um Farben und die Schriftart anzupassen kommentieren Sie in der **_custom_variables.scss** die entsprechenden Zeilen 
aus (Schrägstriche entfernen).

| Variable | Bedeutung |
| ------------- | ------------- |
| $body-font-family | Schriftart |
| $zeroOneColor_1 | Dunkle Schriften und Hintergründe, <br><span style="font-size:12px;">Navigation, Nach-oben-Button, Buttons, Textfarbe bei Verlauf-Hintergrund, Footer, Formular-Labels</span> |
| $zeroOneColor_2 | Dunkle Hauptfarbe, <br><span style="font-size:12px;">Verlauf-Hintergrund rechts, Button- und Link-Hover</span> |
| $zeroOneColor_3 | Helle Hauptfarbe, <br><span style="font-size:12px;">Verlauf-Hintergrund links, Aktives Tab-Element, Hover bei Social Icons, Termine im Kalender</span> |
| $zeroOneColor_4 | Überschriften Dunkle Hauptfarbe |
| $zeroOneColor_5 | Helle Schriften, <br><span style="font-size:12px;">Buttons, Navigation 1. Ebene, Parallax-Element, Nach-oben-Button, Footer, Formulare</span> |
| | |
| $body-bg | Hintergrundfarbe der Seite |
| $body-font-color | Schriftfarbe |
| $link-color | Linkfarbe |
| $link-color-dark | Linkfarbe bei Hover |
| $boxes-background | Hintergrundfarbe für Boxen, <br><span style="font-size:12px;">News- und Eventliste ohne Bilder, Kalender, Formulare, Gestreifte Tabellen</span> |
| | |
| $footer-background_1 | Hintergrundfarbe des oberen Footer-Bereich |
| $footer-color-1 | Schriftfarbe des oberen Footer-Bereich |
| $footer-background-2 | Hintergrundfarbe des unteren Footer-Bereich (Copyright) |
| $footer-color-2 | Schriftfarbe des unteren Footer-Bereich (Copyright) |
