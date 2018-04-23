#### Dokumentation - Mate Theme für Contao

---

# Installation

## Voraussetzungen:

Das Theme kann nur in einer **leeren Contao-Installation** installiert werden und ist mit **Contao 4.4.x oder höher** kompatibel.

## Schritte:

#### **Mate Theme Bundle installieren:**

Rufen Sie als erstes den Contao Manager über die folgende URL auf: [www.ihre-domain.de/contao-manager.phar.php](/www.ihre-domain.de/contao-manager.phar.php). Wählen Sie die Schaltfläche **Pakete installieren** aus und geben im Suchfeld **mate theme** ein \(siehe Bild 1\). Installieren Sie das Bundle **contao-themes-net/mate-theme-bundle**, indem Sie auf den Button **Prüfen & Installieren** klicken und anschließend mit **Änderungen anwenden** die Installation starten. Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank. Im Install-Tool müssen sie noch einen Admin-Benutzeraccount erstellen.

###### Bild 1: Mate Theme Bundle installieren ![](/mate-theme/images/bundle-installieren.png)

#### **Theme-Dateien synchronisieren:**

Loggen Sie sich mit Ihrem erstellten Benutzer-Account im Backend ein und wählen Sie in der linken Navigation unter **MATE THEME** den Menüpunkt **Mate Theme Setup** aus. Anschließend klicken Sie auf den Button **Theme-Dateien synchronisieren** \(siehe Bild 2\). Damit werden alle Dateien in der Dateiverwaltung unter dem Ordner mate angelegt.

###### Bild 2: Theme-Dateien synchronisieren![](/mate-theme/images/dateien-synchronisieren.png)

#### **Datenbank importieren:**

Melden Sie sich im **PHPMyAdmin** an und leeren Sie zuerst nur die Tabelle **tl\_files**. Dies ist notwendig, da sonst der Import der SQL-Datei und die Verknüpfungen der Bilder nicht mehr funktionieren.

Anschließend importieren Sie die mitgelieferte SQL-Datei. Die SQL-Datei wird im Mate Theme Bundle mitgeliefert und ist unter folgendem Pfad zu finden: **vendor/contao-themes-net/mate-theme-bundle/src/templates/mate**. Es existiert eine SQL-Datei für Contao 4.4.x und für 4.5.x.

#### **Symlinks neu erstellen:**

Anschließend wechseln Sie wieder ins Contao-Backend, wählen den Menüpunkt **Systemwartung** aus und erstellen die Symlinks neu, indem Sie die Checkbox bei **Symlinks neu erstellen** auswählen und anschließend den Button **Daten bereinigen** betätigen.

#### Frontend-Einstellungen:

In den **Einstellungen** müssen Sie unter Frontend-Einstellungen **Auto\_item** deaktivieren und **Ordner-URLs verwenden** aktivieren \(siehe Bild 3\).

###### Bild 3: Frontend-Einstellungen![](/mate-theme/images/einstellungen.png)

Unter **Erweiterte CSS-Einstellungen** müssen SIe noch das Klassen-Set **materialize.json** auswählen \(siehe Bild 4\).

###### Bild 4: Erweiterte CSS-Einstellungen

![](/mate-theme/images/advanced_classes_einstellungen.png)

Damit ist die Installation des Themes fertig und Sie können mit der [Einrichtung](/mate-theme/einrichtung.md) beginnen.

