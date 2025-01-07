---
description: >-
  Animatie is een geweldige manier om interactieve elementen te benadrukken. In
  dit hoofdstuk leer je hoe je animatie-effecten kunt toevoegen en beheren met
  CSS.
---

# 6: animaties

CSS-animaties maken het mogelijk om overgangen van de ene CSS-stijlconfiguratie naar de andere te animeren. CSS-animaties zijn als CSS-transities maar krachtiger. Animaties bestaan uit twee componenten:

* Een set **keyframes** die de begin- en eindstatus van de animatie aangeven, evenals mogelijke tussenstops;
* Een CSS eigenschap **animation** die de CSS-animatie beschrijft;

## keyframes

In animatie software, CSS en de vele andere tools waarmee je iets kan animeren, zijn **keyframes** het mechanisme dat je gebruikt om een animatie te definiëren.

{% hint style="info" %}
Een keyframe vertegenwoordigdt een specifiek punt op een tijdlijn.
{% endhint %}

Er moet ten minste één keyframe worden gedefinieerd in een CSS-animatie, maar meestal worden er ten minste twee weergegeven. Ze beschrijven het begin en einde van de animatie. Er kunnen aanvullende keyframes worden gedefinieerd om eventuele tussenstappen tussen het begin en het einde van de animatiecyclus te beschrijven.

Keyframes worden gespecificeerd met behulp van de `@keyframes` at-regel. Laten we eens kijken naar de syntaxis van deze at-regel.

```css
@keyframes name-of-animation {
  0% {
    height: 0px;
  }

  50% {
    height: 400px;
  }

  100% {
    height: 300px;
  }
}
```

In het bovenstaande voorbeeld hebben we 3 keyframes gedefinieerd met als waarden 0%, 50% en 100%. Alle drie de keyframes vertegenwoordigen een punt op de tijdlijn.

**Het betekent het volgende:**

1. Begin de animatie (0%) met height ingesteld op 0px;
2. Animeer height naar 400px terwijl de animatie doorgaat tot het midden van de animatie duur (50%);
3. Animeer height naar 300px terwijl de animatie doorgaat tot het einde van de animatie duur (100%) ;

Je kan een willekeurig aantal punten toevoegen aan de `@keyframes` at-regel.

```css
@keyframes name-of-animation {
  0% {
    height: 0px;
  }

  25% {
    height: 200px;
  }

  50%, {
    height: 300px;
  }

  75% {
    height: 100px;
  }

  100% {
    height: 400px;
  }
}
```

{% hint style="info" %}
**Elk punt dat je toevoegt, moet een procentuele (%) waarde zijn.**

Er zijn hier twee uitzondering op namelijk "`from`" en "`to`". Binnen de `@keyframes` at-regel zijn `from` en `to` trefwoorden die 0% en 100% vertegenwoordigen, het begin en het einde van de animatie.
{% endhint %}

```css
@keyframes name-of-animation {
  from {
    height: 0px;
  }

  to {
    height: 300px;
  }
}
```

## animatie eigenschappen

Als je de `@keyframes` wilt gebruiken, moet je verschillende animatie-eigenschappen definiëren of gebruik maken van de `animation` short-hand notatie.

**animation-duration**

De eigenschap `animation-duration` definieert hoe lang de animatie duurt. Het moet een tijdswaarde zijn, hoe groter de tijdswaarde, hoe groter de lengte van de`@keyframes`-tijdlijn.

{% hint style="info" %}
De standaardwaarde is 0 seconden. Je kan geen negatieve tijdwaarden toevoegen.
{% endhint %}

```css
.animation-element {
    animation-duration: 10s;
}
```

**animation-timing-function**

Om natuurlijke bewegingen in animaties na te bootsen, kan je de `animation-timing-function` gebruiken.&#x20;

**Er zijn verschillende waarden beschikbaar als presets in CSS:**

* `linear`
* `ease`
* `ease-in`
* `ease-out`
* `ease-in-out`

```css
.animation-element {
    animation-timing-function: ease-in-out;
}
```

{% hint style="info" %}
Indien de `animation-timing-function` niet wordt ingevuld, wordt de standaardwaarde `ease` gebruikt.
{% endhint %}

{% embed url="https://codepen.io/ykdenis/pen/zYaarwW" %}

**animation-iteration-count**

De eigenschap `animation-iteration-count` definieert hoe vaak de `@keyframes`-tijdlijn moet worden uitgevoerd. Standaard is dit 1, wat betekent dat wanneer de animatie het einde van je tijdlijn bereikt, deze aan het einde stopt. Het getal kan geen negatief getal zijn.

{% embed url="https://codepen.io/ykdenis/pen/VwddedJ" %}

{% hint style="info" %}
Met de waarde `infinite` wordt je animatie oneindig keer herhaald.
{% endhint %}

```css
.animation-element {
    animation-iteration-count: infinite;
}
```

**animation-direction**

Met `animation-direction` kan je instellen in welke richting de tijdlijn over je `keyframes` loopt:

* `normal`: de standaardwaarde, die vooruit is;
* `reverse`: loopt achteruit over je tijdlijn;
* `alternate`: voor elke animatie-iteratie loopt de tijdlijn achtereenvolgens vooruit of achteruit;
* `alternerend-reverse`: combinatie van `reverse` en `alternate`;

```css
.animation-element {
    animation-direction: reverse;
}
```

{% embed url="https://codepen.io/ykdenis/pen/zYaaqvb?editors=1111" %}

**animation-delay**

De eigenschap `animation-delay` bepaalt hoe lang de start van de animatie moet worden uitgesteld. Net als de eigenschap `animation-duration` accepteert deze een tijdswaarde.

{% hint style="info" %}
In tegenstelling tot de eigenschap `animation-duration` kan je het een negatieve waarde geven. Als je een negatieve waarde instelt, begint de tijdlijn in je `@keyframes` op dat punt. Als je animatie bijvoorbeeld 10 seconden lang is en je `animation-delay` instelt op -5s, begint deze halverwege je tijdlijn.
{% endhint %}

{% embed url="https://codepen.io/ykdenis/pen/ZERRWoZ" %}

**animation-play-state**

Met de eigenschap `animation-play-state` kan je de animatie afspelen en pauzeren. De standaardwaarde is `active` en als je deze instelt op `paused`, wordt de animatie gepauzeerd.

```css
.animation-element {
    animation-play-state: paused;
}
```

**animation-fill-mode**

De eigenschap `animation-fill-mode` definieert welke waarden in je `@keyframes`-tijdlijn blijven bestaan voordat de animatie start of nadat deze is afgelopen. De standaardwaarde is `none`, wat betekent dat wanneer de animatie is voltooid, de waarden in je tijdlijn worden weggegooid.

**andere opties zijn:**

* `forwards`: de waarden beschreven in de laatste keyframe worden behouden, op basis van de richting van de animatie;
* `backwards`: de waarden beschreven in de eerste keyframe worden behouden, op basis van de richting van de animatie;
* `both`: volgt de regels voor zowel `backwards` als `forwards`;

{% embed url="https://codepen.io/ykdenis/pen/GRGGZPO" %}

## animation short-hand notatie

In plaats van alle eigenschappen afzonderlijk te definiëren, kan je ze definiëren met behulp van één eigenschap namelijk `animation`. Hiermee kan je de animatie-eigenschappen in de volgende volgorde kan definiëren:

1. `animation-name`
2. `animation-duration`
3. `animation-timing-function`
4. `animation-delay`
5. `animation-iteration-count`
6. `animation-direction`
7. `animation-fill-mode`
8. `animation-play-state`

```css
.animation-element {
	animation: animation-name 5s ease 1s infinite normal forwards running;
}
```

## animatie voorbeelden

{% embed url="https://codepen.io/ykdenis/pen/ZERRpbK" %}

{% embed url="https://codepen.io/ykdenis/pen/dyKKXVJ" %}
