# Codeschnipsel für kleinere Templateanpassungen

### Listenansicht

**Darstellung von Nettokaltmiete/Kaufpreis in der Filteranzeige im deutschen Format**

Fügen Sie dafür folgenden Quellcode ans Ende des Templates `makler_list.html5` ein.

```
<script>
$(document).ready( function() {
    jQuery("#estate_filter_list .preise-nettokaltmiete .button, #estate_filter_list .preise-kaufpreis .button").each(function(i, obj) {
        jQuery(obj).html(filterGermanNumber(jQuery(obj).html()) + ' €');
    });

    //  Hilfsfunktionen
    function numberWithPoint(x) {
        return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
    }
    function filterGermanNumber(x) {
        var parts = x.toString().split(".");
        parts[0] = parts[0].replace(/\B(?=(\d{3})+(?!\d))/g, ".");
        return parts.join(",");
    }    
});
</script>
```

Anschließend sollten die Preise wie folgt dargestellt werden.

![](../_images/maklermodul/konfiguration/contao4_preis_deutsches_format.png)

![](../_images/maklermodul/konfiguration/contao4_preis_deutsches_format2.png)

