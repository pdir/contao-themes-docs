#### Dokumentation - Mate Theme für Contao

---

# Inhaltselemente

Alle Module sind bereits auf der Seite** Elemente **beispielhaft eingebunden.

## Überschriften

Wenn ein Inhaltselement mit einer Überschrift die Klasse **bordered-left** oder **bordered-right** bekommt, wird die Überschrift mit einem Rahmen unten links bzw. unten rechts dargestellt.

## Content-Slider

#### **Contao-eigener Content-Slider**

Bei dem Element Content-Slider \(Umschlag Anfang\) muss das Template **ce\_sliderStart\_mate** ausgewählt werden. Bei dem abschließenden Element Content-Slider \(Umschlag Ende\) muss das Template **ce\_sliderStop\_mate** ausgewählt werden. Der Slider wird wie im Style Guide Beispiel gestylt, wenn die Textelemente die Klasse **slidebox1** bekommen.

Wenn dem Umschlag-Anfang-Element die Klasse **smaller** vergeben wird, wird der Content Slider nur mit einer Höhe von 250px dargestellt.

#### Content-Slider mit Newsbeiträgen

Bei einem Content-Slider mit Newsbeiträgen müssen beim Umschlag-Anfang und Umschlag-Ende Element die gleichen Templates ausgewählt werden wie beim contao-eigenen Content-Slider. Innerhalb des Umschlages wird ein Nachrichtenlisten-Modul platziert, bei welchem das Nachrichtentemplate **news\_mate\_slider**\_ und das individuelle Template **mod\_newslist\_mate\_slider** ausgewählt sein muss.

## Media-Elemente

#### Galerie

Je nachdem wie viele Vorschaubilder pro Reihe angezeigt werden sollen, passt sich die Anordnung der Bilder automatisch an und nimmt den kompletten Platz, der zur Verfügung steht, ein.

#### YouTube-Video

Für ein YouTube-Video muss das Template **ce\_youtube\_mate** ausgewählt werden.

## Content-Box

Für die Content-Box muss der Elementtyp **Content-Box** ausgewählt werden. Breite und Farben der Boxen werden durch das Vergeben von CSS-Klassen bzw. über die CSS-Datei angepasst.

## Teaser-Box

Für die Teaser-Box muss der Elementtyp **Teaserbox** ausgewählt werden. Die Breite der Boxen kann durch das Vergeben von CSS-Klassen angepasst werden. Wenn ein Bild hinzugefügt wird, muss die Bildgröße **Teaser-Box \(450x270\)** ausgewählt werden.

## Headerbild

Für das Headerbild muss der Elementtyp **Bild** sowie das Template **ce\_image\_mate\_headerimage** ausgewählt werden. Für ein schmaleres Headerbild muss dem Element die Klasse **smaller** gegeben werden. Der Bildausschnitt kann über das Festlegen des wichtigen Bereiches im Bild ausgewählt werden.

Eine Beispielintegration für ein normales Headerbild finden Sie auf der Seite Layout mit linker Spalte. Eine Beispielintegration für ein schmales Headerbild finden Sie auf der Seite Layout mit rechter Spalte.

