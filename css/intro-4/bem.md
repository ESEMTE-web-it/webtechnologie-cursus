# BEM-notatie

{% embed url="https://youtu.be/er1JEDuPbZQ" %}

## definitie BEM

De **Block, Element, Modifier**-methodologie, of kortweg **BEM,** is een populaire naamgevingsconventie voor klassen in HTML en CSS. Het heeft tot doel ontwikkelaars te helpen de relatie tussen HTML en CSS in een bepaald project beter te begrijpen. BEM heeft dus een reeks regels die helpen bij het begrijpen én onderhouden van CSS.

In onderstaand voorbeeld wordt getoond hoe een CSS-ontwikkelaar in de BEM-stijl zou kunnen schrijven:

```css
/* block component is hier 'de parent'*/
.btn {}

/* een element dat afhakelijk is van een block */ 
.btn__price {}

/* aanpassing die de stijl van de blok verandert */
.btn--red {} 
.btn--small {}
```

Een blok is hier een abstractie op het hoogste niveau van een nieuwe component, bijvoorbeeld een knop:`.btn {}`. Dit blok moet gezien worden als een parent.\
Onderliggende items of elementen kunnen erin worden geplaatst en deze worden aangegeven door twee onderstrepingstekens \_\_**\_\_** achter de naam van het blok, zoals `.btn__price {}`.\
Ten slotte kunnen modificatoren het blok manipuleren en aanpassen, zodat we van dat specifieke onderdeel de stijl kunnen aanpassen zonder wijzigingen aan te brengen aan een volledig niet-gerelateerde module. Dit wordt gedaan door twee koppeltekens **--** aan de naam van het blok toe te voegen, net als `.btn--red{}`.

Code zou er zo kunnen uitzien met bovenstaande in het achterhoofd:

```markup
<a class="btn btn--small btn--red" href="https://www.ap.be/">
  <span class="btn__price">12€</span>
  <span class="btn__text">Lid worden</span>
</a>
```

Als een andere ontwikkelaar deze opmaak zou geschreven hebben en CSS zou een onbekende zijn, dan nog is het vrij duidelijk welke klassen waarvoor verantwoordelijk zijn en hoe ze van elkaar afhankelijk zijn. Ontwikkelaars kunnen vervolgens hun eigen componenten bouwen en het bestaande blok naar hartenlust aanpassen. Op deze manier zijn ontwikkelaars zonder veel CSS te schrijven mogelijk in staat om veel verschillende combinaties van knoppen te maken door simpelweg een klasse in de opmaak te wijzigen:

{% embed url="https://flems.io/#0=N4IgZglgNgpgziAXAbVAOwIYFsZJAOgAsAXLKEAGhAGMB7NYmBvAHgwAJCAnGMAXgA6IEsQAOcRAHpJ1OHAC0xLhGoBrOPjpYh7alAxzBIAEbE0QgHwC07diziiMNvQbhHTaAPqfGAD2KWAMrETgAmGFyh7MYArsTE9CySDk5WaEkYadZsnDz8QiLiUjJyispqGlo6LoZCHtFm8vK0XE4A5jANaE3GEG2W1rb2js76tSZm3qLlMJYAJADMSSloaUMrumNudZM+MP6WAEJ90XEJ6ckjaRlZ6RzcvEaFEtKyCkoq6pq02iCbru4zF0elAYp0PD0+gMbHYNjVthMvJ5pipZiALHMACzLK6DWEjf7jDzePwBdHHNqneKJS6pbKSTLWbL3PJPeJFV6lD4Vb6-QkI+oQ+RtHhMYHyXr9dF44ZOfmApEo6hojEAThxdJhstGAJ2SNJRxOsWpFxW1wZFkoIDgMFg1GIEHoCEQIAAjAB2RCYkAAXwo6GwuBd+AAVggqHQGExiHhff6QJgcHhNHIrZHGMwXZIAFTsQ5QWhqdjZyTWfD1YB40nyUIwOitB30RDsND0GAAbjxxgwahFtBiaFC8joBa4zYA7oQIIxOzCRy1mwBiAAcq9ntmMLVrXHkrVCEBiEnYAFZRL51+x9w59ABPZsQNBQB8wCUFtQXrARNoP5uugAMZ4XmA9DEPIcAQAAXjAv7LoBVb7KBShOHAwFcFgzYxKIogwFw1AGB2eLAQw8jjjAfQkM2ABsf5-hejihPuaBtL+AG+CecFoD6TJoDm7AAKKwDgDDFqWaDlrsSqdJWMLdr2XD9oOw60KOE5TjOeLzmO7CLmAul0RgDEPm0u7kcQv4AEwcbY9GMcZsBgGZ7CupZ554p+XDft0yhtBR7DyP+gHsLxPAYE+bQ2Ma5zsKS7A2UZImESBJFkT5jnUbRXY9qofYDkOmlLgshUXrQjjUNOd7sPgmIXpukQ4buBkHkep5sX+7BtS1s5ceYPG5gJMBCcQCVicSez+Ow0nWQZtnNm1AWuTJW71XuTWzexbEte1XXcbxACytD7pAOHDeJ3QSick3sERoHgVBzbmbBC1TYZTEsVZV1JaRpnNpiNHbT1e0HRAR1cCdQrGKCUldktO75dpNHupiAAiqoXnDk7TgRMlZTlilw4uCPI6j1jddYgOHRAx0lmWQotO0UOLXVsPKQu2kAGJs5iroLJRaMs1pGPqdjckKXl-NLhzXM8-9ZO5vtFNU6Jp1NCKMBipdtXbkpKnaQsKOqu6GVzuL7CC1jG44-JuXa6zi566qBtG6TPWbqEN4TYlxFgNg0AVUIkCtGByHyOZQgUOwcDBzayhgDVluizbWmLtQKddVaNp2o2aDOiAlHHogrq+gAuj6QA" %}

## waarom BEM?

* Als een nieuwe stijl van een component gemaakt moet worden, kan makkelijk gezien worden welke modifiers en children er al bestaan. Het lijkt alsof er initieel geen CSS geschreven hoeft te worden, omdat er een reeds bestaande modifier is die doet wat nodig is.
* Als de markup gelezen wordt, is al snel duidelijk welk element afhankelijk is van een ander (in het vorige voorbeeld kan je zien dat `.btn__price` afhankelijk is van `.btn`)
* Ontwerpers en ontwikkelaars kunnen componenten consequent benoemen om de communicatie tussen teamleden te vergemakkelijken, aangezien BEM snel klaarheid en duidelijkheid brengt vanwege de syntax.

Door te werken met BEM geeft het ontwikkelaars zeker een standaard waarop in de toekomst betere en **beter te onderhouden code** kan geschreven worden. Een tweede aspect is dat **alles in BEM een klasse is en waarbij dus niets genest is**. Dat maakt CSS-specificiteit erg toegankelijk, wat een goed idee is.

## problemen met CSS?

Een CSS-selector wordt als volgt geschreven, maar voldoet niet aan de BEM-regels:

```css
.nav .nav__listItem .btn--orange {
  background-color: red;
}
```

In dit voorbeeld staan geneste selectoren en de modifier beschrijft niet echt wat er eigenlijk aan de hand is. Een blok zoals hier `.nav` overschrijft de stijlen van een ander blok of andere modifier zoals hier `.btn - oranje` wat binnen BEM niet mag. Anders wordt het bijna onmogelijk om de HTML te lezen en te begrijpen wat deze component echt doet. Zoiets als bovenstaande code schrijven zou ook de wenkbrauwen fronsen bij andere collega-ontwikkelaars.

Hetzelfde geldt voor HTML: wat te denken bij het zien van volgende opmaak?

```markup
<a class="btn" href="https://www.ap.be/">
  <div class="nav__listItem">item een</div>
  <div class="nav__listItem">item twee</div>
</a>
```

In bovenstaand voorbeeld werd waarschijnlijk een element binnen een volledig niet-gerelateerd blok code geplaatst, omdat de ontwikkelaar die code op dat moment net daar nodig had. De onderliggende elementen verwijzen naar een class `.nav` terwijl de parent een class `.btn` is (button). Dit kan niet binnen BEM en moet ten alle tijde vermeden worden. Kort samengevat:

* Nooit modifiers in een niet-gerelateerd blok overschrijven.
* Vermijd het maken van onnodige parent-elementen, als het child-element op zichzelf kan bestaan.

## voorbeelden BEM

**oefening** van een BEM-accordion met

* één blok `.accordion`
* twee elementen `.accordion__title` en `.accordion__copy`
* één modifier `.accordion__copy--open`

{% embed url="https://flems.io/#0=N4IgZglgNgpgziAXAbVAOwIYFsZJAOgAsAXLKEAGhAGMB7NYmBvAHgBMIA3AAmqgzhwAvAB0QGanQBOHemIB8ItN27suvfoNHjJtGRHoB9QxEZYFSlSpaEAzBoHCxE6bLTHip2NwBWcALSexLAKAEowGFDcADJ6MFjcAJIADnAArgkARgCe3LYA7HAQAOaYUHAsAPR2ispWLMkOWs66+kaGdMm5Lnpuxp3Z-v60yUy+AQMKAEK5aLTE3IQYnBBoxdzEhDDcEFgYxasYnvQbtDt7B2jbAO5LC5vbdAxMC2JYJSRi3JkwFNwY3DY8BKyieRSBUiOBmUEDg3CgtDgxHw3AAshE0Kt1j86Dg4bRMmA0nBqEcYGxvjBScTtmJTAByOE+Yn3GAAD2IYj+aTQEKRGF5GEy0FMuWKMGIcNxySktHecHJlOpCu4c0ytDYuSkESgEAAXorNkcNoRYRt2QskWkwGBuNcBP9qMQ0pEoLkcAL7mcftxtRg2CiAPLJZJ6Z2YzzwbjihYIpFKjA0k3bBHahIQVIZaMYKSZfbbI0LbK0NLcGkU1ZIiIU2i2v1RJ6MBiAiBsND0y1pYri+MjUNScOmCDwFEAFS25o5yeUMbheyBvp1bu4cD2UCgfxxiYVfwZcLmCw9zeI3u25b+12272KJH+cMv694fsY8No-vxtsLr84MGXt1M2xwMkEgwPgVTJLU1iVBwnCQdwliqDBTRODorjQsYAHmCAcHWHYyHaD0bTuIYQTeH4gReDACgAIK+gKbByhslFVDUCHWI0fCOARrR9B0Iy5ORkzYTMqrzIsyxYsm5z7IcxzKCe0mXDcdxSY2LzwSA16fCAlJ-ACQJFKUvD0OCMCQnJOxwnGyJohikk4nKUYEkSJJkhSW5JnSxCMr4LKTpylBlryZn8oKwq6sQYoSlKcoynKsKKh5KpqhqWo6vqhoqZssLgXBVQwXBCFqDwnHNKhvToSYZgWHUuH2KVKGEbxpHbORLU0XRvKMS1LG2DhqgcZojU8ZVAzjP4QnyCJB7iSsaxSbsMmYBZCmLUpdpZROanNm8HwBbp-yAsCRlgq2ZlQicZrWSi6ICvZVKOfihLEqSjDuVS260iAe6+fGjAclyQV8sQ9FCiKkXRtFxlYHF8qJR9SYpZqi6RBlFJftlFSVBBRXQVwhV1MV+EtGh7SYTVViqHhDXcaTxEteN7XYbRkJdQkPXVH1bEDcT5VEf0-HjZN01iUsc3rA8imydCpxS1cG3GpL22vJpe1fD8elHYZoImWd5ky1diI2bdmLzQ5eLcM5L1uQmnnfd5TJ+f9AXcsFUihWwYMRVFkrQ7DCXvcq2xI2lqMGujm05djeV47BCFFUhNMkxVZPVdh3M2PVQ20yn9OUYzlEdazDHs8xnP9Q0vNNaNguCfx0yzKLEnzZLa3Sycq0XKsymK1t9BNirWn7Rrh0GSCxloKZ+uXVZRs3XZZsPRbVuuW9tsql5PnMn9FqAzywOg+FoqQ770qynDgefaJ6rI-WaMmr3Uc44Tse1Pl+OUCACqwE60IIIgIAABMABWRAAA2EAABfCg6BsC4AAfgPwn9lZ4E4DmbgAASBmQhMEAAp6SIICC1ekABKAA3EoNBUhjJdCsDgghdcuj0goWgJQWDKL4D4BAagABrXBRI0C-xOLgkh3BgAIQwbgzGJD8BXA5LggYMi4C6iBKOWg3ZYAiJYSoSR0j8DAW1AwER+AiiZF1GsOAxjqCmigGwQxxi5HEGMcos6ABVZIWiELamdFIZQYBIgKhYZA8hn9v5Ujkv-EA+REC2CgTAkAmAcB4E4YIZB-cXjJOriccRdQ9hsn8NcVsmxEDcDAQABjKckNk2juB7CkJcEpAAWNM-w0gnhqYUtgxTuAAE4ykAFIalgH7v4fx7w3QlLEKESIMB7TZEBnAAUAQFRSAgGAGpeZeHFFlPvEpABiMAjTDmHKCUofAWS87BG2DklQwyGD+CKAaEpZT8D5DTDU52gRWZwGGVILAJS0ghjMqSQJCFYDEEYFIB5wFqBYhKYAqpNTgJsA4GsEpABGFp6L8DAPeQhTZPDtkll5Ps4BUxgEADEen5BqXQVMJT-yMFpWkd2egSmhlWJCj53yhz0BKfgWwcIIigrQJAs5FyPCUUQIQWgP5qE3O+BIQlOySXcD2Y0gAHI0zI+QaVKDFWgc5I12hjQVRwIC-BsglLmFcJF-pUXFAxVinFLTAHOtxfEWltB6XRkhNkGp5iYD+C2HtDF+AwFDJGY8mAGLGmIoQnc4gBSYChu4MAippzDUSr4l0IYIwxhmthMkS1JSzG0F4ZmpQSgb65AVQSoluy1WAObZm0Jv5wl-zwLYMBiAylQIALpUHMTw-+qAElwLwD4AAjmkMy2RCGfxZeQABJBiCpEQJUSoPJkiEs4XKSo07Z1SGyAAAUAfgbFtg8ZIgPTOudC6qCRVGHgEkqzkjEAHZAoAA" %}

**oefening** van een BEM-navigatie met

* één blok `.menu`
* 6 elementen `.menu__trigger` `.menu__row` `.menu__list` `.menu__link` `.menu__dropdown` `.menu__col`
* één modifier `.menu__trigger--active`

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8WCAyQA+ADp0ABDMHN4DGY2YBeSSABuZCAHcADtwBO8TTJ58IfDSD1kk8LGqQQdsCAFp7jrJql0glBkdADWMljGECRqAOQ48AZgqAD0KSS88GAYAObc3DkwDAZk2Ty4KbBgYAD8JEwUAJ5qAEoMMHoMjagALAAMfYQAjAOEAGyjAKwDsTJRUHFg8I2UIhDws8sGEHGIAB7wldWxAYIpImKnAEbcSI0BctKCSGRaFlAM1bbMdACuFiR-NI5IJlJForYAMTmWAfL6aH6-AD6SPgxjIORyEGMMgAVmBPGiMVjjEDZHJ5GR3p8wLYyLxPIx3AzjNxfnQkP4zmQHvIUgxecD5L8oNT4SBESjWXoyRT5MExbSEdZkUjgktZXL5GCojFNNCQIrviqUcEwv4AII3X7wM4CoUglLBXmPckghWwmnGv6m0pmEAuimgiK6qEwuFKiUmtUhUL+ABCUAKdsDZ2dDpkGaCVM94slMY1AYzIJ1EP14a9yp9MfNAYAwpkGAgU1mnTyhWcRYLyc9Xkaq6qkKyDEhuHpZLASHiCYjNSCXm9c5H8zwoHOg1gAEziABiZGMSxkbQ53FwMgAKmR4DAzlvAyCDOIADImCBnshJX5n0dJnFgK8yEw6yECoTAyCEMinnQEBgAAjr8ECQUYpiiPA4F0Esxi-Ag9LGCBNoyMwygQL8pS4LchEMLhX6Qbg0FwQhGAyAAkrIJFnrgNoMGh+5kL8UQgVo0DgUggEQPBiHBFc6JgOBuDbC88AgS8sDcTIUnYjISC-NwKgQExACi8EOG+MjwCY8HcdwskQHsMg6HsIHrDI8G6Vo3AeHwhHIPSsDokoiC4PhYD-LZMi-FcZASTI0BwGiYGWLCvz-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-lg9oGLXpLMyyg9zGMRsZkBxnlT7PAiBF-AC1PQeVvY+7N-9gHEWbi0FgFLy122S+l6x2X4HJhUd-NS+oZuGCMdtTL9jAwZPPJiWIt5IAhj9sSdkgAusQBDbzaA-PyegXEEljCNFqZwfiBB0AJCSKkFI7IDAwoBaeFIgeELB+DVV4VKSAlLGT0HkPRTiBbD+eAPyH4yk5LycwVgFU5a8GyDNgF1Qw-GAjyAKPyQ0g8FcBgGvk5Xb6BMKERPFRe915SFV4zQwjhgBSKPjC+KQiN6BSAIvrAlgrBYFk93WSgA" %}

In het voorbeeld van de BEM-navigatie worden blokken gemaakt zonder modifiers. Een ontwikkelaar kan in de toekomst altijd nieuwe modifiers gebruiken of eraan verbinden), zolang het blok maar consistent blijft.
