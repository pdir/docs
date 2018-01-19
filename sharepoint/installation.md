# Installation

Die Installation des Sharepoint Contao Moduls erfolgt nur auf Anfrage. Nach Kauf des Moduls bekommt der Kunde den Modul-Ordner und alle weiteren Schritte, die zur Installation des Moduls notwendig sind. Kontaktieren Sie uns am besten über unser [Kontaktformular](https://pdir.de/kontakt.html).

## Installationsanleitung

**1. Schritt**

Entpacken Sie den src-Ordner und laden Sie ihn in Ihr Contao Root-Verzeichnis hoch.

**2. Schritt**

Anschließend müssen Sie die composer.json in Ihrem Contao-Root-Verzeichnis um folgende Zeilen erweitern:

```
"require": {
	"pdir/contao-sharepoint-bundle": "dev-master"
},
"repositories": [{
    "type": "path",
    "url": "src/pdir/contao-sharepoint-bundle"
}],
"minimum-stability" : "dev",
"prefer-stable":true
```

**3. Schritt**

Rufen Sie den Contao Manager über die folgende URL auf: **ihre-domain.de/contao-manager.phar.php**. Aktualisieren Sie die Pakete und rufen anschließend das Installtool auf und aktualisieren die Datenbank.