
# Maklermodul

Das MATE Theme liefert bereits Templates und Stylesheets für das [Maklermodul](https://www.maklermodul.de/) mit.

## Dokumentation

In der [Maklermodul-Dokumentation](https://docs.pdir.de/#/maklermodul/index) finden Sie alle Informationen zur Installation und Einrichtung des Maklermoduls.

## Stylesheets einbinden

Fügen Sie folgende Zeile in der **custom.scss** (/files/mate/sass) ein, damit die Listen- und Detailansicht entsprechend den Screenshots dargestellt wird.

```
@import 'maklermodul';
```

## Einrichtung

### Seiten anlegen

Legen Sie zuerst jeweils eine Seite für die Listen- und Detailansicht an.

### Listenansicht-Modul

Legen Sie ein Modul vom Typ **Immobilienliste** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_list_mate** auswählen
* Bildgröße **Maklermodul / Listenansicht** auswählen

<img src="../_images/mate-theme/module/matetheme_maklermodul_modul_listenansicht.png" style="max-width:300px;">

### Detailansicht-Modul

Legen Sie ein Modul vom Typ **Expose** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_details_extended_mate** auswählen

<img src="../_images/mate-theme/module/matetheme_maklermodul_modul_expose.png" style="max-width:300px;">

### Kopfbild-Modul

Legen Sie ein Modul vom Typ **MaklerModul Kopfbild** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/kopfbild_mit_uberschrift) an.

<img src="../_images/mate-theme/module/matetheme_maklermodul_modul_kopfbild.png" style="max-width:300px;">

### Platzieren der Module

Platzieren Sie die Module für die Listenansicht und das Exposé unter den jeweiligen Seiten in den Artikeln. Legen Sie für das Kopfbild noch einen weiteren Artikel an, der in der Kopfzeile platziert ist (über dem Artikel der Detailansicht).

<img src="../_images/mate-theme/module/matetheme_maklermodul_artikel.png" style="max-width:300px;">

## Beispiele

Wenn Sie alle Schritte wie beschrieben durchgeführt haben, sollte die Liste entsprechend den folgenden Screenshots dargestellt werden.

### Listenansicht mit Button-Filter

<img src="../_images/mate-theme/module/matetheme_maklermodul_liste_buttons.png">

### Listenansicht mit Auswahllisten-Filter

<img src="../_images/mate-theme/module/matetheme_maklermodul_liste_selects.png">

### Exposé

<img src="../_images/mate-theme/module/matetheme_maklermodul_details.png">
