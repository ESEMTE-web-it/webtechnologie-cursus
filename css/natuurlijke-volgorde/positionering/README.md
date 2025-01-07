# positionering

## positionering

HTML elementen worden in hun natuurlijke volgorde geplaatst waarbij alleen rekening wordt gehouden met het feit of de elementen blok- of inline elementen zijn. Je kan de HTML elementen uit hun natuurlijke flow halen door ze expliciet te positioneren. Je moet dus weten hoe je elementen precies plaatst. Met de `position` eigenschap bepaal je het type van de methode omtrent positionering die je voor een element wilt gebruiken.

### position: static;

Voor alle elementen in HTML is het `position` attribuut standaard ingesteld op `static`. Dit betekent dat de elementen weergegeven worden in de volgorde waarin ze geplaatst zijn in het HTML element.

### position: relative;

Met `position: relative` wordt een element gepositioneerd ten opzichte van zijn static positie. Dat doe je bijvoorbeeld door een top, left, right en/of een bottom waarde toe te kennen aan het element. De instelling `position: relative;` maakt het dus mogelijk om een element te positioneren ten opzichte van de `position: static;` die dit element standaard heeft.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_position\_relative](https://www.w3schools.com/css/tryit.asp?filename=trycss_position_relative)

### position: absolute;

Bij het absoluut positioneren van een element moet je twee concepten onthouden:

1.  **ouder-kind relaties**:

    In HTML is elk element een op z'n minst een kind-element van het HTML element. Het HTML-element omsluit alle andere elementen, en is daardoor het ouder-element van alle andere HTML-elementen. Op een meer technische manier zeggen we dat alle andere elementen genest zijn in het HTML-element en dus kinderen van het HTML-element zijn. Een kind-element is dus genest in een ouder-element, en een ouder-elementen is ouder van alle elementen die er in genest zijn.
2.  **het absoluut positioneren van een element gebeurd ten opzichte van het eerste gepositioneerde ouder-element**:

    Nu weet je wat ouder- en kind-elementen zijn, is het absoluut positioneren ten opzichte van het eerste gepositioneerde ouder-element, gemakkelijker te begrijpen. Een absoluut gepositioneerd element is gepositioneerd ten opzichte van het eerst gepositioneerde ouder-element. Dit betekent dat een element dat je absoluut positioneert door alle ouder-elementen loopt totdat het het eerste, namelijk een `html` element tegenkomt, of een elementen waarvan het `position` attribuut is ingesteld op `relative` of `absolute`. Op dat element baseert het te positioneren element zijn positie.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_position\_absolute](https://www.w3schools.com/css/tryit.asp?filename=trycss_position_absolute)

### position: fixed;

Door gebruik te maken van `position: fixed;` kunnen we een HTML-element positioneren t.o.v. de 'viewport'. Dit is de beschikbare ruimte op het scherm waarin de website getoond wordt. Dit betekent ook dat het element zich niet zal verplaatsen, zelfs als zou de gebruiker door de pagina gaan scrollen.

De plaatsing doen we met behulp van de top, right, bottom en/of left eigenschappen.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_position\_fixed](https://www.w3schools.com/css/tryit.asp?filename=trycss_position_fixed)

### position: sticky;

`position: sticky;` is een combinatie van `position: relative;` en `position: fixed;`. Tijdens het scrollen wordt de positie aangepast op basis van een voorgeplaatste afstand tot opzichte van de viewport.

```css
div.sticky {
  position: sticky;
  top: 0;
}
```

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_position\_sticky](https://www.w3schools.com/css/tryit.asp?filename=trycss_position_sticky)

## overlappende elementen

Wanneer je gebruik maakt van relative, fixed, or absolute positionering kunnen kaders gaan overlappen. Wanneer dit gebeurd, gaan de HTML-elementen die pas later in de natuurlijke volgorde volgen, bovenaan komen.

Wanneer we dit gedrag willen manipuleren, maken we gebruik van de `z-index` eigenschap. Deze eigenschap manipuleert de volgorde waarin HTML-elementen boven en onder elkaar liggen.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_zindex](https://www.w3schools.com/css/tryit.asp?filename=trycss_zindex)

## zwevende elementen

De box van een zwevend element wordt langs de linker- of rechterrand van het moederelement geplaatst en de kaders van andere elementen ervoor of erna kunnen hun plek ernaast krijgen.

Met behulp van de float eigenschap in CSS kunnen alle elementen zwevend gemaakt worden. Je moet wel de breedte van het element expliciet vast leggen met de width eigenschap. Een element met de `float` eigenschap ingesteld op de waarden `left` of `right`, wordt een element op blokniveau. Een eventueel gebruikte `display` eigenschap wordt genegeerd.

De box van een zwevend element wordt compleet weergegeven, inclusief `padding`, `border` en `margin`. De `margin` van een zwevend element en aangrenzende elementen schuiven niet in elkaar.

Om de kader van twee elementen op blokniveau naast elkaar te plaatsen, moet je voor beide elementen de `float` eigenschap instellen. Je kan eventueel de `margin-left` eigenschap gebruiken om wat witruimte tussen de twee boxen te creëren.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_layout\_float](https://www.w3schools.com/css/tryit.asp?filename=trycss_layout_float)

### stoppen met zweven

Neem aan dat je alleen een titel rechts wil laten zweven van een foto. Er is plaats genoeg naast de foto om de titel en enkele paragrafen ernaast te laten zweven. Dus moet je die standaard mogelijkheid blokkeren door aan de eerste paragraaf na de titel de eigenschap `clear: left;` toe te kennen.

Stoppen met zweven kan zowel links, rechts als aan beide zijden.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_layout\_clear](https://www.w3schools.com/css/tryit.asp?filename=trycss_layout_clear)

{% hint style="info" %}
Met de komst van HTML5 positioneringsmethoden wordt het gebruik van `float` afgeraden.
{% endhint %}

## display

Met de `display` eigenschap kunnen we een HTML-element van gedrag doen veranderen. We kunnen ze kiezen of een element zich al `block-` of als `inline` element gedraagt. Er is ook nog de optie om zich als een `inline-block` te gedragen.

Een inline-block element zal zich net als block elementen gedragen als een vierhoek die op je scherm komt te staan. Wel is het mogelijk voor 2 inline-block elementen om naast elkaar (=inline) te verschijnen.

Met `display: none;` kan je een element uit de natuurlijke flow halen en verbergen voor de gebruikers van de website.

try it yourself: [https://www.w3schools.com/cssref/tryit.asp?filename=trycss\_display](https://www.w3schools.com/cssref/tryit.asp?filename=trycss_display)
