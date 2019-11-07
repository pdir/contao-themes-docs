
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

Legen Sie zuerst jeweils eine Seite für die Listen- und Detailansicht an.

### Listenansicht-Modul

Legen Sie ein Modul vom Typ **Immobilienliste** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_list_odd** auswählen
* Bildgröße **Maklermodul / Listenansicht** auswählen

<img src="../_images/odd-theme/module/oddtheme_maklermodul_modul_listenansicht.png">

### Detailansicht-Modul

Legen Sie ein Modul vom Typ **Expose** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/einrichtung) an.

* Immobilien-Template **makler_details_extended_odd** auswählen

<img src="../_images/odd-theme/module/oddtheme_maklermodul_modul_expose.png">

### Kopfbild-Modul

Legen Sie ein Modul vom Typ **MaklerModul Kopfbild** entsprechend der [Dokumentation](https://docs.pdir.de/#/maklermodul/kopfbild_mit_uberschrift) an.

<img src="../_images/odd-theme/module/oddtheme_maklermodul_modul_kopfbild.png">

### Platzieren der Module

Platzieren Sie die Module für die Listenansicht und das Exposé unter den jeweiligen Seiten in den Artikeln. Legen Sie für das Kopfbild noch einen weiteren Artikel an, der in der Kopfzeile platziert ist (über dem Artikel der Detailansicht).

<img src="../_images/odd-theme/module/oddtheme_maklermodul_artikel.png">

Bei den Artikeln für das Kopfbild und die Detailansicht müssen Sie in den Artikel-Einstellungen (Werkzeug-Icon) unter Template-Einstellungen das Template **mod_article_fullwidth** auswählen.

<img src="../_images/odd-theme/module/oddtheme_maklermodul_artikel_fullwidth.png">

## Anpassungen

### Filter in Listenansicht immer einblenden

Wenn die Filter in der Listenansicht immer eingeblendet werden sollen und nicht erst durch einen Klick auf den Button "Filter ausklappen", können Sie das durch eine kleine Template-Anpassung lösen. Legen Sie dafür das Template **makler_list_odd** an und entfernen Sie etwa bei Zeile 41 die folgenden zwei Zeilen:

```
<a href="<?= $this->staticListPage ?>" class="btn toggle-filter show-filter active">Filter ausklappen</a>
<a href="<?= $this->staticListPage ?>" class="btn toggle-filter hide-filter">Filter einklappen</a>
```

## Beispiele

Wenn Sie alle Schritte wie beschrieben durchgeführt haben, sollte die Liste entsprechend den folgenden Screenshots dargestellt werden.

### Listenansicht mit Button-Filter

<img src="../_images/odd-theme/module/oddtheme_maklermodul_liste_buttons.png">

### Listenansicht mit Auswahllisten-Filter

<img src="../_images/odd-theme/module/oddtheme_maklermodul_liste_selects.png">

### Exposé

<img src="../_images/odd-theme/module/oddtheme_maklermodul_details.png">
