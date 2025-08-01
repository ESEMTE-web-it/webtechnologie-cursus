# box model

Elk HTML-element bevind zich in een **denkbeeldige box**, [dé CSS box](https://www.w3schools.com/css/css_boxmodel.asp). Die rechthoekige box heeft een marge (**margin**), een rand (**border**) en een opvulling (**padding**). Voor zowel margin, border en padding kunnen telkens de vier zijden bepaald worden. Van binnen naar buiten bestaat de CSS-box uit:

* de inhoud van het element (content)
* [padding](https://www.w3schools.com/css/css_padding.asp)
* [border](https://www.w3schools.com/css/css_border.asp)
* [margin](https://www.w3schools.com/css/css_margin.asp)

![CSS-box](../../.gitbook/assets/box-model.png)

## box modellen (box-sizing)

Er zijn verschillende manieren waarop de browser kan omgaan met de CSS-regels afhankelijk van het model dat je specifieert.

### content-box

In het **W3C box model** is de breedte van een element gelijk met de inhoud van het element. De breedte van de box is dus breedte van de inhoud zonder rekening te houden met de padding en border.

![CSS content box model](../../.gitbook/assets/content-box.png)

```css
/* Bij het berekenen van de grootte van een box moeten padding en border 
erbij opgeteld worden om de hoogte en breedte van het element te berekenen.*/
* {
    box-sizing: content-box
}
```

### border box

In het **traditionele box model** is de breedte van een element gelijk aan de breedte van border tot border. Dus de breedte van een element is gelijk aan de breedte van de inhoud, plus de breedte van de padding en die van de border. Met uitzondering van IE in "Quirks Mode" (IE5.5 Mode) gebruiken alle browsers het traditionele box-model.

{% hint style="info" %}
Het is een industrie-standaard om altijd met border-box te werken!
{% endhint %}

![CSS border box model](../../.gitbook/assets/border-box.png)

```css
/* Met de box-sizing eigenschap kan bepaalt worden hoe boxen gemeten worden.*/

/* Padding en border worden meegerekend in de hoogte en breedte van een element. 
Deze is de meest intuïtieve manier om met boxen te werken.*/
* {
    box-sizing: border-box
}
```

### toepassing: flexible inputs

Met border-box kunnen zowel padding als width met gemengde eenheden ingesteld worden zonder rare neveneffecten. Een handige toepassing hiervan is het creëren van flexibele input elementen met een vaste padding-grootte.

In onderstaand voorbeeld heeft het input element een welbepaalde padding in ems en toch kunnen we een width opgeven in percenten:

```css
input[type="text"] {
   /* Flexibility */
   box-sizing: border-box;
   width: 100%;
   /* Styling */
   padding: .4em .55em;
   font-size: inherit;
   font-family: inherit;
   color: inherit;
   border: 0;
   border-radius: .25em;
   outline: none
}
```

{% embed url="https://flems.io/#0=N4IgZglgNgpgziAXAbVAOwIYFsZJAOgAsAXLKEAGhAGMB7NYmBvAHjFoCcsA+AHTQAEAlgAduAIVoAPFgHox-ISwhoRAV2IDqUDHDgBeXuFhSIAI1gBaFeuJGBxAJ4iYhkIyl2QsvmjnsuXxYAEwgAN18lGw0HZ1cjDgw0AHMYe21dAyNo4ks4KAhgmA57LBU3ACYABlKMKTcARiqakAEwjCg1eJAAdgBWI0jhOBEk7hY6Iu4Ad0LiQgEIOAE0WmnEYdHBDL03fMLiy3bOtJBufoBSORGxuUmYcdkbtCHRbgAVQhgBUeDQlIEtDADi+AgCWEWywaMCw+DkCkE-DkoQilBAcBgsGoxAg9AQiBAAE5EAA2EAAXwo6GwuAJ+AAVggqHQGExiHhgrRqGocAx8ABHLocRwAZUxMGxnAAFAByfA5PIFIocGUASnwGD+AFEwmyADJLRhoYqy6iEJKpGUUMFqNDY3FoKUwVXARRtDAcASzYLzAT6AQwfDED2pYj4Y5dACCcAAcjyzMUBABqAQyi4ygDcbs53N5YcFxVF4slHFl+H2yqOHS6avlaGNHAAEu8ALJ6v1euaELOCASRjiJRz4EQcWjEMdxcsFaiB6gdKBSnM8tkCoVFrHjjiRqALuVgEzmKw5NXqgJajBmqVgW32+hSszSF1uoQPqTlpywfDe33+7-dt3kqqPaARmaIYhuDr4iAJKIAAzBSVIgJgOB4Pg1B6GiLJGuyBIAFTWrhiAJgEMAEYgGBgIwnqur2QiWNMMBmAA1hAuSvnkEAAF4qMkGwPhwlavhmAiyLhAgxjAMBFMEYKcAIWC0GY0DfAA6oxADSrECLhsjPgIlgKZxljsXAXE8XxnCCdIwmieJknSbJnoAGIQBwMDsFI2m6bRAgmWZKQWQJhyvvw5L8PwJBkNaD7BI4Ag0UIf4bE0VQXD2QhfBAyQkMlzRpW67AMBxnEwLlqXAeFaDgvFbpmBeTHJKOtrBJYdBQJwGyNRgjjpZ2PqEGV+W9pl2XEBsAAs5Vur8-y8QI0JYBVaC2WYo5oBsnzfFgGDJBA1CAsCADCIoigIJDECIiCyLImrYHAZrTB6xCcWhtCyNtu3UJYQKtXoshmhgIhUXAsgNJY8wwMZ0iyF5-A5MgTguG4HheAAujVPm2U5B5KQUTiwz5SXzXlPZ6bZIofjxBNCEIM3mQI+DjTCDN9H0MK9UIhW5KZJUbCoXwcKxHOyUVYDYNAjh82gAtC3pbUdYs0vFLLPn8cqGxVMLauHIkoRqHAGz4BUbOLXptAaAUxobKsxqhWBxY4nieCwQ0iANBSqPkkAA" %}

meer info: [https://adamschwartz.co/magic-of-css/chapters/preface/](https://adamschwartz.co/magic-of-css/chapters/preface/)\\
