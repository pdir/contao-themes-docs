# Elemente

Auf dieser Seite sind alle Contao-Elemente erklärt und wie Sie diese einsetzen können.

## Elemente mit Schrägen

Auf der Seite [Elemente mit Schrägen](http://odd.contao-themes.net/layouts/elemente-mit-schrägen.html) sind bereits diverse Beispiele von Elementen mit Schrägen platziert.

Jeder Bereich muss in einem eigenen Artikel sein, der verschiedene Klassen bekommen muss:

`primary-bg`: Hintergrundfarbe  
`skw-tl`: Schräge nach oben links  
`skw-tr`: Schräge nach oben rechts  
`skw-bl`: Schräge nach unten links  
`skw-br`: Schräge nach unten rechts  

Um dem Artikel beispielsweise Schrägen nach oben rechts und unten links zu vergeben (wie das erste Beispiel auf der Demo-Seite), fügen Sie in den **Artikeleinstellungen** unter **Experten-Einstellungen** die Klassen `primary-bg skw-tr skw-br` hinzu.

![](_images/odd-theme/elemente/elemente_schraegen_klassen.png)

**Hilfe-Tabelle zum Vergeben der Artikel-Klassen:**

| Schräge | Klassen im Artikel | Screenshot |
| ------------- | ------------- | ------------- |
| oben rechts - unten rechts | `primary-bg skw-tr skw-br` | <img src="_images/odd-theme/elemente/schraege_1.png" width="200"/> |
| oben links - unten links | `primary-bg skw-tl skw-bl` | <img src="_images/odd-theme/elemente/schraege_2.png" width="200"/> |
| oben links - unten rechts | `primary-bg skw-tl skw-br` | <img src="_images/odd-theme/elemente/schraege_3.png" width="200"/> |
| oben rechts - unten links | `primary-bg skw-tr skw-bl` | <img src="_images/odd-theme/elemente/schraege_4.png" width="200"/> |
| oben rechts | `primary-bg skw-tr` | <img src="_images/odd-theme/elemente/schraege_5.png" width="200"/>  |
| unten rechts | `primary-bg skw-br` | <img src="_images/odd-theme/elemente/schraege_6.png" width="200"/>  |
| oben links | `primary-bg skw-tl` |  |
| unten links | `primary-bg skw-bl` |  |

## Headerbild

Um ein Headerbild zu platzieren verwenden Sie den Elementtyp **Bild** und fügen unter Template-Einstellungen das Template **ce\_image\_headerimage\_odd** hinzu. 

#### Headerbild ohne Schrägen

Für ein Headerbild ohne Schrägen wählen Sie bei der Bildgröße **Headerbild (1920x400)** aus. Das Headerbild müssen Sie in einem eigenen Artikel platzieren und in den **Artikeleinstellungen** das Template mod\_article\_fullwidth auswählen.

Ein Beispiel finden Sie auf der Seite [Headerbild ohne Schräge](http://odd.contao-themes.net/layouts/headerbild-layouts/ohne-schräge.html).

<img src="_images/odd-theme/elemente/headerbild_schraege_ohne.png" width="400"/>

#### Headerbild mit Schräge nach links

Für ein Headerbild mit einer Schräge nach links wählen Sie bei der Bildgröße **Headerbild (1920x400)** aus. Das Headerbild müssen Sie in einem eigenen Artikel platzieren, in den **Artikeleinstellungen** das Template mod\_article\_fullwidth auswählen und unter **Experten-Einstellungen** die Klasse `skw-bl` hinzufügen.

Ein Beispiel finden Sie auf der Seite [Headerbild mit Schräge nach links](http://odd.contao-themes.net/layouts/headerbild-layouts/schräge-nach-links.html).

<img src="_images/odd-theme/elemente/headerbild_schraege_links.png" width="400"/>

#### Headerbild mit Schräge nach rechts

Für ein Headerbild mit einer Schräge nach rechts wählen Sie bei der Bildgröße **Headerbild (1920x400)** aus. Das Headerbild müssen Sie in einem eigenen Artikel platzieren, in den **Artikeleinstellungen** das Template mod\_article\_fullwidth auswählen und unter **Experten-Einstellungen** die Klasse `skw-br` hinzufügen.

Ein Beispiel finden Sie auf der Seite [Headerbild mit Schräge nach rechts](http://odd.contao-themes.net/layouts/headerbild-layouts/schräge-nach-rechts.html).

<img src="_images/odd-theme/elemente/headerbild_schraege_rechts.png" width="400"/>

## Überschriften

#### mit Unterstrich linksbündig

Damit die Überschrift linksbündig und mit Unterstrich dargestellt wird, geben Sie dem Textelement die Klasse `bordered-heading`.

<img src="_images/odd-theme/elemente/ueberschrift_unterstrich_links.png" width="500" />

#### mit Unterstrich mittig

Damit die Überschrift mittig und mit Unterstrich dargestellt wird, geben Sie dem Textelement die Klasse `bordered-heading` und `text-sm-center`. 

Die Klasse text-sm-center können Sie bei **Erweiterte CSS-Klassen** unter **Ausrichtung** setzen.

<img src="_images/odd-theme/elemente/text-sm-center.png" />

<img src="_images/odd-theme/elemente/ueberschrift_unterstrich_mittig.png" width="500" />

#### mit Unterstrich rechtsbündig

Damit die Überschrift rechtsbündig und mit Unterstrich dargestellt wird, geben Sie dem Textelement die Klasse `bordered-heading` und `text-sm-right`.

Die Klasse text-sm-right können Sie bei **Erweiterte CSS-Klassen** unter **Ausrichtung** setzen.

<img src="_images/odd-theme/elemente/text-sm-right.png" />

<img src="_images/odd-theme/elemente/ueberschrift_unterstrich_rechts.png" width="500" />

## Hyperlinks

Wenn Sie einem Link die Klasse `btn` geben wird er wie ein Button dargestellt.

<img src="_images/odd-theme/elemente/button.png" />

## Content Slider

folgt ...