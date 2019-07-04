# Zusätzliche Felder

Natürlich steht für die Nutzung von Benutzerdefinierten Felder auch eine Möglichkeit zur Verfügung.<br>

Legen Sie dafür einfach im Ordner `files/maklermodul` eine Datei mit dem Namen `data.mapping.php` an.

Einfaches Mapping "**<etagenzahl>45</etagenzahl> => anzahl_etagen:45**"

```
$userMapping['verwaltung_techn/user_defined_anyfield/etagenzahl'] = 'anzahl_etagen';
```

Ein Beispiel für Benutzerdefinierte Felder von Immobilienscout:

```
<?php
$userMapping["verwaltung_techn/user_defined_anyfield/scout_zustand"] = 'zustand';
$userMapping["verwaltung_techn/user_defined_anyfield/scout_objektart"] = 'objektart'; 
$userMapping["verwaltung_techn/user_defined_anyfield/befeuerungsart"] = 'befeuerung';
$userMapping["verwaltung_techn/user_defined_anyfield/parkplatz_stellplatz"] = 'stellplatzart';
```