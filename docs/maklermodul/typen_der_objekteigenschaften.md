# Typen der Objekteigenschaften

Sie haben die Möglichkeit die Darstellung der Objekteigenschaften für die Filteranzeige in der Listenansicht zu definieren.

Sie können den Typ bzw. die Art wie jede Objekteigenschaft ausgegeben wird beeinflussen, indem Sie eine Datei mit dem Namen **data.filter.ini** in der Dateiverwaltung im Ordner **maklermodul** anlegen.

### Beispielinhalt der data.filter.ini

```
flaechen.wohnflaeche = 'cssMapRange10'
```
Die Ausgabe der Wohnfläche erfolgt dann in 10er-Schritte.

## Zur Verfügung stehen folgende Ausgaben

### Allgemeine Typen:
* 
*cssMapDefault*<br>
Ausgabe ohne Änderung
* 
*cssMapBoolean*<br>
Ausgabe als true oder false Button
* 
*cssMapNumber*<br>
Ausgabe von Preisen im Format *12.000,00*

### Bereiche
* 
*cssMapRange1*
* 
*cssMapRange3*
* 
*cssMapRange10*
* 
*cssMapRange50*
* 
*cssMapRange100*
* 
*cssMapRange200*
* 
*cssMapRange1000*
* 
*cssMapRange10000*
* 
*cssMapRange50000*
* 
*cssMapRange100000**

Verfügbar ab Version 1.2.0 Build16

* 
*cssMapFloor1*
* 
*cssMapFloor3*
* 
*cssMapFloor10*
* 
*cssMapFloor50*
* 
*cssMapFloor100*
* 
*cssMapFloor200*
* 
*cssMapFloor1000*
* 
*cssMapFloor10000*
* 
*cssMapFloor50000*
* 
*cssMapFloor100000*
