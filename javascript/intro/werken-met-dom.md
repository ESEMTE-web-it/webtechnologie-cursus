# Werken met de DOM

Aanpassingen maken in de DOM-tree bestaat uit twee stappen:
1. Het selecteren van de node die je wilt aanpassen.
2. Het gebruiken van eigenschappen of methoden om een wijziging door te voeren.

---

## querySelector()
Een node selecteer je met de methode `document.querySelector()`. Binnen `querySelector()` geef je een string mee die werkt als een CSS-selector.  
Bijvoorbeeld: `.test` selecteert het eerste element met de class _test_.

```js
let elExample = document.querySelector('#example');
elExample.textContent = "Nieuwe tekst";
```

Meer informatie over document.querySelector vind je op [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)

## querySelectorAll()

Met document.querySelectorAll() kun je meerdere elementen tegelijk selecteren die overeenkomen met de opgegeven CSS-selector.
Deze methode geeft een NodeList terug, een array-achtig object waar je op verschillende manieren doorheen kunt loopen, zoals met forEach() of via indexering.

```javascript
let alleItems = document.querySelectorAll('li');
alleItems.forEach(item => {
  item.style.color = 'blue';
});
```

Je kunt ook specifieke elementen selecteren via indexering:

```javascript
let derdeItem = document.querySelectorAll('li')[2];
derdeItem.textContent = "Aangepast item";
```

## Parent
Een parent is het element dat zich direct boven het geselecteerde element bevindt in de DOM-structuur.
In afbeelding 1 zie je bijvoorbeeld één div-element; het parent-element daarvan is de body.

Je kunt het parent-element van een geselecteerd element opvragen met:

```javascript
let elParent = elExample.parentNode;
```

## Child

Je kunt ook in omgekeerde richting werken, van een parent naar child-elementen.
Een element kan meerdere child-elementen bevatten.

Een voorbeeld waarbij we het vierde element uit een lijst verwijderen:

```javascript
let removeEl = document.querySelectorAll("li")[3]; // The element to remove
let containerEl = removeEl.parentNode; // The parent element
containerEl.removeChild(removeEl); // Removing the element
```

