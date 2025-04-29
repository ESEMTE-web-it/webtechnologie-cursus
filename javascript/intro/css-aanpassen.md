# CSS aanpassen met JavaScript


Naast het bewerken van de HTML, kunnen we met JavaScript ook CSS manipuleren.

### Directe CSS-aanpassing via JavaScript

Het is mogelijk om de CSS van een element direct aan te passen door de `style` property van dat element te wijzigen. Bijvoorbeeld:

```javascript
document.querySelector('#p2').style.color = 'blue';
```



Try it yourself: [link](https://www.w3schools.com/js/tryit.asp?filename=tryjs_change_style)

{% hint style="info" %}
Let op: Het aanpassen van CSS via JavaScript op deze manier wordt vaak vermeden, omdat het kan leiden tot complexiteit en onvoorspelbare gevolgen. Het overschrijft inline stijlen en kan de scheiding van verantwoordelijkheden tussen HTML, CSS en JavaScript verstoren.
{% endhint %}

## Classlist

Een betere en meer gestructureerde manier om CSS toe te passen via JavaScript is door gebruik te maken van de classList van een element. Hiermee kun je classes toevoegen of verwijderen, zonder direct inline stijlen te bewerken. Het voordeel hiervan is dat je de styling beheert via de CSS-bestanden en niet direct in de JavaScript-code.

### Classlist ophalen

```javascript
let classesOnSection = document.querySelector("section").classList // toont een lijst van alle classes op de section
```

### Een class toevoegen

Om een class aan een element toe te voegen, gebruik je de add() methode:

```javascript
document.querySelector("section").classList.add("my-class") // voeg de class my-class toe aan de lijst van classes.
```

### Een class verwijderen

Om een class van een element te verwijderen, gebruik je de remove() methode:

```javascript
document.querySelector("section").classList.remove("my-class") // verwijder de class my-class van de classlist. 
```

## CSS uitlezen met JavaScript

CSS die al door de browser verwerkt werd (vanuit een externe stylesheet), kan je niet zomaar uitlezen. Hiervoor gebruiken we de functie `window.getComputedStyle()`.

```js
let color = window.getComputedStyle(
  document.querySelector('#id")
).backgroundColor;
```
