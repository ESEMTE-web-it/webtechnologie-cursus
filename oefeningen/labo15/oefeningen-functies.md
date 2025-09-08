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

### Oefening 1: Groetfunctie

Schrijf een functie `greet` die "Hello, welcome!" in de console toont.
Roep de functie 3 keer aan.


### Oefening 2: Som van twee getallen

Schrijf een functie `sum` die twee parameters (`a`, `b`) ontvangt en de som teruggeeft.
Test de functie met `5` en `7`.


### Oefening 3: Even of oneven

Schrijf een functie `isEven` die een getal als parameter ontvangt en `true` teruggeeft als het even is, en `false` als het oneven is.
Test de functie met minstens 2 getallen.


### Oefening 4: Minimum (declaration)

Gebruik een **function declaration** `minimum` die het kleinste van twee getallen teruggeeft.
- Test met `10` en `20` nadat je de functie hebt gecreeërd.
- Test met `30` en `10` voordat je de functie hebt gecreeërd.


### Oefening 5: Maximum (expression)

Gebruik een **function expression** in een variabele `maximum` die het grootste van twee getallen teruggeeft.
- Test met `15` en `8` nadat je de functie hebt gecreeërd.
- Test met `20` en `42` voordat je de functie hebt gecreeërd.


### Oefening 6: Kwadraat berekenen (beide vormen)

Maak zowel een **function declaration** als een **function expression** die het kwadraat van een getal berekent. 
- Roep de functie aan bovenaan in je JavaScript file en toon beide resultaten in de console.


#### Oefening 7: Vermenigvuldiging

Maak een arrow function `multiply` die twee getallen ontvangt en het product teruggeeft.
Test met `10` en `4`.


#### Oefening 8: Tel alle elementen in een array op

Maak een arrow function `arraySum` die een array van getallen als parameter ontvangt en de som berekent met een lus.
Test met `[10, 20, 30]`.


#### Oefening 9: Zoek grootste getal in een array

Maak een arrow function `largestNumber` die een array als parameter ontvangt en het grootste element teruggeeft.
Test met `[120, 200, 180]`.


#### Oefening 10: Absolute waarde

Maak een éénregelige arrow function `absolute` die de absolute waarde van een getal teruggeeft.
Test met `-15`.

#### Oefening 11: Bereken dubbele

Maak een éénregelige arrow function `double` die een getal ontvangt en het dubbele teruggeeft.
Test met `6`.
