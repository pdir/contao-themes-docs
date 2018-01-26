#### Dokumentation - Mate Theme für Contao

---

# Einrichtung

### CSS-Anpassungen

Wenn das Theme erfolgreich installiert wurde, befinden sich die SCSS-Dateien in der Dateiverwaltung unter dem Pfad **mate/sass**. Für individuelle Anpassungen benennen Sie die **custom.scss.example** in **custom.scss** sowie die** \_custom\_variables.scss.example** in **\_custom\_variables.scss** um.

In der \_custom\_variables.scss können Sie Farben und Schriften über Variabeln festlegen und diese in der custom.scss verwenden. Alle anderen scss- und css-Dateien sollten nicht bearbeitet werden.

### JavaScript-Anpassungen

JavaScript-Anpassungen können in der **theme.js** unter dem Pfad **mate/js** vorgenommen werden.

### Elemente über ein eigenes Insert-Tag platzieren

Unter der Seite **MATE-Elements** befinden sich Artikel, die mittels einem Insert-Tag in anderen Artikeln eingebunden werden können. Beim jeweiligen **Artikel** wählt man dafür unter **Template-Einstellungen** den passenden **Theme Helper Tag** aus \(siehe Bild 2\). Zur Zeit kann man keine eigenen Tags definieren, sondern nur die bereits zur Verfügung stehenden nutzen.

Den Artikel kann man danach über folgenden Insert-Tag in einem **HTML-Inhaltselement** in einem beliebigen Artikel platzieren: `{{theme::content::MATE02/01}}` \(siehe Bild 3\). Die entsprechenden Nummern sind im Titel des Artikels ersichtlich.

###### Bild 1: Artikel unter MATE Elements![](/mate-theme/images/theme-helper.png)

###### Bild 2: Theme Helper Tag im Artikel auswählen![](/mate-theme/images/theme-helper-tag.png)

###### Bild 3: Artikel über den Theme Helper Tag einbinden![](/mate-theme/images/theme-helper-tag-einbinden.png)



