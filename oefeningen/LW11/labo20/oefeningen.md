# oefeningen

## oefening 1: Promises bij notificatie toestemming

**Leerdoelen**

**functionele analyse** 

Om een notificatie aan een gebruiker te sturen, moet je eerst toestemming vragen via de Notifications API. Als de gebruiker toestemming geeft, wordt er een notificatie met de tekst "Hello world" weergegeven. Als de gebruiker de aanvraag weigert, wordt er een bericht "toestemming afgewezen" naar de console geschreven. Hieronder zie je hoe je dit stap voor stap in JavaScript kunt uitvoeren:

**technische analyse**

- Gebruik `Notification.requestPermission()` om de gebruiker na het laden van de webpagina om permissie tot het verzenden van notificaties te vragen.
- Indien de gebruiker toestemt stuur je hem een nieuwe notification met de woorden "hello world".
- Indien de gebruiker de toestemming afwijst print je "toestemming geweigerd" naar de console.

**voorbeeldinteractie**

[//]: # (<figure><img src="../../.gitbook/assets/async-promises-oef1.png" alt=""><figcaption></figcaption></figure>)


## oefening 2

**Leerdoelen**

**functionele analyse**

**technische analyse**

Vertrek vanuit de volgende functie:

```javascript
    const multiply = (number1, number2) => {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve(number1 * number2);
            }, 1000);
        });
    };
```

Deze functie ontvangt twee nummers als parameter en zal meteen een nieuw promise-object teruggeven.
Na 1 seconde zal de promise succesvol resolven met het resultaat van nummer1 vermenigvuldigd met nummer2.

Het is de bedoeling dat jij deze functie aanroept met twee willekeurige getallen. Vervolgens wacht je tot de promise resolved en daarna schrijf je het resultaat weg naar de console.

**voorbeeldinteractie**

[//]: # (<figure><img src="../../.gitbook/assets/async-promises-oef1.png" alt=""><figcaption></figcaption></figure>)

