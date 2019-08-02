# Zusätzliche Felder

Natürlich steht für die Nutzung von Benutzerdefinierten Felder auch eine Möglichkeit zur Verfügung.<br>

Legen Sie dafür einfach im Ordner `files/maklermodul` eine Datei mit dem Namen `data.mapping.php` an.

Nachfolgend sehen Sie einen beispielhaften Ausschnitt aus der XML sowie Beispiele, die in die data.mapping.php eingefügt werden können, um das Mapping zu verdeutlichen.

**Em Ende der Datei muss immer ein `return $userMapping;` erfolgen!**

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
$userMapping["objektkategorie/objektart/buero_praxen/@buero_typ"] = array('objektkategorie.objektart', 'Gewerbeimmobilien');

return $userMapping;
```

**Beispiel: Wert aus Büro-Typ übernehmen**

Wenn der Wert aus buero_typ (im Beispiel PRAXISFLAECHE) übergeben werden soll, fügen Sie in die data.mapping.php folgendes ein.

```
$userMapping["objektkategorie/objektart/buero_praxen/@buero_typ"] = 'objektkategorie.objektart.buero_praxen';

return $userMapping;
```

**Beispiel: Bestimmten Büro-Typ auf einen benutzerdefinierten Wert mappen**

Wenn statt PRAXISFLAECHE der deutsche Begriff Praxisfläche übergeben werden soll, fügen Sie folgendes in die data.mapping.php ein.

```
$userMapping["objektkategorie/objektart/buero_praxen[@buero_typ='PRAXISFLAECHE']"] = array('objektkategorie.objektart.buero_praxen','Praxisfläche');

return $userMapping;
```