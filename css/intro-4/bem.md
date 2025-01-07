# BEM-notatie

{% embed url="https://youtu.be/er1JEDuPbZQ" %}

## definitie BEM

De **Block, Element, Modifier**-methodologie, of kortweg **BEM,** is een populaire naamgevingsconventie voor klassen in HTML en CSS. Het heeft tot doel ontwikkelaars te helpen de relatie tussen HTML en CSS in een bepaald project beter te begrijpen. BEM heeft dus een reeks regels die helpen bij het begrijpen én onderhouden van CSS.

In onderstaand voorbeeld wordt getoond hoe een CSS-ontwikkelaar in de BEM-stijl zou kunnen schrijven:

```css
/* block component is hier 'de parent'*/
.btn {}

/* een element dat afhakelijk is van een block */ 
.btn__price {}

/* aanpassing die de stijl van de blok verandert */
.btn--red {} 
.btn--small {}
```

Een blok is hier een abstractie op het hoogste niveau van een nieuwe component, bijvoorbeeld een knop:`.btn {}`. Dit blok moet gezien worden als een parent.\
Onderliggende items of elementen kunnen erin worden geplaatst en deze worden aangegeven door twee onderstrepingstekens \_\_**\_\_** achter de naam van het blok, zoals `.btn__price {}`.\
Ten slotte kunnen modificatoren het blok manipuleren en aanpassen, zodat we van dat specifieke onderdeel de stijl kunnen aanpassen zonder wijzigingen aan te brengen aan een volledig niet-gerelateerde module. Dit wordt gedaan door twee koppeltekens **--** aan de naam van het blok toe te voegen, net als `.btn--red{}`.

Code zou er zo kunnen uitzien met bovenstaande in het achterhoofd:

```markup
<a class="btn btn--small btn--red" href="https://www.ap.be/">
  <span class="btn__price">12€</span>
  <span class="btn__text">Lid worden</span>
</a>
```

Als een andere ontwikkelaar deze opmaak zou geschreven hebben en CSS zou een onbekende zijn, dan nog is het vrij duidelijk welke klassen waarvoor verantwoordelijk zijn en hoe ze van elkaar afhankelijk zijn. Ontwikkelaars kunnen vervolgens hun eigen componenten bouwen en het bestaande blok naar hartenlust aanpassen. Op deze manier zijn ontwikkelaars zonder veel CSS te schrijven mogelijk in staat om veel verschillende combinaties van knoppen te maken door simpelweg een klasse in de opmaak te wijzigen:

[link naar een BEM-voorbeeld](https://codepen.io/team/css-tricks/pen/226a65c8f7d64615aabd45048d1d3b6d)

## waarom BEM?

* Als een nieuwe stijl van een component gemaakt moet worden, kan makkelijk gezien worden welke modifiers en children er al bestaan. Het lijkt alsof er initieel geen CSS geschreven hoeft te worden, omdat er een reeds bestaande modifier is die doet wat nodig is.
* Als de markup gelezen wordt, is al snel duidelijk welk element afhankelijk is van een ander (in het vorige voorbeeld kan je zien dat `.btn__price` afhankelijk is van `.btn`)
* Ontwerpers en ontwikkelaars kunnen componenten consequent benoemen om de communicatie tussen teamleden te vergemakkelijken, aangezien BEM snel klaarheid en duidelijkheid brengt vanwege de syntax.

Door te werken met BEM geeft het ontwikkelaars zeker een standaard waarop in de toekomst betere en **beter te onderhouden code** kan geschreven worden. Een tweede aspect is dat **alles in BEM een klasse is en waarbij dus niets genest is**. Dat maakt CSS-specificiteit erg toegankelijk, wat een goed idee is.

## problemen met CSS?

Een CSS-selector wordt als volgt geschreven, maar voldoet niet aan de BEM-regels:

```css
.nav .nav__listItem .btn--orange {
  background-color: red;
}
```

In dit voorbeeld staan geneste selectoren en de modifier beschrijft niet echt wat er eigenlijk aan de hand is. Een blok zoals hier `.nav` overschrijft de stijlen van een ander blok of andere modifier zoals hier `.btn - oranje` wat binnen BEM niet mag. Anders wordt het bijna onmogelijk om de HTML te lezen en te begrijpen wat deze component echt doet. Zoiets als bovenstaande code schrijven zou ook de wenkbrauwen fronsen bij andere collega-ontwikkelaars.

Hetzelfde geldt voor HTML: wat te denken bij het zien van volgende opmaak?

```markup
<a class="btn" href="https://www.ap.be/">
  <div class="nav__listItem">item een</div>
  <div class="nav__listItem">item twee</div>
</a>
```

In bovenstaand voorbeeld werd waarschijnlijk een element binnen een volledig niet-gerelateerd blok code geplaatst, omdat de ontwikkelaar die code op dat moment net daar nodig had. De onderliggende elementen verwijzen naar een class `.nav` terwijl de parent een class `.btn` is (button). Dit kan niet binnen BEM en moet ten alle tijde vermeden worden. Kort samengevat:

* Nooit modifiers in een niet-gerelateerd blok overschrijven.
* Vermijd het maken van onnodige parent-elementen, als het child-element op zichzelf kan bestaan.

## voorbeelden BEM

**oefening** van [een BEM-accordion](https://codepen.io/team/css-tricks/pen/EaJEBZ) met

* één blok `.accordion`
* twee elementen `.accordion__title` en `.accordion__copy`
* één modifier `.accordion__copy--open`

**oefening** van [een BEM-navigatie](https://codepen.io/team/css-tricks/pen/RNOMzJ) met

* één blok `.menu`
* 6 elementen `.menu__trigger` `.menu__row` `.menu__list` `.menu__link` `.menu__dropdown` `.menu__col`
* één modifier `.menu__trigger--active`

In het voorbeeld van de BEM-navigatie worden blokken gemaakt zonder modifiers. Een ontwikkelaar kan in de toekomst altijd nieuwe modifiers gebruiken of eraan verbinden), zolang het blok maar consistent blijft.
