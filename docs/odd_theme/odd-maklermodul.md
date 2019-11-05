# Maklermodul

Das ODD Theme liefert bereits Templates und Stylesheets für das [Maklermodul](https://www.maklermodul.de/) mit.

## Dokumentation

In der [Maklermodul-Dokumentation](https://docs.pdir.de/#/maklermodul/index) finden Sie alle Informationen zur Installation und Einrichtung des Maklermoduls.

## Stylesheets einbinden

Fügen Sie folgende Zeile in der custom.scss (/files/odd/scss) ein, damit die Listen- und Detailansicht entsprechend den Screenshots dargestellt wird.

```
@import 'maklermodul';
```

## Einrichtung

### Seiten anlegen

Legen Sie zuerst eine jeweils eine Seite für die Listen- und Detailansicht an.

### Listenansicht-Modul

Legen Sie ein Modul vom Typ **Immobilienliste** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_list_odd** auswählen
* Bildgröße **Maklermodul / Listenansicht** auswählen

<img src="_images/odd-theme/module/oddtheme_maklermodul_modul_listenansicht.png" style="max-width:500px;">

### Detailansicht-Modul

Legen Sie ein Modul vom Typ **Expose** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_details_extended_odd** auswählen

### Kopfbild-Modul

Legen Sie ein Modul vom Typ **MaklerModul Kopfbild** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/kopfbild_mit_uberschrift) an.
