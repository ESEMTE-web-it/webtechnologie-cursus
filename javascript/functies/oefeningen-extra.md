# extra oefeningen

## oefening: bubble-sort

**leerdoelen**

* gebruiken van lussen
* schrijven van eigen functies
* arrays

**functionele analyse**

Je programma sorteert een array van getallen

**technische analyse**

Je maakt een array aan van getallen in een willekeurige volgorde. Je geeft deze array de naam `getallen`.

Voor een array te kunnen sorteren kan je best 3 functies aanmaken:

* Je maakt een functie `isSorted` die een array van getallen als parameter aanvaardt en true teruggeeft als de array in stijgende volgorde staat en false als dit niet zo is. Je kan dit op de volgende manier doen:
  * Je maakt een lus over elk element van de array
  * Je vergelijkt dan het huidige element (i) met het volgende element (i+1).
    * Als element `i` groter is dan element `i+1`, dan is de array niet gesorteerd en geef je `false` terug.
    * Als dit niet zo is dan staan deze elementen op volgorde en ga je gewoon door met de lus.
  * Als alle elementen op volgorde stonden geef je `true` terug.
  * Probeer de functie uit op een zelfgekozen array
* Je maakt een functie `swapElements` die een array van getallen als parameter aanneemt en een array van getallen teruggeeft.
  * Je maakt een lus over elk element van de array
  * Je vergelijkt dan het huidige element (i) met het volgende element (i+1)
    * Als element `i` groter is dan element `i+1` dan wissel je het om in de array.
    * Anders laat je het element staan.
  * Op het einde geef je de array terug als return waarde.
* Je maakt een functie `sort` die een array van getallen als parameter aanneemt en een array van getallen teruggeeft.
  * Voer de `swapElements` functie uit zolang de array niet volledig gesorteerd is.
  * Zorg ervoor dat het resultaat van `swapElements` altijd de vorige array vervangt.

**voorbeeldinteractie**

```
Unsorted: 
[
  5, 1, 4, 2, 8,
  1, 2, 6, 3, 2
]
Sorted: 
[
  1, 1, 2, 2, 2,
  3, 4, 5, 6, 8
]
```
