Um die Vollversion des Maklermoduls nutzen zu können, benötigen Sie zusätzlich zum **Maklermodul Bundle** noch das **Maklermodul Sync Bundle**.

## 1 Maklermodul Sync Bundle installieren:

Installieren Sie das Maklermodul Sync Bundle, indem Sie die Datei **composer.json** im Contao Root-Verzeichnis bearbeiten. An das Ende von `require` fügen Sie die folgende Zeile ein, vergessen Sie dabei nicht nach der vorletzten Zeile ein Komma zu setzen (siehe Beispiel der composer.json).

Für Contao 4.4 bitte VERSION mit 1.3 ersetzen.   
Für Contao 4.6 bitte VERSION mit 2.0 ersetzen.

```
"pdir/maklermodul-sync-bundle": "^VERSION"
```

Anschließend fügen Sie **an das Ende der Datei vor der letzten schließenden geschweiften Klammer** folgende Zeilen ein und ersetzen Benutzername und Passwort mit den Zugangsdaten, die wir Ihnen bei der Bestell-Email mitgesendet haben. In der Zeile davor muss nach der geschweiften Klammer auch wieder ein Komma gesetzt werden.

```
,
"repositories": [
    {
        "type": "composer",
        "url": "https://BENUTZERNAME:PASSWORT@packages.contao.store"
    }
]
```

**Beispiel, wie die composer.json für Contao 4.4 aussehen sollte:**

```
{
    "type": "project",
    "require": {
        "contao/calendar-bundle": "^4.4",
        "contao/comments-bundle": "^4.4",
        "contao/conflicts": "*@dev",
        "contao/faq-bundle": "^4.4",
        "contao/listing-bundle": "^4.4",
        "contao/manager-bundle": "4.4.*",
        "contao/news-bundle": "^4.4",
        "contao/newsletter-bundle": "^4.4",
        "pdir/maklermodul-bundle": "^1.4",
        "pdir/maklermodul-sync-bundle": "^1.3"
    },
    "extra": {
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
    ]
}
```

## 2 Pakete und Datenbank aktualisieren ##

Rufen Sie anschließend den **Contao Manager** über die folgende URL auf: www.ihre-domain.de/contao-manager.phar.php. Starten Sie den Contao Manager und wählen Sie die Schaltfläche **Pakete aktualisieren** aus. Anschließend klicken Sie auf **Prüfen & Installieren** und warten den Installations-Prozess ab.

Danach rufen Sie das **Install-Tool** auf und aktualisieren die Datenbank.
