# Opbouw mobiele website met HTML en CSS

In deze deelopdracht ga je mobiele webpagina's bouwen. Zorg ervoor dat je browservenster is ingesteld als een gangbare smartphone en voer de stappen in dit document uit. Volg hierbij altijd de [wireframes](algemeen.md#wireframes). Pas de ontwerpen aan op basis van de styleguide die je hebt geschreven tijdens [deelopdracht 1](deelopdracht-1-concept-content.md).



## Mappenstructuur & bestanden

Maak de volgende mappenstructuur aan:

```
- projectopdracht-webtechnologie-\<je naam\>/
  index.html
  shop.html
  contact.html
  product-naam.html
  - css/
    general.css
    home.css
    normalize.css
    shop.css
    product.css
    contact.css
  - assets/
    - images/
      foto-1.jpg
      foto-2.jpg
      foto-3.jpg
  - js/
 ``` 
Maak de volgende HTML-pagina's aan:

- `index.html`
- `shop.html`
- `product-<naam>.html` (minimaal 6 pagina's)
- `contact.html`

Voorzie 1 CSS-bestand voor de algemene opmaak (`general.css`) en aparte CSS-bestanden voor pagina-specifieke opmaak (`home.css`, `shop.css`, `product.css`, `contact.css`).

Maak ook een `normalize.css` aan, gebaseerd op [modern-normalize.css](https://github.com/sindresorhus/modern-normalize).

Link elke HTML-pagina met de juiste CSS-bestanden. `index.html` zal bijvoorbeeld 3 `<link>`-tags hebben: `normalize.css`, `general.css` en `home.css`.

> **TIP**: Houd de volgorde van de CSS-bestanden aan: eerst `normalize.css`, daarna `general.css` en vervolgens de pagina-specifieke CSS-bestanden. Dit zorgt ervoor dat de meer specifieke CSS-regels een hogere specificiteit hebben.


## Wireframe analyse 
### Algemene features

Elke pagina moet de volgende elementen bevatten, die op elke pagina hetzelfde zijn:

- Typografie: Lettertype, font-size, headings (h1, h2, h3, etc.)
- Een header met een logo
- Navigatie in de header met links naar de andere pagina's
- Een footer
- ...

> **TIP**: 
> - Bouw de algemene elementen eerst op één pagina (bijvoorbeeld `index.html`). Wanneer deze correct zijn, kopieer je de HTML naar de andere .html-bestanden. Door `global.css` in alle .html-bestanden te linken, zal de styling overal hetzelfde zijn, wat veel tijd bespaart en zorgt voor uniformiteit.
> - Zorg ervoor dat je op elke pagina de juiste semantische elementen gebruikt (header, nav, main, aside, section, article, footer, ...) zoals geleerd in de les.

### Pagina-specifieke features

- **index.html**: De homepage van je webshop
  - Naam van de webshop
  - Algemene uitleg over je webshop zoals je die beschreven hebt in je styleguide document uit deelopdracht 1.
  - De 3 best verkochte producten
  - Een professionele foto van jezelf
  - Een korte uitleg of bio van jezelf

- **shop.html**: De overzichtspagina van de webshop
  - Titel
  - Korte beschrijving gebaseerd op de productbeschrijving uit deelopdracht 1
  - Foto van het product
  - Over de volledige productcard een link naar de detailpagina van het desbetreffende product

- **6 detailpagina's**: Pagina's voor elk van de producten, met:
  - Een titel
  - Een beschrijving
  - Afbeelding in een `figure` met de bronvermelding in de `figcaption`
  - Een opsomming van de productspecificaties

- **contact.html**: Een pagina met:
  - Een contactformulier
