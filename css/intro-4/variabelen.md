# variabelen

CSS-variabelen, ook wel aangeduid als CSS Custom Properties, voegen een nieuwe dimensie toe aan de stijldefinitie van webpagina's. Ze bieden flexibiliteit en herbruikbaarheid door het mogelijk te maken waarden te declareren en te hergebruiken op meerdere plaatsen in je stylesheet. Laten we dieper ingaan op het concept van CSS-variabelen.

## declaratie van CSS-Variabelen

CSS-variabelen beginnen met twee streepjes `--` en worden gedeclareerd binnen een selector zoals een root-element, bijvoorbeeld `:root` of een specifiek element.

```css
:root {
  --primary-color: #3498db;
  --font-family: 'Arial', sans-serif;
  --spacing: 8px;
}
```

In dit voorbeeld worden drie variabelen gedeclareerd: `--primary-color`, `--font-family`, en `--spacing`.

## gebruik van CSS-variabelen

Je kunt CSS-variabelen in je stijlregels gebruiken met de functie `var()`.

```css
body {
  background-color: var(--primary-color);
  font-family: var(--font-family);
  margin: var(--spacing);
}
```

De `var()`-functie haalt de waarde op die aan de variabele is toegewezen. Hierdoor kun je gemakkelijk een uniforme stijl handhaven en snel wijzigingen aanbrengen.

## herbruikbaarheid en onderhoud

CSS-variabelen verbeteren de herbruikbaarheid en het onderhoud van je stylesheet. Stel je voor dat je de primaire kleur van je website wilt wijzigen. Met variabelen hoef je slechts één keer de waarde van `--primary-color` in de `:root` selector aan te passen, en deze wijziging wordt automatisch doorgevoerd in alle stijlregels waar deze variabele wordt gebruikt.

## dynamisch gebruik

CSS-variabelen kunnen ook dynamisch worden bijgewerkt met JavaScript, wat de mogelijkheid biedt om stijlen op basis van gebruikersinteractie aan te passen.

```css
:root {
  --button-bg-color: #3498db;
}

.button {
  background-color: var(--button-bg-color);
}
```

```javascript
// JavaScript
document.documentElement.style.setProperty('--button-bg-color', '#e74c3c');
```

Door de waarde van `--button-bg-color` met JavaScript bij te werken, kun je de achtergrondkleur van alle elementen met de klasse `.button` dynamisch veranderen.

CSS-variabelen vormen een krachtige toevoeging aan de toolkit van een webontwikkelaar, waardoor flexibiliteit en efficiëntie worden bevorderd in het beheer van stijlen. Experimenteer met deze variabelen en ontdek hoe ze je stijlworkflow kunnen verbeteren.
