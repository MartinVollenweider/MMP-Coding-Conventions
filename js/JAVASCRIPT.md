<h1 align="center">JavaScript</h1>

<div align="center">Der verbindliche Guide für JavaScript</div>

<br>
<div align="center">
<img src="https://www.fhgr.ch/typo3conf/ext/sfptemplate/RootPage/Default/Resources/Public/Partials/Logo/Images/Logo.svg" width="30%">
</div>
<br>
<div align="center">
  <h4>
    <a href="../README.md">
      Start
    </a>
    <span> | </span>
    <a href="../html/HTML.md">
      HTML
    </a>
    <span> | </span>
    <a href="../css/CSS.md">
      CSS
    </a>
    <span> | </span>
    <span>
      JavaScript
    </span>
    <span> | </span>
    <a href="../php/PHP.md">
      PHP
    </a>
    <span> | </span>
    <a href="../mysql/MYSQL.md">
      MySQL
    </a>
  </h4>
</div>

<br><br>

-----

## Grundlagen

[go to top](#JavaScript)

- [Naming](#Naming)
- [Kommentare](#kommentare)
- [Selektion](#selektion)
- [Fehlersuche](#fehlersuche)
- [Objekte/Arrays](#objektearrays)
- [Funktionen](#funktionen)
- [Events](#events)
- [Bedingungen](#bedingungen)
- [Schleifen](#schleifen)



### Naming

In modernen Applikationen müssen viele Informationen verwaltet werden. Dazu gehört, dass jede Information mindestens drei Operationen kennt: add, edit, delete (AED). Wird eine Funktion geschrieben, sollen gerade Methoden für alle drei Operationen geschrieben werden. Es bietet sich an, die AED-Ausdrücke als Prefix zu nehmen: addName(), editName(), ...

Selbes gilt für boolsche Ausdrücke. Informationen, die nur true oder false sind, beginnen mit 'is...'. Das hat den grossen Vorteil, dass man weiss was der Zustand true bedeutet. Bei der Variablen ``isMale`` ist klar, dass true 'männlich' bedeutet.

Auch in JavaScript: **Variablen und Funktionen haben sinnvolle Namen**.
Die Variablen und Funktionen in JavaScript werden in camelCase geschrieben.

```js
let userName = 'Paul'; // eine Variable gesetzt
let aktuelleMWST = 7.7; // aktuelle Mehrwertsteuer
```

In den Variabelnamen sollen möglichst **keine Schlüsselwörter aus der Programmiersprache** vorkommen: for, else, each, if, usw.

### Kommentare

[Kommentare - w3schools](https://www.w3schools.com/js/js_comments.asp)

**Kommentare erklären Code.** Das wichtigste dabei ist, dass sie nicht alt sind. Kommentare anpassen, wenn sich der Code verändert - ist im Nachhinein Goldwert!

```js
// gültiger Kommentar
/*
 * Kommentar über mehrere
 * Zeilen mit Sternen die das zeigen.
 */
```

### Selektion

[DOM-Elemente - w3schools](https://www.w3schools.com/js/js_htmldom_elements.asp)

Um Interaktion mit der Webseite zu erzielen, müssen wir zu gewissen HTML-Elementen JavaScript-Code 'hinzufügen'. Um Elemente im JavaScript auszuwählen (selektieren) nutzen wir die Funktion ``querySelector``. Damit kann via CSS-Selektor ein HTML-Element angewählt werden.

```js
let buttonZurueck = document.querySelector('#btnZurueck');  // id
let subtitleText = document.querySelector('.subtitle'); // Klasse
```

### Fehlersuche

[console.log() - w3schools](https://www.w3schools.com/jsref/met_console_log.asp)

In Javascript muss oft nach einem Fehler gesucht werden. Die eleganteste und zielführendste **Methode ist mit ``console.log(...)``** die Variable oder das Objektauszugeben.

```js
console.log(userName);
```

### Objekte/Arrays

[Objekte - w3schools](https://www.w3schools.com/js/js_objects.asp)
[Arrays - w3schools](https://www.w3schools.com/js/js_arrays.asp)

Variablen werden **immer mit ``let`` definiert**. Das garantiert, dass die Variable gültig ist. Objekte und assoziative Arrays werden immer über mehrere Zeilen definiert. Theoretisch unterscheidet JavaScript zwischen Variablen und Konstanten. Letztere werden aus didaktischen Gründen im Unterricht nicht behandelt.

```js
let userId = 7;
let fruitArray = ['Banane', 'Orange', 'Apfel'];
let carObject = {
    color: '#ffffff',
    size: '5',
    brand: 'Audi'
}
```
Mehrdimensionale Variablen, d.h. Arrays werden mit den eckigen Klammern [] definiert; Objekte mit den geschweiften Klammern {}

### Funktionen

[Funktionen - w3schools](https://www.w3schools.com/js/js_functions.asp)

Die Funktionen bieten einen guten Weg, **Code zu recyclen**. Für gute Lesbarkeit soll einen starken [Namen](#Grundlagen) gewählt und der Code korrekt eingerückt werden. Immer einen ``return``-Wert definieren.

```js
function rechnenMultiplizieren(paraZahl1, paraZahl2) {
    return 'Das Ergebnis von ' + paraZahl1 + 'x' + paraZahl2 + ' ist ' + paraZahl1*paraZahl2;
}
console.log(rechnenMultiplizieren(7,3));  // Das Ergebnis von 7x3 ist 21
```

Funktionen werden mit lowerCamelCase benennt. Jeder Parameter enthält ein ``para``-Prefix.

### Events oder Ereignisse

[Events - w3schools](https://www.w3schools.com/jsref/met_element_addeventlistener.asp)

In HTML kann man Elementen einen Event zuweisen. Dieser sogenannte 'EventListener' lauscht, bis das Ereignis passiert. Dies ist meistens mit User-Interaktionen verbunden. Diese werden wie folgt definiert:

```js
// Erste mögliche Form
let wettbewerbFormular = document.querySelector("#wettbewerbFormular");
wettbewerbFormular.addEventListener('submit', wettbewerbSubmit); // Dieser EventListener hört auf den 'submit' Event des Formulars. In diesem Falle ist das das Absenden des Formulars

function wettbewerbSubmit() {
  //...
}

// Zweite mögliche Form
let wettbewerbFormular = document.querySelector("#wettbewerbFormular");
wettbewerbFormular.addEventListener('submit', function() {
  //...
 })
```


### Bedingungen

[Bedingungen - w3schools](https://www.w3schools.com/js/js_if_else.asp)

If-Bedingungen werden immer über mehrere Zeilen geschrieben. Die geschweiften Klammern erhalten keine neue Zeile.

```js
if (userObject.isMale) {
    console.log('Der User ist männlich.');
} else {
    console.log('Die Userin ist weiblich.');
}
```

### Schleifen

[for-Schleife - w3schools](https://www.w3schools.com/js/js_loop_for.asp)

Selbes wie bei der Bedingung zählt für die Schleifen. In der For-Schleife gibt es nach den Semikolon jeweils ein Leerzeichen.

```js
for (let counter = 1; counter < 15; counter++) {
    console.log('Durchgang ' + counter);
}
```

----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conventions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>
