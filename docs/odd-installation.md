
# Installation

## Voraussetzungen

Installieren Sie zuerst Contao, führen Sie das Datenbank-Update aus und befolgen danach folgende Schritte.

---

## Schritte

## 1 Theme Odd Bundle installieren:

Nach Abschluss Ihrer Bestellung erhalten Sie die Datei **composer.json,** die Sie in das Root-Verzeichnis von Contao übertragen müssen.

**Alternativ** können Sie die composer.json auch direkt bearbeiten. Fügen Sie folgende Zeile am Ende von `require` ein:

`",pdir/theme-odd-bundle": "1.0"`

Danach fügen Sie nach `scripts` folgende Zeilen ein und ersetzen den Platzhalter mit den Zugangsdaten, die wir Ihnen bei der Bestell-Email mitgesendet haben.

`,"repositories": [
    {
        "type": "composer",
        "url": "https://BENUTZERNAME:PASSWORT@packages.contao.store"
    }
]`

---

## 2 Pakete und Datenbank aktualisieren ##

Rufen Sie als erstes den **Contao Manager** über die folgende URL auf: www.ihre-domain.de/contao-manager.phar.php. Starten Sie den Contao Manager und wählen Sie die Schaltfläche **Pakete aktualisieren** aus. Anschließend klicken Sie auf **Prüfen & Installieren** und warten den Installations-Prozess ab.

Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank. Im Install-Tool müssen sie noch einen Admin-Benutzeraccount erstellen.

## 3 Theme-Dateien synchronisieren und Tabelle 'tl\_files' leeren:

Loggen Sie sich mit Ihrem erstellten Benutzer-Account im Backend ein und wählen Sie in der linken Navigation unter **PDIR THEMES** den Menüpunkt **odd Theme Setup** aus. Anschließend klicken Sie auf den Button **Theme-Dateien synchronisieren**. Damit werden alle Dateien in der Dateiverwaltung unter dem Ordner odd angelegt und die SQL-Dateien zum Importieren der Datenbank in den templates-Ordner kopiert.

Danach müssen die die Datenbank-Tabelle 'tl\_files' leeren, indem Sie auf den Button **Tabelle 'tl\_files' leeren** klicken. Dieser Schritt muss vor dem Importieren der Datenbank erfolgen.

---

## 4 Datenbank importieren:

Rufen Sie nun das Install-Tool auf. Unter dem Reiter **Ein Template importieren ** können Sie eine .sql-Datei aus dem templates-Verzeichnis importieren. Wählen Sie die Datei für Ihre Contao-Version aus und aktivieren Sie den Haken **Tabellen nicht leeren**. Anschließend klicken Sie auf **Ein Template importieren**.

Wenn die Datenbank erfolgreich importiert wurde, sollten Sie eine Meldung, dass ein Template importiert wurde, wie im folgenden Screenshot, erhalten.

Alternativ können Sie die sql-Datei auch über phpMyAdmin importieren.

---

## 5 Symlinks neu erstellen:

Anschließend wechseln Sie wieder ins Contao-Backend, wählen den Menüpunkt **Systemwartung** aus und erstellen die Symlinks neu, indem Sie die Checkbox bei **Symlinks neu erstellen** auswählen und anschließend den Button **Daten bereinigen** betätigen.

---

## 6 Einstellungen

In den **Einstellungen** müssen Sie unter Frontend-Einstellungen **Auto\_item** und **Ordner-URLs verwenden** aktivieren.

Unter **Erweiterte CSS-Einstellungen** müssen SIe noch das Klassen-Set **bootstrap4.json** auswählen.

Damit ist die Installation des Themes fertig und Sie können mit der [Einrichtung](odd-theme/einrichtung.md) beginnen.