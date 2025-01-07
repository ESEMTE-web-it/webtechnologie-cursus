# invoervelden

Er zijn verschillende soorten invoerelementen voorzien in HTML5. Alle invoerelementen maken gebruik van het `name`-attribuut. Dit attribuut geeft aan wat de naam is van de waarde die wordt ingevoerd.

## \<input>

Het `<input>`-element wordt gebruikt om verschillende soorten invoer te voorzien. Je geeft aan welk soort invoer je wenst met het `type`-attribuut.

```html
<input type="text" name="username">
```

### tekst

Het `text`-type creëert een tekstveld waar de gebruiker tekst kan invullen. Je kan hier ook de `size`- en `maxlength`-attributen gebruiken om aan te geven hoe groot het tekstveld moet zijn en hoe lang de ingegeven tekst mag zijn.

```html
<form action="https://www.example.com" method="GET">
    <input type="text" name="username" size="20" maxlength="30">
</form>
```

### wachtwoord

Dit type dient om wachtwoorden in te voeren. De ingetypte karakters zullen dus niet op het scherm verschijnen. De attributen zijn identiek aan die van het tekstveld.

```html
<form action="https://www.example.com" method="GET">
    <label for="username">Username:</label>
    <input type="text" name="username" size="20" maxlength="30">
    <label for="password">Password:</label>
    <input type="password" name="password" size="20">
</form>
```

### e-mail

Met het type `email` wordt aan de gebruiker een e-mailadres gevraagd.

```html
<form action="https://www.example.com" method="GET">
    <label for="email">e-mail:</label>
    <input type="email" name="email">
</form>
```

### URL

Met het type `url` kan de gebruiker om een URL gevraagd worden.

```html
<form action="https://www.example.com" method="GET">
    <label for="website">website:</label>
    <input type="url" name="website">
</form>
```

### datum

Met `<input type="date">` kan je de gebruiker om een datum vragen.

```html
<form action="https://www.example.com" method="GET">
    <label for="birthDate">Geboortedatum:</label>
    <input type="date" name="geboortedatum" id="birthDate">
</form>
```

### bestand(en)

Het type `file` van input laat gebruikers toe een bestand te uploaden.

```html
<form action="https://www.example.com" method="GET">
    <input type="file" name="fav-song">
</form>
```

### verzenden

De verzendknop staat de gebruiker toe om alle ingevulde informatie in te dienen. Als deze knop wordt ingedrukt zal de informatie in het formulier worden verzonden naar de pagina aangegeven in het `action`-attribuut van het `<form>`-element.

```html
<form action="https://www.example.com" method="GET">
    <input type="submit" value="Upload">
</form>
```

### afbeelding(en)

We hebben ook een invoerveld van het type `image` ter beschikking om een afbeelding als knop te gebruiken. Deze input heeft ook het `src`-attribuut nodig om de locatie van de afbeelding aan te geven. Alsook zijn de `height`- en `width`-attributen beschikbaar om de grootte van de afbeelding in te stellen.

```html
<form action="https://www.example.com" method="GET">
    <input type="image" src="images/subscribe.svg" width="100" height="20">
</form>
```

### verborgen invoer

Het `<input type="hidden">` element staat toe om een verborgen waarde aan het formulier toe te voegen. Deze waarde kan info bevatten over de pagina waarop het formulier staat.

### zoekveld

Het `<input type="search">` element zorgt voor een zoekbalk. Sommige browsers voorzien een kruisje in een searchbar zodat input kan worden weggehaald. Met het `placeholder`-attribuut kan een voorlopige tekst worden ingesteld. Deze verdwijnt van zodra de gebruiker zelf tekst wil ingeven.

```html
<form action="https://www.example.com" method="GET">
    <input type="search" name="searchTerm" id="searchInput" placeholder="Zoek...">
</form>
```

## tekstgebied

Met het `<textarea>`-element kan je een veld invoegen waar de gebruiker meerdere lijnen tekst in kan invoeren.

```html
<form action="https://www.example.com" method="GET">
    <textarea name="comments"  cols="30" rows="10">Enter your comments</textarea>
</form>
```

## keuzerondje

Het keuzerondje `type="radio"` gaat het mogelijk maken om een optie te selecteren. Je koppelt meerdere opties om tussen te selecteren aan elkaar door ze hetzelfde `name`-attribuut mee te geven. De gebruiker kan slechts 1 van de aan elkaar gekoppelde opties tegelijkertijd selecteren. Wil je dat de gebruiker meerdere opties tegelijkertijd kan selecteren gebruik dan een selectievak.

Het attribuut `checked` kan in het element geplaatst worden om aan te duiden dat deze optie moet aangevinkt zijn bij het laden van de pagina.

```html
<form action="https://www.example.com" method="GET">
    <input type="radio" name="sport" value="lopen" checked>lopen<br>
    <input type="radio" name="sport" value="fietsen">fietsen<br>
    <input type="radio" name="sport" value="zwemmen">zwemmen<br>
</form>
```

## selectievak

Het selectievak wordt gebruikt als de gebruiker 1 of meerdere dingen moet kunnen aanvinken. Selectievakken mogen een verschillende naam hebben aangezien ze niet met elkaar in verbinding staan zoals de keuzerondjes. Je hebt hier ook het `checked`-attribuut om al één of meerdere selecties te maken bij het laden van de pagina.

```html
<form action="https://www.example.com" method="GET">
    <input type="checkbox" name="spotify" id="spotify" checked>Spotify<br>
    <input type="checkbox" name="itunes" id="itunes" checked>iTunes<br>
    <input type="checkbox" name="youtube" id="youtube">Youtube<br>
</form>
```

## keuzelijst

Het `<select>`-element creëert een keuzelijst. Hier kan de gebruiker een item uit de lijst selecteren. Om items aan de selectie toe te voegen gebruik je het `<option>`-element. Aan dit `<option>`-element moet je het `value`-attribuut toevoegen, deze value wordt dan meegezonden indien de optie geselecteerd werd.

```html
<form action="https://www.example.com" method="GET">
    <select name="devices">
        <option value="ipod">iPod</option>
        <option value="radio">radio</option>
        <option value="computer">computer</option>
    </select>
</form>
```

### keuzelijst met meerdere opties

Het `<select>`-element heeft het `multiple`-attribuut. Dit is een keuzelijst waarbij de gebruiker meerdere opties kan selecteren door op de ctrl-toets (pc) of cmd-toets (mac) te blijven duwen terwijl hij de opties aanklikt. Met het `size`-attribuut kan je aangeven hoeveel opties je tegelijkertijd aan de gebruiker wil tonen.

```html
<form action="https://www.example.com" method="GET">
    <select name="instruments" multiple>
        <option value="guitar" selected>Guitar</option>
        <option value="drums">Drums</option>
        <option value="bass">Bass</option>
    </select>
</form>
```

## knoppen

Met het `<button>`-element kunnen we een knop op het scherm plaatsen waar de gebruiker op kan klikken. Het `type`-attribuut kan gebruikt worden om het gedrag van de knop in te stellen. Er zijn 3 mogelijke waarden:

1. `button` - De gebruiker kan op de knop klikken.
2. `submit` - De knop wordt gebruikt als verzendknop.
3. `reset` - De knop dient als resetknop voor het formulier.

```html
<form action="https://www.example.com" method="GET">
    <button type="button">testKnop</button>
</form>
```

{% hint style="info" %}
Als er slechts 1 `button` in een formulier te vinden is, zal dit automatisch een `sumbit`-button zijn.
{% endhint %}
