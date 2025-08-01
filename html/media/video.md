# video

Het integreren van video in een webpagina gebeurt met behulp van het `<video>`-element. Dit element biedt de mogelijkheid om via het `<source>`-element één of meerdere videobestanden van verschillende formaten toe te voegen, waarbij het `src`- en `type`-attribuut de bronbestanden specificeren. Daarnaast is het ook mogelijk om ondertitels en opmerkingen aan de video toe te voegen met behulp van het `<track>`-element. Let op dat de tekst binnen het `<video>`-element alleen wordt weergegeven in browsers die dit element niet ondersteunen.

Hier is een voorbeeld van hoe je het `<video>`-element kunt gebruiken:

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp0AjbkgCe+7boCM66VgjKAbmSQRuy6BGZ9BAeizXtCycXNwB3Z3gsAF5NEABmACYABljVCDIAcxwYkASAFhSQZR4+ACduKDB9ZWVBMG4AV1LYezBmnJx4AAcwVB8fUoZQjAyySIaDBshm3n54DB5cHwBBeQBaAElpNYBxAAkfBjBIeDA1l1xuM9CIA0RYLAGIEjA-CAYkV9wGMjofS6cEAwuC6eVS8BMXQgOWCrn+oNi1Vq9SaLWUbVgHXg3V6-UGw1G40m0xKcwW3CWq02232h2OEFO508VzWNzucEepWerzsHy+Pz+ALIQO4GQy4Mh0NisO4PlF4pASNkjVKygM5VC02USG4EDAyjo3Hg6IaXS63FKxsi9hlyngDAyGAsPhl5h0PiMpn0vj02k4kBgCDIvCo6EseVQSRAAF9CPQmCx0BgAFZUYikiACdAxuMgRjMVgLY6cDNZkAxgC60aAA" %}

Laten we de verschillende onderdelen nader bekijken:

* Het `width`- en `height`-attribuut bepaalt de breedte en hoogte van het videoframe in pixels.
* Het `controls`-attribuut voegt afspeelbedieningselementen toe, zoals een afspeelknop, volumeregelaar en tijdsbalk.
* Het `<source>`-element wordt gebruikt om verschillende bronnen van het videobestand te definiëren. In dit voorbeeld zijn er twee bronnen, één in het MP4-formaat en één in het WebM-formaat. De browser selecteert automatisch de best passende bron op basis van de ondersteuning van het formaat.
* De tekst "Your browser does not support the video tag." wordt weergegeven in browsers die het `<video>`-element niet ondersteunen.

## ondertitels en opmerkingen

Met het `<track>`-element kun je ondertitels en opmerkingen toevoegen aan de video. Hier is een voorbeeld:

```html
<video width="640" height="360" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.webm" type="video/webm">
  <track label="Nederlands" kind="subtitles" srclang="nl" src="subtitles/nl.vtt" default>
  Your browser does not support the video tag.
</video>
```

In dit voorbeeld wordt een Nederlandse ondertitel toegevoegd met het bestand "nl.vtt". Het `label`-attribuut geeft de naam van de ondertiteltaal weer, en `srclang` geeft de taalcode aan. Het `default`-attribuut geeft aan dat deze ondertitel standaard moet worden weergegeven als de gebruiker geen specifieke keuze maakt.

Door deze toevoegingen wordt jouw video-inhoud niet alleen toegankelijker, maar ook veelzijdiger voor een breder publiek.
