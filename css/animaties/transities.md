---
description: >-
  In dit hoofdstuk leer je hoe je overgangen tussen toestanden van een element
  kan definiëren. Transities verbeteren de gebruikerservaring en -interactie van
  je website.
---

# transities

Wanneer je met een website communiceert, merk je misschien dat veel elementen een toestand hebben dat verandert bij het zweven over of aanklikken van dat element. Dropdownmenu's kunnen bijvoorbeeld geopend of gesloten zijn. Knoppen kunnen van kleur veranderen wanneer ze worden gefocust of erover wordt gezweefd (hover). Pop-ups verschijnen en verdwijnen.

Standaard verandert CSS de stijl van deze toestanden onmiddellijk.

Met behulp van CSS-transities kunnen we interpoleren tussen de beginstatus en de doelstatus van het element. De overgang tussen de twee verbetert de gebruikerservaring door visuele richting, ondersteuning en hints te geven over de oorzaak en het gevolg van de interactie.

{% embed url="https://codepen.io/ykdenis/pen/PoaQZEJ" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

## transition properties

Om transities in CSS te gebruiken, kan je de verschillende transition properties gebruiken of de `transition` shorthand property.

**transition-property**

De eigenschap `transition-property` specificeert op welke CSS-eigenschap (css property) je een transitie wilt toepassen.

```css
button {
  transition-property: background-color;
}
```

De `transition-property` accepteert een of meer CSS-eigenschapsnamen in een door komma's gescheiden lijst.

Optioneel kan je gebruik maken van `transition-property:all` om aan te geven dat je op elke eigenschap een transitie wilt toepassen.

{% embed url="https://codepen.io/ykdenis/pen/RwJQrdZ" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

**transition-duration**

De eigenschap `transition-duration` wordt gebruikt om de tijd te definiëren die nodig is om een transitie te voltooien.

{% embed url="https://codepen.io/ykdenis/pen/BaVYjeV" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

`transition-duration` accepteert tijdseenheden, in seconden (**s**) of milliseconden (**ms**) en is standaard ingesteld op 0s.

**transition-timing-function**

Gebruik de eigenschap `transition-timing-function` om de snelheid van een CSS-transitie in de loop van de transitie duur te variëren.

Standaard zal CSS je elementen met een constante snelheid overzetten (`transition-timing-functie: lineair`). Lineaire overgangen kunnen er echter wat kunstmatig uitzien: in het echte leven hebben objecten gewicht en kunnen ze niet meteen stoppen en starten. Door een overgang gemakkelijker in of uit te gaan, kunnen je overgangen levendiger en natuurlijker worden.

{% embed url="https://codepen.io/ykdenis/pen/BaVYKaP" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

**transition-delay**

Gebruik de eigenschap `transition-delay` om het tijdstip op te geven waarop een transitie moet beginnen. Als de `transition-delay` niet is opgegeven, beginnen de overgangen onmiddellijk omdat de standaardwaarde 0s is. Deze eigenschap accepteert een tijdseenheid, bijvoorbeeld seconden (**s**) of milliseconden (**ms**).

{% embed url="https://codepen.io/ykdenis/pen/LYrQNGy" %}

Deze eigenschap is handig voor verspringende transities, bereikt door een langere transitievertraging in te stellen voor elk volgend element in een groep.

{% embed url="https://codepen.io/ykdenis/pen/RwJQaaQ" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

## shorthand notatie: transition

Zoals de meeste CSS-eigenschappen, is er een verkorte versie. `transition` combineert `transition-property`, `transition-duration`, `transition-timing-function` en `transition-delay`.

```css
transition: [transition-property] [transition-duration] [transition-timing-function] [transition-delay];
```

```css
.longhand-notation {
  transition-property: color;
  transition-duration: 250ms;
  transition-timing-function: ease-in;
  transition-delay: 500ms;
}

.shorthand-notation {
  transition: color 250ms ease-in 500ms;
}
```

## Op welke eigenschappen kan je een transitie toepassen?

Bij het schrijven van CSS kan je aangeven welke eigenschappen geanimeerde overgangen moeten hebben. Bekijk deze [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties)-lijst met animeerbare CSS-eigenschappen.

Over het algemeen is het alleen mogelijk om elementen over te zetten die een "middentoestand" kunnen hebben tussen hun begin- en eindtoestand. Het is bijvoorbeeld onmogelijk om overgangen voor `font-family` toe te voegen, omdat het onduidelijk is hoe de "middentoestand" tussen serif en monospace eruit moet zien. Aan de andere kant is het mogelijk om overgangen voor lettergrootte toe te voegen, omdat de eenheid een lengte is waartussen kan worden geïnterpoleerd.

Hier zijn enkele algemene eigenschappen die je kan overzetten.

**transform**

De CSS-eigenschap `transform` wordt vaak overgezet omdat het een GPU-versnelde eigenschap is die resulteert in vloeiendere animaties die ook minder batterij verbruiken. Met deze eigenschap kan je een element willekeurig schalen, roteren, vertalen of scheeftrekken.

**waarden**

* **scale()**: beïnvloedt de grootte van het element. Dit geldt ook voor de lettergrootte, opvulling, hoogte en breedte van een element. Het is ook een verkorte functie voor de functies **scaleX()** en **scaleY()**.
* **skewX()** en **skewY()**: Kantelt een element naar links of rechts, bv. je kan een rechthoek in een parallellogram veranderen. **skew()** is een afkorting die **skewX()** en **skewY()** combineert door beide waarden te accepteren.
* **translate()**: Verplaatst een element zijwaarts of op en neer.
* **rotate()**: Draait het element met de klok mee vanaf zijn huidige positie.

**color**

Voor, tijdens en na interactie kan kleur een goede indicatie zijn van de toestand. Een knop kan bijvoorbeeld van kleur veranderen als er met de muisaanwijzer over wordt bewogen. Deze kleurverandering kan de gebruiker feedback geven dat er op de knop kan worden geklikt.

De eigenschappen `color`, `background-color` en `border-color` zijn slechts een paar plaatsen waar kleur kan worden aangepast na interactie.

**shadows**

Schaduwen worden vaak overgezet om hoogteveranderingen aan te geven.

{% embed url="https://codepen.io/ykdenis/pen/wvXyGpZ" %}
Voorbeeld is gebaseerd op [https://web.dev/learn/css/transitions/](https://web.dev/learn/css/transitions/)
{% endembed %}

## overgangstriggers

Je CSS moet een statuswijziging bevatten en een gebeurtenis die de statuswijziging triggert, anders kunnen CSS-transities niet worden geactiveerd. Een typisch voorbeeld van zo'n trigger is de pseudo-klasse `:hover`. Deze pseudo-klasse komt overeen wanneer de gebruiker met de cursor over een element beweegt.

**Hieronder vind je een lijst met enkele pseudo-klassen en gebeurtenissen die statusveranderingen in je elementen kunnen veroorzaken:**

* `:hover`: wordt afgevuurd als de cursor zich boven het element bevindt.
* `:focus`: wordt afgevuurd als het element gefocust is.
* `:focus-within`: wordt afgevuurd als het element of een van zijn afstammelingen gefocust is.
* `:target`: wordt afgevuurd wanneer het huidige URL-fragment overeenkomt met de id van het element.
* `:active`: wordt afgevuurd wanneer het element wordt geactiveerd (meestal wanneer er op het element wordt gedrukt).
* **klassewijziging van JavaScript**: wanneer de CSS-klasse van een element verandert via JavaScript, zal CSS de in aanmerking komende eigenschappen die zijn gewijzigd gradueel aanpassen.
