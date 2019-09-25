
# Installation

## Voraussetzungen

Das Theme kann nur in einer leeren Contao-Installation installiert werden und ist mit Contao 4.4.x oder höher kompatibel.

<div class="info-box">
Die folgenden Schritte sind <strong>nur bei der ersten Installation</strong> notwendig und nicht bei einem Update des Odd Themes. Wenn Sie das Theme aktualisieren wollen, können Sie das ganz einfach über den Contao Manager durchführen. Anschließend rufen Sie das Install-Tool auf und aktualisieren die Datenbank. <br><br>Ein <strong>Backup der Datenbank</strong> kann nie schaden!</div>

---

## Schritte

## 1 Theme Odd Bundle installieren:

Rufen Sie als erstes den Contao Manager über die folgende URL auf: [www.ihre-domain.de/contao-manager.phar.php](/www.ihre-domain.de/contao-manager.phar.php). Wählen Sie die Schaltfläche **Pakete installieren** aus und geben im Suchfeld **odd theme** ein. Installieren Sie das Bundle **contao-themes-net/odd-theme-bundle**, indem Sie auf den Button **Prüfen & Installieren** klicken und anschließend mit **Änderungen anwenden** die Installation starten.


---

## 2 Datenbank aktualisieren ##

Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank. Im Install-Tool müssen sie noch einen Admin-Benutzeraccount erstellen.

## 3 Theme-Dateien synchronisieren und Tabelle 'tl\_files' leeren:

Loggen Sie sich mit Ihrem erstellten Benutzer-Account im Backend ein und wählen Sie in der linken Navigation unter **PDIR THEMES** den Menüpunkt **ODD Theme Setup** aus. Anschließend klicken Sie auf den Button **Theme-Dateien synchronisieren**. Damit werden alle Dateien in der Dateiverwaltung unter dem Ordner odd angelegt und die SQL-Dateien zum Importieren der Datenbank in den templates-Ordner kopiert.

Danach müssen die die Datenbank-Tabelle 'tl\_files' leeren, indem Sie auf den Button **Tabelle 'tl\_files' leeren** klicken. Dieser Schritt muss vor dem Importieren der Datenbank erfolgen.

<div class="info-box">Mit dem Leeren der <strong>tl_files</strong> Tabelle werden die Bilder-Verknüpfungen gelöscht. Das ist nur bei der ersten Installation des Themes notwendig.</div>

![](../_images/odd-theme/installation/odd_installation_schritt3.png)

---

## 4 Datenbank importieren:

Rufen Sie nun das Install-Tool auf. Unter dem Reiter "Ein Template importieren" können Sie eine .sql-Datei aus dem templates-Verzeichnis importieren. Wählen Sie die Datei für Ihre Contao-Version aus und aktivieren Sie den Haken **Tabellen nicht leeren**. Anschließend klicken Sie auf **Ein Template importieren**.

![](../_images/odd-theme/installation/odd_installation_schritt4_db_importieren.png)

Wenn die Datenbank erfolgreich importiert wurde, sollten Sie eine Meldung, dass ein Template importiert wurde, wie im folgenden Screenshot, erhalten.

![](../_images/odd-theme/installation/odd_installation_schritt4_db_importieren_erfolgreich.png)

Alternativ können Sie die sql-Datei auch über phpMyAdmin importieren.

---

## 5 Symlinks neu erstellen:

Anschließend wechseln Sie wieder ins Contao-Backend, wählen den Menüpunkt **Systemwartung** aus und erstellen die Symlinks neu, indem Sie die Checkbox bei **Symlinks neu erstellen** auswählen und anschließend den Button **Daten bereinigen** betätigen.

![](../_images/odd-theme/installation/odd_installation_schritt5.png)

---

## 6 Einstellungen

In den **Einstellungen** müssen Sie unter Frontend-Einstellungen **Auto\_item** und **Ordner-URLs verwenden** aktivieren. In Contao 4.7 gibt es die Einstellung Auto_Item aktivieren im Backend nicht mehr, es ist immer standardmäßig aktiv.

![](../_images/odd-theme/installation/odd_installation_schritt6_ordner_urls.png)

Unter **Erweiterte CSS-Einstellungen** müssen SIe noch das Klassen-Set **bootstrap4.json** auswählen.

![](../_images/odd-theme/installation/odd_installation_schritt6_advanced_classes.png)