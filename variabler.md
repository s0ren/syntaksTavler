# Variabler

![breakout af variablers struktur](variabler.svg)

En variabel er det samme som memory på en lommeregner. 

![Lommeregner med memory](images/sharp_mem.png) 

Man kan gemme en værdi i variblen og bruge den senere.
Hver gang man laver en ny varibel, bliver der oprettet et nyt "memory" i RAM'en på computeren.

[MDN reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)

[ECMA specification](http://www.ecma-international.org/ecma-262/5.1/#sec-12.2)

## Opret variabel

<div id="VARIABLEDECLARATION"></div>

``` js
var fornavn; 
```
Her bliver variablen oprettet, men der er stadig ikke nogen værdi i den. Hvis vi prøver at udlæse den, får vi en fejl. Indholdet i variablen `fornavn` er `undefined`. 
``` js 
console.log(fornavn);
```
**`undefined`**

Variablen kan gemme en værdi, til senere brug, hvis man *tilskriver* en værdi til den.
``` js
var fornavn;
fornavn = "Jens";
```
Man kan også give variablen en værdi samtidig med at man opretter den:
``` js
var efternavn = "Hansen";
```

## Brug variabler

<div id="VARIABELINITIALISERING"></div>

Når variablerne er oprettet, og har fået en værdi,
```
var alder = 17;
var navn = "Justin Bieber";
```
kan man bruge dem som stedfortrædere for den værdi de indeholder:
```
console.log(navn + " er "  + alder + " år gammel.");
```
**`Justin Bieber er 17 år gammel.`**

Når variablerne er tekst strenge fungerer `+`-tegnet som "sammen-limer" der sætter tekster sammen.
Variabler kan jo også indeholde tal,
``` js
var nettoPris = 17;
var momsSats = 0.25; 
```
og når variablerne har fået tal, kan de bruges i regnestykker som dem herunder. Her udregner vi først hvor meget moms der skal på en is, der koster 17 kr før moms, ved at gange `nettoPris` med `momsSats`. 
Derefter lægger vi denne `moms` sammen med `nettoPris`'en, og får `bruttoPris`'en, som er hvad vi skal betale for isen.
``` js
var moms = nettoPris * momsSats;
var bruttoPris = nettoPris + moms;
console.log("En is koster " + bruttoPris + " kr med moms og det hele.");
```
**`En is koster 21.25 kr med moms og det hele.`**


## Typer
De fleste programmeringssprog skelner mellem forskellige typer af værdier vi putter i variablerne. Det har betydning for hvor meget RAM der skal afsættes til variablen, og hvordan værdien skal behandles.
I JavaScript er der 

+ `String` (tekst)
    
    f.eks. `"Her er en tekst"`

+ `Number` (tal)
    
    f.eks `42` eller `3.14`. 
    
    Bemærk at kommatal skrives med `.` i stædet for `,` fordi amerikanerne bruger engesk skivemåde.

+ Logiske tilstande (Boolske variabler)
    
    `TRUE` eller `FALSE`.

+ *`Object`* 

    som bruges til mere komplekse ting[^objekter]. 
    
    [^objekter]: Se tavlen [Objekter](Objekter.md "Tavlen med Objekter").

I nogen sprog skal man også deklarere hvilken type værdier variablen skal indeholde, men det behøver vi ikke i JavaScript.