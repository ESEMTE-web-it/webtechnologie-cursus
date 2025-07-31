# kleur

## kleur

Kleuren kunnen voor meerdere onderdelen van een HTML-document vastgelegd worden en er zijn verschillende manieren waarop deze kleuren benoemd kunnen worden. Ze kunnen gespecificeerd worden door hun kleurennaam, of HEX, RGB, RGBA, HSL of HSLA-waarden. Een waaier aan mogelijkheden dus.

### kleurnaam

De meest eenvoudige manier om een kleur vast te leggen is door middel van een naam, wat makkelijker te onthouden is dan een combinatie van cijfers en/of letters. CSS ondersteunt [140 standaard kleuren](https://www.w3schools.com/colors/colors_names.asp) op basis van de naam van de kleur zelf

```css
/* kleurnaam */
h1 {
    color: yellow;}
```

### HEX-code

Deze code begint met een # en telt 6-elementen, waarbij de intensiteit van rood, groen en blauw binnen een kleur geduid wordt. Hiervoor worden telkens een paar van twee karakters uit de range 0 t/m 9 en A t/m F gebruikt.

```css
/* hex-code */
h2 {
    
color: #ee3e80;}
```

### RGB en RGBA-waarde

Om een RGB-kleur te definiëren wordt de waarde van elk van de basiskleuren rood, groen en blauw in een getal tussen 0 en 255 uitgedrukt.

```css
/* rgb-waarde */
p {
    color: rgb(102,205,170);}
```

Bij een RGBA-waarde wordt er tevens rekening gehouden met de transparantie of opacity van een kleur. Aangezien de rgba-notatie geïntroduceerd werd binnen CSS3, wordt deze dus niet ondersteund door oudere browsers en zal enkel de kleur weergegeven worden.

```css
/* rgba-waarde met een transparantie (opacity) van 50%, dus 0.5 */
p {
    color: rgba(102,205,170,0.5);} 
```

### HSL & HSLA-waarde

CSS3 introduceert een nieuwe notatie om een kleur te benoemen met behulp van een tint, (**h**ue) verzadiging (**s**aturation) en lichtheid (**l**ightness).\
**hue**: Tint is een graad op het kleurenwiel van 0 tot 360 graden. 0 is rood, 120 is groen en 240 is blauw.\
**saturation**: Verzadiging is een procentuele waarde, 0% betekent een grijstint en 100% is de volledige kleur.\
**lightness**: Lichtheid is ook een percentage, 0% is zwart, 50% is niet licht of donker, 100% is wit.\
**alpha**: Transparantie wordt uitgedrukt als een getal tussen 0 en 1,0. 0,5 staat bijvoorbeeld voor 50% transparantie en 0,75 staat voor 75% transparantie.

```css
/* hsl-waarde */
body {
    background-color: #C8C8C8;
    background-color: hsl(0,0%,78%);}
    
/* hsla-waarde met een transparantie (opacity) van 15%, dus 0.15 */
p {
    background-color: #ffffff;
    background-color: hsla(0,100%,100%,0.15);}
```

## tekstkleur

De `color` eigenschap bepaalt de tekstkleur van een element.

```css
body {
    color: darkgrey;
}
```

## achtergrondkleur

De `background-color` eigenschap bepaalt de achtergrondkleur van een element.

```css
body {
    background-color: lightgrey;
}
```

### achtergrondafbeelding

Naast achtergrondkleuren, is het ook mogelijk om met achtergrondafbeeldingen te werken. Met de `background-image` eigenschap kunnen we achter elk HTML-element een afbeelding plaatsen. Dit kan over de ganse website of slechts een deel van de pagina. Het pad naar de afbeelding wordt meegegeven via een URL.

```css
body { 
    background-image: url("../images/pattern.gif");
}
```

extra info: artikel [A Deep Dive Into object-fit And background-size In CSS](https://www.smashingmagazine.com/2021/10/object-fit-background-size-css/)

#### herhaling

Standaard staat de afbeelding ingesteld om zichzelf te herhalen tot de volledige kader gevuld is. Uiteraard is dit niet altijd de gewenste uitkomst.

```css
body {
    background-image: url("../images/tulp.gif");
    background-repeat: no-repeat;
}
```

Andere opties zijn:

* `repeat`: afbeelding wordt verticaal en horizontaal herhaald;
* `repeat-x`: afbeelding wordt horizontaal herhaald;
* `repeat-y`: afbeelding wordt verticaal herhaald;
* `no-repeat`: afbeelding wordt niet herhaald.

#### positionering

Wanneer we een afbeelding niet herhalen, kunnen we met de `background-position` eigenschap bepalen waar in de kader de afbeelding geplaatst moet worden. Je kan zowel de horizontale als de verticale positie bepalen.

```css
body {
    background-image: url("../images/tulp.gif");
    background-repeat: no-repeat;
    background-position: center top;
}
```

#### korte schrijfwijze

Zoals wel vaker het geval is in CSS, kunnen we ook bij de achtergrondafbeeldingen de eigenschappen in een kortere weergave meegeven.

```css
body {
    background: #ffffff url("../images/tulp.gif") no-repeat top right;
}
```

### sprites

Sprites zijn bestanden in het afbeeldingsformaat waar meerdere afbeeldingen in samen worden gezet. Door gebruik te maken van de eigenschappen van de achtergrondafbeelding kunnen we dan wisselen tussen de verschillende afbeeldingen in het bestand.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCLAPYB2YpMaJ1UAhgA6QrEBmAljGGgNqhyDXBFrY8BYmXKIZtADwBCACIB5AMIAVAJoAFAKIACHPgB8AHXLyTUC1awQGSO-LDwAnjDsBiIQDcoTjdDYEtDQyZSME54TgpUQwAnaAZYvwgAbksAX0tLXwYAoPhDQJCww1wGRIBzTnIEgAYs8nCmJyR6mqaW8MC3AFo3TwgE8gpMisjo2PjDBgAjKigAV0Rew3hSJh6cvPICouDAwkND-pKGctbjCE4anASAFiemAA8NzrAmRncEhagpFgAGsWrlyPksKQRNc+hB2PAmu8NgB3ThIeBYZ4ANmRFQWDBBNUSpBW5CQCRWiSgAAoAOQ4eAsVAAehZiQYKIwdUxKwWK0giWksngGDIuBZAEFdAMAJKaAYAcQAEiyGGBIPAwAMkBBcFEBiiIAtELAsCyAOzYxoAJgYNoAnA7rQwLU8bQtsbBsewng6GOx2AAON2OJDsRoAZgtQYDNoArI0WZxcDUAPr+b6JGIQMDczjsOkASkMjVLYP23iYyT8sNK8MRhmxkbxNzRGKxhieLY++MJwOJpPJlOp9MZzLZHK5PKwfIFECFFBFYuhUpl8qVqvVmu1uv12qNJrg5qttvtTpdbo9Xp9foDwdDTgj0dj7ATSZT6cz1ZzebqhZLAYngtd5yz2CEDnICA3hKUIbhgBEEgARkdVtwnbTFnh7DYCSJEkyQpQwqVpBl4CZMBWXZTl815flBWFCAZBXCVpTlBUVTVDUIC1HU9QNQ9TRPa07UdZ1Gldd1PW9X1-UDEMnjDZ8YzjRNk1TDNCizX98wAwwBgdJDQOacD5BZYYvEsUyHCcFwFlIJB3DsSyVigQx0QAXnMEB-AuLy7HCeQyg8ryoREPz5CuLBknYTyQHHCi2RRJKMGYDAFggcK1VMUzAn8wxAs4NykFi6sID8cLIui2L4so5gUVFHk7NIYEMDiTKGGyllcoqAqitiqCYIq4wqpCsiJxZJKuQYGQjUSJhGLSjKQE6jqcs4FwWRcpyrBZOyHI2mxTCIcBoDgWZKFoRpUEaICHVQC0QGyQhBGEUR0AwAArXgpCXRj4FoR7nu816xFgDVjoYuR0EegBdbIgA" %}

