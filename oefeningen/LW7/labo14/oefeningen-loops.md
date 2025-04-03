# Oefeningen loops labo 13

## Folderstructuur

Zorg ervoor dat je de volgende folderstructuur volgt:

```plaintext
webtechnologie/
├─ labo-x/
│  ├─ oefening-01/
│  │  ├─ index.html
│  │  ├─ assets/
│  │  │  ├─ image-1.jpg 
│  │  │  ├─ image-n.jpg 
│  │  ├─ css/
│  │  │  ├─ reset.css
│  │  │  ├─ style.css
│  │  ├─ js/
│  │  │  ├─ script.js
│  ├─ oefening-02/
│  ├─ oefening-n/
├─ labo-y/
├─ labo-z/      
```

### Belangrijke richtlijnen

- Gebruik altijd **JS modules** om globale variabelen te vermijden:
  ```html
  <script type="module" src="./path/to/script.js" defer></script>
  ```
- Schrijf JavaScript in **strict mode**:
  ```javascript
  "use strict";
  ```
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)

---
# Oefeningen loops - Labo 13

## Oefening 1: Maaltafel Generator

**Leerdoelen**

- Werken met een for-loop
- Wiskundige bewerkingen
- Variabelen declareren met let en const
- Werken met controlestructuren

**Functionele analyse**

Je programma genereert op basis van een hardcoded waarde een maaltafelreeks voor een bepaalde maaltafel met een vast aantal iteraties.

**Technische analyse**

- Declareer een const genaamd `maalTafel` en ken hier een getal aan toe.
- Declareer een const genaamd `iteraties` en ken hier een getal aan toe.
- Gebruik een stringvariabele om de maaltafelreeks bij te houden.
- Gebruik een for-loop om de maaltafelreeks op te bouwen en voeg elk resultaat toe aan de string, gescheiden door een ", ".
- Print de maaltafelreeks uit in de console.

---

## Oefening 2: Raster Generator

**Leerdoelen**

- Werken met een for-loop
- Werken met strings
- Variabelen declareren met let en const

**Functionele analyse**

Je programma genereert een raster van kruisjes op basis van hardcoded waarden.

**Technische analyse**

- Declareer een const `kolommen` en ken hier een getal aan toe.
- Declareer een const `rijen` en ken hier een getal aan toe.
- Gebruik een for-loop om de rijen te doorlopen.
- Gebruik een geneste for-loop om de kolommen te doorlopen.
- Print elke rij met kruisjes (`X`), gescheiden door een spatie.

---

## Oefening 3: Raad het Getal

**Leerdoelen**

- Werken met een do-while-loop
- Werken met getallen
- Werken met controlestructuren

**Functionele analyse**

Het programma laat de gebruiker een getal raden tussen 0 en 30. De invoer is hardcoded en wordt gecontroleerd in een loop.

**Technische analyse**

- Stel een variabele `teRadenGetal` in op een vaste waarde.
- Gebruik een array met hardcoded gokpogingen.
- Gebruik een do-while-loop om de ingevoerde waarde te controleren.
- Geef aan of het getal hoger of lager moet zijn.
- Stop zodra het juiste getal geraden is.

---

## Oefening 4: Som van Even Getallen

**Leerdoelen**

- Werken met een for-loop
- Werken met wiskundige bewerkingen
- Variabelen declareren met let en const

**Functionele analyse**

Je programma berekent de som van alle even getallen tot en met een bepaalde hardcoded grens.

**Technische analyse**

- Declareer een const `grens` en ken hier een getal aan toe.
- Declareer een variabele om de som bij te houden.
- Gebruik een for-loop om door de getallen te itereren.
- Controleer of het getal even is en tel het op bij de som.
- Print de uiteindelijke som uit.

---

## Oefening 5: Aftellen

**Leerdoelen**

- Werken met een while-loop
- Werken met aftellussen
- Variabelen declareren met let en const

**Functionele analyse**

Je programma telt af vanaf een hardcoded startwaarde tot nul en print bij elke stap een melding.

**Technische analyse**

- Declareer een const `startWaarde` en ken hier een getal aan toe.
- Gebruik een while-loop om af te tellen.
- Print bij elke iteratie het huidige getal.
- Stop zodra het getal nul bereikt.

---

## Oefening 6: Fibonacci-reeks

**Leerdoelen**

- Werken met loops
- Werken met arrays
- Variabelen declareren met let en const

**Functionele analyse**

Je programma genereert de eerste N getallen van de Fibonacci-reeks op basis van een hardcoded waarde.

**Technische analyse**

- Declareer een const `aantalGetallen` en ken hier een getal aan toe.
- Gebruik een array om de Fibonacci-getallen op te slaan.
- Gebruik een loop om de reeks op te bouwen.
- Print de reeks uit in de console.


# Extra oefeningen

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

{% hint style="info" %}
Je kunt input van de gebruiker vragen door gebruik te maken van de [prompt() functie](https://developer.mozilla.org/en-US/docs/Web/API/Window/prompt)
{% endhint %}

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

Schrijf een programma dat een woord vraagt aan de gebruiker (zet deze in een constante variabele) en vervolgens dit woord achterstevoren afprint op het scherm.

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

Schrijf een programma dat een vierkant tekent op het scherm. De hoogte en de breedte van het vierkant wordt aan de gebruiker gevraagd (via variabelen)

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
