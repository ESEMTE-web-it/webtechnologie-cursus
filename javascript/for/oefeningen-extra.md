# extra oefeningen

## oefening: maaltafel generator (alt)

Maak oefening 1 opnieuw maar deze keer maak je **geen** gebruik van for-loops. Je gebruikt hiervoor de while-loop.

## oefening: raster generator (alt)

Maak oefening 2 opnieuw maar deze keer maak je **geen** gebruik van for-loops. Je gebruikt hiervoor de while-loops.

## oefening: raad het getal (uitbreiding)

Breid oefening 3 uit door het vast te raden getal nu een willekeurig getal tussen 0 en 30 te maken. Zoek zelf op hoe je een willekeurig getal kan genereren in JS.

## oefening: ontploffen

Schrijf een App die gebruik van een `for`-lus om af te tellen van een bepaald getal en vervolgens “BOOM” te printen.

Vraag aan de gebruiker van welk getal je wil aftellen.

**voorbeeldinteractie**

```
Van welk getal wil je aftellen? 5
5
4
3
2
1
BOOM!
```

## oefening: ontploffen (while)

Schrijf de ontploffen oefening nu met een `while`-lus.

## oefening: pijl

Maak een programma dat een getal vraagt aan de gebruiker en vervolgens een pijl tekent op het scherm met de lengte van het meegegeven getal. Je mag hier geen `repeat` gebruiken.

```
Hoe lang moet de pijl zijn? 10
==========>
```

```
Hoe lang moet de pijl zijn? 3
===>
```

## oefening: even getallen

Maak een programma dat alle even getallen tussen 0 en een gegeven getal op het scherm toont. Gebruik een for lus

```
Geef een getal in: 10
0
2
4
6
8
10
```

## oefening: even getallen op een lijn

Pas het programma aan zodat de even getallen op 1 lijn getoond worden

```
Geef een getal in: 10
0,2,4,6,8,10
```

## oefening: verticale naam

Schrijf een programma dat je naam vraagt en het dan de letters onder elkaar afprint. Hiervoor kan je een for lus gebruiken. Gebruik .length van een string om het aantal letters van de naam op te vragen.

```
Wat is jouw naam? Andie
A
n
d
i
e
```

## oefening: verticale naam maal tien

Pas het voorgaande programma aan zodat elke letter 10 keer wordt herhaald.

```
Wat is jouw naam? Andie
AAAAAAAAAA
nnnnnnnnnn
dddddddddd
iiiiiiiiii
eeeeeeeeee
```

## oefening: naam blijven vragen

Maak een programma dat je naam vraagt en vervolgens "Dag \<Naam>" zegt.

Zorg ervoor dat het programma blijft vragen tot de gebruiker STOP invoert. Daarna zal het programma Bye Bye! zeggen

Voorbeeldinteractie

```
Wat is je naam? Andie
Dag Andie!
Wat is je naam? Joske
Dag Joske!
Wat is je naam? Brent
Dag Brent!
Wat is je naam? STOP
Bye bye!
```

## oefening: gemiddelde vragen

Maak een programma dat de gebruiker blijft getallen vragen tot de gebruiker het getal leeg laat. Als de gebruiker dit gedaan heeft dan toont het programma het gemiddelde van deze getallen.

```
Geef een getal in: 10
Geef een getal in: 20
Geef een getal in: 5
Geef een getal in: 
Het gemiddelde is 11.67
```

## oefening: faculteit

Maak een programma dat met behulp van een **for** loop de faculteit van een getal berekent.

Voorbeeld: `6! = 6 x 5 x 4 x 3 x 2 x 1` (lees: 6 faculteit)

Eis een geheel getal bij input.

Zet een limiet op het aantal herhalingen (bvb 100), zorg dat de gebruiker dat ook weet.

Voorzie ook een oplossing voor een 0.

**voorbeeldinteractie**

```
Geef een getal in: 3
1*2*3=6
```

```
Geef een getal in: 6
1*2*3*4*5*6=720
```

## oefening: uren en minuten

Schrijf een programma dat alle uren en minuten tussen een bepaald tijdstip (in uren weergeeft) op het scherm toont. Je moet gebruik maken van een if structuur om uren/minuten kleiner dan 10 weer te geven met een 0 vooraan (bv. 9 wordt 09).

```
Wat is het begin uur?5
Wat is het eind uur?13
05:00
05:01
05:02
05:03
05:04
enzovoort...
12:52
12:53
12:54
12:55
12:56
12:57
12:58
12:59
```

## oefening: faculteit blijven vragen

Zorg ervoor dat het programma blijft getallen vragen totdat de gebruiker STOP ingeeft. Het programma zegt dan Doei en stopt.

**voorbeeldinteractie:**

```
Geef een getal in: 3
1*2*3=6
Geef een getal in: 6
1*2*3*4*5*6=720
Geef een getal in: 2
1*2=2
Geef een getal in: STOP
Doei!
```

## oefening: op en neer

Maak een programma dat het volgende patroon kan genereren:

**voorbeeldinteractie:**

```
Geef een getal in? 5
*
**
***
****
*****
*****
****
***
**
*
```

Je kan hier een geneste lus voor gebruiken

Nog **voorbeeldinteracties**:

```
Geef een getal in? 3
*
**
***
***
**
*
```

```
Geef een getal in? 10
*
**
***
****
*****
******
*******
********
*********
**********
**********
*********
********
*******
******
*****
****
***
**
*
```

## oefening: letters omdraaien

Schrijf een programma dat een woord vraagt aan de gebruiker en vervolgens dit woord achterstevoren afprint op het scherm.

```
Geef een woord in? auto
otua
```

Je kan dit doen met een lus die begint op de lengte van de string - 1 en gaat naar 0 (de lus gaat dus van boven naar beneden). Bij het voorbeeld van auto moet de lus dus van index **3** naar **0** gaan. Bij dinosaurus van 9 naar 0.

## oefening: palindroom

Breidt het vorige programma uit zodat in plaats van het woord af te printen het tegen de gebruiker zegt of het een palindroom is of niet

```
Geef een woord in? auto
auto is geen palindroom
```

```
Geef een woord in? otto
otto is een palindroom
```

## oefening: palindroom tot stop

Zorg ervoor dat het programma pas stopt op de moment dat de gebruiker een palindroom heeft ingegeven.

```
Geef een woord in? auto
Geef een woord in? dinosaurus
Geef een woord in? otto
otto is een palindroom
```

## oefening: vierkant tekenen

Schrijf een programma dat een vierkant tekent op het scherm. De hoogte en de breedte van het vierkant wordt aan de gebruiker gevraagd

```
Hoogte: 10
Breedte: 30
******************************
*                            *
*                            *
*                            *
*                            *
*                            *
*                            *
*                            *
*                            *
******************************
```

Gebruik hiervoor for lussen en geen repeat.
