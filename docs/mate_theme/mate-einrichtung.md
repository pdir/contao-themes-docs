
# Einrichtung

## CSS-Anpassungen

Wie Sie Farben und Schriften sowie eigenes CSS definieren können, ist auf der Seite [Farben und Schriften](mate_theme/mate-farben-und-schriften.md) erklärt.

## JavaScript-Anpassungen

Für eigenes JavaScript legen Sie sich bitte eine eigene Datei an und binden diese im Theme ein.

## Elemente über ein eigenes Insert-Tag platzieren

Unter der Seite **MATE-Elements** befinden sich Artikel, die mittels eines Insert-Tags an jeder beliebigen Stelle der Webseite eingebunden werden können. Zu den Artikeln gelangen Sie, indem Sie im linken Menü auf Artikel klicken und ganz nach unten scrollen. In den Artikel-Einstellungen des jeweiligen **Artikels **\(Werkzeug-Icon\) wählt man dafür unter **Template-Einstellungen** den passenden **Theme Helper Tag** aus \(siehe Bild 2\).

Es ist nicht möglich neue Theme Helper Tags anzulegen. Das Theme bringt allerdings jeweils 10 Theme Helper Tags für Header, Modules und Footer mit, die man für neu angelegte Artikel nutzen kann.

Den Artikel kann man danach über folgenden Insert-Tag in einem **HTML-Element** oder einem **Template** platzieren: z. B.  `{{theme::content::MATE02/01}}` \(siehe Bild 3\). Die erste Nummer bezeichnet den Typ \(Header, Modules oder Footer\). Die zweite Nummer entspricht der Nummer des Theme Helper Tags im Artikel.

###### Bild 1: Artikel unter MATE Elements

![](../_images/mate-theme/theme-helper.png)

###### Bild 2: Theme Helper Tag im Artikel auswählen

![](../_images/mate-theme/theme-helper-tag.png)

###### Bild 3: Artikel über den Theme Helper Tag einbinden

![](../_images/mate-theme/theme-helper-tag-einbinden.png)

## Header anpassen

Die Inhalte des Headers liegen in den Artikeln unter **MATE Elements - 01 Header**. Wählen Sie dafür im linken Menü Artikel aus und scrollen Sie bis ganz nach unten. Die Öffnungszeiten, Telefonnummer und E-Mail sowie die dazugehörigen Icons sind im Modul **Header / Top** eingebunden. Das Logo, die Navigation und die Suche werden über das Modul **Navigation / Hauptnavigation** geladen.

Das Logo kann im Artikel **01/04 Logo** ausgetauscht werden. Wählen Sie dafür im linken Menü Artikel aus und scrollen Sie bis ganz nach unten. Es sind hier zwei Logos eingebunden, wobei das zweite Logo dann erscheint, wenn man in der Seite nach unten scrollt und die Navigation einen grünen Hintergrund bekommt. Das zweite Logo muss die Klasse **fixed-nav** bekommen.

## Footer anpassen

Die Inhalte vom Footer liegen in den Artikeln unter **MATE Elements - 05 Footer**. Wählen Sie dafür im linken Menü Artikel aus und scrollen Sie bis ganz nach unten. Eingebunden sind diese, genau wie die Newsletter-Box \(Infos dazu unter [Theme-Elemente](mate_theme/mate-theme-elemente.md)\) im Modul **Footer**.

