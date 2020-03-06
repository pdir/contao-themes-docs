
# Module

Alle Module sind bereits auf der Seite **Module** beispielhaft eingebunden.

Folgende Elemente werden auf dieser Seite erklärt:
- [Breadcrumb](mate_theme/mate-module?id=breadcrumb)
- [Events](mate_theme/mate-module?id=events)
- [Formulare](mate_theme/mate-module?id=formulare)
- [Login-Formular](mate_theme/mate-module?id=login-formular)
- [Modale Dialoge](mate_theme/mate-module?id=modale-dialoge)
- [Navigation](mate_theme/mate-module?id=navigation)
- [News](mate_theme/mate-module?id=news)
- [Suche](mate_theme/mate-module?id=suche)

## Breadcrumb

Um eine Breadcrumb hinzuzufügen, legen Sie unter **Themes > Frontend-Module des Theme bearbeiten** (Zahnrad-Icon) 
ein neues Modul vom Typ **Navigationspfad** an. Bei Individuelles Template muss **mod_breadcrumb_mate** ausgewählt werden.

![](../_images/mate-theme/module/breadcrumb_modul.png)

Danach navigieren Sie wieder zu **Themes** und bearbeiten die **Seitenlayouts** des Themes (rechts neben dem 
Zahnrad-Icon). Unter **Frontend-Module - Eingebundene Module** fügen Sie eine neue Zeile ein, indem Sie auf das grüne 
Plus klicken. Beim Modul wählen Sie das eben angelegte **Modul** und bei Layoutbereich **Kopfzeile** aus.

![](../_images/mate-theme/module/breadcrumb_layout.png)

Am Ende sollte die Breadcrumb wie im folgenden Beispiel aussehen.

![](../_images/mate-theme/module/breadcrumb_beispiel.png)

## Events

#### **Eventliste mit Bildern und Teaser**

Für eine Eventliste mit Bildern und einem Teasertext muss im Modul das Template **event\_mate\_teaser** sowie die Bildgröße **News-Box \(520x350\)** ausgewählt werden. Im Modul der Detailansicht muss das Template **event\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/events-mit-bildern-und-teasertext.png)

#### **Eventliste ohne Bilder und mit Teaser**

Für eine Eventliste ohne Bilder und mit einem Teasertext muss im Modul das Template **event\_mate\_list** ausgewählt werden. Im Modul der Detailansicht muss das Template **event\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/events-mit-teasertext.png)

#### **Eventliste**

Für eine einfache Eventliste ohne Bilder und Teasertext muss im Modul das Template **event\_mate\_upcoming** ausgewählt werden. Im Modul der Detailansicht muss das Template **event\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/events-simple.png)

## Formulare

Für das Feld Dateiupload muss das individuelle Template **form\_mate\_upload**\_ \_ausgewählt werden.

## Login-Formular

Für den Modultyp Login-Formular muss das individuelle Template **mod\_login\_mate** ausgewählt werden.

## Modale Dialoge

Ab der Version 2.0.0 des Mate Themes ist es möglich [Modale Dialoge](https://materializecss.com/modals.html) per Modul zu setzen. Navigieren Sie zu den Frontend-Modulen und legen ein neues Modul vom Typ **Modal** an. Dort können Sie einen Link setzen sowie Diesem zusätzliche Klassen vergeben und den eigentlichen Inhalt des Modalen Dialoges bearbeiten. Das Modul können Sie an einer beliebigen Stelle, z. B. im Artikel, einbinden.

Wenn der Modale Dialog am unteren Bildschirmrand fixiert sein soll, fügen Sie im Feld **CSS-Klassen für den Modalen Dialog**
 die Klasse **bottom-sheet** ein.
 
![](../_images/mate-theme/module/modal_einstellungen.png)

## News

#### **News mit Bildern und Teaser**

Für News mit Bildern und einem Teasertext muss im Modul das Template **news\_mate\_latest** sowie die Bildgröße N**ews-Box \(520x350\)** ausgewählt werden. Im Modul der Detailansicht muss das Template **news\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/news-mit-bildern-und-teasertext.png)

#### **News ohne Bilder und mit Teaser**

Für News ohne Bilder und mit einem Teasertext muss im Modul das Template **news\_mate\_short** ausgewählt werden. Im Modul der Detailansicht muss das Template **news\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/news-mit-teasertext.png)

#### **Einfache Newsliste**

Für eine einfache Newsliste ohne Bilder und Teasertext wird kein eigenes Template mitgeliefert. Im Modul der Detailansicht muss das Template **news\_mate\_full** ausgewählt werden.

![](../_images/mate-theme/module/news-simple.png)

## Navigation

Für die Navigationen gibt es einen eigenen Modultyp **Navbar**. In den Navbar-Einstellungen \(siehe Bild 1\) gibt es die Möglichkeit zwei verschiedene **Navbar-Typen** auszuwählen: **Navbar mit Dropdown** und **Linksbündig**. Beispielintegrationen finden Sie unter dem Menüpunkt Module - Navigation.

###### Bild 1: Navbar-Einstellungen![](../_images/mate-theme/navbar.png)

#### **Dropdown-Navigation**

Das Icon für die Suche und die mobile Navigation sind standardmäßig ausgeblendet, wenn die Navigation nicht im Header platziert wird. Als Navigations-Template wird **mod\_mate\_navbar** verwendet.

![](../_images/mate-theme/module/navigation-dropdown.png)

#### **Linksbündige Navigation**

Die linksbündige Navigation kann nur eine Navigationsebene darstellen. Das Icon für die Suche und die mobile Navigation sind ebenfalls standardmäßig ausgeblendet, wenn die Navigation nicht im Header platziert wird. Als Navigations-Template wird **mod\_mate\_navbar\_left** verwendet.

![](../_images/mate-theme/module/navigation-linksbuendig.png)

#### **Unterseiten-Navigation**

Für eine Unterseiten-Navigation, wie sie z. B. in der Demo in der linken und rechten Spalte platziert ist, wählt man den Navbar-Typ **Linksbündig** aus und vergibt dem Modul die Klasse **subnav**. Logo, Suche und mobile Navigation müssen ausgeblendet werden.

![](../_images/mate-theme/module/navigation-unterseiten.png)

## Suche

Für das Suchmaschinen-Modul muss das Template **search\_mate** ausgewählt werden.