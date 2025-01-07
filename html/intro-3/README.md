# 4: tabellen

In HTML kan informatie getoond worden in tabellen. Tabellen maken het mogelijk om complexe data visueel overzichtelijk weer te geven. Je kan een tabel in HTML maken met het `<table>`-element. In deze tabel kan je dan rijen aanmaken met het `<tr>`-element (**t**able **r**ow) en kolommen in deze rijen met het `<td>`-element (**t**able **d**ata). De `<td>`-elementen definiëren dus de cellen van de tabel.

Op deze manier kunnen we al een simpele tabel opstellen:

```html
<table>
    <tr>
        <td>linksboven</td>
        <td>rechtsboven</td>
    </tr>
    <tr>
        <td>linksonder</td>
        <td>rechtsonder</td>
    </tr>
</table>
```

{% hint style="info" %}
De `<td>`-element staat altijd binnenin de `<tr>`-element en niet andersom. De tabel wordt dus rij per rij opgebouwd.
{% endhint %}

## titels

We kunnen aan onze tabel nu ook titels toevoegen door gebruik te maken van het `<th>`-element (**t**able **h**ead) i.p.v. het `<td>`-element.

Een tabel met titels:

```html
<table>
    <tr>
        <th></th>
        <th>Zaterdag</th>
        <th>Zondag</th>
        <th>Totaal</th>
    </tr>
    <tr>
        <th>Verkochte tickets:</th>
        <td>110</td>
        <td>140</td>
        <td>250</td>
    </tr>
    <tr>
        <th>Inkomsten:</th>
        <td>660</td>
        <td>850</td>
        <td>1450</td>
    </tr>
</table>
```

## buitenformaat cellen

Het is mogelijk om cellen meerdere rijen of kolommen te laten innemen met de `colspan`- en `rowspan`-attributen. Dit wordt op volgende manier toegepast:

### colspan

```html
<table>
    <tr>
        <th></th>
        <th>9u</th>
        <th>10u</th>
        <th>11u</th>
        <th>12u</th>
    </tr>
    <tr>
        <th>Maandag</th>
        <td colspan="2">Netwerken</td>
        <td>Linux</td>
        <td>Webtech</td>
    </tr>
    <tr>
        <th>Dinsdag</th>
        <td colspan="3">Webtech labo</td>
        <td>IT-esentials</td>
    </tr>
</table>
```

try it yourself: [https://www.w3schools.com/html/tryit.asp?filename=tryhtml\_table\_colspan](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_table_colspan)

### rowspan

```html
<table>
    <tr>
        <th>Lokaal:</th>
        <th>-01.006</th>
        <th>-01.007</th>
        <th>-01.008</th>
    </tr>
    <tr>
        <th>18-19h</th>
        <td rowspan="3">Linux</td>
        <td rowspan="2">Webtech</td>
        <td>IT-essentials</td>
    </tr>
    <tr>
        <th>19-20h</th>
        <td rowspan="2">Elektronica</td>
    </tr>
    <tr>
        <th>20-21h</th>
        <td>communicatie</td>
    </tr>
</table>
```

try it yourself: [https://www.w3schools.com/html/tryit.asp?filename=tryhtml\_table\_rowspan](https://www.w3schools.com/html/tryit.asp?filename=tryhtml_table_rowspan)

## tabel onderdelen

Een goede tabel bestaat uit een head, body en foot. Deze worden gedefinieerd door de `thead`- , `tbody`- en `tfoot`-elementen. In de head zet je alle titels van de kolommen, in body de data, en in foot de opsomming van de data in de cellen.

{% hint style="info" %}
De onderdelen `thead` , `tbody` en `tfoot` zijn eigenlijk altijd aanwezig bij het maken van een `<table>`. Als jij ze er niet zet, zal de browser dit voor jou invullen.
{% endhint %}

```html
<table>
    <thead>
        <tr>
            <th>Datum</th>
            <th>Inkomsten</th>
            <th>Uitgaven</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>1 mei</th>
            <td>300</td>
            <td>200</td>
        </tr>
        <tr>
            <th>2 mei</th>
            <td>350</td>
            <td>150</td>
        </tr>
        <tr>
            <th>3 mei</th>
            <td>400</td>
            <td>350</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th>Totaal</th>
            <td>1050</td>
            <td>700</td>
        </tr>
    </tfoot>
</table>
```

try it yourself: [https://www.w3schools.com/tags/tryit.asp?filename=tryhtml\_tbody](https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_tbody)

## tabel titel

Je kan ook nog een titel toevoegen aan je tabel met het `caption`-element. Dan wordt onze eerdere tabel vervolledigd als:

```html
<table>
    <caption>Inkomsten tabel</caption>
    <thead>
        <tr>
            <th>Datum</th>
            <th>Inkomsten</th>
            <th>Uitgaven</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th>1 mei</th>
            <td>300</td>
            <td>200</td>
        </tr>
        <tr>
            <th>2 mei</th>
            <td>350</td>
            <td>150</td>
        </tr>
        <tr>
            <th>3 mei</th>
            <td>400</td>
            <td>350</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th>Totaal</th>
            <td>1050</td>
            <td>700</td>
        </tr>
    </tfoot>
</table>
```

try it yourself: [https://www.w3schools.com/tags/tryit.asp?filename=tryhtml\_caption\_test](https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_caption_test)

{% hint style="info" %}
Het `<caption>`-element moet altijd als eerste element binnen de `<table>` staan.
{% endhint %}

## tabellen opmaken in html

Alvorens het bestaan van CSS werden websites opgemaakt met behulp van tabellen. Er waren dus enkele attributen voorzien voor het opmaken van tabellen in de HTML-standaarden voor HTML5. Sinds HTML5 zijn deze attributen echter verwijderd. Toch worden ze nog gebruikt in toepassingen zoals e-mail campagnes omdat de meeste e-mail clients geen CSS ondersteunen.
