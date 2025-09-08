# Labo 13 - Conditionals

## Folderstructuur

Zorg ervoor dat je de volgende folderstructuur volgt:

```plaintext
webtechnologie/
├─ labo-x/
│  ├─ oefening-01/
│  │  ├─ index.html
│  │  ├─ assets/
│  │  │  ├─ image-1.jpg 
│  │  │  ├─ image-n.jpg 
│  │  ├─ css/
│  │  │  ├─ reset.css
│  │  │  ├─ style.css
│  │  ├─ js/
│  │  │  ├─ script.js
│  ├─ oefening-02/
│  ├─ oefening-n/
├─ labo-y/
├─ labo-z/      
```

### Belangrijke richtlijnen

- Gebruik altijd **JS modules** om globale variabelen te vermijden:
  ```html
  <script type="module" src="./path/to/script.js" defer></script>
  ```
- Schrijf JavaScript in **strict mode**:
  ```javascript
  "use strict";
  ```
- Volg de [Coding Guidelines](https://apwt.gitbook.io/webtechnologie/coding-guidelines)

---

## Oefening 1: Hello World!

{% hint style="info" %}
Als een oefening uit een deel "a" en een deel "b" bestaat, mogen beide in dezelfde map worden gemaakt.
{% endhint %}

### Oefening 1a: Lees informatie uit

#### Leerdoelen

- String interpolatie

#### Functionele analyse

Sla een voornaam, achternaam en leeftijd op in drie verschillende variabelen en druk deze informatie af in één boodschap.

#### Technische analyse

Schrijf een JavaScript-programma dat:

1. Drie waarden opslaat in aparte variabelen: voornaam, achternaam en leeftijd.
2. Een variabele aanmaakt met de zin:
   ```plaintext
   "U bent Voornaam Achternaam en u bent Leeftijd jaar oud."
   ```
   waarbij de voornaam en achternaam starten met een hoofdletter en de rest in kleine letters staat.
3. De resulterende boodschap weergeeft in de console met `console.log()`.

---

### Oefening 1b: Lees gevalideerde informatie uit

#### Leerdoelen

- String interpolatie
- Beslissingen maken (conditionals)

#### Functionele analyse

Het programma leest een naam, achternaam en leeftijd in en toont de informatie enkel als de invoer correct is.

#### Technische analyse

Schrijf JavaScript dat:

1. Drie variabelen inleest: voornaam, achternaam en leeftijd.
2. Controleert dat naam en achternaam niet leeg zijn.
3. Controleert dat de leeftijd tussen 12 en 60 jaar ligt.
4. Geeft passende meldingen bij ongeldige invoer:
    - **Naam/Achternaam ontbreekt:** "Vul zowel voornaam als achternaam in!"
    - **Leeftijd niet tussen 12 en 60:** "U behoort niet tot de gezochte leeftijdsklasse!"
5. Vormt de boodschap correct en toont deze met `console.log()`.

---

## Oefening 2: Schrikkeljaar

#### Leerdoelen

- Beslissingen maken

#### Functionele analyse

De website bevat een invoerveld voor een jaartal en jouw programma bepaalt of het een schrikkeljaar is.

#### Technische analyse

1. Een variabele bevat het jaartal.
2. Het programma bepaalt of het een schrikkeljaar is volgens de regels:
    - Een jaar is een schrikkeljaar als het deelbaar is door **4**,
    - Behalve als het deelbaar is door **100**, tenzij het ook deelbaar is door **400**.
3. Zet volgende flowchart om in code: ![](<../../.gitbook/assets/image (11).png>)

---

## Oefening 3a: Simpele Rekenmachine (if-statements)

#### Leerdoelen

- Beslissingen
- Geneste `if`-statements

#### Functionele analyse

Het programma voert een eenvoudige berekening uit met twee getallen en een operator (`+`, `-`, `*`, `/`).

#### Technische analyse

1. Twee variabelen bevatten de getallen.
2. Een derde variabele bevat de operator.
3. Gebruik `if`-statements om de juiste berekening uit te voeren.
4. Voer een controle uit zodat er niet door **0** wordt gedeeld.
5. Toon een foutmelding bij een ongeldige operator.

---

## Oefening 3b: Simpele Rekenmachine (switch-case)

#### Leerdoelen

- Beslissingen
- Gebruik van `switch`

#### Functionele analyse

Zelfde opdracht als oefening 3a, maar nu met een `switch`-statement.

#### Technische analyse

1. Gebruik een `switch`-constructie voor de operator-keuze.
2. Controleer dat delen door **0** niet gebeurt.
3. Toon een foutmelding bij een ongeldige operator.

---

## Oefening 4: Days, Hours and Minutes

#### Leerdoelen

- Gebruik van de **modulo-operator**

#### Functionele analyse

Het programma simuleert een klok die een tijdstip berekent na optelling van een bepaalde duur.

#### Technische analyse

1. De gebruiker voert een **startuur** en **startminuten** in.
2. Twee extra variabelen bevatten de uren en minuten die moeten worden opgeteld.
3. Controleer dat alle invoervelden ingevuld zijn.
4. Bereken het nieuwe tijdstip:
    - **Minuten overschrijden 60?** → Tel extra uren op.
    - **Uren overschrijden 24?** → Bereken hoeveel dagen erbij komen.
5. Geef de output correct weer:
    - "Dit tijdstip valt nog op dezelfde dag."
    - "Dit is het tijdstip **1 dag later**."
    - "Dit is het tijdstip **X dagen later**."
6. Gebruik **modulo (`%`)** en `Math.floor()` voor de berekening.

---

## Oefening 5: Cijfer omzetten naar tekst

### **Leerdoelen:**
- Switch-statements
- Beslissingen

### **Functionele analyse:**
Een student krijgt een cijfer (0-10). Het programma zet dit cijfer om in een tekstuele beoordeling.

### **Technische analyse:**
- Lees een cijfer in een variabele.
- Gebruik een switch-statement om het cijfer om te zetten naar:
    - 0-2: "Zeer slecht"
    - 3-4: "Onvoldoende"
    - 5-6: "Voldoende"
    - 7-8: "Goed"
    - 9-10: "Uitstekend"
- Als het cijfer buiten de 0-10 range ligt, geef dan een foutmelding.
- Toon het resultaat in de console.

---  

## Oefening 6: Omrekenen van graden

### **Leerdoelen:**
- Functies
- Rekenkundige operaties

### **Functionele analyse:**
Schrijf een programma dat temperaturen kan omrekenen tussen Celsius en Fahrenheit.

### **Technische analyse:**
- Vraag de gebruiker om een temperatuur en een eenheid (C of F).
- Gebruik een functie die:
    - Celsius omzet naar Fahrenheit met de formule: (C × 9/5) + 32
    - Fahrenheit omzet naar Celsius met de formule: (F - 32) × 5/9
- Toon de omgezette waarde in de console.
- Geef een foutmelding als de eenheid niet correct is ingevoerd.

---  

## Oefening 7a: Getal raden

### **Leerdoelen:**
- Beslissingen
- Willekeurige getallen

### **Functionele analyse:**
Kies zelf een willekeurig getal tussen 1 en 10 en sla deze op in een variabele "answer". De gebruiker moet raden welk getal het is.

### **Technische analyse:**
- Genereer een willekeurig getal tussen 1 en 10.
- Vraag de gebruiker om een gok (simuleer dit met een variabele).
- Controleer of het getal juist is:
    - Zo ja, toon: "Gefeliciteerd, je hebt het juiste getal geraden!"
    - Zo nee, toon: "Helaas, het juiste getal was X."
- Toon het resultaat in de console.

## Oefening 7b: Willekeurig getal

### **Leerdoelen:**
- Willekeurige getallen

### **Functionele analyse:**
Genereer een willekeurig getal tussen 1 en 10 en sla deze op in een variabele "answer". De gebruiker moet raden welk getal het is.

### **Technische analyse:**
- Genereer een willekeurig getal tussen 1 en 10 en sla deze op in een variabele "answer".
- Vraag de gebruiker om een gok (simuleer dit met een variabele).
- Controleer of het getal juist is:
    - Zo ja, toon: "Gefeliciteerd, je hebt het juiste getal geraden!"
    - Zo nee, toon: "Helaas, het juiste getal was X."
- Toon het resultaat in de console.

{% hint style="info" %}

Om een willekeurig getal te genereren kun je gebruik maken van de `Math.random()` functie. Deze functie zal altijd een kommagetal teruggeven. Met de volgende functie kun je dit willekeurig kommagetal omzetten naar een geheel getal tussen twee getallen:
```Math.floor(Math.random() * (maximumGetal - minimumGetal) + minimumGetal)```

Sla de [MDN documentatie van Math.random()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) er op na
{% endhint %}