# werken met DOM

Aanpassingen maken in de DOM tree bestaat uit 2 stappen: het selecteren van de node die je wil aanpassen en de eigenschappen of methoden ervan gebruiken om een verandering te maken.

```js
let elExample = document.getElementById("example");
elExample.textContent = "Nieuwe tekst";
```

Try it yourself: [link](https://www.w3schools.com/js/tryit.asp?filename=tryjs_dom_getelementbyid)

## parent

Een parent is de node net boven de geselecteerde node. In de DOM tree in afbeelding 1 zien we 1 div-element staan. Het parent-element van deze div is body.

Je kan van een geselecteerd element altijd de parent selecteren, aangezien elk element maar één parent kan hebben.

```js
let elParent = elExample.parentNode;
```

## child

In de andere volgorde kan je van een element ook het onderliggende element selecteren. Uiteraard kan een element meerdere child-elementen bevatten.

Een voorbeeld waarbij we het vierde element uit een opsomming verwijderen:

```js
let removeEl = document.getElementsByTagName("li")[3]; //The element to remove
let containerEl = removeEl.parentNode; //The parent element
containerEl.removeChild(removeEl); //Removing the element
```
