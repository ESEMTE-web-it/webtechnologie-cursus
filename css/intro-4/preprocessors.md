# preprocessors

Een CSS-preprocessor is een scriptingtaal die wordt gebruikt om CSS te schrijven. Het biedt programmeerconstructies zoals variabelen, functies en herbruikbare stukken code, waardoor het schrijven en onderhouden van CSS aanzienlijk wordt verbeterd. Een populaire CSS-preprocessor is SASS (Syntactically Awesome Stylesheets).

## SASS

SASS introduceert enkele krachtige concepten die niet beschikbaar zijn in standaard CSS. De belangrijkste kenmerken zijn:

1.  **variabelen:** Definieer variabelen om herbruikbare waarden zoals kleuren, lettertypen en afmetingen vast te leggen.

    ```scss
    $primary-color: #3498db;
    body {
      background-color: $primary-color;
    }
    ```
2.  **nesten:** Nest regelsets binnen elkaar voor een duidelijkere en gestructureerde opmaak.

    ```scss
    nav {
      ul {
        margin: 0;
        padding: 0;
        list-style: none;
      }
      li { display: inline-block; }
    }
    ```
3.  **partials en importeren:** Splits je SASS-code op in meerdere bestanden, genaamd partials, en importeer ze waar nodig.

    ```scss
    // _variables.scss
    $primary-color: #3498db;

    // main.scss
    @use 'variables';
    body {
      background-color: $primary-color;
    }
    ```
4.  **mixin:** Definieer herbruikbare stukken CSS-code met mixins.

    ```scss
    @mixin border-radius($radius) {
      -webkit-border-radius: $radius;
      -moz-border-radius: $radius;
      border-radius: $radius;
    }

    .box {
      @include border-radius(10px);
    }
    ```

## SASS met componenten

Wanneer je met SASS werkt, kun je het concept van componenten introduceren om je CSS nog beter te organiseren. Hier is een voorbeeld van hoe je SASS kunt gebruiken met componenten:

### 1. **structuur:**

Organiseer je SASS-bestanden in een duidelijke structuur, bijvoorbeeld:

```
styles/
├── components/
│   ├── _buttons.scss
│   ├── _forms.scss
│   └── _nav.scss
├── layout/
│   ├── _header.scss
│   ├── _footer.scss
│   └── _grid.scss
└── main.scss
```

### 2. **importeren:**

Gebruik de `@import`-regel om componenten in je hoofdbestand te integreren.

```scss
// main.scss
@use 'components/buttons';
@use 'components/forms';
@use 'components/nav';
```

### 3. **modulariteit:**

Houd de styling van elk component binnen zijn eigen bestand. Bijvoorbeeld, in `_buttons.scss`:

```scss
// _buttons.scss
.button {
  // stijlen voor knoppen
}

.icon-button {
  // stijlen voor icoonknoppen
}
```

### 4. **herbruikbaarheid:**

Maak gebruik van variabelen en mixins om de herbruikbaarheid van je componenten te vergroten.

```scss
// _buttons.scss
$primary-color: #3498db;

.button {
  background-color: $primary-color;
  color: white;
  padding: 10px 15px;
  @include border-radius(5px);
}

.icon-button {
  @extend .button;
  // extra stijlen voor icoonknoppen
}
```

SASS met componenten maakt je CSS-code georganiseerd, onderhoudbaar en gemakkelijk te begrijpen. Het bevordert herbruikbaarheid en modulariteit, waardoor het beheer van grote codebases efficiënter wordt.
