<h1 align="center">CSS</h1>

<div align="center">Der verbindliche Guide für Cascading Style Sheets</div>

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
    <span>
      CSS
    </span>
    <span> | </span>
    <a href="../js/JAVASCRIPT.md">
      JavaScript
    </a>
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

[go to top](#CSS)

- [CSS-Sprache](#CSS-sprache)
  - [Naming/Spacing](#Naming-Spacing)
  - [Media Querys](#Media-Querys)
  - [Pseudo-Klassen](#Pseudo-Klassen)
  - [Variablen](#Variablen)
  - [Files einbinden](#Files-einbinden)
- [BEM](#BEM)
  - [Block](#Block)
  - [Element](#Element)
  - [Modifier](#Modifier)


Jeder hat andere Ansätze, in CSS die Namen (Selektoren) zu benennen. Mit einfachen Regeln und dem BEM (CSS Naming Convention) wird alles einfacher! Die FHGR setzt auf ``BEM`` als Naming-Konvention.

Die folgende CSS-Naming Konvention ist nicht eine FHGR-Konvention, sondern wird auch in grossen Projekten angewendet. 
Wieso BEM? Meinungen aus der Industrie:
- [FreeCodeCamp](https://medium.freecodecamp.org/css-naming-conventions-that-will-save-you-hours-of-debugging-35cea737d849)
- [CSS-Tricks](https://css-tricks.com/bem-101/)

## CSS-Sprache

[go to top](#CSS)

Zuerst ein paar Grundlagen zu CSS.

### Naming/Spacing

Die Selektoren im CSS werden mit ``kebab-case`` getrennt. Eine ID verdient ein Element nur, wenn es ***wirklich* einzigartig im gesamten Dokument** ist!
Bei einem Selektor hat jede Eigenschaft eine neue Zeile.

```css
.stick-man { 
  height: 80vh; 
}
.iron-man {
  background-color: red;
  margin: 0 auto;
}
```

### Media Querys

Mit Mediaquerys wird das CSS dynamisch auf einen Umstand (meistens Bildschirmgrösse) angepasst. Diese ‘Spezialfälle’ werden nach dem regulären Selektor geschrieben (damit die Eigenschaften überschrieben werden).

```css
.stick-man { 
  height: 50vh; 
}
@media screen and (max-width: 991px) {
  .stick-man { 
    height: 100vh; 
  }
} /* Auf Smartphones ist der stick-man in voller Grösse */
```

### Pseudo-Klassen

Pseudo-Klassen werden direkt nach der Urspungsklasse definiert. Eine Dokumentation zu Pseudo-Klassen ist auf [w3schools](https://www.w3schools.com/css/css_pseudo_classes.asp) zu finden.

```css
.stick-man { 
  height: 50vh;
}
/* Ist die Maus über dem stick-man, ist er fullscreen */
.stick-man:hover { 
  height: 100vh;
}
/* Erstes Element von .user-name-list ausgewählt */
.user-name-list:first-child { /* ... */ }
```

### Variablen

In CSS kann man Variablen definieren. Der beste Anwendungsbereich liegt bei den Corporate Farben, die man so einmal definiert und anschliessend nur noch als Name verwendet.

```css
:root {
  --primary-color: red;
  --secundary-color: blue;
}
.submit-button {
  background-color: var(--primary-color);
}
```
### Files einbinden

Wenn man mit mehreren CSS-Files arbeitet, kann man alle in index.html einbinden. Das kann aber mit der Zeit sehr unübersichtlich werden. Daher wird empfohlen, ein CSS-File (z.B. “style.css“) in index.html einzubinden und dort alle nötigen Files in der richtigen Reihenfolge zu importieren.

```css
@import url(“game.css”);
```

**Achtung**: der Pfad muss von dem File ausgehen, bei dem dieser Import stattfindet.
**Tipp**: Das “Ursprungs-CSS-File” (oben “style.css” benennt) ist ein idealer Ort, um die Variablen zu definieren, die dann in allen Stylesheets verwendet werden können. Dies kann aber auch in einem separaten File geschehen.


## BEM

[go to top](#CSS)

### Block

Das CSS arbeitet eng mit dem HTML zusammen. Eine Section, der Header oder der Footer stellen einzelne Abschnitte auf deiner Webseite dar. Diese Bereiche haben mehrere untergeordnete Tags und bestimmt ganz verschiedene Inhalte. **Das sind Blöcke.**
Blöcke eignen sich sehr gut, in separate CSS Files unterzubringen. Als Beispiel nehmen wir ein Strichmännchen. Unser stick-man ist der Block.

```css
.stick-man { /* ... */ }
```


### Element

Dieser Block hat diverse Elemente. Die Elemente haben alle andere Anforderungen, daher sollen sie auch einen eigenen Selektor bekommen. Mit diesen Selektoren **werden elementspezifische Eigenschaften definiert**. Die Arme sollen andere Eigenschaften bekommen wie der Kopf usw.

```css
.stick-man__head { /* ... */ }
.stick-man__arms { /* ... */ }
.stick-man__legs { /* ... */ }
```

### Modifier

Die Elemente auf einer Webseite haben meistens immer die gleichen Eigenschaften. Doch es kann vorkommen, dass man **eine Farbe eines div-Elements** ändern will, z.B. wenn das Strichmännchen rot werden muss. Die Kennzeichnung des Modifiers wird mit zwei ``--`` angehängt. Somit kann es durchaus sein, dass **das Element 'Beine' drei Klassen besitzt**.

```css
.stick-man--red { /* ... */ }
.stick-man--blue { /* ... */ }
.stick-man__legs--green { /* ... */ }
```



----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>
