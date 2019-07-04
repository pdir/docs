# Bezeichnungen & Übersetzungen

Die Bezeichnungen und Übersetzungen des Maklermoduls finden Sie in folgendem Ordner:

```
/vendor/pdir/maklermodul-bundle/src/Resources/contao/languages/de
```

Die Bezeichnungen aller Felder finden Sie im genannten Ordner in der Datei `makler_modul_mplus.php`.

Für eine updatesichere Anpassung bzw. Überschreibung der Variablen legen Sie unter dem Ordner `system/config` die Datei `langconfig.php` an bzw. editieren diese, wenn sie schon angelegt ist.

**Beispiel:**

```php
<?php
$GLOBALS['TL_LANG']['makler_modul_mplus']['field_keys']['preise.nettokaltmiete'] = 'Kaltmiete';
```

**Hinweis:**

Die Labels der Felder aus der Listenansicht müssen Sie im Template \(makler\_list.html5\) anpassen.

