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

### Oefening 1: Maak een object

Maak een object `car` met de properties `brand`, `model` en `year`. Toon het object in de console.

### Oefening 2: Lees properties

Geef de `brand` en `model` van het object `car` uit de vorige oefening weer in de console.

### Oefening 3: Voeg een property toe

Voeg aan het object `car` een property `color` toe met waarde `red`. Toon daarna het volledige object in de console.

### Oefening 4: Array van objecten

Maak een array `students` met 3 objecten, elk met de properties `name` en `age`. Toon de array in de console.

### Oefening 5: Itereren over objecten in array

Gebruik een lus om de `name` van elke student uit de array `students` te tonen in de console.

### Oefening 6: Gemiddelde leeftijd

Bereken met behulp van een lus de gemiddelde `age` van alle studenten in de array `students` en toon dit in de console.

### Oefening 7: Zoek student

Zoek in de array `students` de student met de naam `Bob` en toon het volledige object in de console.

### Oefening 8: Bestaat student?

Controleer of er een student met de naam `Daisy` in de array `students` zit. Toon `true` of `false` in de console.

### Oefening 9: Toon alle properties

Gebruik een `for...in` lus om alle properties en hun waarden van het object `car` weer te geven in de console.

### Oefening 10: Tel aantal properties

Schrijf code die telt hoeveel properties het object `car` heeft. Toon het aantal in de console.
