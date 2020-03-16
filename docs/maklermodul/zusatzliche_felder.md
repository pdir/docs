# Zusätzliche Felder

Natürlich steht für die Nutzung von Benutzerdefinierten Felder auch eine Möglichkeit zur Verfügung.<br>

Legen Sie dafür einfach im Ordner `files/maklermodul` eine Datei mit dem Namen `data.mapping.php` an.

Nachfolgend sehen Sie einen beispielhaften Ausschnitt aus der XML sowie Beispiele, die in die data.mapping.php eingefügt werden können, um das Mapping zu verdeutlichen.

Em Ende der Datei muss immer ein `return $userMapping;` erfolgen! Die Änderungen werden erst nach erneutem Import der Immobilienobjekte übernommen!

**Ausschnitt aus der XML:**

```
<objektkategorie>
    <nutzungsart WOHNEN="false" GEWERBE="true"/>
    <vermarktungsart KAUF="false" MIETE_PACHT="true"/>
    <objektart>
        <buero_praxen buero_typ="PRAXISFLAECHE"/>
    </objektart>
</objektkategorie>
```

**Beispiel: Alle Büro/Praxen auf Gewerbeimmobilien mappen**

Fügen Sie folgendes in die data.mapping.php ein, um alle Büro/Praxen, egal welchen Büro-Typ sie haben, auf Gewerbeimmobilien zu mappen.

```
<?php

$userMapping["objektkategorie/objektart/buero_praxen/@buero_typ"] = array('objektkategorie.objektart', 'Gewerbeimmobilien');

return $userMapping;
```

**Beispiel: Wert aus Büro-Typ übernehmen**

Wenn der Wert aus buero_typ (im Beispiel PRAXISFLAECHE) übergeben werden soll, fügen Sie in die data.mapping.php folgendes ein.

```
<?php

$userMapping["objektkategorie/objektart/buero_praxen/@buero_typ"] = 'objektkategorie.objektart.buero_praxen';

return $userMapping;
```

**Beispiel: Bestimmten Büro-Typ auf einen benutzerdefinierten Wert mappen**

Wenn statt PRAXISFLAECHE der deutsche Begriff Praxisfläche übergeben werden soll, fügen Sie folgendes in die data.mapping.php ein.

```
<?php

$userMapping["objektkategorie/objektart/buero_praxen[@buero_typ='PRAXISFLAECHE']"] = array('objektkategorie.objektart.buero_praxen','Praxisfläche');

return $userMapping;
```

**Beispiel um Objektart mit allen Objekttypen zu mappen:**

```
<?php

$userMapping["objektkategorie/objektart/zimmer"] = array('objektkategorie.objektart', 'Zimmer');
$userMapping["objektkategorie/objektart/wohnung"] = array('objektkategorie.objektart', 'Wohnung');
$userMapping["objektkategorie/objektart/haus"] = array('objektkategorie.objektart', 'Haus');
$userMapping["objektkategorie/objektart/grundstueck"] = array('objektkategorie.objektart', 'Grundstück');
$userMapping["objektkategorie/objektart/buero_praxen"] = array('objektkategorie.objektart', 'Gewerbeimmobilien');
$userMapping["objektkategorie/objektart/einzelhandel"] = array('objektkategorie.objektart', 'Gewerbeimmobilien');
$userMapping["objektkategorie/objektart/gastgewerbe"] = array('objektkategorie.objektart', 'Gastgewerbe');
$userMapping["objektkategorie/objektart/hallen_lager_prod"] = array('objektkategorie.objektart', 'Gewerbeimmobilien');
$userMapping["objektkategorie/objektart/land_und_forstwirtschaft"] = array('objektkategorie.objektart', 'Land- & Forstwirtschaft');
$userMapping["objektkategorie/objektart/parken"] = array('objektkategorie.objektart', 'Parken');
$userMapping["objektkategorie/objektart/sonstige"] = array('objektkategorie.objektart', 'Sonstige');
$userMapping["objektkategorie/objektart/freizeitimmobilie_gewerblich"] = array('objektkategorie.objektart', 'Freizeitimmobilie, Gewerblich');
$userMapping["objektkategorie/objektart/zinshaus_renditeobjekt"] = array('objektkategorie.objektart', 'Zinshaus, Renditeobjekt');

return $userMapping;
```

Wenn Sie die vorhanden Objekte erneut importieren steht dann ein Filter **objektkategorie.objektart** zur Verfügung.

**Suchen & Ersetzen**

Ab der Version 2.5.0 des Maklermodul Sync Bundle ist es möglich Buchstaben und Zeichen zu ersetzen. Fügen Sie z. B. 
folgendes in die data.mapping.php ein, um in der Objektnummer Klammern, Schrägstriche und Leerzeichen zu entfernen.

```
<?php

$userMapping['verwaltung_techn/objektnr_extern'] = ['sortierung', ['search' => '(,), ,/', 'replace' => ',,,']];

return $userMapping;
```

Vorher: 21 (1/16)  
Nachher: 21116

Wenn Sie die vorhanden Objekte erneut importieren steht dann ein Filter **sortierung** zur Verfügung.
