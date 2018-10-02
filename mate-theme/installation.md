#### Dokumentation - Mate Theme für Contao

---

# Installation

## Voraussetzungen:

Das Theme kann nur in einer **leeren Contao-Installation** installiert werden und ist mit **Contao 4.4.x oder höher** kompatibel.

## Schritte:

#### **Mate Theme Bundle installieren:**

Rufen Sie als erstes den Contao Manager über die folgende URL auf: [www.ihre-domain.de/contao-manager.phar.php](/www.ihre-domain.de/contao-manager.phar.php). Wählen Sie die Schaltfläche **Pakete installieren** aus und geben im Suchfeld **mate theme** ein \(siehe Bild 1\). Installieren Sie das Bundle **contao-themes-net/mate-theme-bundle**, indem Sie auf den Button **Prüfen & Installieren** klicken und anschließend mit **Änderungen anwenden** die Installation starten. Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank. Im Install-Tool müssen sie noch einen Admin-Benutzeraccount erstellen.

###### Bild 1: Mate Theme Bundle installieren ![](/mate-theme/images/bundle-installieren.png)

#### **Theme-Dateien synchronisieren und Tabelle 'tl\_files' leeren:**

Loggen Sie sich mit Ihrem erstellten Benutzer-Account im Backend ein und wählen Sie in der linken Navigation unter **MATE THEME** den Menüpunkt **Mate Theme Setup** aus. Anschließend klicken Sie auf den Button **Theme-Dateien synchronisieren** \(siehe Bild 2\). Damit werden alle Dateien in der Dateiverwaltung unter dem Ordner mate angelegt.

Danach müssen die die Datenbank-Tabelle 'tl\_files' leeren, indem Sie auf den Button **Tabelle 'tl\_files' leeren** klicken. Dieser Schritt muss vor dem Importieren der Datenbank erfolgen.

###### Bild 2: Theme-Dateien synchronisieren![](/mate-theme/images/dateien-synchronisieren.png)

#### **Datenbank importieren:**

**Für Contao 4.5.x und 4.6.x:**

Verbinden Sie sich per FTP mit Ihrem Server und navigieren Sie zu dem Pfad **vendor/contao-themes-net/mate-theme-bundle/src/templates/mate**. Dort finden Sie jeweils eine SQL-Datei für Contao 4.5 und 4.6. Die benötigte Datei kopieren Sie nun in den templates-Ordner und rufen anschließend das Install-Tool auf.

Unter dem Reiter **Ein Template importieren **\(siehe folgender Screenshot\) können Sie eine .sql-Datei aus dem templates-Verzeichnis importieren. Wählen Sie die Datei aus und aktivieren Sie den Haken **Tabellen nicht leeren**. Anschließend klicken Sie auf Ein Template importieren.

Wenn die Datenbank erfolgreich importiert wurde, sollten Sie eine Meldung, dass ein Template importiert wurde, wie im folgenden Screenshot, erhalten.

###### Bild 3: Ein Template importieren

![](/mate-theme/images/template_importieren.png)

**Für Contao 4.4.x:**

Melden Sie sich im **PHPMyAdmin** an und importieren Sie die mitgelieferte SQL-Datei **mate\_theme\_contao\_demo\_4.4.x.sql**, die im Mate Theme Bundle mitgeliefert wird und unter folgendem Pfad zu finden ist: **vendor/contao-themes-net/mate-theme-bundle/src/templates/mate**.

#### **Symlinks neu erstellen:**

Anschließend wechseln Sie wieder ins Contao-Backend, wählen den Menüpunkt **Systemwartung** aus und erstellen die Symlinks neu, indem Sie die Checkbox bei **Symlinks neu erstellen** auswählen und anschließend den Button **Daten bereinigen** betätigen.

#### Einstellungen:

In den **Einstellungen** müssen Sie unter Frontend-Einstellungen **Auto\_item** deaktivieren und **Ordner-URLs verwenden** aktivieren \(siehe Bild 4\).

###### Bild 4: Frontend-Einstellungen![](/mate-theme/images/einstellungen.png)

Unter **Erweiterte CSS-Einstellungen** müssen SIe noch das Klassen-Set **materialize.json** auswählen \(siehe Bild 5\).

###### Bild 5: Erweiterte CSS-Einstellungen

![](/mate-theme/images/advanced_classes_einstellungen.png)

Damit ist die Installation des Themes fertig und Sie können mit der [Einrichtung](/mate-theme/einrichtung.md) beginnen.

