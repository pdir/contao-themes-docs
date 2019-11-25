
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

## Geburtsdatum per Datepicker auswählen

Damit im Datepicker nur vergangene Datumsangaben auszuwählen sind, ist ein bisschen JavaScript notwendig, das z. B. im Layout bei "Eigener JavaScript-Code" eingefügt werden kann.

**yearRange** = Jahre, die man über die Select-Auswahl auswählen kann  
**minDate** = minimales Datum, was auswählbar ist  
**maxDate** = maximales Datum was auswählbar ist (in dem Beispiel das heutige Datum)  

```
<script>
jQuery(document).ready(function($) {
	$('input.datepicker').datepicker({
		yearRange: [1900,new Date().getFullYear()],
		minDate: new Date(1900,1,1),
		maxDate: new Date( new Date().getFullYear(), new Date().getMonth(), new Date().getDate() ),
		selectMonths: true,
		autoClose: true,
		format: 'dd.mm.yyyy',
		container: 'div.datepicker',
		firstDay: 1,
		i18n: {
			nextMonth: 'Nexter Monat',
			previousMonth: 'Vorheriger Monat',
			labelMonthSelect: 'Monat wählen',
			labelYearSelect: 'Jahr wählen',
			months: [ 'Januar', 'Februar', 'März', 'April', 'Mai', 'Juni', 'Juli', 'August', 'September', 'Oktober', 'November', 'Dezember' ],
			monthsShort: [ 'Jan', 'Feb', 'Mär', 'Apr', 'Mai', 'Jun', 'Jul', 'Aug', 'Sep', 'Okt', 'Nov', 'Dez' ],
			weekdays: [ 'Sonntag', 'Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag', 'Samstag' ],
			weekdaysShort: [ 'So', 'Mo', 'Di', 'Mi', 'Do', 'Fr', 'Sa' ],
			weekdaysAbbrev: ['S','M','D','M','D','F','S'],
			today: 'Heute',
			clear: 'Löschen',
			done: 'OK',
			cancel: 'Abbrechen'
		}
	});
});
</script>
```


