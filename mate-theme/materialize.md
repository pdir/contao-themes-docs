#### Dokumentation - Mate Theme für Contao

---

# Materialize

Das Mate Theme nutzt das Front-End-Framework [Materialize](http://materializecss.com/) basierend auf [Material Design](https://material.io/guidelines/).

## Farben

Eine Palette der Farben, die Materialize mitbringt, finden Sie [hier](http://materializecss.com/color.html). Jede der Farben besteht aus einer Grundklasse und optionalen Klassen, die die Farbe heller oder dunkler machen.

#### Hintergrundfarbe

Um die Hintergrundfarbe eines Elementes anzupassen, fügen Sie dem Element einfach eine Klasse mit dem Farbnamen und eine Klasse mit der gewünschten Helligkeitsstufe hinzu.

![](/mate-theme/images/materialize/hintergrundfarbe.png)

#### Textfarbe

Um eine Textfarbe anzugeben, müssen Sie nur den Farbnamen mit dem Suffix -text verwenden.

![](/mate-theme/images/materialize/textfarbe.png)

## Grid

Materialize nutzt ein 12-Spalten-Grid-System. Beispiele und Erläuterungen dazu finden Sie auch auf der [Materialize-Webseite](http://materializecss.com/grid.html).

#### Bildschirmgrößen

|  | Mobile Geräte | Tablet-Geräte | Desktop-Geräte | große Desktop-Geräte |
| :--- | :--- | :--- | :--- | :--- |
| Auflösung | &lt;= 600px | &gt; 600px | &gt; 992px | &gt; 1200px |
| Klassen-Prefix | .s | .m | .l | .xl |
| Spalten-Anzahl | 12 | 12 | 12 | 12 |

Es muss immer die Klasse **col** vorangestellt werden. Werden beispielsweise die Klassen `col s12 m6 l4` verwendet, bewirkt dies, dass das Element ...

* bei mobilen Geräten 12 Spalten breit dargestellt wird.
* bei Tablet-Geräten 6 Spalten breit dargestellt wird.
* bei Desktop-Geräten 4 Spalten breit dargestellt wird.

#### Anwendung

Um Elementen diese Klassen vergeben zu können, wird die Erweiterung Advanced Classes verwendet. 

## Icons



