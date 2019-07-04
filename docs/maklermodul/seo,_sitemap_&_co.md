# Seo, Sitemap & Co.

Das Maklermodul generiert Suchmaschinenfreundliche \(SEF\) URLs aus dem Title und der Objektnummer. Diese URLs werden außerdem bei jedem Import auch an den Suchindex für die Contao eigene Suche übergeben.

### Beispiel

```
www.ihrewebsite.de/expose/wow-klein-und-fein-gemuetlich-wohnen-mit-blick-in-ruhiger-lage-14266.html
```

## Google Sitemap

Verwenden Sie die Contao eigene XML-Sitemap Funktion unter Layout -&gt; Seitenstruktur -&gt; Startpunkt der Website -&gt; XML-Sitemap um ein Sitemap-Protokoll an die Suchmaschinen zu übergeben. Bitte beachten Sie das Sie den Ort der sitemap.xml Datei in der robots.txt angeben müssen.

### Beispiel

Sitemap: [http://www.maklermodul.de/share/sitemap.xml](http://www.maklermodul.de/share/sitemap.xml)  
Alternativ können Sie die Adresse der Sitemap auch direkt in den Google [Webmastertools](http://www.google.com/webmasters/tools) angeben.

```
User-agent: *
Disallow: /check/
Disallow: /contao/
Disallow: /system/
Disallow: /templates/
Disallow: /vendor/
Disallow: /share/index.php
Disallow: /build.xml
Disallow: /composer.json
Disallow: /composer.lock
Disallow: /README.md
```

Sitemap: [http://www.maklermodul.de/share/sitemap.xml](http://www.maklermodul.de/share/sitemap.xml)

## Contao Sitemap

Zusätzlich können Sie auch eine für den Seitenbesucher nutzbare Sitemap erstellen.

Ein Beispiel wie Sie das für Contao einrichten können, finden Sie hier: [Sitemap erstellen](http://de.contaowiki.org/Sitemap_erstellen). Das Maklermodul liefert auch das Template **nav\_makler\_sitemap** mit, das Sie angeben können, wenn Sie Ihre Immobilienobjekte in der Sitemap darstellen möchten.

