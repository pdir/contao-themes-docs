
# Update auf MATE Theme 2.0

In der Version 2.0 des MATE Theme wird die Version 1.0.0 des [Materialize Framework](https://materializecss.com), statt der Version 0.100.2 verwendet. Wenn Sie Template-, Javascript- oder CSS-Anpassungen vorgenommen haben, kann es sein, dass nach dem Update Änderungen von Ihrer Seite notwendig sind, da z. B. CSS-Klassen umbenannt wurden und Funktionen anders aufgerufen werden müssen. In dieser neuen Version wurden einige Bugs, die mit neueren Browserversionen auftraten, gefixt.

Eine komplette Liste mit allen Änderungen in der Version 1.0.0 des Materialize Framework finden Sie [hier](https://github.com/Dogfalo/materialize/blob/v1-dev/v1-upgrade-guide.md).

## Navigation

#### Template: mod_mate_navbar.html5 und mod_mate_navbar_left.html5

- Statt **data-activates** muss **data-target** verwendet werden
- Klasse **button-collapse** muss zu **sidenav-trigger** geändert werden
- Klasse **side-nav** muss zu **sidenav** geändert werden

**MATE 1.x**

```
<?php if($this->showMobileMenu == 1): ?>
    <a href="#" data-activates="mobile-menu<?= $this->id ?>" class="button-collapse"><i class="material-icons">menu</i></a>
<?php endif; ?>

<?php if($this->showMobileMenu == 1): ?>
    <ul id="mobile-menu<?= $this->id ?>" class="mobile-menu side-nav <?= $this->level ?>">
    <?= $this->mobileNav ?>
    </ul>
<?php endif; ?>
```

**MATE 2.0**

```
<?php if($this->showMobileMenu == 1): ?>
    <a href="#" data-target="mobile-menu<?= $this->id ?>" class="sidenav-trigger"><i class="material-icons">menu</i></a>
<?php endif; ?>

<?php if($this->showMobileMenu == 1): ?>
    <ul id="mobile-menu<?= $this->id ?>" class="mobile-menu sidenav <?= $this->level ?>">
    <?= $this->mobileNav ?>
    </ul>
<?php endif; ?>
```  

#### Template: nav_mate_root.html5

- Statt **data-activates** muss **data-target** verwendet werden

**MATE 1.x**

```
<?php if (!empty($item['subitems'])): ?> data-activates="nav<?= $this->id ?>dropdown<?= $item['id'] ?>"<?php endif; ?>
```

**MATE 2.0**

```
<?php if (!empty($item['subitems'])): ?> data-target="nav<?= $this->id ?>dropdown<?= $item['id'] ?>"<?php endif; ?>
```

## Sidenav

- Aufruf per JavaScript erfolgt nun über **sidenav()** statt **sideNav()**

**MATE 1.x**

`
$(".sidenav").sideNav();
`

**MATE 2.0**

`
$(".sidenav").sidenav();
`

## Select-Felder

- Aufruf per JavaScript erfolgt nun über **formSelect()** statt **materialSelect()**

**MATE 1.x**

`
$('select').material_select();
`

**MATE 2.0**

`
$('select').formSelect();
`

## Radio-Buttons

Wenn Sie das Template **form_radio.html5** angepasst haben, ist eine Anpassung notwendig, da sich die HTML-Struktur etwas verändert hat.

**MATE 1.x**

```
<?php if ($option['type'] == 'option'): ?>
    <span><input type="radio" name="<?= $option['name'] ?>" id="opt_<?= $option['id'] ?>" class="radio" value="<?= $option['value'] ?>"<?= $option['checked'] ?><?= $option['attributes'] ?>> <label id="lbl_<?= $option['id'] ?>" for="opt_<?= $option['id'] ?>"><?= $option['label'] ?></label></span>
<?php endif; ?>
```

**MATE 2.0**


```
<?php if ($option['type'] == 'option'): ?>
    <label id="lbl_<?= $option['id'] ?>" for="opt_<?= $option['id'] ?>">
        <input type="radio" name="<?= $option['name'] ?>" id="opt_<?= $option['id'] ?>" class="radio" value="<?= $option['value'] ?>"<?= $option['checked'] ?><?= $option['attributes'] ?>>
        <span><?= $option['label'] ?></span>
    </label>
<?php endif; ?>
```

## Checkboxen

Wenn Sie das Template **form_checkbox.html5** angepasst haben, ist eine Anpassung notwendig, da sich die HTML-Struktur etwas verändert hat.

**MATE 1.x**

```
<?php if ($option['type'] == 'option'): ?>
    <span><input type="checkbox" name="<?= $option['name'] ?>" id="opt_<?= $option['id'] ?>" class="checkbox" value="<?= $option['value'] ?>"<?= $option['checked'] ?><?= $option['attributes'] ?>> <label id="lbl_<?= $option['id'] ?>" for="opt_<?= $option['id'] ?>"><?= $option['label'] ?></label></span>
<?php endif; ?>
```

**MATE 2.0**


```
<?php if ($option['type'] == 'option'): ?>
    <label id="lbl_<?= $option['id'] ?>" for="opt_<?= $option['id'] ?>">
        <input type="checkbox" name="<?= $option['name'] ?>" id="opt_<?= $option['id'] ?>" class="checkbox" value="<?= $option['value'] ?>"<?= $option['checked'] ?><?= $option['attributes'] ?>>
        <span><?= $option['label'] ?></span>
    </label>
<?php endif; ?>
```

## Datepicker

- Aufruf erfolgt nun über **datepicker()** statt **pickadate()**
- Namen der Optionen haben sich teilweise geändert

**Mate 1.x**

```
$inputDatepicker = $('.datepicker').pickadate({
    selectMonths: true,
    selectYears: '150',
    max: new Date( new Date().getFullYear() + 30, new Date().getMonth(), new Date().getDate() ),
    closeOnSelect: true,
    format: 'dd.mm.yyyy',
    container: 'div.datepicker',
    labelMonthNext: 'Nexter Monat',
    labelMonthPrev: 'Vorheriger Monat',
    labelMonthSelect: 'Monat wählen',
    labelYearSelect: 'Jahr wählen',
    monthsFull: [ 'Januar', 'Februar', 'März', 'April', 'Mai', 'Juni', 'Juli', 'August', 'September', 'Oktober', 'November', 'Dezember' ],
    monthsShort: [ 'Jan', 'Feb', 'Mär', 'Apr', 'Mai', 'Jun', 'Jul', 'Aug', 'Sep', 'Okt', 'Nov', 'Dez' ],
    weekdaysFull: [ 'Sonntag', 'Montag', 'Dienstag', 'Mittwoch', 'Donnerstag', 'Freitag', 'Samstag' ],
    weekdaysShort: [ 'So', 'Mo', 'Di', 'Mi', 'Do', 'Fr', 'Sa' ],
    weekdaysLetter: [ 'S', 'M', 'D', 'M', 'D', 'F', 'S' ],
    today: 'Heute',
    clear: 'Löschen',
    close: 'OK',
    firstDay: 1
});
$inputDatepicker.pickadate('picker');
```

**Mate 2.0**

```
$('input.datepicker').datepicker({
    selectMonths: true,
    selectYears: '150',
    maxDate: new Date( new Date().getFullYear() + 30, new Date().getMonth(), new Date().getDate() ),
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
```

## Timepicker

- Aufruf erfolgt nun über **timepicker()** statt **pickatime()**
- Namen der Optionen haben sich teilweise geändert

**Mate 1.x**

```
$inputTimepicker = $('.timepicker').pickatime({
    default: 'now',
    fromnow: 0, 
    twelvehour: false,
    donetext: 'OK',
    cleartext: 'Reset',
    canceltext: 'Abbrechen',
    autoclose: false,
    ampmclickable: true,
    aftershow: function(){},
    container: 'div.timepicker'
});
$inputTimepicker.pickatime('picker');
```

**Mate 2.0**

```
$('input.timepicker').timepicker({
    defaultTime: 'now',
    fromNow: 0,
    twelveHour: false,
    autoClose: false,
    container: 'div.timepicker',
    i80n: {
        done: 'OK',
        clear: 'Löschen',
        cancel: 'Abbrechen'
    }
});
```

