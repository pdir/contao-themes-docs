#### Dokumentation - Mate Theme für Contao

---

# Theme-Elemente

Auf dieser Seite sind alle Elemente aufgelistet, die das Theme bereits mitbringt.

## News-Slider

Im News-Slider ist es möglich Newsbeiträge in einem Slider darzustellen. Der Slider ist auf der Startseite der Demo-Seite eingebunden. Im Theme ist der Slider im Artikel **Start** in der **Kopfzeile** über den Insert-Tag `{{theme::content::MATE02/01}}` eingebunden.

Sie benötigen dafür keine Content-Slider Umschlag-Elemente, sondern müssen lediglich ein Modul vom Typ **Nachrichtenliste** einbinden. Beim Nachrichtentemplate muss **news\_mate\_slider** sowie beim individuellen Template **mod\_newslist\_mate\_slider** ausgewählt werden. Die Gesamtanzahl der Beiträge ist variabel auswählbar.

Das Bild sowie die Teasertexte können Sie jeweils in den Beitragseinstellungen des Newsbeitrages auswählen.

![](/mate-theme/images/mate-elemente/news-slider.jpg)

## Content-Box

Für die Content-Box muss der Elementtyp **Content-Box** ausgewählt werden. Die Hintergrundfarbe kann geändert werden, indem man dem Element Klassen vergibt \(z. B. "grey lighten-3", für mehr Informationen siehe Abschnitt [Farben](/mate-theme/materialize.md)\) oder man das CSS \(custom.scss\) anpasst. Erläuterungen, wie Elemente nebeneinander dargestellt werden können, finden Sie im Abschnitt [Grid](/mate-theme/materialize.md).

![](/mate-theme/images/mate-elemente/content-box.jpg)

## Teaser-Box

Für die Teaser-Box muss der Elementtyp **Teaserbox** ausgewählt werden. Die Breite der Boxen kann durch das Vergeben von CSS-Klassen angepasst werden. Wenn ein Bild hinzugefügt wird, muss die Bildgröße **Teaser-Box \(450x270\)** ausgewählt werden.

![](/mate-theme/images/mate-elemente/teaser-box.jpg)

## Headerbild

Für das Headerbild muss der Elementtyp **Bild** sowie das Template **ce\_image\_mate\_headerimage** ausgewählt werden. Für ein schmaleres Headerbild muss dem Element die Klasse **smaller** gegeben werden. Der Bildausschnitt kann über das Festlegen des wichtigen Bereiches im Bild ausgewählt werden.

Eine Beispielintegration für ein normales Headerbild finden Sie in der Demo-Seite auf den Layout-Seiten. Eine Beispielintegration für ein schmales Headerbild finden Sie auf der Seite Kontakt.

**Normales Headerbild:**

![](/mate-theme/images/mate-elemente/headerbild-normal.jpg)

**Schmales Headerbild:**

![](/mate-theme/images/mate-elemente/headerbild-schmal.jpg)

## Einfache Inhaltsbox

Man kann einem Element vom **Elementtyp Text** einen weißen Hintergrund mit etwas Abstand geben, indem man dem Element das individuelle Template **ce\_text\_simplebox\_mate** vergibt.

![](/mate-theme/images/mate-elemente/simple-box.jpg)

## Newsletter-Box

Im Footer ist es möglich einen Bereich für die Newsletter-Anmeldung zu integrieren. Die Newsletter-Box ist im **Modul Footer** über den Insert-Tag `{{theme::content::MATE02/01}}` eingebunden. Das Modul dazu ist in einem Artikel unter **MATE Elements - Moduls - 02/02 newsletter** eingebunden. Damit das CSS geladen wird, muss der Artikel die ID **newsletter** besitzen.

![](/mate-theme/images/mate-elemente/newsletter-box.jpg)

