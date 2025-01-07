# oefening

{% hint style="warning" %}
Deze oefening wordt behandeld tijdens LW3 (HTML & CSS): Labo 05
{% endhint %}

{% embed url="https://www.loom.com/share/8aec678096cd4aab80a2de0f7ec729e9" %}

**bijlagen**:

{% file src="../../../.gitbook/assets/labo-05-teksten.txt" %}

{% file src="../../../.gitbook/assets/assets.zip" %}

**instructies**

Maak een HTML-structuur voor de `index.html`. Gebruik hierbij volgende HTML5 layout-elementen:&#x20;

* header
* nav
* main
* aside
* footer

#### header

* De header toont het AP-logo (200px breed).
* De afbeelding heeft een id “logo”.
* Op het logo staat een link naar de home-pagina.

#### Nav

* “home” linkt naar de index-pagina en heeft een class=“active”
* "contact” linkt naar “#”

#### Main

Main bestaat uit 2 sections en een quote:

1. De eerste section heeft een class intro, een titel, een paragraaf en een afbeelding.
2. De tweede section heeft een class info en toont de volgende elementen:
   * een afbeelding (breedte 350px) ,
   * 5 ondertitels,
   * paragrafen,
   * een lijst.

#### Aside

Aside bestaat uit:

* een ondertitel
* een paragraaf
* een ondertitel
* socials iconen met links (30px x 30px)
* een link (https://www.ap.be/ik-schrijf-me-in) met class “button”

#### Footer

Footer bestaat uit een paragraaf, waarbij&#x20;

* het eerste deel linkt naar de ap.be
* het tweede deel linkt naar het logo

#### CSS (algemeen)

De index.html laadt eerst reset.css in. Nadien volgt de eigen css/style.css.

Zowel html als body hebben standaard

* border-box
* een witte achtergrond
* een lettertype Arial of Helvetica
* hoogte & breedte = hoogte & breedte van het scherm

De body bestaat uit grid-template areas:&#x20;

* header
* nav
* main (2/3) & aside (1/3)
* footer

#### CSS (titels en tekst)

Alle titels

* staan in hoofdletters,
* zijn links uitgelijnd
* en de letters staan 0.2rem uit elkaar.
* h1 is 2rem groot en heeft onder een padding van 2rem
* h2 is 1.2rem groot, heeft boven een padding van 2rem, onder 1 rem
* h3 is 1rem groot
* De h2 in aside is 0.8rem groot, de letters staan 0.2rem uit elkaar en hebben een kleur van #7d7d7d.

De tekst van de paragrafen hebben volgende eigenschappen:&#x20;

* 1 rem groot
* een interlinie van 1.5rem
* een padding onder van 1rem
* een kleur van #232226&#x20;
* en links uitgelijnd

#### CSS (Header)

* De header heeft bovenaan een marge van 2rem.&#x20;
* Het logo wordt als “blok” geplaatst in het midden (tip: gebruik hiervoor margin)

#### CSS (Nav)

* In de navigatie worden de onderdelen “inline” geplaatst.&#x20;
* Boven en onder is er een padding van 2rem,&#x20;
* en een marge zowel links als rechts van 2 rem, en onder 1rem.&#x20;
* De lijn heeft een kleur #7d7d7d en is 1px dik.
* De menu heeft een fontgrootte van 0.8rem, letters staan 0.2rem uit elkaar en hebben een kleur #7d7d7d.
* De onderdelen van de menu hebben boven een marge van 4rem, en rechts 1rem.

Als er met de muis over het menu gegaan wordt, of als de link actief is&#x20;

* gaan de letters 0.25rem uit elkaar staan
* wordt de tekst vet
* en kleur deze #e60005&#x20;

#### CSS (main en verder)

Probeer vanaf nu zelf goed te kijken naar de screenshot in bijlage en tracht zo goed mogelijk de overige elementen op de pagina te stijlen. Hieronder volgen nog enkele tips:

* De eerste foto is 100% breed, de tweede 50%.
* De oranje achtergrondkleur is #f59c00.
* De kleur van de tekst is #232226.
* De grijze achtergrondkleur (quote) is #efefef.
* De border-radius van “inschrijven” is 5px.
