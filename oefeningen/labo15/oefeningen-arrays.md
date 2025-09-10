# Oefeningen labo 15

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

- Gebruik steeds JS modules om globale variabelen te vermijden (`<script type="module" src="./path/to/script.js" defer></script>`)
- Zet je Javascript file steeds in strict mode (`"use strict"`);
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)

## Oefeningen arrays

### Oefening 1: Array aanmaken en element toevoegen

Maak een array `colors` met de waarden `"red"`, `"green"`, `"blue"`.

* Voeg `"yellow"` toe aan het einde van de array.
* Voeg `"purple"` toe aan het begin van de array.
* Toon de volledige array in de console.

### Oefening 2: Elementen vervangen

Je hebt een array `numbers = [10, 20, 30, 40, 50]`.

* Vervang het derde element (`30`) door `99`.
* Toon de nieuwe array in de console.

### Oefening 3: Array lengte

Maak een array `animals = ["dog", "cat", "fish", "parot"]`.

* Toon in de console hoeveel elementen de array bevat.
* Voeg een extra dier toe.
* Toon opnieuw de lengte in de console.

### Oefening 4: Doorloop een array

Maak een array `people = ["Anna", "Bram", "Celine", "David"]`.

* Gebruik een **for-lus** om elke naam afzonderlijk in de console te tonen.

### Oefening 5: Som van getallen

Maak een array `numbers = [5, 10, 15, 20, 25]`.

* Gebruik een **for-lus** om de som van alle getallen te berekenen.
* Toon de som in de console.

### Oefening 6: Even getallen

Maak een array `numbers = [3, 8, 12, 5, 7, 20]`.

* Gebruik een lus om enkel de **even getallen** in de console te tonen.

### Oefening 7: Toegang tot elementen

Maak een array:

```js
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
```

* Toon het middelste element (`5`) in de console.
* Toon het laatste element van de eerste rij (`3`) in de console.

### Oefening 8: Som van een rij

Gebruik dezelfde `matrix` uit oefening 7.

* Bereken de som van alle getallen in de tweede rij (`[4, 5, 6]`).
* Toon het resultaat in de console.

### Oefening 9: Bestaat het element?

Maak een array `fruit = ["apple", "banana", "cherry", "mango"]`.

* Controleer met een **if-statement** of `"mango"` in de array zit.
* Toon een boodschap in de console: `"Mango found!"` of `"Mango not found!"`.

### Oefening 10: Zoek de index

Maak een array `letters = ["a", "b", "c", "d", "e"]`.

* Zoek de index van `"c"`.
* Toon het resultaat in de console.