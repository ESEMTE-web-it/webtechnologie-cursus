# 4: lay-out

## natuurlijke volgorde

Met de _natuurlijke volgorde_ van een webpagina bedoelen we de manier waarop een pagina weergegeven wordt wanneer je helemaal niets anders doet dan een aantal `html`-elementen onder elkaar plaatsen. Zonder de toevoeging van CSS heb je een natuurlijke flow, die met CSS gewijzigd kan worden. Met behulp van css kunnen een aantal zaken beïnvloed worden:

* teksten opmaken,
* op een bepaalde manier lay-outen,
* bepaalde elementen op een bepaalde manier positioneren.

Er gaat dus aan de natuurlijke volgorde van de pagina gesleuteld worden.

Het is belangrijk te begrijpen wat deze natuurlijk volgorde precies betekent. Indien je niet begrijpt hoe elementen op een 'natuurlijke' wijze en dus zonder tussenkomst van CSS weergegeven worden, is het onmogelijk in te zien hoe je die volgorde met CSS kan wijzigen.

### geforceerde flow

Je kunt via CSS op een groot aantal manieren de natuurlijke volgorde van een pagina beïnvloeden en wijzigen.

De natuurlijke volgorde van een pagina, dus de opbouw die een pagina heeft wanneer er niets aan veranderd wordt, moet het vertrekpunt zijn. De pagina moet vanaf het begin, ook zonder de lay-out, gestructureerd zijn. En dat is anders dan bijvoorbeeld in XAML of Windowsformulieren waarbij alle elementen op de pagina expliciet gepositioneerd moeten worden. In plaats daarvan geeft de browser de inhoud direct leesbaar weer, zonder dat de positie van de elementen expliciet moet opgeven worden.

Als de CSS niet kan worden geladen, kan de gebruiker de inhoud nog steeds lezen. Gebruikers, die geen gebruik maken van CSS, bijvoorbeeld iemand die een schermlezer gebruikt, krijgt de inhoud van de webpagina in de volgorde waarin ze in het document staan. Als de inhoud in de volgorde staat die een gebruiker verwacht, moet je de lay-out niet grondig wijzigen om de elementen op de juiste plaats te krijgen. Met de nieuwere lay-outmethoden zal je verbaasd zijn hoe weinig je moet doen.

Voordat je aan lay-out denkt, moet je nadenken over de documentstructuur en de volgorde waarin je wilt dat je inhoud vanaf de bovenkant van het document tot onderaan moet worden gelezen, m.a.w. de natuurlijke volgorde van het document.
