# toegankelijkheid

## semantiek

Bij het schrijven van HTML5 wordt er gebruik gemaakt van beschrijvende HTML-elementen:

### koppen: h1-h6

Wat er visueel als een titel (`<h1>` tot `<h6>`) uitziet, moet ook zo gemarkeerd worden. Het is dus fout te denken dat je een groter lettertype en een iets vettere font hetzelfde effect heeft. Kies dus bij een (onder)titel het juiste kopniveau en respecteer de volgorde binnen de kopniveau's.\
Spring dus nooit zomaar van `<h1>` naar `<h3>`, of gebruik niet zomaar een \<h6> voor een kleine tekst.

#### tools?

* web developer toolbar
* outline > outline headings
* aanvinken 'show element names when outlining'

### lijsten: ol & ul

Gebruik geen manuele opsommingstekens of cijfers, maar maak gebruik van `<ol>`, `<ul>` en bijhorende list-items `<li>`. Een lijst met slechts één item is geen lijst.

### tabellen: th & caption

Bij het opmaken van een tabel in HTML dient gebruik gemaakt te worden van `<th>` en `<caption>`. `<th>`-elementen worden gebruikt voor tabelhoofdingen, `<caption>` wordt gebruikt als titel van die tabel. Zowel `<th>` als `<caption>` worden ingelezen voor slechtzienden, waardoor ze direct de nodige info krijgen over de informatie in de tabel.\
`<thead>`, `<tbody>`, `<tfoot>` heeft echter geen toegevoegde waarde voor accessibility (screenreader) binnen HTML5.

### HTML5-lay-out-elementen

Maak zeker gebruik van volgende HTML5-lay-out-elementen:

* `<header>` en `<footer>`
* `<nav>` voor menu (enkel voor hoofdnavigatie): `<ul>` blijven gebruiken, want bij het gebruik van screen readers zal `<ul>` aangeven over hoeveel items het gaat binnen een menu.
* `<main>` voor de hoofdinhoud
* `<article>:` Dit element gebruik je best enkel bij uitneembare blokken.

### formulieren

Bij het gebruiken van formulieren worden instructies bij voorkeur meegegeven, gelinkt aan de velden binnen een formulier. Hieronder enkele tips en tricks:

* identieke waarde in `<label for="">` en `<input id="">`
* `<type=date>` datumnotatie (dd/mm/jjjj)
* `<required>` verplichte velden aanduiden met (\*)
* `<radiobutton>` samen met title
* `<fieldset>` samen met legend (=label voor alle velden in een fieldset)
* velden zonder instructie: gebruik title-attribuut of aria-label (vb. bij items op een schaal)
* `<placeholder>` vervangt label niet (artikel: [placeholder is geen label](https://www.anysurfer.be/nl/blog/detail/placeholder-is-geen-label))
* Geef velden een `autocomplete`-atribuut als er een waarde voor bestaat in de HTML5 specificatie onder [Autofill (ongeveer 50 items)](https://html.spec.whatwg.org/multipage/forms.html#sec-autofill): voor standaardgegevens als naam, adres, e-mail, telefoonnummer ...

```html
<label for="name">Last name</label>
<input autocomplete="family-name" type="text" id="name" name="name" />
```

```html
<label for="country">Country</label>
<input autocomplete="country" type="text" id="country" name="country" />
```

* validatie formulieren
  * spam vermijden zonder captcha (artikel: [captcha en andere anti-spamtechnieken](https://www.anysurfer.be/nl/documentatie/artikels/detail/captcha))
  * Beschrijf de fout tekstueel en zeg bij welk veld de fout werd gemaakt of combineer met kleur of iconen.

### afbeeldingen

Zorg bij afbeeldingen voor een **tekstalternatief**. De inhoud is afhankelijk van het soort afbeelding en de context. Decoratieve afbeeldingen worden best als achtergrondafbeelding in css gezet.\
Indien er afbeeldingen worden ingevoegd met grafische tekst wordt deze tekst best herhaald in het alt-attribuut. Denk maar aan afbeeldingen met tekst bij de solden, dus best tekst in afbeeldingen vermijden.\
Zorg bij **complexe afbeeldingen** zoals een kaart, organogram, diagram of infografiek een beknopte alt-tekst en een volwaardig alternatief.

## ARIA

ARIA of Accessible Rich Internet Applications omvat het toegankelijk en bruikbaar maken van geavanceerde webtoepassingen voor mensen met een handicap, concreet met het toevoegen van aanvullende elementen bij HTML.

artikel van Anysurfer: [Wat is ARIA](https://www.anysurfer.be/nl/documentatie/artikels/detail/wat-is-aria)?\
abstract W3C: [Using ARIA](https://w3c.github.io/using-aria/)

#### tools?

* chrome developer toolbar
* accessibility

### role-attribuut

Een ARIA-role-attribuut kan aan een component worden toegevoegd. Als een component geen impliciete rol heeft, kan het toevoegen van het role-attribuut ondersteunende technologieën instrueren.

In HTML bestaat er geen element voor een tabpanel. De ARIA role="tabpanel" betekent een meerwaarde voor de toegankelijkheid van slechtzienden.

```html
<div id="tab2" role="tabpanel">
```

### slechts 1 rol

Als een component al een impliciete rol had, zal het role-attribuut die dus overschrijven. Een component kan maar 1 rol hebben en ARIA wint!\
**voorbeeld**: Een `<a>`-element met `role="button"` zal bijvoorbeeld behandeld worden als een knop en niet als een link.

Stel dat er naast de hoofdmenu nog een navigatielijst is, dan kan gebruikt gemaakt worden van `role="navigation"`. De `role="navigation"` verandert de rol naar navigatie. De lijst zal dus niet meer als lijst worden aangekondigd.

```html
<ul role="navigation">...
```

Beter is om onderstaande code te schrijven.

```html
<div id="nav" role="navigation"><ul>...
```

Een role-attribuut verandert niets aan het gedrag, eigenschappen of uitzicht van een HTML-element. Enkel een role toevoegen aan een component volstaat dus niet. Er zullen functionaliteiten met JavaScript geprogrammeerd moeten worden.

```html
<div onClick="..." class="iLookLikeAButton" role="button">zoeken</div>
```

Beter is het om onderstaande code te gebruiken, want indien toch liever een HTML-element dan een role.

```html
<button>zoeken</button>
```

meer info: [https://www.w3.org/WAI/ARIA/apg/#button](https://www.w3.org/WAI/ARIA/apg/#button)
