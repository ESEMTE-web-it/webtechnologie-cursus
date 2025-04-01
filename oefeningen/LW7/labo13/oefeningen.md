# Oefeningen labo 13

Zorg dat je de volgende folder structuur volgt:

```
webtechnologie/
├─ labo-x/
│  ├─ oefening-01/
│  │  ├─ index.html
│  │  ├─ assets/
│  │  │  ├─ image-1.jpg 
│  │  │  ├─ image-n.jpg 
│  │  ├─ css/
│  │  │  ├─ reset.css
│  │  │  ├─ style.css
│  │  ├─ js/
│  │  │  ├─ script.js
│  ├─ oefening-02/
│  ├─ oefening-n/
├─ labo-y/
├─ labo-z/      
```

- Gebruik steeds JS modules om globale variabelen te vermijden (`<script type="module" src="./path/to/script.js" defer></script>`)
- Zet je Javascript file steeds in strict mode (`"use strict"`);
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)

## oefening 1: hello world!

**leerdoelen**

* een eigen JS-script kunnen uitvoeren in de browser
* console.log gebruiken

**functionele analyse** Het script gaat in de console van de browser de tekst `Hello world!` uitlezen.

**technische analyse** Maak een script.js-bestand aan. Koppel dit bestand aan jouw HTML-pagina (index.html) door middel van het `<script>`-element.

Maak een variabele aan met daarin de tekst "Hello world!".

Gebruik een `console.log`-statement om de inhoud van de variabele uit te lezen in de console van de browser.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h1-oef1.png" alt=""><figcaption></figcaption></figure>

voorbeeldinteractie oefening 1

## oefening 2: teksten uitlezen

**Leerdoelen**

* console.log gebruiken
* string expressies

**functionele analyse** Het programma laat de informatie van de programmeur (jouw eigen informatie) zien in de console.

**technische analyse** Plaats jouw naam, leeftijd, e-mailadres en klasgroep in een variabele.

Gebruik vier `console.log`-statements om de informatie van de programmeur te laten zien in de console.

Tip: Gebruik string-manipulatie om de voorvoegsels (de woorden naam, leeftijd, e-mail en klasgroep) voor de variabele te plaatsen.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h1-oef2.png" alt=""><figcaption></figcaption></figure>

voorbeeldinteractie oefening 2

## oefening 3: getallen uitlezen

**Leerdoelen**

* console.log gebruiken
* getallen gebruiken

**functionele analyse** Het programma laat de berekende leeftijd van de programmeur (jouw eigen informatie) zien in de console.

**technische analyse** Plaats jouw **geboortejaar** in een variabele.

Bereken jouw leeftijd o.b.v. het jaartal van dit jaar en de inhoud van de variabele.

Lees enkel het resulaat uit met 1 `console.log`-statement.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h1-oef3.png" alt=""><figcaption></figcaption></figure>

voorbeeldinteractie oefening 3: getallen krijgen een kleur in de console

## oefening 4: bmi berekenen

**leerdoelen**

* werken met variabelen
* expressies toevoegen
* console.log gebruiken

**functionele analyse** BMI berekenen aan de hand van hoogte en gewicht

**technische analyse** Maak een variabele `myWeight` en `myLength` waar je het gewicht in kg en de lengte in meter bijhoudt. Maak vervolgens een variabele `myBmi` die de bmi op de volgende manier berekend:

![](../../../.gitbook/assets/bmi-formula.png)

Je kan een getal afronden door [Number.toFixed()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number/toFixed) te gebruiken (bv. result.toFixed(2)).

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef1.png" alt=""><figcaption></figcaption></figure>

voorbeeldinteractie oefening 1: BMI tonen

## oefening 5: bmi-namen

**leerdoelen**

* variabelen
* expressies
* string expressies
* console.log

**functionele analyse** BMI berekenen aan de hand van hoogte en gewicht voor twee personen

**technische analyse** Pas de oefening aan over bmi zodat er een gewicht en een lengte variabele bestaat voor twee verschillende personen. Maak ook een variabele aan die de naam van de persoon bevat.

Toon de naam van de persoon met zijn bij behorende bmi op het scherm.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef2.png" alt=""><figcaption></figcaption></figure>

voorbeeldinteractie oefening 2: meerdere BMI's tonen

## oefening 6: bmi-namen uitbreiding

**leerdoelen**

* `Number.toFixed()` gebruiken

**functionele analyse** Het programma rond het BMI af tot een geheel getal

**technische analyse** Kopieer jouw oplossing van de vorige oefening.

Zorg ervoor dat de BMI deze keer afgrond is door `Number.toFixed()` te gebruiken.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef3.png" alt=""><figcaption>voorbeeldinteractie oefening 3: afgeronde BMI's tonen</figcaption></figure>

## oefening 7: interest

**leerdoelen**

* string-interpolatie
* machtsverheffing

**functionele analyse** Je programma toont hoe veel je huidig bezit waard zal zijn over een vast aantal jaar, indien je een vaste rentevoet toepast.

**technische analyse** In je programma hou je je startbezit bij, de rentevoet en het aantal jaren. Je mag deze getallen in je code zetten.

De rentevoet bepaalt met welke hoeveelheid je bezit op een jaar stijgt. Bijvoorbeeld, als je rentevoet 2% is en je startbedrag is 100 euro:

* na één jaar bezit je 102 euro (er is 2% van 100 bij gekomen)
* na twee jaar bezit je 104,04 euro (er is 2% van 102 bij gekomen)
* enzovoort

Rond het eindbedrag af naar een geheel getal.



{% hint style="info" %}
Eind saldo = Inleg \* ( 1 + rente)^looptijd
{% endhint %}



**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef4.png" alt=""><figcaption>voorbeeldinteractie oefening 4: interest berekenen</figcaption></figure>

## oefening 8: uren

**leerdoelen**

* gebruik maken van modulo

**functionele analyse** Je programma werkt als de kleine wijzer van een klok.

**technische analyse** In je programma maak je twee variabelen: één voor het huidige uur, één voor het aantal uur dat je hierbij wil optellen. Je hoeft hierbij de systeemklok niet te raadplegen. Vul gewoon een uur naar keuze in.

Je programma toont dan hoe laat het zal zijn als je de som maakt.

Let op: de klok telt maar 24 uur. Wat doe je als je hierboven gaat?

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef5.png" alt=""><figcaption>voorbeeldinteractie oefening 5: uren berekenen</figcaption></figure>

## oefening 9: wisselgeld

**Leerdoelen**

* const gebruiken
* Math.ceil gebruiken
* expressies
* string-interpolatie

**functionele analyse** Je programma geeft weer hoeveel briefjes van 50 euro je nodig hebt om een bepaald bedrag te kunnen betalen. Het geeft ook weer wat het wisselgeld dan is.

**technische Analyse** Maak een constante `amountToPay` aan dat het te betalen bedrag bevat.

Bereken het aantal briefjes dat nodig is door het te betalen bedrag te delen door 50 en dit naar boven af te ronden. Zet het resultaat in een nieuwe constante `amountOf50s`.

{% hint style="info" %}
Zoek even op het internet op hoe je getallen naar boven en naar beneden afrondt!
{% endhint %}

Bereken het wisselgeld en plaats het in een 3de constante `change`.

Print deze waarden af gebruikmakende van string concatinatie of string interpolatie.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef6.png" alt=""><figcaption>voorbeeldinteractie oefening 6: wisselgeld berekenen</figcaption></figure>


## oefening 10: lotto

**leerdoelen**

* functionaliteit van strings (substring, replaceAll)

**functionele analyse** Haal de lotto getallen uit een tekst en geef ze op een overzichtelijke manier weer (gescheiden door een pipe-symbool |).

```javascript
let text =
  "De winnende lottonummers van deze week: 05,09,13,18,27,44. Proficiat aan alle deelnemers.";
```

**technische analyse**  Haal alle lottonummers uit bovenstaande tekst en zet ze in de varabele `lottoNumbers`.

Vervang de komma's door het pipe-symbool | en zet deze output in de variabele `formattedLottoNumbers`. Log vervolgens deze variabele.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/Screenshot 2024-11-08 at 16.29.53.png" alt=""><figcaption>voorbeeldinteractie oefening 10: lotto</figcaption></figure>

## oefening 11: name-from-mail

**leerdoelen**

* functionaliteit van strings (substring, indexOf, replace, toUpperCase)
* string-interpolatie

**Functionele analyse** Het programma toont het gedeelte van de e-mailadres dat de naam voorstelt.

**technische analyse** Het e-mailadres kan je in een variabele `email` plaatsen.

We veronderstellen dat de variabele een juist e-mailadres bevat. Het e-mailadres zal zich altijd in het ap.be domein bevinden.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef8.png" alt=""><figcaption>voorbeeldinteractie oefening 8: e-mailadres</figcaption></figure>

## oefening 12: short-name

**leerdoelen**

* functionaliteit van strings (indexOf, replace)
* string-interpolatie

**functionele analyse** Je programma toont je voor en achternaam. Je voornaam moet afgekapt worden zodat enkel de eerste letter zichtbaar is. Achter deze letter moet een punt komen.

Voor en achternaam moeten getoond met in het begin een hoofdletter.

**technische analyse** Je voorziet twee variabelen voor voor- en achternaam. Daarna zorg je ervoor dat je enkel de eerste letter van de voornaam zichtbaar is.

Let er op dat de variabelen ook zonder hoofdletters kunnen ingegeven worden.

Je kan deze string opbouwen aan de hand van string interpolatie.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef9.png" alt=""><figcaption>voorbeeldinteractie oefening 9: naam</figcaption></figure>

## oefening 13: color-blind

**leerdoelen**

* functionaliteit van strings (replace)
* string-interpolatie

**functionele analyse** Je programma moet een tekst aanpassen wetende dat de schrijver van deze tekst een bepaalde vorm van kleuren blindheid heeft.

**technische analyse** De tekst waarvan de kleuren fout zijn kan je in een variabele `colorBlindText` plaatsen. Deze tekst is altijd lowercase.

De volgende kleuren worden foutief geschreven:

* blue -> red
* yellow -> green

Gelukkig wordt de fout maar in 1 richting gemaakt. De kleuren `red` en `yellow` worden wel correct aanzien.

Je mag er vanuit gaan dat elke kleur maar 1 keer voorkomt in de tekst.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef10.png" alt=""><figcaption>voorbeeldinteractie oefening 10: colorblind</figcaption></figure>

## oefening 14: text-box

**leerdoelen**

* functionaliteit strings (replace)
* escapen van bepaalde karakters

**functionele analyse** Je programma toont een stuk tekst in je console in een tekstvak

**technische analyse** Je plaatst het stuk tekst in een variabele genaamd `text`.

Maak met de karakters \ / - en \_ een tekstvak.

Het stuk tekst moet altijd in het tekstvak passen. Je kan de lengte opvragen van de variabele tekst en er voor zorgen dat de - en \_ karakters herhaald worden.

Zorg ervoor dat je maar 1 console.log statement gebruikt. Je zal dus moeten gebruik maken van newlines.

**voorbeeldinteractie**

<figure><img src="../../../.gitbook/assets/js-h2-oef11.png" alt=""><figcaption>voorbeeldinteractie oefening 11: text-box</figcaption></figure>

## oefening 15 (extra): color-blind

**leerdoelen**

* functionaliteit strings (replace, meerdere keren replace)
* escapen van karakters

**functionele analyse** De color-blind applicatie dient uitgebreid te worden zodat de foutieve kleur meerdere keren kan vervangen worden. De fout wordt nu wel ook in omgekeerde richting gemaakt.

**technische analyse** We kunnen de applicatie van color-blind overnemen en uitbreiden. We moeten er nu voor zorgen dat de kleuren meerdere keren worden vervangen.

De volgende kleuren worden foutief geschreven:

* blue -> red
* yellow -> green maar ook:
* red -> blue
* green -> yellow

Om te voorkomen dat een bepaalde kleur die al omgezet werd terug wordt omgezet naar het origineel vervangen we de kleur met de kleur in hoofdletters.

**voorbeeldinteractie**

```
roses are blue, violets are red, strawberries are blue and we always define variables with let
=
roses are red, violets are blue, strawberries are red and we always define variables with let.
```

## Oefening 16 (extra) - Caesar rotation

**leerdoelen**

* functionaliteit strings (replace, meerdere keren replace)

**functionele analyse** We willen een programma maken dat geheimschrift decodeert dat gemaakt is aan de hand van de de Caesar-rotatie (rot13). De tekst is in **lowercase**.

**technische analyse** Je voorziet een variabele voor de inputString. Je zorgt dat de vertaling gebeurd volgens het volgende schema. Wij gebruiken hier wel alleen kleine letters.

<figure><img src="../../../.gitbook/assets/rot13.webp" alt=""><figcaption></figcaption></figure>

Caesar-rotation

<figure><img src="../../../.gitbook/assets/oefeningen/resultaten/labo13/oef-14.png" alt=""><figcaption>
voorbeeldinteractie oefening 14: Caesar-rotation
</figcaption></figure>
