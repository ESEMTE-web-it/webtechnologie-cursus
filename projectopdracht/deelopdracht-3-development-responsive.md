# Deelopdracht 3 - Development responsive webshop

In deze deelopdracht werken we de desktopversie van het design in Figma - aangepast aan jouw styleguide uit opdracht 1 - uit. Gebruik "min-width" in je media-queries en behoud zo de _mobile-first_ aanpak. Zorg dat je jouw site minstens optimaliseert voor smartphones en desktops. Tablets zijn geen must.

{% hint style="info" %}
Indien je in opdracht 1 geen gebruik gemaakt hebt van flexbox of grid voor lay-outing zal je dit wat moeten herwerken. Zorg daarbij dat je site er nog steeds goed uitziet op mobile.
{% endhint %}


Een overzicht van de dingen die anders moeten zijn in de desktop view:

* algemeen (op elke pagina van toepassing)
  - beperk de maximum breedte van de body tot 1440px en zorg dat deze gecentreerd staat op het scherm. 
  - Horizontale layout van de header: de nav en de searchbar komen naast het logo te staan. Gebruik hiervoor een media query en flexbox.

* index.html: 
  - Plaats de 3 meest verkochte items in een grid zoals in het wireframe. Zorg dat op mobiel de 3 elementen onder elkaar komen.
  - Het kaartje met de foto en uitleg van de auteur is nu horizontaal gepositioneerd.
  - De algemene lay-out veranderd: de meest verkochte items staan nu rechts van de introductie en het auteurkaartje. 

* shop.html:
  - Zet de 6 producttegels in een flexbox. Zorg dat de beschikbare schermbreedte zo optimaal mogelijk benut wordt. 
  - Beperk het maximum aantal productegels op 1 rij tot 3 zoals in de wireframe. Reken daarvoor de ideale flex-basis uit.
  - Zet de product lijst en de shopping cart + wishlist in een flexbox. Deze mogen langs elkaar komen als ze daarvoor ruimte genoeg hebben.

* de 6 detailpagina's*
  - De afbeelding en de tekst worden horizontaal naast elkaar geplaatst in plaats van onder elkaar. Gebruik daarvoor flexbox of grid in combinatie met een media query.
  
* contact.html:
  - Deze pagina hoeft voorlopig nog niet uitgewerkt te worden. Dit volgt in de volgende deelopdracht.