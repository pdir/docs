# Darstellung von Bildern

Hier finden Sie verschiedene Code-Schnipsel, die Sie im Template der Detailansicht einfügen können, um Bilder darzustellen.

**Alle Bilder ausgeben:**

```
<?php foreach ($this->estate->attachments()->startAt(0) as $attachment) : ?>
    <?php $attachment->size(600,350)->render() ?>
<?php endforeach; ?>
```

Mit diesem Code-Schnipsel werden alle Anhänge der Gruppe BILD ausgegeben. Bei `startAt()` können Sie eine beliebige Position angeben, an der gestartet werden soll. Mit `size()` können Sie die Bildbreite und -höhe angeben.

**Bestimmte Anzahl von Bildern ausgeben:**

```
<?php foreach ($this->estate->attachments()->range(0,3) as $attachment) : ?>
    <?php $attachment->size(600,350)->render() ?>
<?php endforeach; ?>
```

Mit `range()` können Sie eine Startposition \(beginnend bei 0\) und die Länge angeben. Die Angabe `range(0,3)` gibt beispielsweise 3 Bilder ab der Position 0 aus.

**Bilder einer oder mehrerer Gruppen ausgeben:**

```
<?php foreach ($this->estate->attachments()->startAt(0) as $attachment) : ?>
    <?php $attachment->group("BILD,GRUNDRISS")->size(600,350)->render() ?>
<?php endforeach; ?>
```

mit `group()` können Sie Anhänge einer bestimmten Gruppe angeben. Mehrere Anhänge können Sie kommagetrennt eingeben.

