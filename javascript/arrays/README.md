# 7: arrays

Tijdens het onderdeel van datatypes hebben we heel kort het concept `array` laten vallen. In JavaScript is een array een lijst van waarden. Elke waarde kan aangesproken worden aan de hand van een index.

## gebruik

Net zoals bij andere variabelen moeten we in JavaScript bij het maken van een variabele voor een array geen type geven.

De declaratie van de variabele zal er als volgt uit zien:

```js
let numbers = new Array();
```

We kunnen ook als beginwaarde een lege array meegeven. Er zitten dus op dat moment nog geen waarden in. We kunnen een lege array toekennen aan de variabele op de volgende manier:

```js
let numbers = [];
```

{% hint style="info" %}
In andere talen zoals Java en C# moet je de lengte van de array meegeven. In JavaScript is dat niet zo. De array zal groeien met het aantal elementen er in geplaatst worden.
{% endhint %}

Je kan ook op voorhand al een aantal elementen meegeven:

```js
let numbers = [1,2,3,4,5];
```

Om een element op te vragen van een array kan je dat doen aan de hand van vierkante haakjes met daarin een getal. Dit getal komt overeen met de positie van het element dat je wil opvragen. Let op: ook in JavaScript begint het eerste element bij 0.

```js
let fruits = ["Banana", "Apple", "Orange"];

console.log(fruits[0]); // Banana
console.log(fruits[1]); // Apple
console.log(fruits[2]); // Orange
```

Vraag je een element voor een index op die niet bestaat dan krijg je undefined

```js
console.log(fruits[3]); // undefined
```

Als je een element wil vervangen kan je dit op de volgende manier doen:

```js
fruits[2] = "Pear";
```

Je kan ook elementen toevoegen nadat je de array hebt gedeclareerd:

```js
fruits[3] = "Kiwi";
```

Soms is het nodig om te weten hoeveel elementen er in de array zitten. Dit kan je met `length` doen.

```js
let fruits = ["Banana", "Apple", "Orange"];

console.log(fruits.length); // 3
```

Je kan ook de array uitprinten in je console venster. Dit is vooral handig tijdens het debuggen

```js
let fruits = ["Banana", "Apple", "Orange"];

console.log(fruits); // [ 'Banana', 'Apple', 'Orange' ]
```

### push/pop

We hebben hiervoor een element toegevoegd aan de hand van een nieuwe index.

```js
fruits[3] = "Kiwi";
```

Je kan dit ook doen aan de hand van de `push` methode op de array aan te roepen. Je hoeft hier geen index van de array mee te geven. Het element wordt achteraan de array toegevoegd:

```js
fruits.push("Kiwi");
```

Wil je het laatste element verwijderen van de array dan gebruik je de `pop` methode.

```js
fruits.pop();
```

Handig hierbij is dat de `pop()` methode het element zelf teruggeeft. Zo kan je dit toekennen aan een variabele en ermee werken

```js
let lastFruit = fruits.pop();
console.log(lastFruit); // Kiwi
```

### shift/unshift

We hebben al elementen toegevoegd en verwijderd van de achterkant van een array. Maar je kan hetzelfde doen aan de voorzijde van de array.

We kunnen een element vooraan de array toevoegen met de `unshift` methode:

```js
let fruits = ["Banana","Apple","Orange"];

fruits.unshift("Pear");

console.log(fruits[0]); // Pear
```

Wil je het eerste element uit de array halen dan doe je dit met `shift` methode:

```js
let fruits = ["Banana","Apple","Orange"];

console.log(fruits.shift()); // Banana
console.log(fruits);
```

### join

De .join() methode wordt gebruikt op arrays en plaatst een separator (scheidingsteken) tussen de elementen om één grote string te vormen.
```javascript
const words = ['Dit', 'is', 'een', 'zin'];
const result = woorden.join(' ');
console.log(resultaat); // Output: Dit is een zin 
```

.join() verandert de originele array niet, maar retourneert een nieuwe string.

Je kunt ook .join() gebruiken op arrays met getallen of gemengde types – ze worden automatisch omgezet naar strings.