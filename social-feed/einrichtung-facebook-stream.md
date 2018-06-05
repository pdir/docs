# Einrichtung des Facebook-Streams

Nach der Installation des Moduls werden Sie im linken Menü unter **PDIR APPS** den neuen Menüpunkt **Social Feed Accounts** sehen.

![](/social-feed/img/neuer_menupunkt_socialfeed.png)

Auf dieser Seite können Sie neue Accounts anlegen und deren Einstellungen bearbeiten.

![](/social-feed/img/accountliste_socialfeed.png)

## Account anlegen

Um einen Account anzulegen, wählen Sie die Schaltfläche **Neuen Social-Feed Account anlegen** aus. Anschließend öffnet sich eine Seite mit dem Formular, wo Sie alle notwendigen Daten zum Account hinterlegen müssen.

**Facebook-Account:** Geben Sie hier den Namen des Facebook-Accounts ein. Den Namen sehen Sie immer in der URL, wenn Sie Ihre Facebook-Seite aufrufen \(z. B. [facebook.com/account-name/](https://www.facebook.com/**meissen.online**/\)\).

**App ID:** Geben Sie hier die App ID Ihrer Facebook-App ein. Ihre App ID und den App Secret \(oder auch App Geheimcode\) können Sie in Ihrer Facebook-App unter Einstellungen &gt; Allgemeines einsehen. Bitte beachten Sie, dass Sie Ihre App erst zum App Review einreichen müssen, bevor Sie einen Social Feed Stream auf Ihrer Webseite anzeigen können. Ihre App-Einstellungen können Sie auf folgender Webseite einsehen: [https://developers.facebook.com/](https://developers.facebook.com/).

**App Secret: **Geben Sie hier den App Secret bzw. den App Geheimcode ein.

**News-Archiv:** Wählen Sie hier das News-Archiv aus, in welches die Facebook-Posts importiert werden sollen. Dies sollten Sie vorher anlegen. Eine Weiterleitungsseite müssen Sie beim News-Archiv angeben, da dies ein Pflichtfeld ist, wobei es für das Social Feed Bundle nicht relevant ist, da es keine News-Detailseite gibt. Idealerweise legen Sie für jeden Facebook-Account ein neues News-Archiv aus, da Sie so im Nachrichtenlisten-Modul später auch einzelne Accounts wieder abwählen können.

**Ausführung des Cronjobs:** Wählen Sie hier aus, wie oft der Cronjob aufgerufen werden soll, um neue Facebook-Posts zu importieren. Sie haben folgende Einstellmöglichkeiten: kein Cronjob, minütlich, stündlich, täglich, wöchentlich und monatlich.

**Letzter Import:** Die zwei Textfelder für den letzten Import dienen nur zur Information, wann der letzte Import stattfand.

_\(Die eingebenen Daten im Screenshot sind lediglich Beispieldaten\)_![](/social-feed/img/account_anlegen_socialfeed.png)

## Modul anlegen

Wenn Sie Ihre Accounts angelegt haben, legen Sie nun das dazugehörige Modul an. Dazu navigieren Sie zu **Themes &gt; Die Frontend-Module des Theme ID x bearbeiten **\(Zahnrad-Icon\) und legen ein neues Modul an.

Als Modultyp wählen Sie unter Nachrichten die **Nachrichtenliste** aus. Wählen Sie die entsprechenden **Nachrichtenarchive** aus, die Sie in Ihrem Social Feed Stream darstellen möchten. Über das Feld **Gesamtzahl der Beiträge** können Sie noch die Anzahl der Beiträge begrenzen. Möchten Sie eine Pagination darstellen, füllen Sie das Feld **Elemente pro Seite** aus.

Beim Nachrichtentemplate müssen Sie das Template **news\_social\_feed** auswählen. Beim individuellen Template wählen Sie **mod\_newslist\_social\_feed** aus. Unter Bildeinstellungen bei **Bildgröße** können Sie die Größe der Bilder anpassen.

Unter dem Punkt Social Feed Einstellungen können Sie die **maximale Textlänge**, die **Anzahl der Spalten** einstellen sowie **Masonry** aktivieren/deaktivieren und **Bilder anzeigen/ausblenden**.

## Modul platzieren

Nachdem Sie das Modul angelegt haben, platzieren Sie das Modul an einer beliebigen Stelle im Artikel.

