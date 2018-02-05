#### Dokumentation - Mate Theme für Contao

---

# Materialize

Das Mate Theme nutzt das Front-End-Framework [Materialize](http://materializecss.com/) basierend auf [Material Design](https://material.io/guidelines/).

## Farben {#farben}

Eine Palette der Farben, die Materialize mitbringt, finden Sie auf der [Materialize-Seite](http://materializecss.com/color.html) oder im Theme unter Elemente und Farben. Jede der Farben besteht aus einer Grundklasse und optionalen Klassen, die die Farbe heller oder dunkler machen.

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

Es muss immer die Klasse **col** vorangestellt werden. Sollen mehrere Elemente nebeneinander dargestellt werden, muss dem Eltern-Element die Klasse **row** vergeben werden. Werden beispielsweise die Klassen `col s12 m6 l4` verwendet, bewirkt dies, dass das Element ...

* bei mobilen Geräten 12 Spalten breit dargestellt wird.
* bei Tablet-Geräten 6 Spalten breit dargestellt wird.
* bei Desktop-Geräten 4 Spalten breit dargestellt wird.

#### Anwendung

Um Elementen diese Klassen vergeben zu können, wird die Erweiterung **Advanced Classes** verwendet. Die Klassen kann man bei Inhaltselementen unter **Erweiterte CSS-Klassen** hinzufügen \(siehe Bild 3\), wobei nicht alle Elemente unterstützt werden \(bspw. die Teaser- oder Content-Box\). Wird das Element nicht unterstützt, muss man die Klassen händisch in den **Experten-Einstellungen **hinzufügen.

###### Bild 3: Erweiterte CSS-Klassen setzen![](/mate-theme/images/materialize/grid.png)

Damit die Elemente richtig dargestellt werden, muss das umfassende Element die Klasse **row** bekommen. Dafür wurde die Erweiterung **Contao Bootstrap Grid** verwendet. Sie legen dafür einfach ein Element vom Elementtyp **Grid Start** an und wählen das Grid **Umschlag mit Klasse row** aus \(siehe Bild 4\). Anschließend sollte es wie auf Bild 5 aussehen. Das Grid Stop Element wird automatisch angelegt.

Unter **Themes** und **Manage grid definitions** \(das vorletzte Icon\) wurde einfach ein leeres Grid-Element angelegt, das dafür sorgt, dass ein Div-Element mit der Klasse row angelegt wird.

###### Bild 4: Grid-Umschlag anlegen![](/mate-theme/images/grid_umschlag_row.png)

###### Bild 5: Elemente in einem Grid-Umschlag![](/mate-theme/images/bootstrap-grid.png)

## Icons

Um Icons zu verwenden, geben Sie dem Element einfach die **material-icons** Klasse und den **Icon Namen** als Inhalt. Alle Icons und die dazugehörigen Namen finden Sie entweder auf der [Material Design Webseite](https://material.io/icons/) oder im Theme unter Elemente und Icons.

**Zum Beispiel:**

```
<i class="material-icons">insert_schedule</i>
```

Größe und Farben können Sie durch das Hinzufügen von weiteren Klassen beeinflussen.

![](/mate-theme/images/materialize/icons-farben-groesse.png)

