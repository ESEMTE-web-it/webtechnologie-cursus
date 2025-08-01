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

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp0AjbkgCe+7boBM6gLInlAMTIAnMPGUB1CAeXyGAcwhBAHosawsAB1t7J1d3P2cAxIisDBCo7UjlMiQAXk0QJAhcbgL1dPMdMFhnMgj4fSRuWABXZj4MQPhFGHb4ACETAEkkAAoCopKCgEoMMjo6CGcACWkbABllXOUAVmUAamUANgBuC2Dq2vrKkKNTfRC9ZW1OSBgEMl4qdABGHdQAAwgAC+hHoTBY6AwACsqMQeHwIAJ0CCwSBGMxWBhYGA4VxePx4KwQQBdYFAA %}

## element.textContent = ""

Met `textContent` kunnen we tekstuele inhoud van een HTML-element lezen en aanpassen. Deze gaan we regelamtig gebruiken in onze oefeningen!

```js
let element = document.querySelector('#result');
element.textContent = "Nieuwe tekst";
```

## eigenschappen

We kunnen ook alle eigenschappen van een HTML-element wijzigen. Denk hierbij bijvoorbeeld aan de `src` van een afbeelding.

```javascript
document.querySelector('#myImage").src = "landscape.jpg";
```

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp0AjbkgCe+7boBM6gFIMAbgwDKsAE5kADvGUAJaQFkAGWUJf0EAeixrCzJcAHNlMiQAXk0QWIY4iDTlMFdYVJAceA8wVHDw1wYAdww4sngsAFcDJsh83n54DB5ccIBBeQBaAElpIYBxH3CGMEh4MCGkCFxuReqIA0RYLEqIEjBIiAYkQ9wGMjpw2LiAfXhXCAgMDzo4nOqkxsKARgA2AAMOSwEDIcRwv0sQJA5h0YDcnng+iQ3FgTWYfDqEHgihgGPgACETCMkAAKNIZLJpACUGDysGUyWUaWKpXKlRqdQazVa7R4fAgmN6A2GY0m01m80Wy1W602212jwORxOZwuVw8l2OHg8MAwACsPO8QABuCzheHuLywwQedTSEHKbjueqMKCJc5ZZTVWYeu4PJ4vN6EZStbyNCC5BFeZQ7BhvZCJcPcZSauja3XPQ1xCJ27TmoymfQRPTaTiQGAIMi8KjoH4AVlQAJAAF9CPQmCx0AaqMR+V1WK32yBGMxWD05px+4L4IOWwBdFtAA" %}

## HTML toevoegen

`appendChild()` voegt een node toe als child (laatste onderliggende object) van een node.

Als u een nieuwe alinea met tekst wilt maken, vergeet dan niet om de tekst te maken als een node die u aan de alinea toevoegt en voeg dan die alinea vervolgens aan het document toe.

U kunt deze methode ook gebruiken om een ​​element van het ene naar het andere element te verplaatsen.

Gebruik insertBefore () om een ​​nieuw child-node in te voegen in een reeds bestaande, onderliggende node.

meer info: [link](https://www.w3schools.com/jsref/met_node_appendchild.asp) {% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp0AjbkgCe+3QEZ10rBGWKYzPsvEGAVnHiCA9FivbdACZrW2UGAAdwiDokSSwKJAAKAEplAFkIeCxjHyxg7QCAVyhlMiQAXk0QXBMAGTIweCr9ZWVBKDJ1SW4SEggIHw6WtqHpCAZBzoDvYv0A8K6O2ABrZSqAQUjopCrleG4wrZiwulLEXD2DrLtt5R690I7G1B8FgsNC+H3T3lgl5cq1RMADFCnQEGReClmpsojEfAZPt85jowLAAE5kcLwfQkMEQ3jKGqg8HwSF0FLKYDvbzeZSSdHjRAnNYgDq7OjGCCobQ8OiNZScpB2crKJDcWCFJzwDAYpkQBwQaWJKrskDJADcNLpDPlYT2EAAHvBBVyeeDeALEMahSKxRKpdEZXKGIgxsaAHJclUgADqrog6Kqmu1ylht2uBuNpuFlwedlVZA5Zu0towEThsXiUCS1vgtpDdG0tLDRyQ8dZapjdn2Fae8HN4sl0owAHNMorpQAhEwASSSVRq9UawfTZbiCUSBa1dAAvtM0ZjsSiEcYzNM9NpOJAYAT+awAMwAFlQAAYQLPCPQmCx0Bg3FRiHz+PBWBeryBGMxWLKwI+uLwL5vrOAC6s5AA %}
