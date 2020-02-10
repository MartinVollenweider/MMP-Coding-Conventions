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
- [Kollation](#Kollation)

### Naming

In modernen Applikationen müssen viele Informationen verwaltet werden. Dazu gehört, dass jede Information mindestens drei Operationen kennt: add, edit, delete (AED). Wird eine Funktion geschrieben, sollen gerade Methoden für alle drei Operationen geschrieben werden. Es bietet sich an, die AED-Ausdrücke als Prefix zu nehmen: addName(), editName(), ...

Selbes gilt für boolsche Ausdrücke. Informationen, die nur true oder false sind, beginnen mit 'is...'. Das hat den grossen Vorteil, dass man weiss was der Zustand true bedeutet. Bei der Variable ``isMale`` ist klar, dass true 'männlich' bedeutet.

Auch in JavaScript: **Variablen und Funktionen haben sinnvolle Namen**.
Die Variablen und Funktionen in JavaScript werden in camelCase geschrieben.

```js
let userName = 'Paul'; // eine Variable gesetzt
```

In den Variabelnamen sollen möglichst **keine Schlüsselwörter aus der Programmiersprache** vorkomen: for, else, each, if, usw.

### Kommentare

**Kommentare erklären Code.** Das wichtigste dabei ist, dass sie nicht alt sind. Kommentare anpassen, wenn sich der Code verändert - ist im Nachhinein goldwert!

```js
// gültiger Kommentar
/*
 * Kommentar über mehrere
 * Zeilen mit Sternen die das zeigen.
 */
```

### Fehlersuche

In Javascript muss oft nach einem Fehler gesucht werden. Die eleganteste und zielführendste **Methode ist mit ``console.log(...)``** die Variable oder das Objektauszugeben.

```js
console.log(userName);
```

### Objekte/Arrays

Variablen werden **immer mit ``let`` definiert**. Das garantiert, dass die Variable gültig ist. Objekte und assoziative Arrays werden immer über mehrere Zeilen definiert.

```js
let userId = 7;
let fruitArray = [‘Banane’, ‘Orange’, ‘Apfel’];
let carObject = {
    color: ‘#ffffff‘,
    size: ‘5’,
    brand: ‘Audi’
}
```

### Funktionen

[Funktionen - w3schools](https://www.w3schools.com/js/js_functions.asp)

Die Funktionen bieten einen guten Weg, **Code zu recyclen**. Für gute Lesbarkeit soll einen starken [Namen](#Grundlagen) gewählt und der Code korrekt eingerückt werden. Immer einen ``return``-Wert definieren.

```js
function addFruitToUser(paraFruit, paraUser) {
    return user.currentFruit = fruit;
}
```

Funktionen werden mit lowerCamelCase benennt. Jeder Parameter enhält ein ``para``-Prefix.

### Events

[Events - w3schools](https://www.w3schools.com/jsref/met_element_addeventlistener.asp)

In HTML kann man Elementen einen Event zuweisen. Dieser sogenannte 'EventListener' lauscht, bis das Ereigniss passiert. Dies ist meistens mit User-Interaktionen verbunden. Diese werden wiefolg definiert:

```js
let wettbewerbFormular = document.querySelector("#wettbewerbFormular");
wettbewerbFormular.addEventListener('submit', wettbewerbSubmit); // Dieser EventListener hört auf den 'submit' Event des Formulars. In diesem Falle ist das das Absenden des Formulars

function wettbewerbSubmit() {
  //...
}
```


### Bedingungen

If-Bedingungen werden immer über mehrere Zeilen geschrieben. Die geschweiften Klammern erhalten keine neue Zeile.

```js
if (userObject.isMale) {
    console.log('Der User ist männlich.');
} else {
    console.log('Die Userin ist weiblich.');
}
```

### Schleifen

Selbes wie bei der Bedingung zählt für die Schleifen. In der For-Schleife gibt es nach den Semikolon jeweils ein Leerzeichen.

```js
for (let counter = 1; counter < 15; counter++) {
    console.log('Durchgang ' + counter);
}
```

----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>
