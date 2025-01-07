# HTML aanpassen

Er bestaan verschillende manieren om HTML aan te passen vanuit JavaScript. Elk van deze manieren heeft voor- en nadelen. Het is dan ook belangrijk het verschil te kennen om goed te kunnen beslissen welke manier je wanneer gebruikt.

## document.write();

Met document.write(); kunnen we heel eenvoudig nieuwe inhoud aan de pagina (DOM) toevoegen.

{% hint style="warning" %}
Dit is echter een manier van werken die we zelden zullen adviseren. Je kan hiermee nl. jouw volledige pagina overschrijven!
{% endhint %}

## element.innerHTML = "";

Met de innerHTML-eigenschap kan je de volledige inhoud (incl. markup) van een node verkrijgen en aanpassen als een string.

{% hint style="warning" %}
**XSS** Cross-site scripting attacks zijn manieren om bepaalde data toe te voegen aan een website die daar niet thuis hoort. (video: https://youtu.be/zv0kZKC6GAM )
{% endhint %}

try it yourself: [link](https://www.w3schools.com/js/tryit.asp?filename=tryjs_output_dom)

## element.textContent = ""

Met `textContent` kunnen we tekstuele inhoud van een HTML-element lezen en aanpassen. Deze gaan we regelamtig gebruiken in onze oefeningen!

```js
let element = document.getElementById('result');
element.textContent = "Nieuwe tekst";
```

## eigenschappen

We kunnen ook alle eigenschappen van een HTML-element wijzigen. Denk hierbij bijvoorbeeld aan de `src` van een afbeelding.

```javascript
document.getElementById("myImage").src = "landscape.jpg";
```

Try it yourself: [link](https://www.w3schools.com/js/tryit.asp?filename=tryjs_dom_image)

## HTML toevoegen

`appendChild()` voegt een node toe als child (laatste onderliggende object) van een node.

Als u een nieuwe alinea met tekst wilt maken, vergeet dan niet om de tekst te maken als een node die u aan de alinea toevoegt en voeg dan die alinea vervolgens aan het document toe.

U kunt deze methode ook gebruiken om een ​​element van het ene naar het andere element te verplaatsen.

Gebruik insertBefore () om een ​​nieuw child-node in te voegen in een reeds bestaande, onderliggende node.

meer info: [link](https://www.w3schools.com/jsref/met_node_appendchild.asp) try it yourself: [link](https://www.w3schools.com/jsref/tryit.asp?filename=tryjsref_node_appendchild)
