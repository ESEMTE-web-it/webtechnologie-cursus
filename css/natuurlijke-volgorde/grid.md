# grid

## grid intro

Lay-outs zijn gemakkelijk te maken met behulp van rasters (grids). Tot nu toe beschikte het web niet over een raster. Er werden daarom allerlei methoden en hacks uitgeprobeerd om een webpagina in een raster weer te geven. Het begon met op tabellen gebaseerde lay-outs, gevolgd door op float gebaseerde lay-outs. Maar dit zijn enkel nepoplossingen omdat **tabellen en float niet bedoeld waren om lay-out**s te maken.

Lay-out met grid biedt een **raster-gebaseerd layout-systeem met rijen en kolommen**, waardoor het gemakkelijker wordt om webpagina's te ontwerpen zonder gebruik te maken van floats en positionering.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0sxhAGhADMBLGXVAbVADsBDAWwjUwAt56p8RYB7axfswA8AIx5IAngD4AOtQAEi+UJYRaSCACcpACTUbNQgPSr1W2QqVC6ANykA5WjeO2LS5fVrFqUgLJfqY09vNytaMGINKQBBCI1jcMiIUMUhQh4eRG0AMQys43TM8zljMUkpLkgYBGI+chAANlQAdhAAXzwaBiZ0DAArXAJefghBdHbOkDpGZiwcLmGBeGZ5ACp5YHk5JTEADwBaCIAvbwBzVHkxTQN9vYBuOTa5OTYOPEvxCQ3t+U9NU+8FwADHctpYAA7qJBnYEPahPajPahlL7AH5GdYAchRmPkxDA8ggo3kkM0o3g8hsGU0hOJp00kX2UFoEh4AFcKUhqfJMdCwODmRILvTIrjVkYfnyBSzhQykHDFCKkPtEPRpYh9rQyeFUD9FJjTAZ5IatMb9KaTTTLbiMfIAKzyQiaWg1CAEy3yAC88gAjECgQBSNYSyz6xjUNlKYKh6NRgJKBmnNg29a+p2-UaR70AJkD8gAPooAMzp2Pehp5ws+9OJthe+S5oPisHuTHhyOKQpZR15U1dvu9zSY0G26s09v1xsF+QAFnT-Zp3oAHHnxT8lftTrRwRc-eDdgrLi6ANb09nUZW8KA8TQXADE2Z9AE4Gtki4fIUhodRzr6gfu4QRF5zRpYANy1NQLktO4EVsDZwO1C52xguRYzAuVNUQ34AhQug4ggeCMIg2gLlreBcIXQjGWIi4F1wuQUXkKR5GhGx3ktd5bHeaN3kSDR3kotFLFtWAWFIJAyQUERvGoYkiQUDdFgCU0AHcbw0BRaA5HhPHgfFRPkDdiFVAk10sEQTzPNkL32K8b1I04LIACmzO07XeVz3IbNz3iBDAlwASkPRBdngTUoGIU5qAuWByS0D8oRhBt-12eQQR+dJ+EOYgjggC4ixSwCkQAAUYaFaHkMBYDJYlaAveQnM8A4VMieAWAuCsUoC75zM+HrFFteTDIwwV2QpVQIEICkhtJcl5GocRIozTl8WlL5MSVXEeEIHlvAi2TNzlMUQ0UKVBVlSJDw3VV1QgTC1DAXVQx5D1XpAs0zCtd7rXkW0GnTD0zNbWNFBB7DvDjCHFDI6HIuTX71jHDMI2nEtx3jQts3kGHmz1HlKM7QceyKGlKLJwdhwRtNx0zac7XnImgeGxktx3P8AJ+CzYFPTRz0vHhr1veQH2fV93x+T9v1-PcD0eJFFDkOD0OorDkMlVbzoW2TDwRNpKmgOA9LqZg7SLVAfXaABdNogA" %}

info [box-sizing: border-box | content-box (default)](https://www.w3schools.com/cssref/tryit.asp?filename=trycss3_box-sizing)

### grid-elementen

Een grid-lay-out heeft een _parent_ nodig met een **display: grid** of **display: inline-grid**\
Alle directe _children_ binnen een grid-container worden automatisch **grid-elementen.**\\

***

### grid columns

De **verticale lijnen** van de grid-elementen worden **kolommen** (grid columns) genoemd.

![](../../.gitbook/assets/css-grid-1.png)

### grid-rows

De **horizontale lijnen** van de grid-elementen worden **rijen** (grid rows) genoemd.

![](../../.gitbook/assets/css-grid-2.png)

### grid-gaps

De **spaties of witruimte** tussen elke kolom of rij worden **gaps** genoemd. Gebruik de CSS-eigenschap "gap" om dit aan te passen.

![](../../.gitbook/assets/css-grid-3.png)

{% embed url="https://codepen.io/APwebtechnologie/pen/JjKxPLb" %}

### grid-lines

De lijnen tussen kolommen worden **kolomlijnen** (column lines) genoemd.\
De lijnen tussen rijen worden **rijlijnen** (row lines) genoemd.\
Naar deze lijnen wordt verwezen bij het plaatsen van een grid-item binnen een grid-container.

![](../../.gitbook/assets/css-grid-4.png)

{% embed url="https://codepen.io/APwebtechnologie/pen/VwjgwZX" %}

{% embed url="https://codepen.io/APwebtechnologie/pen/NWroKEJ" %}

Het bovenstaande voorbeeld geeft een raster met 3 kolommen waarbij de rijen minimaal 100px zijn.\\

## grid container

Om ervoor te zorgen dat een HTML-element zich gedraagt ​​als een grid-container moet de display-eigenschap ingesteld worden op **grid** of **inline-grid**. Grid-containers bestaan ​​uit grid-items die in kolommen en rijen worden geplaatst.

try it yourself:[https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_container](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_container)\\

### grid-template-columns

De **grid-template-columns** bepaalt het aantal kolommen in een grid en de **breedte van elke kolom**. Bij een door spaties gescheiden lijst, definieert elke waarde de breedte van de respectieve kolom. Als het grid 4 kolommen bevat, moet telkens de breedte van de 4 kolommen gedefinieerd worden. Indien alle kolommen dezelfde breedte moeten hebben, wordt er gebruik gemaakt van `auto`.

{% embed url="https://codepen.io/APwebtechnologie/pen/mdEvyOe" %}

try it yourself:[https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-template-columns2](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-template-columns2)\\

### grid-template-rows

De **grid-template-rows** definieert de **hoogte van elke rij**. Bij een door spaties gescheiden lijst, definieert elke waarde de breedte van de respectieve rij.

{% embed url="https://codepen.io/APwebtechnologie/pen/eYzxmvj" %}

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-template-rows](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-template-rows)\\

### justify-content

De **justify-content** wordt gebruikt om het hele grid binnen de container uit te lijnen, waarbij justify-content de volgende waarden kan aannemen:

justify-content: **space-evenly | space-around | space-between | center | start | end**

```css
.grid-container {
  display: grid;
  justify-content: space-evenly;
}
```

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_justify-content\_space-evenly](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_justify-content_space-evenly)\\

### align-content

De **align-content** wordt gebruikt om het hele grid binnen de container **verticaal** uit te lijnen, waarbij align-content de volgende waarden kan aannemen:

align-content: **space-evenly | space-around | space-between | center | start | end**

```css
.grid-container {
  display: grid;
  height: 400px;
  align-content: center;
}
```

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_align-content\_center](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_align-content_center)

## grid item

### child elements (items)

Een grid-container bevat grid-items. Standaard heeft een container één grid-item voor elke kolom, in elke rij, maar grid-items kunnen zo opgemaakt worden dat ze meerdere kolommen en/of rijen beslaan.

### grid-column

De **grid-column** definieert op welke kolom(men) een item moet worden geplaatst. Er kan bepaald worden waar het item begint en waar het eindigt. Enkele voorbeelden:

* .item1 { grid-column: 1 / 5; } item 1 start in kolom 1 en eindigt voor kolom 5
* .item1 { grid-column: 1 / span 3; } item 1 start in kolom 1 en voegt 3 kolommen samen
* .item2 { grid-column: 2 / span 3; } item 1 start in kolom 2 en voegt 3 kolommen samen

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-column2](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-column2)\\

### grid-row

De **grid-row** definieert op welke rij(en) een item moet worden geplaatst. Er kan bepaald worden waar het item begint en waar het eindigt. Enkele voorbeelden:

* .item1 { grid-row: 1 /4; }\
  \=> item 1 start in rij 1 en eindigt voor rij 4
* .item1 { grid-column: 1 / span 2; }\
  \=> item 1 start in rij 1 en voegt 2 rijen samen

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-row2](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-row2)\\

### grid-area

De **grid-area** kan worden gebruikt als een verkorte eigenschap voor de volgende 4 eigenschappen **grid-row-start, grid-column-start, grid-row-end** en **grid-column-end**. Enkele voorbeelden:

* .item1 { grid-area: 1 / 2 / 5 / 6; }\
  \=> item 1 start op rijlijn 1 en kolomlijn 2, en eindigt op rijlijn 5 en kolomlijn 6
* .item1 { grid-area: 2 / 1 / span 2 / span 3; }\
  \=> item 1 start op rijlijn 2 en kolomlijn 1, en omvat 2 rijen en 3 kolommen

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-area1](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-area1)\
try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_grid-area2](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_grid-area2)\\

### grid-template-areas

De eigenschap **grid-area** kan ook worden gebruikt om **namen toe te wijzen aan grid-items**. Door alle items correct te benoemen en toe te wijzen aan een grid-area kan een kant-en-klare grid-template gemaakt worden voor een webpagina.

```css
header {grid-area: header;}
nav {grid-area: menu;}
main {grid-area: main;}
aside {grid-area: right;}
footer {grid-area: footer;}

body {
  display: grid;
  grid-template-areas:
    'header header header header header header' /* 6fr header */
    'menu   main   main   main   right  right' /* 1fr menu | 3fr main | 2 right */ 
    'menu   footer footer footer footer footer'; /* 1fr menu | 5fr footer */
    }
```

{% embed url="https://codepen.io/APwebtechnologie/pen/PozXMRW" %}

### ordenen

Door te werken met grid kunnen de grid-items overal geplaatst worden waar je maar wil. Het eerste item in de HTML-code hoeft dus niet als eerste item in het raster te verschijnen.

```css
.item1 { grid-area: 1 / 3 / 2 / 4; }
.item2 { grid-area: 2 / 3 / 3 / 4; }
.item3 { grid-area: 1 / 1 / 2 / 2; }
.item4 { grid-area: 1 / 2 / 2 / 3; }
.item5 { grid-area: 2 / 1 / 3 / 2; }
.item6 { grid-area: 2 / 2 / 3 / 3; }
```

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_flexible\_order](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_flexible_order)

```css
@media only screen and (max-width: 500px) {
  .item1 { grid-area: 1 / span 3 / 2 / 4; }
  .item2 { grid-area: 3 / 3 / 4 / 4; }
  .item3 { grid-area: 2 / 1 / 3 / 2; }
  .item4 { grid-area: 2 / 2 / span 2 / 3; }
  .item5 { grid-area: 3 / 1 / 4 / 2; }
  .item6 { grid-area: 2 / 3 / 3 / 4; }
}
```

try it yourself:n [https://www.w3schools.com/css/tryit.asp?filename=trycss\_grid\_flexible\_order2](https://www.w3schools.com/css/tryit.asp?filename=trycss_grid_flexible_order2)\\

## video: single-line CSS layouts voor o.a. flex en grid

{% embed url="https://www.youtube.com/watch?v=qm0IfG1GyZU" %}
10 modern layouts in 1 line of CSS
{% endembed %}

{% hint style="info" %}
Je kan oefenen op CSS Grid met:

* [Grid Garden](https://cssgridgarden.com)
* [An Interactive Guide to CSS Grid](https://www.joshwcomeau.com/css/interactive-guide-to-grid/)
{% endhint %}
