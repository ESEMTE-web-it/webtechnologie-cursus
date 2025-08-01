# media queries

## definitie

Websites kunnen tegenwoordig bekeken worden op smart-phones, tablets, pc of op een breedbeeld scherm. CSS heeft hiervoor media queries waarmee **op basis van de breedte van een scherm aparte CSS geschreven kan worden**.

Een media query is een stuk CSS-code in de stylesheet van een website, die informatie zoals de grootte van het browserscherm van de bezoeker opvraagt tijdens het laden van jouw website. Op basis van opgevraagde informatie worden specifieke CSS-stijlregels weergegeven voor een welbepaalde schermgrootte of **viewport**.

{% embed url="https://ap.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=1e1407b1-8ac1-4d5c-82b5-ac680130c711" %}

## syntax

```css
@media media-type and (media-feature-rule) {
   / * CSS-regels komen hier * /
}
```

* **media-type** vertelt de browser voor wat voor soort media deze code bestemd is (bijv. print of screen)
* **media-expressie**, een regel of een voorwaarde waaraan voldaan moet zijn, vooraleer de opgegeven CSS kan worden toegepast
* **CSS-regels** worden toegepast als aan de voorwaarde voldaan wordt en het media-type correct is

## media-types

```css
/* Als de pagina wordt afgedrukt heeft de body een lettergrootte van 12pt . 
Het is niet van toepassing wanneer de pagina in een browser geladen wordt. */
@media print {
    body {
        font-size: 12pt;
    }
}
```

* **all**
* **print**
* **screen**
* **speech**

## **media-kenmerken**

Nadat het media-type werd opgegeven, kan een stijlregel opgesteld worden voor het opgegeven media-kenmerk, veelal de breedte en de hoogte van het opgegeven media-type.

De functie die het vaakst gebruikt wordt om responsieve ontwerpen te maken (en mét brede browser-ondersteuning) is de **breedte van de viewport** door middel van `min-width`, `max-width` en `width` media-kenmerken.

### mobile first design

```css
/* stijlregels voor alle schermen kleiner dan 320px breed */
@media only screen and (min-width: 320px) {
    /* stijlregels voor browserschermen > 320px en < 720px */
}

@media only screen and (min-width: 720px) {
    /* stijlregels voor browserschermen > 720px en < 1024px */
}

@media only screen and (min-width:1024px) {
    /* stijlregels voor browserschermen ≥ 1024px */
}
```

### desktop first design

```css
/* stijlregels voor schermen groter dan 1024px breed */
@media only screen and (max-width: 1024px) {
    /* stijlregels voor schermen > 720px en ≤ 1024px breed */
}

@media only screen and (max-width: 720px) {
    /* stijlregels voor schermen > 320px en ≤ 720px breed */
}

@media only screen and (max-width:320px) {
    /* stijlregels voor schermen ≤ 320px breed */
}
```

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6ARtyQXlwbcuU2GsANYBzAE7cAVzokAFoeKG5fVGV4BjoAbhdlcMjomygPT0S6AF9tbQB6ACplcTplMFhfCAg6MBisBnhlBmrlAE52gCYABwAPZQB3MiQIZUjlSjBCBrH3Lz9A4OTuCN9lMnr0gLGigu0AAWYkMgYKqpryuKRlAApcBj6Q4aR4LGjO3r6ASickuwcf3KrjcmUWQVCKSibigO2yIJWa2igywZEQ8OUeVy+ToxVK5Uq1Vq9TeTRabQAbAAGKn9IYjMYTKYzN5zMH+CGIiabcZQMgAN12+zoR2Qp3ORKuy3uj2eIze0WptJ+QNcAMczmBavZS0hq1SvIFEAxrihyNR6KSWKxggK5isEFMBUMxlM6v02l0AEZ1AAlCBgMgALzGrLc-kGkHWw2C3EGMW4FRqs2UEBIJDg8GEtqwPs9PXUACFHKMSAwAlB4CzDKCFhzllDxiQU0huLAAsw+Bt6poQLE6L2MMoAJLNsOEy4VYNjHmfOlMgPTFON4ZQKDJRp0byhxO97YQQcj5to7vKJXz9bMjbNVfr2Cb7cJ5S91ZGwe2gs423uz3OvAaHFtE4SAYAQMheCodAAGYAFZUCpEAckIegmBYdAMAAKyoYgeD4Wp4FYRDkJARhmFYDBYDAbCuF4fgCPQRCAF0ciAA %}

### breakpoints en media-queries

![](../../../.gitbook/assets/css-mediaqueries-1.png)

## voorbeelden

### media-queries en font-size

{% embed url="https://codepen.io/APwebtechnologie/pen/yLJZPbO" %}

### media-queries en background-color

{% embed url="https://codepen.io/APwebtechnologie/pen/PozVOJg" %}

### media-queries en flexbox

{% embed url="https://codepen.io/APwebtechnologie/pen/LYZqOOm" %}
