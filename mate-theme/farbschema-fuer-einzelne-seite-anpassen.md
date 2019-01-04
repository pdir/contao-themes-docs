#### Dokumentation - Mate Theme für Contao

---

# Farbschema für bestimmte Seiten anpassen

Wenn Sie das Farbschema nur für bestimmte Seiten anpassen möchten, z. B. einer Seite das dunkle Farbschema und bei dem Rest der Webseite das grüne Farbschema behalten wollen, ist dies derzeit noch nicht vom Theme vorgesehen, aber über Umwege möglich. Nachteil ist aber, dass es künftige CSS-Anpassungen für diese Seite nicht mehr greifen.

**Folgende Schritte sind nötig:**

### 1. neues Template fe\_page\_mate anlegen

Sie müssen das Template fe\_page\_mate anpassen. Klicken Sie auf **Neues Template**, wählen das Original-Template **fe\_page\_mate.html5** aus und erstellen dieses. Benennen Sie dieses Template um, z. B. in:  fe\_page\_mate\_custom.html5. 

Bearbeiten Sie dieses Template und passen folgende Zeilen wie folgt an \(Zeile 15-19\):

```php
<link rel="stylesheet" type="text/css" media="all" href="<?php
// add stylesheets
$combiner = new Combiner();
$combiner->add('files/mate/sass/mate_custom.scss');
echo $combiner->getCombinedFile(); ?>">
```

Dies bewirkt, dass die Datei mate\_custom.scss, statt der originalen mate.scss, eingebunden wird. Sie können die Datei auch anders nennen, dann müssten Sie den Dateinamen in der oben erwähnten Datei und bei den nachfolgenden Schritten anpassen.

### 2. neues Layout anlegen

Navigieren Sie jetzt zu Themes / Seitenlayouts und duplizieren ein bestehendes Layout. Bei diesem Layout müssen Sie ganz unten bei Experten-Einstellungen das eben angelegte Template auswählen.

Außerdem müssen Sie in der Seitenstruktur bei der Seite, wo ein anderes Farbschema dargestellt werden soll, unter Layout-Einstellungen das neuangelegte Layout zuweisen.

### 3. Anlegen der SCSS-Dateien

#### mate\_custom.scss anlegen:

Sie müssen nun die **mate\_custom.scss** in der **Detailverwaltung** im Ordner **files/mate/sass** anlegen. Fügen Sie in diese Datei den kompletten Inhalt aus folgendem Link: [https://raw.githubusercontent.com/contao-themes-net/mate-theme-bundle/master/src/Resources/public/sass/mate.scss](https://raw.githubusercontent.com/contao-themes-net/mate-theme-bundle/master/src/Resources/public/sass/mate.scss).

Ein paar Zeilen müssen aber noch angepasst werden. Ersetzen Sie die ersten Zeilen bis zur letzten @font-face Anweisung durch die folgenden Zeilen \(bis ca. Zeile 28\).

```css
@import 'materialize_custom';

@font-face {
  font-family: "Lato Light";
  src: url("/bundles/matetheme/fonts/Lato/Lato-Light.ttf");
}

@font-face {
  font-family: "Lato Regular";
  src: url("/bundles/matetheme/fonts/Lato/Lato-Regular.ttf");
}

@font-face {
  font-family: "Old Standard";
  src: url("/bundles/matetheme/fonts/Old_Standard_TT/OldStandard-Regular.ttf");
}

@font-face {
    font-family: 'Material Icons';
    font-style: normal;
    font-weight: 400;
    src: url(/bundles/matetheme/fonts/Material_Icons/MaterialIcons-Regular.eot); /* For IE6-8 */
    src: local('Material Icons'),
    local('MaterialIcons-Regular'),
    url(/bundles/matetheme/fonts/Material_Icons/MaterialIcons-Regular.woff2) format('woff2'),
    url(/bundles/matetheme/fonts/Material_Icons/MaterialIcons-Regular.woff) format('woff'),
    url(/bundles/matetheme/fonts/Material_Icons/MaterialIcons-Regular.ttf) format('truetype');
}
```

Ganz am Ende der Datei müssen Sie noch die @import Anweisung durch folgende Zeile ersetzen:

```
@import 'custom';
```

#### materialize\_custom.scss anlegen:

Legen Sie nun im gleichen Ordner die Datei **materialize\_custom.scss** mit folgendem Inhalt an:

```css
@charset "UTF-8";

// Mixins
// @import "components/prefixer";
@import "../../../web/bundles/matetheme/sass/components/mixins";
@import "../../../web/bundles/matetheme/sass/components/color";

// Variables;
@import "../../../web/bundles/matetheme/sass/_mate_colors";
@import "_custom_colors_2";
@import "../../../web/bundles/matetheme/sass/_mate_variables";
@import "_custom_variables_2";
@import "../../../web/bundles/matetheme/sass/components/variables";

// mate theme overrides

// end mate theme overrides

// Reset
@import "../../../web/bundles/matetheme/sass/components/normalize";

// components
@import "../../../web/bundles/matetheme/sass/components/global";
@import "../../../web/bundles/matetheme/sass/components/badges";
@import "../../../web/bundles/matetheme/sass/components/icons-material-design";
@import "../../../web/bundles/matetheme/sass/components/grid";
@import "../../../web/bundles/matetheme/sass/components/navbar";
@import "../../../web/bundles/matetheme/sass/components/roboto";
@import "../../../web/bundles/matetheme/sass/components/typography";
@import "../../../web/bundles/matetheme/sass/components/transitions";
@import "../../../web/bundles/matetheme/sass/components/cards";
@import "../../../web/bundles/matetheme/sass/components/toast";
@import "../../../web/bundles/matetheme/sass/components/tabs";
@import "../../../web/bundles/matetheme/sass/components/tooltip";
@import "../../../web/bundles/matetheme/sass/components/buttons";
@import "../../../web/bundles/matetheme/sass/components/dropdown";
@import "../../../web/bundles/matetheme/sass/components/waves";
@import "../../../web/bundles/matetheme/sass/components/modal";
@import "../../../web/bundles/matetheme/sass/components/collapsible";
@import "../../../web/bundles/matetheme/sass/components/chips";
@import "../../../web/bundles/matetheme/sass/components/materialbox";
@import "../../../web/bundles/matetheme/sass/components/forms/forms";
@import "../../../web/bundles/matetheme/sass/components/table_of_contents";
@import "../../../web/bundles/matetheme/sass/components/sideNav";
@import "../../../web/bundles/matetheme/sass/components/preloader";
@import "../../../web/bundles/matetheme/sass/components/slider";
@import "../../../web/bundles/matetheme/sass/components/carousel";
@import "../../../web/bundles/matetheme/sass/components/date_picker/default";
@import "../../../web/bundles/matetheme/sass/components/date_picker/default.date";
@import "../../../web/bundles/matetheme/sass/components/date_picker/default.time";
```

#### \_custom\_colors\_2.scss anlegen:

**Duplizieren** Sie die Datei **\_custom\_colors.scss** und benennen die Datei um, z. B. in: **\_custom\_colors\_2.scss**. Wenn Sie der Datei einen anderen Namen geben wollen, müssen Sie den Dateinamen in der materialize\_custom.scss in Zeile 10 anpassen.

In der angelegten Datei ersetzen Sie folgende drei Zeilen \(Zeile 18 - 20\):

```
//@import '../../../web/bundles/matetheme/sass/mate_color_schemes/mate_dark_colors';
//@import '../../../web/bundles/matetheme/sass/mate_color_schemes/mate_blue_colors';
//@import '../../../web/bundles/matetheme/sass/mate_color_schemes/mate_yellow_colors';
```

Durch das Auskommentieren \(Entfernen der zwei Schrägstriche\), können Sie das Farbschema ändern.

#### \_custom\_variables\_2.scss anlegen:

**Duplizieren** Sie die Datei **\_custom\_variables.scss** und benennen die Datei um, z. B. in: **\_custom\_variables\_2.scss**. Wenn Sie der Datei einen anderen Namen geben wollen, müssen Sie den Dateinamen in der materialize\_custom.scss in Zeile 12 anpassen.

