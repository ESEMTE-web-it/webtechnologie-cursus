# positionering

## positionering

HTML elementen worden in hun natuurlijke volgorde geplaatst waarbij alleen rekening wordt gehouden met het feit of de elementen blok- of inline elementen zijn. Je kan de HTML elementen uit hun natuurlijke flow halen door ze expliciet te positioneren. Je moet dus weten hoe je elementen precies plaatst. Met de `position` eigenschap bepaal je het type van de methode omtrent positionering die je voor een element wilt gebruiken.

### position: static;

Voor alle elementen in HTML is het `position` attribuut standaard ingesteld op `static`. Dit betekent dat de elementen weergegeven worden in de volgorde waarin ze geplaatst zijn in het HTML element.

### position: relative;

Met `position: relative` wordt een element gepositioneerd ten opzichte van zijn static positie. Dat doe je bijvoorbeeld door een top, left, right en/of een bottom waarde toe te kennen aan het element. De instelling `position: relative;` maakt het dus mogelijk om een element te positioneren ten opzichte van de `position: static;` die dit element standaard heeft.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6kZAG4YATtAbx7EZcG3LlAB25gZG68qMrOUK7uANzeyjAk8KEAzAAMvgAeMXQ+AEbcjkgQjskZymDcUGRIygDEAOxJAIKiAEwAjFkAvtqCAPTmVhCmvYbGpnlIFvo9WC3q-oHBdKHhkXYQUX2z0zq+6o3Z0BDMfMoA7kFYfgFBZCFhLm7rUcpkYNeLd3TIDxFPHvBuK94O86PlcAwoB9biE+nttD1bHZlLAImAwABeTQgVb-bH6aRYN7KJHKI4neCqBjvBYw5a-NYbHq9JE7PoTKbMvQIujaTiQGAIL5UdAtACsqBSIE6hHoTBY6AwACsqMQeHwIAJ0NLZSBGMxWBhYOjOOr+PBWNKALqdIA %}

### position: absolute;

Bij het absoluut positioneren van een element moet je twee concepten onthouden:

1.  **ouder-kind relaties**:

    In HTML is elk element een op z'n minst een kind-element van het HTML element. Het HTML-element omsluit alle andere elementen, en is daardoor het ouder-element van alle andere HTML-elementen. Op een meer technische manier zeggen we dat alle andere elementen genest zijn in het HTML-element en dus kinderen van het HTML-element zijn. Een kind-element is dus genest in een ouder-element, en een ouder-elementen is ouder van alle elementen die er in genest zijn.
2.  **het absoluut positioneren van een element gebeurd ten opzichte van het eerste gepositioneerde ouder-element**:

    Nu weet je wat ouder- en kind-elementen zijn, is het absoluut positioneren ten opzichte van het eerste gepositioneerde ouder-element, gemakkelijker te begrijpen. Een absoluut gepositioneerd element is gepositioneerd ten opzichte van het eerst gepositioneerde ouder-element. Dit betekent dat een element dat je absoluut positioneert door alle ouder-elementen loopt totdat het het eerste, namelijk een `html` element tegenkomt, of een elementen waarvan het `position` attribuut is ingesteld op `relative` of `absolute`. Op dat element baseert het te positioneren element zijn positie.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6kZAG4YATtAbx7EZcG3LlAB25gZG68qMrOUK7uANzeygDuZEjwWKEALAAM6b4AHjF0PoZkAOY4oQBMmTl5PgBG3I5IEI6hAMw5ymDcUInKAMQA7C0AgqJlAIx5AL7K2tq2Dgw1nVAAroiesf6BwXShi8trENXK8Ny+oQAcWbmxjsWlyunHCUkpyhXXx4Ul8KFjlTd8so6g0mq12ssegNhqMJtpJtpBAB6cxWCCmJGGYymOpICz6RFYMrqLZBMghZT7LqHKLIokEnS+dRDfLQCDMPjxIJYPwBMkUqmrRBRZRkMC87bkujIMIuNx2DynE6GZTShjOcwS-nSpCUuiwCDmerKAAUZDo5iMuu4JC1Oxl4UiCpO3GVHjsZAgcX8jnghGU3QA1h5yNlkABKVDIpmzHTzZSwCJgMAAXk0IEd8og6fU0iwYuU8bZHPgqgY4tJO1CmeisUE8cT5dT6cFhxzeYLRZgJbLFb5VcpS2pwuR8wxY9jyNx+MRmLwGlj2k4kBgCClVHQLQArKh0iBJoR6EwWOgMAArKjEHh8CACdD7w8gRjMVgYWDJzjX-jwVj7gC6kxAA %}

### position: fixed;

Door gebruik te maken van `position: fixed;` kunnen we een HTML-element positioneren t.o.v. de 'viewport'. Dit is de beschikbare ruimte op het scherm waarin de website getoond wordt. Dit betekent ook dat het element zich niet zal verplaatsen, zelfs als zou de gebruiker door de pagina gaan scrollen.

De plaatsing doen we met behulp van de top, right, bottom en/of left eigenschappen.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6kZAG4ZyAD2TLg25coAO3MGXhkvKjKzsgA3B7KAEbc8PDcuMEADBF0ngBOZADmOMmpngDuZEjwWMEAzElJXk750dzpSBDpFTXKYNxQxcoAxADs5QCCogBMAIypAL7aggD05lYQprOGxqYxSBb6M1gj6j5+AUEhZC5IYXO72zpe6oNp0BDMfMpFpd6+-oF0waHnymQwB9Dt9XOloAwAnYIMp4rDDMo7GQIAUfOl4IRXlgyLAsMpmAw6ED-MoGFACgwLEDzJTiWlSjCwEwYV4oAxYDCINC0mQSPCWQwsjDAe1YOlOjAkKg5rdtDNbHZlLA2WAwABeTSkU7ITX6aTYoEK5SPZ7wVQMIEHL7HP6pOYK65zDZbGYrPAaOV0bScSAwBDfKjoEZ9VBJECTQj0ZmsDAAKyoxB4fAgAnQ4cjIEYzBjsFVnCT-HgrHDAF1JkA %}

### position: sticky;

`position: sticky;` is een combinatie van `position: relative;` en `position: fixed;`. Tijdens het scrollen wordt de positie aangepast op basis van een voorgeplaatste afstand tot opzichte van de viewport.

```css
div.sticky {
  position: sticky;
  top: 0;
}
```

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6kZAG4ZzZWAGsLy4NuXKADtzBk8GS8qMpOrhYA3F7K8Nw+oQAM0XTePsa2dADmoQCsPgAeKd4ARgyuWQBO3ACudEgAtDxQ3JWhAMSwDBAAHF3FyiWtSBBtygBMhWHcUGRIyu0ALJIAggBiucnaAL7aggD05lYQpvuGxqZDSBb6ez7q0pXuccqCJepgsNVQUAfvymQ6AERrEsGQwMoSJUmBBYtxlHURpVzAx6qpuAB3MJBCK+fyBYJ0QFZZQY1ouMAYA73bR7Wx2ZSwKAMMBgAC8mnAOLcnPUAEllExsc43MIDvTbjp6djjhyQOkkJksg0hvA4rhUONEtrCryYoJ7nzUvAwRCIAUmD4YIRQbDwm5lNAIMw+MLXBCXibYXEfMpuCRbb4GFlYQAKH1JACUNoxhlSFlqykqRlgWAB8Ahn2+UDxASCvCp+xpqVe9wAyl8Zjmyq4Eb6XsncNw7N7DG63HQIKzC8XvAb1GXuMxYub4HDHYwSjAwpWfsSMBhlAAZVrOgE+MA1XDKJAzVphQKC5jwG0UKBbncQchE-OdiF0eEARxq3BtuAY5-BkDHPDoTJqSAMPANSVM+sIQGOEBbjaH6INCkIMCUNTMhCNRjs+3CLis8DPmQjIMDUYDdMoWQtJUZBASBAKESOp7zMGQpDkSZotpUQTAZUjpblhJAkKMY7MkM0K4DRyY+ABFH1MRnawI68CLkasBzKMgKQbxziSRxqjgoKSCLooF4PsoTaUEExF2DMNQ+PAQFkEhlLUvofblkO3qjuOECTtOWZVvOi4ro266btuu5kQeY4wieAI-BeIzXgSvBdsoRkYW+H41F+EGMrw-6ARxYFyVxuAwVAcEMAhSEoQi6EvlhOEZfhhHEaRrQUVpZA0YgdGClkjG4MxjqsexVFQbgPF8WxyiCa0TCiRA4m2KigGwjJckKX+ynka6V7kEpqJaaaun6YZ8ImV2ZmwhZ57WbZ9k9qcEq0jo+xXDcexnHgGhPdonCQDACCElQ6AAMyJKgiQgNshD0DCrAYAAVlQxC-vw8CsJD0MgIwzBw7ArKcCjnlo+gkMALrbEAA %}

## overlappende elementen

Wanneer je gebruik maakt van relative, fixed, or absolute positionering kunnen kaders gaan overlappen. Wanneer dit gebeurd, gaan de HTML-elementen die pas later in de natuurlijke volgorde volgen, bovenaan komen.

Wanneer we dit gedrag willen manipuleren, maken we gebruik van de `z-index` eigenschap. Deze eigenschap manipuleert de volgorde waarin HTML-elementen boven en onder elkaar liggen.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6yuAObLg25coAO3MGXhleqZQwAjMG4oAFdEAG5nZRgSeD8ABlcADyi6F3huV0SUtJcALwBaMjokCGS-QoBGNIBfbUEAenMrCFNGw2NTAO4kC30GrCr1aSwyMGVx-1UjJBK7JqHTWwcwACdYAF5NEBx4VzBURsa1hgB3DDsvLFCA0MgN3n54DB5cRoBBeUKASWlCgDiAAlGgwwJB4GBCmVcB5CmcIAFELAsI1YABWBgAJixJAAbOiACxYgIAdnRpISpIAHLAAoSSFi8aSqsS8SQAJxYzFVCCU6kQADMjRWAH14GsIBAMK46HYdqZXOoAEJwBj3CDKeCGSa4Bh2TVYMHTIolMrJZTcEjKaqESbwZRnChQZQBTWuKAMWDIV0QMalLU6xDJF5NJXaBqNHp9dp6CN0bScSAwBA+OhUdAJVAJQo47MgWqEehMFjoDAAKyoxB4fAgAnQBaLIEYzFYr3BnBrz1YBYAurUgA %}

## zwevende elementen

De box van een zwevend element wordt langs de linker- of rechterrand van het moederelement geplaatst en de kaders van andere elementen ervoor of erna kunnen hun plek ernaast krijgen.

Met behulp van de float eigenschap in CSS kunnen alle elementen zwevend gemaakt worden. Je moet wel de breedte van het element expliciet vast leggen met de width eigenschap. Een element met de `float` eigenschap ingesteld op de waarden `left` of `right`, wordt een element op blokniveau. Een eventueel gebruikte `display` eigenschap wordt genegeerd.

De box van een zwevend element wordt compleet weergegeven, inclusief `padding`, `border` en `margin`. De `margin` van een zwevend element en aangrenzende elementen schuiven niet in elkaar.

Om de kader van twee elementen op blokniveau naast elkaar te plaatsen, moet je voor beide elementen de `float` eigenschap instellen. Je kan eventueel de `margin-left` eigenschap gebruiken om wat witruimte tussen de twee boxen te creëren.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6yuAObLg25cpJRuDeKmUAnMnZwAbm0AX21BAHpzKwhTCMNjUwAjbiQLfXCsACZ1ADF3T2UAJX8cSOyMnQAHdQBJOmV4LDIwZQgADyYqmEJGw2VbBjsIZQB3CihXAvhG7j6RvwCZsgamkaqGHyGtqqxehjokecaO5dX+ja27HawxibGd5U3uAFdD48HhjEia7XCawS2BxgHywAC8mhAOHgVTAqAiES2owwdjITReSRekFBvH48AwPFwEQAgvIALS1aRkgDiAAkIgwwJB4GAyUgILhuKzRhAkohYFgIrAkkkSAA2AAsJAAHOykhAJQwAJxZaUAZgADABWBUARmlWtgJDV0t1GqVSogSt1yqyGoiVRWRiq3QgGAAVlU7JCnlB4BCQPInQwXTAfdEYAHxkgmqhdQB2DVVdqBQylLwJpMp3CbVF0MkwEgZrXJ4IgfQAGW4Pg5A1hL1wyiQ3HcPmUYDRT2Y8F6PDokAQEHgLzbxjIjrAsBWDmgaIwynkWEZ0CgWIGuCqEB8SDIQ96dBeUCgDDaMx3CAbAz4W6QDf3LTIylbtYgw3MjOUqTI3F6ADc0QwIyTtAW4tAAji8IwQHQthPv4h4nr+0HQZ4LRNi21bzgAsoBsAoa0MFgJMEDmL0h7wH4eEEXAyh9nYkFtMMPZPC8CDVso-7wIByg5kyDDzrkWJ4U+rHDq0SHmGQmKro2DAvPRIwvDMDBQGQEFDthcl+K0ByIHB9HHr0JAMFOqkdq0kBHNWjA1m0Ly9O4KQ+PAaErJ+O7cPO8hbCR0EzH2v4qWZygjowTxPiZa4rIg26XkpqjQUgNZ+DM2lrnRkHzgAcm8sDtkMaIua057Do2hFkL0lkhUeTA8D4m5tuOYCXjudiER2smwPO9RPDMqnyj4cxVQedB5UhdAoUV64NTuQ7tsgn4+DZIzDvVLTzqIvA0Zx3G3o+r5zYgR5rtcDD-kgiHIYwRXddewxtiQfh0KiNW0bwCltINBG8K4W7MHwDbzgAygtF2OpirRVIe-42coMFJLciAbuxVTVlx86SFsOl5TAcxQz4WKaSOaEQWhO5MBxs74j8lSRCkaRxHofx0NonCQDACDfv2rC6lqcZqrqIAhIQ9BMCw6AelQxB9nirBCyLICMMwrAEkynAy35cshAAuiEQA %}

### stoppen met zweven

Neem aan dat je alleen een titel rechts wil laten zweven van een foto. Er is plaats genoeg naast de foto om de titel en enkele paragrafen ernaast te laten zweven. Dus moet je die standaard mogelijkheid blokkeren door aan de eerste paragraaf na de titel de eigenschap `clear: left;` toe te kennen.

Stoppen met zweven kan zowel links, rechts als aan beide zijden.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6MSMgDcAjMuDblyklG4N4qZTBJ4AG43ZQAHYzs6AHM-RwAGMIAPELp3ACNuACckCCy-AGZk5TBuKDIkZQBiAHYCgEFRACZHVIBfbW1bByaXUIikKNjlBOTUjOzc-OUipJKyiuUs5HbOum77Ar60jy8fPwDg-siyGLjElPdQzJy8wuLS8srahubW7Q66Lrt7ABZt9wDIbnMbXSZ3GYPBaVZZIcbKWAwBjTQ6rHQAenMVggpnRhmMpkySAs+m0uia6gA6mR4FhuABXeAIpFZQR4ilkn7MhhgMAAXk0IB+jkF6mFbJ+pi5iJ5-MFPyaooVygAtMoAHLceBkWAQZS0nzKZVkMDKBiBPJGhzOU76wzKAAS0gAsgAZBHcXIYR3cADuEHseUIJVOuqtTl23ngpvg3DtesOwdpesQSSZtuVnj9puRDLolWFGAlDkJWXUgnSZbW5KpNKwzKMrPZUoc3N5AqFDgKSq7xfsLfsbblnb+Pb+qsdeQgwcRjYOEECQWUuG4gdNP3+SD9aXS0D98cjPlO0XDBW90nt9gYUHpesFh0FDeRpugEGYfFNWZ8yH1ceT-gXeBvVkBkEQYNJr1KJ8smUQUsjIaIcEfcDKkFTJaUFIt0Ulat0SJEkyTxPANDWbROEgGAEDIXgqHQX4ClQeIQDaQh6CYFh0AwAArKhiB4PgIAEdBmNYkBGGYVgMFgXlOH4-h4FYZiAF02iAA %}

{% hint style="info" %}
Met de komst van HTML5 positioneringsmethoden wordt het gebruik van `float` afgeraden.
{% endhint %}

## display

Met de `display` eigenschap kunnen we een HTML-element van gedrag doen veranderen. We kunnen ze kiezen of een element zich al `block-` of als `inline` element gedraagt. Er is ook nog de optie om zich als een `inline-block` te gedragen.

Een inline-block element zal zich net als block elementen gedragen als een vierhoek die op je scherm komt te staan. Wel is het mogelijk voor 2 inline-block elementen om naast elkaar (=inline) te verschijnen.

Met `display: none;` kan je een element uit de natuurlijke flow halen en verbergen voor de gebruikers van de website.

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6ADsuA8o3AE6plz5AG4Avtu02MCAAPAEZ7JDIwGygGCzc6Xggff0CggCZwyOjYtzI6KDyk3zoA4IBmTKiYuOUAIydYAGtkktSAFkrsmryCuggAWnruJpbBAHpzKwhTMcNjU1ruJAtTLBD1aUNlCKrY5XlnbhsIZ0txtf1tXTT1Ha74xNRzm6uIgDd9ABkXCFxlMhsYAArn8kNwnM4MFCMMpBHZYDEwGAALyaEDBEJo9QACUUn0+4mUAHVxAAlT6iYTjGzqZQANQg5jItSBUBByje4KB8BsDHgykQUDZYG2ZCY0IwVzG70uBhud2quXyhSesxeOhl2m+Hj+AOBoPBLglsPhiJRaOCaSxuPxhJJ5Mp1NpDKZLLZf05bJ5fIF0GFovF0KlmroVyw8qyirqDUaqvDphD2t+-0B7LBEONcOUCIYSNR6KCZWteIJxLJFKpYxp9MZ8GZrPZnu5vP5gv9EUDUODZA+fjlt0jOX+yr6gxjcfVgkTP11qYNGehJuzZvzwTaxdtZYdlerLrrbsbXO9rb9QJFHdwEu7vdDOjGi2WMz0nEgMAQZF4VHQZQAbKgAOwgN4hD0EwLDoBgABWVDEDwfAQAI6BASBICMMwrAYLASKcHB-DwKwQEALreEAA %}
