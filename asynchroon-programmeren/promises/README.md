# Hoofdstuk 2: Werken met Promises

In dit hoofdstuk leer je werken met **Promises** in JavaScript. Je leert begrijpen wat een Promise is, hoe je ermee werkt, en hoe je foutafhandeling toepast.

## Wat is een Promise?

Een Promise is een object dat de **toekomstige uitkomst** van een asynchrone operatie vertegenwoordigt. Die uitkomst kan succesvol zijn (**resolved**) of fout gaan (**rejected**).

Je hoeft **geen eigen Promises** te leren maken. Je gebruikt vooral bestaande functies die al een Promise teruggeven.

## Een eenvoudige Promise gebruiken

Stel dat je werkt met een functie `doeIetsAsynchroon()` die een Promise teruggeeft:

```javascript
doeIetsAsynchroon()
  .then(() => {
    console.log("De promise is resolved");
  })
  .catch((fout) => {
    console.error("Er ging iets mis:", fout);
  });
```

- `.then()` wordt uitgevoerd als de Promise succesvol is.
- `.catch()` wordt uitgevoerd als er iets misgaat.

## Then-chaining

```javascript
fetch("https://jsonplaceholder.typicode.com/todos/1")
  .then((response) => {
    // De eerste .then() verwerkt de response en zet deze om naar JSON
    return response.json();
  })
  .then((data) => {
    // De tweede .then() verwerkt de data die we hebben ontvangen
    console.log("Todo ontvangen:", data);
    // We kunnen ook een extra bewerking doen, zoals het loggen van de titel
    return data.title;
  })
  .then((title) => {
    // De derde .then() ontvangt de titel en logt deze
    console.log("Titel van de todo:", title);
  })
  .catch((error) => {
    // Als er een fout optreedt, wordt deze opgevangen door .catch()
    console.error("Er ging iets mis:", error);
  });
```

Promise chaining wordt bereikt door meerdere `.then()`-methoden achter elkaar te plaatsen.

Elke `.then()` ontvangt de output van de vorige stap.

De `.catch()` vangt eventuele fouten op die optreden tijdens het proces.

In dit voorbeeld worden de stappen in de fetch()-operatie gechained: eerst de response omzetten naar JSON, dan de data verwerken, en uiteindelijk de titel loggen.

## Browser-API's die Promises gebruiken

Er zijn verschillende API’s in de browser die standaard Promises teruggeven. Hier zijn drie eenvoudige voorbeelden:

### 1. fetch()

Met fetch kun je data ophalen van een server

```javascript
fetch("https://jsonplaceholder.typicode.com/todos/1")
  .then((response) => response.json())
  .then((data) => console.log("Todo:", data))
  .catch((error) => console.error("Fout bij ophalen:", error));
```

> Opgelet: de `response.json()` methode returned op zijn beurt ook weer een promise waar we de `.then()` methode van kunnen oproepen. Meer daarover in het hoofdstuk over fetch.

### 2. navigator.clipboard.readText()

Met deze browser functie kun je tekst uit het klembord van de gebruiker halen

```javascript
navigator.clipboard
  .readText()
  .then((tekst) => {
    console.log("Tekst uit klembord:", tekst);
  })
  .catch((fout) => {
    console.error("Klembord niet beschikbaar:", fout);
  });
```

### 3. Notification.requestPermission()

Met deze browser functie kun je gebruikers om toestemming vragen om notificaties te verzenden.

```javascript
    Notification.requestPermission().then((permission) => {
      if (permission === "granted") {
        new Notification("Hello!");
      }
    });
```

## (Optioneel) Zelf een Promise aanmaken

```javascript
function wachtEven(ms) {
  return new Promise((resolve, reject) => {
    if (ms < 0) {
      reject("Tijd mag niet negatief zijn");
    } else {
      setTimeout(() => {
        resolve("Klaar!");
      }, ms);
    }
  });
}

wachtEven(1000)
  .then((resultaat) => {
    console.log(resultaat);
  })
  .catch((fout) => {
    console.error(fout);
  });
```

## (Optioneel) `Promise.all()` en `Promise.race()`

- `Promise.all([p1, p2, ...])`: wacht tot **alle** promises voltooid zijn.
- `Promise.race([p1, p2, ...])`: geeft resultaat van de **eerste** Promise die af is, of faalt.

```javascript
const belofte1 = wachtEven(1000);
const belofte2 = wachtEven(1500);

Promise.all([belofte1, belofte2])
    .then((resultaten) => {
        console.log("Alle beloften klaar:", resultaten);
    })
    .catch((fout) => {
        console.error("Eén van de beloften faalde:", fout);
    });

Promise.race([belofte1, belofte2])
    .then((resultaat) => {
        console.log("Eerste belofte klaar:", resultaat);
    })
    .catch((fout) => {
        console.error("Eerste fout:", fout);
    });
```
