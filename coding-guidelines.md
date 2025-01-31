# Coding Guidelines

## Algemeen
- **Code Formatting**: Zorg ervoor dat je **HTML**, **CSS** en **JavaScript** altijd goed formatteert. Gebruik de tool **Prettier** voor automatische opmaak. Zorg ervoor dat Prettier is ingesteld als de **default formatter** in je editor.
- **Correcte Indentatie**: Stuur enkel code in die correct geïndenteerd is. Foutieve indentatie maakt je code moeilijker te lezen en te onderhouden.

## Paths
Gebruik altijd relatieve paden (_paths_) om te linken naar bestanden en afbeeldingen. Hou er rekening mee dat je website gehost (en beoordeeld) zal worden op UNIX-gebaseerde systemen. Als je je path met een ```/``` laat beginnen zal dit niet werken op Linux of Mac.

## HTML

- **Foutloze HTML**: Zorg ervoor dat je HTML valide en foutloos is. Gebruik de plugin [HTMLHint](https://marketplace.visualstudio.com/items?itemName=htmlhint.htmlhint) om fouten te detecteren.
- **Minimalisme**: Gebruik alleen de HTML-tags die strikt noodzakelijk zijn voor je ontwerp. Vermijd overbodige of dubbele tags.
- **Semantisch Correct**: Gebruik altijd semantisch correcte HTML-tags zoals `<header>`, `<main>`, `<footer>`, en `<article>`. Dit verbetert zowel de toegankelijkheid als de zoekmachineoptimalisatie (SEO).

## CSS

- **Engelse Benamingen**: Alle waarden voor **class**, **id** en andere attributen moeten in het **Engels** zijn.
- **Kebap-case voor CSS-variabelen**: Gebruik de [kebap-case](https://developer.mozilla.org/en-US/docs/Glossary/Kebab_case) voor CSS-variabelen. Bijvoorbeeld: `--main-color`, `--font-size-lg`.
- **Geen Overbodige CSS**: Laat geen onnodige of niet-gebruikte CSS-eigenschappen staan in je stylesheet. Dit maakt je bestand groter en moeilijker te onderhouden.
- **CSS Variabelen**: Definieer **CSS-variabelen** altijd bovenaan je stylesheet, binnen de `:root {}` selector, zodat ze overal in je CSS beschikbaar zijn.

## JavaScript

- **Strict Mode**: Begin elke JavaScript-file met de volgende statement om "strict mode" in te schakelen:

    ```javascript
    "use strict";
    ```

  **Waarom?**: Dit helpt om veel voorkomende fouten te voorkomen, doordat JavaScript strikter met variabelen en functies omgaat. Lees meer over het verschil tussen **strict mode** en **sloppy mode** op [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode).

- **Vermijd Globale Variabelen**: Beperk de _scope_ van je variabelen tot de file zelf. Zorg voor een duidelijke **main functie** en roep deze onmiddellijk aan:

    ```javascript
    function main() {
        // je code hier
    }

    main();
    ```

- **Variabelen in CamelCase**: Gebruik **camelCase** voor variabele- en functienamen. Dit betekent dat je begint met een kleine letter en de eerste letter van elke nieuwe woord in hoofdletters schrijft, bijvoorbeeld: `userName`, `totalPrice`, `fetchData`.

- **Engelse variabelen**: Geef alle variabelen Engelse namen. Dit maakt je code internationaal leesbaar en voorkomt verwarring.

## Extra Aanbevelingen

- **Gebruik van Commentaar**: Voeg **duidelijke commentaren** toe waar nodig om je code begrijpelijk te maken, vooral bij complexe logica.