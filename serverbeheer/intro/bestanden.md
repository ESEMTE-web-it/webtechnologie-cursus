# bestandstructuur

## root directory

Plaats alle bestanden die toegankelijk zijn via de website in de root directory van de webserver. Dit is vaak de `public_html` of `www` map. Dit is in principe ook de map die je in VS Code opent als working directory.

## bestandsstructuur

Organiseer je bestanden in logische mappen. Bijvoorbeeld, afbeeldingen kunnen worden opgeslagen in een map genaamd `images`, scripts in `js`, en stijlbladen in `css`. Dit verbetert niet alleen de leesbaarheid, maar maakt het ook gemakkelijker om bestanden te onderhouden.

We spreken af dat we binnen de root van een website altijd op eenzelfde manier gaan werken. Bepaalde frameworks of CMS-en kunnen andere manieren hanteren omdat deze meer geschikt zijn voor het doeleinde dat zij willen behalen. Bij een statische website gaan we als volgt te werk:

```html
root
|- index.html
|- other-page.html
|- some-page.html
|- contact.html
|- css
   |- reset.css
   |- some-style.css
   |- other-style.css
   |- style.css
|- js
   |- some-script.js
   |- other-script.js
   |- script.js
|- assets
   |- images
      |- image-01.jpg
      |- image-02.jpg
      |- image-03.jpg
      |- image-04.jpg
   |- fonts
      |- cool-font.woff
      |- other-font.woff
   |- icons
      |- logo.png
      |- logo_small.png
      |- favicon.ico
```

![Een voorbeeld van de root van een webserver](<../../.gitbook/assets/Schermafbeelding 2021-11-29 om 17.04.37.png>)

## index bestand

Zorg ervoor dat het indexbestand (meestal `index.html` of `index.php`) aanwezig is. Dit bestand wordt geladen wanneer iemand de hoofdmap van de website bezoekt.

## 404-pagina

Creëer een aangepaste 404-foutpagina. Dit is de pagina die wordt weergegeven wanneer een bezoeker een niet-bestaande pagina probeert te openen. Standaard zal een moderne webserver hier een eigen template voor hebben maar het is beter om deze in de stijl van de website te voorzien.
