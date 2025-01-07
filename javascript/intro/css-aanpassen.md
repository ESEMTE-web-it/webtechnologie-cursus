# CSS aanpassen

Naast het bewerken van de HTML, kunnen we met JavaScript ook CSS gaan manipuleren.

```javascript
document.getElementById("p2").style.color = "blue";
```

Try it yourself: [link](https://www.w3schools.com/js/tryit.asp?filename=tryjs_change_style)

{% hint style="info" %}
Het aanpassen van CSS via JS wordt vermeden aangezien dit ongelooflijk complexe gevolgen kan hebben.
{% endhint %}

## CSS uitlezen

CSS die al door de browser verwerkt werd (vanuit een externe stylesheet), kan je niet zomaar uitlezen. Hiervoor gebruiken we de functie `window.getComputedStyle()`.

```js
let color = window.getComputedStyle(
  document.getElementById("id")
).backgroundColor;
```
