<h1 align="center">PHP</h1>

<div align="center">Der verbindliche Guide für PHP: Hypertext Preprocessor</div>

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
    <a href="../js/JAVASCRIPT.md">
      JavaScript
    </a>
    <span> | </span>
    <span>
      PHP
    </span>
    <span> | </span>
    <a href="../mysql/MYSQL.md">
      MySQL
    </a>
  </h4>
</div>

<br><br>

-----

## Grundlagen

[go to top](#PHP)

- [PHP-Sprache](#PHP-Sprache)
  - [Variablen](#Variablen)
  - [Klassen](#Klassen)
  - [Debugging](#Debugging)

Die meisten Code Conventions für If-Bedingung, Schleifen und Kommentare können von JavaScript übernommen werden. 

**Gross- und Kleinschreibung wird in PHP unterschieden!**

*Diese Conventions werden nach und nach übernommen*

## PHP-Sprache

[go to top](#PHP)

### Variablen

Variablen und Arrays werden nach einem klaren Schema definiert.

```php
// falsch
$a=$b+$c;
$array=[‘taa’,’daa’];

// richtig - genug Abstände!
$a = $b + $c;
$array = [ ‘taa’, ‘daa’ ];
```

### Klassen

Das Einrücken ist bei Klassen sehr wichtig, **um die Struktur zu erkennen**. Klassen werden immer mit einem Grossbuchstaben am Anfang geschrieben.

```php
class UserClass {
    public $userGroup = 'admin';
    private $userName = 'Tobias';

    function getUserName() {
        return $userName;
    }
}
```

### Debugging

Um Variablen, Objekte oder Arrays vollständig auszugeben, empfiehlt es sich, dies mit ``print_r(...)`` zu tun. Jeder Index eines Arrays wird aufgelistet.

```php
print_r($_POST); // gibt alle POST-Werte aus.
```


----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>
