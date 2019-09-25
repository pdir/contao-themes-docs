
# Sonstige Anpassungen

## Geschwindigkeit des Top-Links anpassen

Wenn Sie die Geschwindigkeit des Top-Links selbst bestimmen wollen, können Sie das über eine JavaScript-Anpassung ändern.

Navigieren Sie als Erstes in der linken Navigation über **Themes** zu den **Frontend-Modulen** und bearbeiten das Modul mit dem Titel **Footer**. Ändern Sie folgende Zeile wie folgt \(die Klasse custom wird hinzugefügt\):

```
<a href="{{env::request}}#top" class="toplink custom"><i class="material-icons">arrow_upward</i></a>
```

Nun können Sie in Ihrer JavaScript-Datei die Geschwindigkeit durch folgenden Code-Schnipsel anpassen. 500 steht hier für die Anzahl der Millisekunden.

```
$(document).on('click', 'footer .toplink.custom', function(event){
    event.preventDefault();
    $("html, body").animate({ scrollTop: 0 }, 500);
});
```



