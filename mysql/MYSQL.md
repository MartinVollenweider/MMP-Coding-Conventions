<h1 align="center">MySQL</h1>

<div align="center">Der verbindliche Guide für MySQL Datenbanken</div>

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
    <a href="../php/PHP.md">
      PHP
    </a>
    <span> | </span>
    <span>
      MySQL
    </span>
  </h4>
</div>

<br><br>

-----

## Grundlagen

[go to top](#MySQL)

- [Naming](#Naming)
- [Kollation](#Kollation)

Auch für MySQL gibt es Konventionen, damit eine Datenbank logisch und konsistent bleibt. Dabei trifft es hauptsächlich das Naming der Tabellen und Spalten.

## Naming

[go to top](#MySQL)

Tabellen und Spalten werden grundsätzlich in camelCase beschriftet. In einem Name in der Datenbank sind Leerzeichen verboten. Je nach System (Windows, Linux, usw.) wird nicht zwischen Gross- und Kleinschreibung unterschieden.

```sql
CREATE TABLE user (
    ID INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
    firstName VARCHAR(30) NOT NULL,
    lastName VARCHAR(30) NOT NULL,
    eMail VARCHAR(50)
)
```

Die Identifikations-Zahl kann in UPPERCASE geschrieben werden. Je nach grösse des Projekts macht anstatt ``ID`` auch ``userID`` sinn.
Wenn zwei Tabellen eine m:n-Verbindung haben, wird die **Zwischentabelle** mit den beiden **Namen der verbundenen Tabellen** geschrieben.

```
user --> userPost --> post
```

Die Tabellen werden **immer in der Einzahl bennent**! Im obigen Beispiel haben die User wahrscheinlich mehrere Posts, jedoch sorgt die Ein-/Mehrzahl von Tabellen-/Spaltennamen stets für Verwirrung.


## Kollation

[go to top](#MySQL)

Zeichensätze können für Fehler bei Umlauten sorgen. Die MySQL-Datenbank hat immer eine UTF-8 Kollation (Einstellbar unter ``Operationen``).



----

<div align="center">
  <h4>Besten Dank für deine Aufmerksamkeit!</h4>
  
  Wenn du Anmerkungen zu den obigen Coding-Conentions hast, so schreibe eine [Mail](mailto:samuel.rhyner@fhgr.ch).
</div>
