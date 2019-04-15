
# Installation

## Voraussetzungen

Installieren Sie zuerst Contao, führen Sie das Datenbank-Update aus und befolgen danach folgende Schritte.

---

## Schritte

## 1 Theme Odd Bundle installieren:

Installieren Sie das Theme Odd Bundle, indem Sie die Datei **composer.json** im Contao Root-Verzeichnis bearbeiten. An das Ende von `require` fügen Sie die folgende Zeile ein, vergessen Sie dabei nicht nach der vorletzten Zeile ein Komma zu setzen (siehe Beispiel der composer.json).

`"pdir/theme-odd-bundle": "^1.0"`

Anschließend fügen Sie **an das Ende der Datei vor der letzten schließenden geschweiften Klammer** folgende Zeilen ein und ersetzen Benutzername und Passwort mit den Zugangsdaten, die wir Ihnen bei der Bestell-Email mitgesendet haben. In der Zeile davor muss nach der geschweiften Klammer auch wieder ein Komma gesetzt werden.

`,
"repositories": [
    {
        "type": "composer",
        "url": "https://BENUTZERNAME:PASSWORT@packages.contao.store"
    }
]`

**Beispiel, wie die composer.json für Contao 4.4 aussehen sollte:**

`
{
    "name": "contao/managed-edition",
    "type": "project",
    "description": "Contao Open Source CMS",
    "license": "LGPL-3.0-or-later",
    "authors": [
        {
            "name": "Leo Feyer",
            "homepage": "https://github.com/leofeyer"
        }
    ],
    "require": {
        "php": "^5.6 || ^7.0",
        "contao/calendar-bundle": "^4.4",
        "contao/comments-bundle": "^4.4",
        "contao/faq-bundle": "^4.4",
        "contao/listing-bundle": "^4.4",
        "contao/manager-bundle": "4.4.*",
        "contao/news-bundle": "^4.4",
        "contao/newsletter-bundle": "^4.4",
	    "pdir/theme-odd-bundle": "^1.0"
    },
    "conflict": {
        "contao-components/installer": "<1.3",
        "contao/core-bundle": "<4.4.8"
    },
    "extra": {
        "branch-alias": {
            "dev-4.4": "4.4.x-dev"
        },
        "contao-component-dir": "assets"
    },
    "scripts": {
        "post-install-cmd": [
            "Contao\\ManagerBundle\\Composer\\ScriptHandler::initializeApplication"
        ],
        "post-update-cmd": [
            "Contao\\ManagerBundle\\Composer\\ScriptHandler::initializeApplication"
        ]
    },
    "repositories": [
        {
            "type": "composer",
            "url": "https://BENUTZERNAME:PASSWORT@packages.contao.store"
        }
    ],
}
`

---

## 2 Pakete und Datenbank aktualisieren ##

Rufen Sie als erstes den **Contao Manager** über die folgende URL auf: www.ihre-domain.de/contao-manager.phar.php. Starten Sie den Contao Manager und wählen Sie die Schaltfläche **Pakete aktualisieren** aus. Anschließend klicken Sie auf **Prüfen & Installieren** und warten den Installations-Prozess ab.

Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank. Im Install-Tool müssen sie noch einen Admin-Benutzeraccount erstellen.

## 3 Theme-Dateien synchronisieren und Tabelle 'tl\_files' leeren:

Loggen Sie sich mit Ihrem erstellten Benutzer-Account im Backend ein und wählen Sie in der linken Navigation unter **PDIR THEMES** den Menüpunkt **ODD Theme Setup** aus. Anschließend klicken Sie auf den Button **Theme-Dateien synchronisieren**. Damit werden alle Dateien in der Dateiverwaltung unter dem Ordner odd angelegt und die SQL-Dateien zum Importieren der Datenbank in den templates-Ordner kopiert.

Danach müssen die die Datenbank-Tabelle 'tl\_files' leeren, indem Sie auf den Button **Tabelle 'tl\_files' leeren** klicken. Dieser Schritt muss vor dem Importieren der Datenbank erfolgen.

![](_images/odd-theme/installation/odd_installation_schritt3.png)

---

## 4 Datenbank importieren:

Rufen Sie nun das Install-Tool auf. Unter dem Reiter "Ein Template importieren" können Sie eine .sql-Datei aus dem templates-Verzeichnis importieren. Wählen Sie die Datei für Ihre Contao-Version aus und aktivieren Sie den Haken **Tabellen nicht leeren**. Anschließend klicken Sie auf **Ein Template importieren**.

![](_images/odd-theme/installation/odd_installation_schritt4_db_importieren.png)

Wenn die Datenbank erfolgreich importiert wurde, sollten Sie eine Meldung, dass ein Template importiert wurde, wie im folgenden Screenshot, erhalten.

![](_images/odd-theme/installation/odd_installation_schritt4_db_importieren_erfolgreich.png)

Alternativ können Sie die sql-Datei auch über phpMyAdmin importieren.

---

## 5 Symlinks neu erstellen:

Anschließend wechseln Sie wieder ins Contao-Backend, wählen den Menüpunkt **Systemwartung** aus und erstellen die Symlinks neu, indem Sie die Checkbox bei **Symlinks neu erstellen** auswählen und anschließend den Button **Daten bereinigen** betätigen.

![](_images/odd-theme/installation/odd_installation_schritt5.png)

---

## 6 Einstellungen

In den **Einstellungen** müssen Sie unter Frontend-Einstellungen **Auto\_item** und **Ordner-URLs verwenden** aktivieren. In Contao 4.7 gibt es die Einstellung Auto_Item aktivieren im Backend nicht mehr, es ist immer standardmäßig aktiv.

![](_images/odd-theme/installation/odd_installation_schritt6_ordner_urls.png)

Unter **Erweiterte CSS-Einstellungen** müssen SIe noch das Klassen-Set **bootstrap4.json** auswählen.

![](_images/odd-theme/installation/odd_installation_schritt6_advanced_classes.png)

Damit ist die Installation des Themes fertig und Sie können mit der [Einrichtung](odd-einrichtung.md) beginnen.