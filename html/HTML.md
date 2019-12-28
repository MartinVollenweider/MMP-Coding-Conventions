<h1 align="center">HTML</h1>

<div align="center">Der verbindliche Guide für Hypertext Markup Language</div>

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
    <span>
      HTML
    </span>
    <span> | </span>
    <a href="../css/CSS.md">
      CSS
    </a>
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

[go to top](#HTML)

- [HTML](#HTML-sprache)
  - [Attribute](#attribute)
  - [Bilder](#Bilder)
  - [Medien](#Medien)
- [Head](#head)
  - [Meta-Tags](#meta-tags)
  - [Stylesheets](#stylesheets)
  - [Skripte](#skripte)


HTML Dokumente erfordern einen systematischen und strukturierten Aufbau. Halte deinen Code stets aufgeräumt, sauber und schön formatiert - _auch nach dem kopieren_!

Beispiel mit jeweils 1 Tab (4 Leerschläge) Zeileneinschub. Die Punkte zeigen an, wieviele Leerschläge sich bei den Abständen verbringen

```html
<!DOCTYPE html>
<html>
....<head>
........<meta charset="utf=8">
        <title>Test</title>
    </head>
    <body>
        <p>Webseite</p>
        <!-- Kommentar -->
    </body>
</html>
```

## HTML-Sprache

[go to top](#HTML)

Genau genommen ist HTML keine Programmiersprache, sondern eine **"Struktur-Sprache"**. Also mit HTML kann man keine Logik programmieren, sondern nur angeben, wie eine Webseite strukturiert sein soll. Diese Struktur geben wir in Hierarchien wieder. Jedes Element hat ein Eltern-Element und eventuell ein Kinder-Element. Damit die Hierarchie eindeutig ist, **muss jeweils der Start und das Ende eines Tags angegeben** werden.

```html
<section>   </section>
```

Der End-Tag wird mit einem **vorangehenden Slash** definiert. Es gibt also pro Tag zwei ``<..>``-Texte im Dokument. Das ergibt folgende Regel:

```html
ALLE TAGS SIND IMMER GESCHLOSSEN
```

Zwischen zwei Tags ist der Tag-Inhalt. Ist dieser Inhalt einen oder mehrere weitere Tags. Der Übersichtlichkeithalber kommen diese auf **je eine neue, eins weiter eingerückte** Zeile:

```html
<section>                   <-- Neue Zeile, neuer Tag
    <article class="...">   <-- Neue Zeile, neuer Tag
        <h1>Titel</h1>      <-- Gleiche Zeile
        <p>Fliesstext, der seeehr lange sein darf!</p>
    </article>
</section>
```

### Attribute

Alle HTML-Starttags können Attribute aufnehmen. Diese sind immer nach einem Leerschlag in lowercase und mit doppelten Quotes.

```html
<article class="mainArticle"> ... </article>
```

### Bilder

Nebst dem ``src="..."`` und evtl. ``class="..."`` Attribut hat jedes Bild einen ``alt="..."``-Text. Das ist **die minimalste Form** der Accessibility im Web.

```html
<img src="img_html5.png" alt="Bild des HTML5 Logos">
```

#### Dateigrössen
1. Bilder retuschieren, dann auf die richtige Grösse bringen. Zuerst verkleinern, dann komprimieren. jpg-Bilder immer auf die effektiv benötigte Grösse skalieren (bei Retina-Auflösungen das Doppelte) und anschliessend mittels Photoshop [fürs Web optimieren](https://helpx.adobe.com/ch_de/photoshop-elements/using/optimizing-images.html).
2. Bilder werden in Photoshop über Datei>Exportieren>Exportieren als… (File>Export>Export as…) exportiert. Dateiformat und Kompressionsstufe hängen vom Bild und Einsatzzweck ab. Nur JPG, PNG oder GIF verwenden!

Alternativen:
- JPG optimieren mit [jpegmini](https://www.jpegmini.com/)
- PNG optimieren mit [kraken.io](https://kraken.io/)

### Medien

Weitere Medien-Dateien wiefolgt aufbereiten:
- Audio
  - Audiodateien nie als wav, sondern immer nur als mp3 oder ogg verwenden. Bei mp3 gilt als Faustregel für normale Aufnahmen eine Auflösung von 128 kbps als gut (Musik und Ambi/Atmo stereo, Voice ond off-Text mono). Bei Hochqualitätsprojekten gelten 192 kbps als gut.
- Video
  - Videodateien grundsätzlich nie in Webprojekte einbinden, sondern falls immer möglich mittels Youtube oder Vimeo ausspielen und anschliessend via Embedcode einbinden. Der Grund liegt, neben der teils enormen Dateigrössen, im intelligenten Qualitäts- und Verbindungsmanagement der Plattformen, die in Echtzeit die Verbindungsqualität zum Endgerät messen und automatisch die dafür optimierte Variante streamen.
- Webseiten
  - Embedcodes auf der Basis von <iframe> sind per se nicht responsiv. Mit dem nachstehenden CSS-Hack aber (zusätzliches Elternelement <div> der Klasse "videocontainer") kann jeder iFrame ohne weiteres responsiv gemacht werden.

```css
/* Responsive Video */ 
.videocontainer { 
  position: relative; 
  padding-bottom: 56.25%; /* ratio 16x9 */ 
  height: 0; 
  overflow: hidden; 
  width: 100%; 
  height: auto; 
}

.videocontainer iframe { 
  position: absolute; 
  top: 0; 
  left: 0; 
  width: 100%; 
  height: 100%; 
  border: 0; 
}
```


## Head

[go to top](#HTML)

Im Head werden Seiteneigenschaften und weitere Dateien eingebunden.

### Meta-Tags

[Meta tags - w3schools](https://www.w3schools.com/html/html_head.asp)

Die Metadaten werden genutzt, das HTML-File besser zu spezifizieren (Stichwort: SEO).Zwei wichtige - und in jedem Dokument vorhandene - Metatags sind:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Stylesheets

[Stylesheets - w3schools](https://www.w3schools.com/tags/att_link_rel.asp)

Eine wichtige Funktion des HTML-Heads ist das Einbinden der Stylesheets. Jeder Link-Tag hat ein rel=".. ." das die Beziehung (relationship) zwischen den Dokumenten beschreibt.

```html
<link rel="stylesheet" type="text/css" href="theme.css">
```

In grösseren Projekten gibt es viele Stylesheets. Da empfiehlt sich folgende Reihenfolge in einem externen File (siehe Kapitel CSS - FIles einbinden):
1. Bootstrap
2. Frameworks (CDN)
3. Schriften
4. Eigene Stylesheets

### Skripte

[Skripte - w3schools](https://www.w3schools.com/tags/tag_script.asp)

Um einer Webseite interaktivität zu verleihen, werden Skripte eingebunden. Diese werden als letzte Elemente vor dem </body>-Tag eingebunden, da zu diesem Zeitpunkt die ganze Webseite schon steht (DOM ist vollständig).

```html
<body>
    <!-- Viel HTML-Code -->
    <script src="bootstrap.min.js"></script>
    <script src="..."></script>
</body>
```

Auch bei den Skripten spielt die Reihenfolge eine Rolle. Empfehlenswert ist folgende:
1. Bootstrap
2. Frameworks
3. Eigene Skripte


----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>