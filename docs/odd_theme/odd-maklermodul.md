
# Maklermodul

Das ODD Theme liefert bereits Templates und Stylesheets für das [Maklermodul](https://www.maklermodul.de/) mit.

## Dokumentation

In der [Maklermodul-Dokumentation](https://docs.pdir.de/#/maklermodul/index) finden Sie alle Informationen zur Installation und Einrichtung des Maklermoduls.

## Stylesheets einbinden

Fügen Sie folgende Zeile in der **custom.scss** (/files/odd/scss) ein, damit die Listen- und Detailansicht entsprechend den Screenshots dargestellt wird.

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

<img src="/_images/odd-theme/module/oddtheme_maklermodul_modul_listenansicht.png" style="max-width:500px;">

### Detailansicht-Modul

Legen Sie ein Modul vom Typ **Expose** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_details_extended_odd** auswählen

<img src="/_images/odd-theme/module/oddtheme_maklermodul_modul_expose.png" style="max-width:500px;">

### Kopfbild-Modul

Legen Sie ein Modul vom Typ **MaklerModul Kopfbild** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/kopfbild_mit_uberschrift) an.

<img src="/_images/odd-theme/module/oddtheme_maklermodul_modul_kopfbild.png" style="max-width:500px;">

### Platzieren der Module

Platzieren Sie die Module für die Listenansicht und das Exposé unter den jeweiligen Seiten in den Artikeln. Legen Sie für das Kopfbild unter der Seite für die Detailansicht noch einen Artikel an, der in der Kopfzeile platziert ist.

<img src="/_images/odd-theme/module/oddtheme_maklermodul_artikel.png" style="max-width:500px;">

Bei den Artikeln für das Kopfbild und die Detailansicht müssen Sie in den Artikel-Einstellungen unter Template-Einstellungen das Template **mod_article_fullwidth** auswählen.

<img src="/_images/odd-theme/module/oddtheme_maklermodul_artikel_fullwidth.png" style="max-width:500px;">
