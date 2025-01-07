# oefeningen

## oefening 1: som

**leerdoelen**

* werken met arrays
* lengte van arrays opvragen
* arrays doorlopen met een for-loop

**functionele analyse**

Je programma geeft de som van een rij getallen terug.

**technische analyse**

Je begint met een `array` te maken van de getallen 1, 2, 3, 4, 5 en 6. Je maakt een variabele `som` en kent er de waarde 0 aan toe.

Vervolgens maak je een lus die van 0 tot het aantal getallen in de array itereert. Elke iteratie tel je het huidige getal op bij een variabele som.

De som print je af op in de console.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef1.png" alt=""><figcaption></figcaption></figure>

## oefening 2: namen

**leerdoelen**

* werken met arrays
* lengte van arrays opvragen
* arrays doorlopen met een for-loop

**functionele analyse**

Je programma genereert op basis van 2 arrays een lijst van voor- en achternamen.

**technische analyse**

Maak 2 string-arrays aan. De eerste geef je 5 voornamen, de andere 5 achternamen.

Controleer dat de lengte van beide arrays gelijk is. Zo niet print je een foutboodschap.

Gebruik een for-loop om door de lijst van namen te loopen.

Toon vervolgens een lijst uit met voor- en achternamen op de scherm van de browser.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef2.png" alt=""><figcaption></figcaption></figure>

## oefening 3: vrienden

**leerdoelen**

* werken met gebruikersinteractie
* werken met for-loop
* toevoegen van elementen in een array

**functionele analyse**

Je programma vraagt hoeveel vrienden er moeten worden ingevoerd. Op basis daarvan kan je daarna je vrienden toevoegen aan een lijst. Nadien wordt de lijst uitgeprint (laatste ingave eerst).

**technische analyse**

Vraag de gebruiker hoeveel namen er moeten worden ingegeven. Maak hiervoor gebruik van input-veld.

Vraag dan X aantal keer de naam van de vriend dat je wenst toe te voegen. **Hint**: je kan voor deze oefening `prompt()` gebruiken om de gebruiker te vragen achter de namen.

Voeg de vrienden toe aan een array van vrienden.

Toon vervolgens de lijst met vrienden in een lijst.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef3.gif" alt=""><figcaption></figcaption></figure>

## oefening 4: punten

**leerdoelen**

* werken met for-of-loop
* werken met arrays
* wiskundige bewerkingen

**functionele analyse**

Je programma verwerkt een puntenlijst aan resultaten en print het gemiddelde, het percentage en het aantal gebuisde vakken uit.

**technische analyse**

Gebruik voor deze oefening volgende array:

```
const grades = [16,12,16,7,17,14,9,8,18,12];
```

Gebruik een for-of-loop om door de grades te loopen.

Bereken het gemiddelde, het percentage en het aantal gebuisde vakken.

Toon deze waardes op het scherm in een lijst.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef4.png" alt=""><figcaption></figcaption></figure>

## oefening 5: punten met vragen

**leerdoelen**

* gebruiken van do while loop
* werken met arrays
* input vragen

**functionele analyse**

Je breidt de punten oefening uit zodat de gebruiker zelf de punten kan ingeven.

**technische analyse**

Schrijf eerst een do while loop om de punten te vragen. Op de moment dat de gebruiker geen getal meer ingeeft dan worden dezelfde waarden getoond aan de gebruiker als in de vorige oefening.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef5.gif" alt=""><figcaption></figcaption></figure>

## oefening 6: pokémon team

**leerdoelen**

* gebruiken van loops
* werken met arrays
* zoeken in arrays

**functionele analyse**

Je programma maakt het mogelijk om de gebruiker een team van pokémon samen te stellen.

**technische analyse**

Gegeven is de volgende array van 20 pokemon:

```
let pokemon = [
    "Bulbasaur",
    "Ivysaur",
    "Venusaur",
    "Charmander",
    "Charmeleon",
    "Charizard",
    "Squirtle",
    "Wartortle",
    "Blastoise",
    "Caterpie",
    "Metapod",
    "Butterfree",
    "Weedle",
    "Kakuna",
    "Beedrill",
    "Pidgey",
    "Pidgeotto",
    "Pidgeot",
    "Rattata",
    "Raticate",
    "Spearow",
];
```

* Maak een array `team`. Deze array bevat de pokémon van de gebruiker van het programma.
* Gebruik een lus om de pokémon in een genummerde lijst te tonen aan de gebruiker.

```
1. Bulbasaur
2. Ivysaur
3. Venusaur
4. Charmander
5. Charmeleon
...
```

* Vraag daarna aan de gebruiker welke pokémon er moet toegevoegd worden aan het team. Dit doe je aan de hand van de index van de pokemon. Dit doe je tot de gebruiker STOP ingeeft. Je kan dit doen aan de hand van een `do while` loop.

```
Welke pokemon wil je in je team? [1-21]: 4
Welke pokemon wil je in je team? [1-21]: 3
Welke pokemon wil je in je team? [1-21]: STOP
```

* Als de gebruiker een pokémon ingeeft die al in het team zet dan krijgt hij hiervan een melding en wordt de pokémon niet toegevoegd:

```
Welke pokemon wil je in je team? [1-20]: 4
Welke pokemon wil je in je team? [1-20]: 3
Welke pokemon wil je in je team? [1-20]: 4
Deze pokemon zit al in je team
Welke pokemon wil je in je team? [1-20]: 2
Welke pokemon wil je in je team? [1-20]: STOP
```

* Als de pokémon niet bekend is (dus het ingegeven nummer groter is dan de lengte van de array) wordt er ook een melding gegeven:

```
Welke pokemon wil je in je team? [1-21]: 22
Deze pokemon ken ik niet
Welke pokemon wil je in je team? [1-21]: 4
```

* Als je STOP hebt ingegeven dan wordt het team van de gebruiker op het scherm getoond:

```
Welke pokemon wil je in je team? [0-20]: 1
Welke pokemon wil je in je team? [0-20]: 2
Welke pokemon wil je in je team? [0-20]: 3
Welke pokemon wil je in je team? [0-20]: 4
Welke pokemon wil je in je team? [0-20]: 5
Welke pokemon wil je in je team? [0-20]: 6
Welke pokemon wil je in je team? [0-20]: STOP
Jouw team van pokemon is: 
1. Ivysaur
2. Venusaur
3. Charmander
4. Charmeleon
5. Charizard
6. Squirtle
```

**voorbeeld interactie**

<figure><img src="../../.gitbook/assets/js-7-oef6.gif" alt=""><figcaption></figcaption></figure>

## oefening 7: twee dimensionale som

**leerdoelen**

* twee dimensionale arrays

**functionele analyse**

We gaan de som berekenen van alle waarden van een tabel (of tweedimensionale array).

**technische analyse**

We beginnen met de volgende twee dimensionele array:

```
let spreadsheet = [
    [100, 104, 105],
    [144, 110, 109],
    [105, 107, 111]
];
```

* Maak een variabele `sumRow1` en ken de som van de drie elementen van de eerste rij hieraan toe.
* Print de som uit op het scherm.
* Doe hetzelfde voor de andere rijen.

**voorbeeldinteractie**

<figure><img src="../../.gitbook/assets/js-7-oef7.png" alt=""><figcaption></figcaption></figure>
