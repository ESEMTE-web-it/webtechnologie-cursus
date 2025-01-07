# lijsten

Opsomminglijsten zijn een belangrijk element voor de indeling van een pagina. HTML beschikt over vijf verschillende soorten waarvan we er drie bespreken. Je kan lijsten altijd in elkaar verwerken en zo met sublijsten werken.

## ongeordende lijst

In een ongeordende lijst hebben de items een symbool als markering. De ongeordende lijst wordt gemaakt met de elementen `<ul>` en `<li>`.

Bij dit soort lijsten is de volgorde van de opgesomde items van geen enkel belang.

```html
<ul>
   <li>Dit is een item van de ongeordende lijst</li>
   <li>Dit is een item van de ongeordende lijst</li>
   <li>Dit is een item van de ongeordende lijst</li>
</ul>
```

## geordende lijst

In een geordende lijst zijn de items genummerd met behulp van een getal of een letter. De geordende lijst wordt gemaakt met de elementen `<ol>` en `<li>`.

We gaan gebruik maken van het `<ol>`element wanneer de volgorde of waarde van de opgesomde items wel van belang is.

```html
<ol>
   <li>Dit is het eerste item van de geordende lijst</li>
   <li>Dit is het tweede item van de geordende lijst</li>
   <li>Dit is het derde item van de geordende lijst</li>
</ol>
```

## definitielijst

Een definitielijst is een lijst, welke bestaat uit termen en bijbehorende beschrijvingen. Het `<dl>`-element bepaalt het begin en einde van een definitielijst en de elementen `<dt>` en `<dd>` definiëren respectievelijk de term en de beschrijving.

```html
<dl>
   <dt>Term 1</dt>
   <dd>Hier staat de definitie van term 1</dd>
   <dt>Term 2</dt>
   <dd>Hier staat de definitie van term 2</dd>
</dl>
```
