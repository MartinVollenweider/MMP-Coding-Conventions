<h1 align="center">CodingConventions</h1>

<div align="center">Der verbindliche Guide für einheitlichen Code an der FHGR</div>

<div align="center">
  <sub>Dies ist Version 2.1</sub>
</div>
<br>
<div align="center">
<img src="https://www.fhgr.ch/typo3conf/ext/sfptemplate/RootPage/Default/Resources/Public/Partials/Logo/Images/Logo.svg" width="30%">
</div>
<br><br>

<h2 align="center">Technologien</h2>
<div align="center">
  Wähle eine Technologie um die Konventionen anzuzeigen
  <h4>
    <a href="html/HTML.md">
      HTML
    </a>
    <span> | </span>
    <a href="css/CSS.md">
      CSS
    </a>
    <span> | </span>
    <a href="js/JAVASCRIPT.md">
      JavaScript
    </a>
    <span> | </span>
    <a href="php/PHP.md">
      PHP
    </a>
    <span> | </span>
    <a href="mysql/MYSQL.md">
      MySQL
    </a>
  </h4>
</div>

<br><br>

-----

## Grundlagen

[go to top](#CodingConventions)

Folgend werden die Grundlagen erklärt, die unabhängig von der Programmiersprache anzuwenden sind.

- [Grundlagen](#grundlagen)
  - [Sprache](#sprache)
  - [Zeichen](#zeichen)
  - [Wieso CodingConventions?](#wieso-codingconventions)
- [Dateien und Ordner](#dateien-und-ordner)
  - [Dateinamen](#dateinamen)
  - [Ordnerstruktur](#ordnerstruktur)
- [Naming](#naming)
  - [Worttrennung](#worttrennung)
  - [Story](#story)

### Sprache
Die Sprache beim Coden ist **Englisch**. An der FHGR verwenden wir für Variabelnamen, Funktionsnamen und Dateinamen aber die **deutsche Sprache**.

### Zeichen
Alle Klassen-, id-, Funktions-, Variabel-, Dateinamen beginnen mit **einem Buchstaben**. In speiziellen Fällen (z.B. wenn alte Dateien/Ordner) sind Underscores (_) erlaubt.

Folgende Zeichen sind **erlaubt**:

- Buchstaben (a-z, A-Z)
- Zahlen (0-9)
- Sonderzeichen (_; in speziellen Fällen: -)

Folgende Zeichen sind **verboten**:

- Europäische Sonderzeichen (ä, ö, ü, à, é, è, ç, usw.)
- Leerzeichen
- Programmier-Sonderzeichen (. , ,, ?, !, $, /, |, \, >, <, usw.)
- Grossbuchstaben bei Dateinamen

### Wieso CodingConventions?

Aus folgenden Gründen sind Code Conventions wichtig:
- Code Conventions erhöhen die Lesbarkeit der Software und ermöglichen es, neuen Code schneller und gründlicher zu verstehen
- 80% der Kosten/Zeit einer Software entfallen auf Instandhaltung und Wartung
- Kaum eine Software wird für die gesamte Dauer ihrer Existenz vom selben Autor gepflegt -  also muss man sich auf eine "Grammatik" einigen.
- Für den Fall, dass Sie Ihren Quellcode verkaufen möchten, sollten Sie sicherstellen, dass er genauso gut verpackt und sauber daherkommt, wie jedes andere von Ihnen erzeugte Produkt auch.

## Dateien und Ordner

[go to top](#CodingConventions)

Dateien und Ordner wollen sinnvoll und korrekt angeschrieben werden, sodass sich jeder im Dateibaum schnell zurecht findet.

### UNIX

Windows sowie Mac unterscheiden bei Dateinamen nicht zwischen Gross- und Kleinschreibung. Daher sind **Grossbuchstaben in Dateinamen verboten**, wenn sie zur Unterscheidung von Dateien dienen.

### Dateinamen

Ideale Dateinamen erfüllen folgende Konventionen:
- Kleinbuchstaben, keine Leerzeichen
- Keine Abkürzungen, **selbsterklärend** (siehe Naming)
- Mit Underscores (_), Punkten oder Bindestrichen getrennt

Gute Beispiele:
```
index.html              script-nav.js 
about_us.html           main.js
style.css               img-logo.png 
style_index.css         icon-help.gif 
style-no-flash.css      bg-gradient.svg
```

### Ordnerstruktur

Eine einheitliche und sinnvolle Ordnerstruktur hilft, **Dateien schneller zu finden**. Zudem wissen **fremde Entwickler**, wo sie z.B. eine Javascript-Datei suchen müssen.

```
-projekt_fhgr_beispiel
  ├ css
  ├ html
  ├ img
  ├ js
  ├ php
  └ index.html
```

Diese Ordnerstruktur ist natürlich nicht in Stein gemeisselt. z.B. Für die Kreativ-Projekte wird eine andere Ordnerstruktur empfohlen.

```
-bridgeos
 ├ app
 │ ├ pinklabs
 │ ├ post2paper1
 │ ├ post2paper2
 │ ├ brain2go
 │ ├ simplyprototyping
 │ ├ kompresion
 │ └ bewertung
 ├ css
 ├ img
 ├ js
 ├ php
 │ ├ system
 │ └ backend
 └index.php
```

Je nach Grösse werden die Ordner (css, js, img, php, html) innerhalb ausgebaut. Es ist aber empfehlenswert, die index.html/index.php ausserhalb **alleine** stehen zu lassen.

## Naming

[go to top](#CodingConventions)

Sinnvoles Naming erleichtert die Programmierung und vor allem **die Fehlerkorrektur** erheblich. Wer Code schreibt, soll ihn so schreiben, sodass auch andere diesen Lesen können. **Ein Programmierer ist der Schriftsteller seines Codes**. Der Code soll in jeder Zeile ohne Kommentar erklären, was er gerade macht.

### Grundsätzlich
Bei Namen von Variablen, Funktionen, Dateien usw. möglichst **ganze Wörter** brauchen. Ein paar Abkürzungen sind erlaubt:
```
btn = Button / str = String / img = Image / msg = Message / ...
```

### Worttrennung
Aussagekräftige Namen enthalten **mehr als ein Wort**. Für das Trennen der Wörter gibt es mehrere Konventionen, die verschiedene Anwendung haben:

- **camelCase**: erstes Wort klein geschrieben, die folgenden ohne Trennung gross
  - Variablen, Funktionen, Methoden, Eigenschaften
- **kebab-case**: alle Wörter klein geschrieben, mit einem Trennstrich getrennt
  - CSS-Klassen, CSS-ID, HTML
- **underscore_case**: alle Wörter klein geschrieben, mit einem Underscore getrennt
  - Dateinamen, Ordnernamen
- **lowercase**: alles klein und aneinander geschrieben
  - URLs, 
- **UPPERCASE**: alles gross und aneinander geschrieben
  - Konstanten

### Story

Der eigene Code soll einem anderen Programmierer eine Geschichte erzählen. Das bedeutet, alles soll so benannt werden, damit eindeutig klar ist, was passiert.

[Clean Code](https://github.com/ryanmcdermott/clean-code-javascript#variables)

```js
let userObject = new User(7);
userObject.editUserName(‘Markus‘);
let schoolName = userObject.getSchoolName();
```

Ohne den Code der obigen Funktionen und Methoden eigesehen zu haben, weiss man, was sie machen.

----

<div align="center">
  #### Besten Dank für deine Aufmerksamkeit!
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>