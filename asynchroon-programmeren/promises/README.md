# 2: promises

## asynchroon vs. synchroon

### synchrone code

Tot nu toe hebben we enkel met synchrone code gewerkt. Dit betekent dat de code die we schrijven, één voor één wordt uitgevoerd. Als we een functie aanroepen, wordt de functie uitgevoerd en wanneer de functie klaar is, wordt de volgende regel code uitgevoerd. Dit is de manier waarop we over het algemeen code schrijven. We schrijven code van boven naar beneden en de code wordt van boven naar beneden uitgevoerd.

```js
console.log("Stap 1");
console.log("Stap 2");
console.log("Stap 3");
```

Als we deze code uitvoeren, zien we dat de drie regels code één voor één worden uitgevoerd. De eerste regel wordt uitgevoerd, dan de tweede en dan de derde. Dit is synchrone code.

### asynchrone code

Bij asynchrone code is het bovenstaande niet het geval. Bij asynchrone code wordt de code niet één voor één uitgevoerd. In plaats daarvan kan het zijn dat een bepaald stuk code wordt uitgevoerd, terwijl een ander stuk code wordt uitgevoerd. We hebben in principe al eens een voorbeeld gezien van asynchrone code. Dit was bijvoorbeeld het geval bij de setTimeout-functie. We hebben gezien dat we een functie kunnen meegeven aan de setTimeout-functie. Deze functie wordt pas na een bepaalde tijd uitgevoerd. Dit is een voorbeeld van asynchrone code. De code die in de functie staat, wordt niet direct uitgevoerd. In plaats daarvan wordt de code uitgevoerd na een bepaalde tijd.

```js
console.log("Stap 1");
setTimeout(() => console.log("Stap 2"), 1000);
console.log("Stap 3");
```

Dit geeft ons het volgende resultaat:

```
Stap 1
Stap 3
Stap 2
```

Je ziet nu dat hoewel de code van "Stap 2" op lijn 2 staat, deze pas na "Stap 3" wordt uitgevoerd. Dit komt omdat de code van "Stap 2" pas na 1 seconde wordt uitgevoerd.

## promises

Een belangrijk mechanisme om asynchrone code te schrijven is het gebruik van promises. Een **promise** is een object dat een waarde bevat die pas op een later moment beschikbaar zal zijn. Zoals het engelse woord al aangeeft, is een promise een belofte dat de functie die een promise teruggeeft, op een later moment een waarde zal teruggeven.

Een van de meest bekende functies die een promise gebruikt is de fetch-functie. Deze functie wordt gebruikt om data op te halen van een server. Alle communicatie tussen je programma en de server moet synchroon gebeuren. Dit komt omdat je niet wil dat je programma wacht tot er een antwoord komt van de server. Zelfs al gaat de communicatie met de server heel snel, ze gaat in vergelijking met de uitvoering van een gewone instructie veel trager.

### verschillende statussen van een promise

Een promise heeft verschillende statussen. Een promise kan in één van de volgende statussen zitten:

* pending: de Promise is nog niet afgerond. We hebben dus nog geen waarde.
* fulfilled: de Promise is afgerond. We hebben nu een waarde.
* rejected: de Promise is afgerond, maar er is een fout opgetreden. We hebben nu een fout.

De promise begint altijd in de pending status. Wanneer de promise afgerond is, kan deze in de fulfilled status zitten of in de rejected status.

### aanmaken van een promise

We gaan het gebruik van een promise bekijken aan de hand van een voorbeeld. We gaan een promise maken die een getal teruggeeft. Deze zal een vermenigvuldiging uitvoeren. We maken een promise aan met de `new Promise()`-constructor. Deze constructor heeft als argument een functie die twee argumenten heeft: resolve en reject. Deze twee argumenten zijn functies die we kunnen aanroepen om de promise te laten veranderen van status.

```js
const promise = new Promise((resolve, reject) => {
    resolve(2 * 2);
});
```

Je ziet dat we hier de resolve-functie aanroepen met de vermenigvuldiging van 2 en 2. Dit betekent dat de Promise nu in de fulfilled status zit en we dus een waarde hebben.

### then-functie

Willen we deze waarde gebruiken, dan moeten we een then-functie aanroepen op de promise. Deze functie heeft als argument een functie die als argument de waarde bevat die de promise teruggeeft. In ons geval is dit een number.

```js
const promise = new Promise((resolve, reject) => {
    resolve(2 * 2);
});

promise.then((result) => {
    console.log(result);
});
```

De functie die we meegeven aan de then-functie wordt pas uitgevoerd wanneer de promise in de fulfilled status zit. Dit betekent dat de functie die we meegeven aan de then-functie pas uitgevoerd wordt wanneer de promise afgerond is.

Uiteraard is dit een vreemd voorbeeld omdat de vermenigvuldiging van 2 en 2 heel snel gebeurt. In de praktijk duurt de code die in de promise staat veel langer. We kunnen dit eenvoudig simuleren door de resolve functie pas aan te roepen na een bepaalde tijd. Dit doen we met de setTimeout-functie.

```js
const promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve(2 * 2)
    }, 1000);
});

promise.then((result) => {
    console.log(result);
});
```

Bij het uitvoeren van deze code ga je zien dat de then-functie pas na 1 seconde wordt uitgevoerd. Dit komt omdat de promise pas na 1 seconde in de fulfilled status zit.

### promise als return type

Meestal maken we niet zelf een promise aan, maar gebruiken we een functie die een promise teruggeeft. Deze functie kan dan als return type promise hebben. We breiden ons voorbeeld uit met een functie die een promise teruggeeft. Deze functie zal een vermenigvuldiging uitvoeren. We geven de functie een argument mee: number1 en number2. Deze functie zal de vermenigvuldiging van deze twee getallen teruggeven.

```js
const multiply = (number1, number2) => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve(number1 * number2);
        }, 1000);
    });
};
```

Als je deze functie gewoon aanroept alsof het een normale functie is kan je zien dat deze een promise teruggeeft.

```js
const result = multiply(2, 2);
console.log(result); 
```

Je zal hier als output het volgende krijgen: `Promise { <pending> }`.

Dit betekent dat de promise nog niet afgerond is. We kunnen de then-functie aanroepen op deze promise om de waarde te gebruiken.

```js
const result = multiply(2, 2);
result.then((result) => {
    console.log(result);
});
```

of we kunnen de then-functie meteen aanroepen op de functie.

```js
multiply(2, 2).then((result) => {
    console.log(result);
});
```

### then chaining

Willen we bijvoorbeeld de multiply functie twee keer gebruiken, dan zouden we dit op de volgende manier kunnen doen.

```js
multiply(2, 2).then((result) => {
    multiply(result, 2).then((result) => {
        console.log(result);
    });
});
```

Hoewel dat dit werkt is dit niet de beste manier om dit te doen. Je zal al snel zien als je dit vaker moet doen dat je code heel snel onoverzichtelijk wordt. Gelukkig is er een betere manier om dit te doen. We kunnen de then-functie meerdere keren aanroepen op dezelfde promise. Dit noemen we then chaining. We kunnen dit ook doen met de multiply-functie.

```js
multiply(2, 2)
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        console.log(result); // 8
    });
```

Je ziet hierboven dat als je iets wil uitvoeren nadat de eerste then functie is uitgevoerd, je dan een nieuwe promise moet teruggeven. Deze nieuwe promise zal dan weer gebruikt worden in de volgende then functie. Dit is de manier om then chaining te doen. Zo kan je meerdere multiply functies aan elkaar koppelen. Dit kan je zoveel keren doen als je wil zonder dat je code onoverzichtelijk wordt.

```js
multiply(2, 2)
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        console.log(result); // 32
    });
```

### catch

Zoals we al vermeld hadden kan een promise in de **rejected** status komen te zitten. Dit betekent dat er een fout is opgetreden. Bijvoorbeeld als we onze multiply-functie zouden uitbreiden met een foutmelding als het resultaat groter is dan 10.

```js
const multiply = (number1, number2) => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            if (number1 * number2 > 10) {
                reject("Result is greater than 10");
            } else {
                resolve(number1 * number2);
            }
        }, 1000);
    });
};
```

Willen we deze foutmelding opvangen kunnen we een catch-functie toevoegen achter de then-functie:

```js
multiply(2, 2)
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        return multiply(result, 2);
    })
    .then((result) => {
        console.log(result); // 16
    })
    .catch((error) => {
        console.log(error);
    });
```

Bij het uitvoeren van deze code zal je zien dat de foutmelding wordt afgedrukt en de rest van de then functies niet meer worden uitgevoerd.

### promise helper functions

#### Promise.all

De Promise.all-functie wordt gebruikt om meerdere promises tegelijkertijd uit te voeren. Als je bijvoorbeeld 2 promises hebt die je tegelijkertijd wil uitvoeren en vervolgens wil je de resultaten van beide promises gebruiken, dan kan je dit doen met de Promise.all-functie.

Stel dat we een twee functies hebben die een promise teruggeven. De eerste functie haalt de naam van een gebruiker op en de tweede functie haalt de leeftijd van een gebruiker op. En we gaan er vanuit dat deze twee functies tegelijkertijd moeten worden uitgevoerd. De functie die de naam ophaalt duurt 1 seconde en de functie die de leeftijd ophaalt duurt 2 seconden.

```js
const getName = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("John");
        }, 1000);
    });
};

const getAge = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve(25);
        }, 2000);
    });
};
```

Als we deze twee functies willen uitvoeren, dan kunnen we dit doen met de Promise.all-functie. We geven de Promise.all-functie een array mee met de promises die we willen uitvoeren. De Promise.all-functie zal een promise teruggeven die fulfilled zal worden wanneer alle promises uitgevoerd zijn. De Promise.all-functie zal een array teruggeven met de resultaten van de promises.

```js
Promise.all([getName(), getAge()])
    .then((result) => {
        console.log(result); // ["John", 25]
    }).catch((error) => {
        console.log(error);
    });
```

En de tijd die nodig is om de promises uit te voeren is de langste tijd van alle promises. In dit geval is dat 2 seconden.

#### Promise.race

Wil je meerdere promises tegelijkertijd uitvoeren en enkel de waarde hebben die het snelste beschikbaar is dan kan je Promise.race gebruiken. Stel dat je twee functies hebt die allebei de naam van een gebruiker ophalen. De eerste functie duurt 1 seconde en de tweede functie duurt 2 seconden.

```js
const getNameFromDatabase = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("John");
        }, 3000);
    });
};

const getNameFromCache = () => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("John");
        }, 500);
    });
};
```

Wil je enkel de name gebruiken van de functie die het snelste klaar is, dan gebruiken we hiervoor de Promise.race-functie. Deze zal al na 500ms uitgevoerd worden omdat de `getNameFromCache` functie het snelste klaar is.

```js
Promise.race([getNameFromDatabase(), getNameFromCache()])
    .then((result) => {
        console.log(result); // "John"
    });
```
