#### Dokumentation - Mate Theme für Contao

---

# Einrichtung

## CSS-Anpassungen

Wenn das Theme erfolgreich installiert wurde, befinden sich die [SCSS](https://sass-lang.com/documentation/file.SASS_REFERENCE.html)-Dateien in der Dateiverwaltung unter dem Pfad **mate/sass**. Für individuelle Anpassungen benennen Sie die **custom.scss.example** in **custom.scss** sowie die** \_custom\_variables.scss.example** in **\_custom\_variables.scss** um.

In der \_custom\_variables.scss können Sie Farben und Schriften über Variabeln festlegen und diese in der custom.scss verwenden. Alle anderen scss- und css-Dateien sollten nicht bearbeitet werden.

## JavaScript-Anpassungen

JavaScript-Anpassungen können in der **theme.js** unter dem Pfad **mate/js** vorgenommen werden.

## Elemente über ein eigenes Insert-Tag platzieren

Unter der Seite **MATE-Elements** befinden sich Artikel, die mittels einem Insert-Tag an jeder anderen beliebigen Stelle eingebunden werden können. In den Artikel-Einstellungen des jeweiligen **Artikel** wählt man dafür unter **Template-Einstellungen** den passenden **Theme Helper Tag** aus \(siehe Bild 2\).

Es ist nicht möglich neue Theme Helper Tags anzulegen. Das Theme bringt allerdings jeweils 10 Theme Helper Tags für Header, Moduls und Footer mit, die man für neu angelegte Artikel nutzen kann.

Den Artikel kann man danach über folgenden Insert-Tag in einem **HTML-Element** oder einem **Template** platzieren: z. B.  `{{theme::content::MATE02/01}}` \(siehe Bild 3\). Die erste Nummer bezeichnet den Typ \(Header, Moduls oder Footer\). Die zweite Nummer entspricht der Nummer des Theme Helper Tags im Artikel.

###### Bild 1: Artikel unter MATE Elements![](/mate-theme/images/theme-helper.png)

###### Bild 2: Theme Helper Tag im Artikel auswählen![](/mate-theme/images/theme-helper-tag.png)

###### Bild 3: Artikel über den Theme Helper Tag einbinden![](/mate-theme/images/theme-helper-tag-einbinden.png)

## Header anpassen

Die Inhalte des Headers liegen in den Artikeln unter **MATE Elements - 01 Header**. Die Öffnungszeiten, Telefonnummer und E-Mail sowie die dazugehörigen Icons sind im Modul **Header / Top** eingebunden. Das Logo, die Navigation und die Suche werden über das Modul **Navigation / Hauptnavigation** geladen.

Das Logo kann im Artikel **01/04 Logo** ausgetauscht werden. Es sind hier zwei Logos eingebunden, wobei das zweite Logo dann erscheint, wenn man in der Seite nach unten scrollt und die Navigation einen grünen Hintergrund bekommt. Das zweite Logo muss die Klasse **fixed-nav** bekommen.

## Footer anpassen

Die Inhalte vom Footer liegen in den Artikeln unter **MATE Elements - 05 Footer**. Eingebunden sind diese, genau wie die Newsletter-Box \(Infos dazu unter [Theme-Elemente](/mate-theme/theme-elemente.md)\) im Modul **Footer**.

