# extra oefeningen

## oefening: days-hours-and-minutes

**leerdoelen**

* gebruik maken van modulo

**functionele analyse**

Je programma werkt als een klok.

**technische analyse**

Je voorziet HTML-elementen voor het huidig aantal uur en minuten. Je voorziet ook HTML-elementen voor het aantal uur en minuten dat je hierbij wenst op te tellen. Deze extra waarden bij het huidigte tijdstip tellen kan het uur op 24 of meer brengen en kan het aantal minuten op 60 of meer brengen.

Geen enkele van deze ingevoerde gegevens mag leeg zijn. Indien dit toch het geval is, dan moet er een melding gegeven worden: “Vul zowel het startuur, startminuten als bij te tellen uur en minuten in”.

In de oorspronkelijke versie van deze oefening die je maakte in het eerste labo JavaScript, werd er enkel gevraagd om het nieuwe tijdstip weer te geven in uren en minuten. In deze opdracht dien je ook weer te geven of het nieuwe uur nog op dezelfde dag valt. Indien er meerdere dagen bijgeteld werden, dan moet dit ook aan de gebruiker worden meegedeeld.

Zorg er ook voor dat dit in het correct Nederlands wordt meegedeeld:

1 dag erbij geteld? Dan geeft het programma de melding “Dit is het tijdstip 1 dag later”.

Meerdere dagen bijgeteld? Dan geeft het programma weer “Dit is het tijdstip .... dagen later” (puntjes vervangen door het aantal dagen)

Geen dag bijgeteld? Dan verschijnt de melding “Dit tijdstip valt nog op dezelfde dag”. Tip: werk onderstaande voorbeelden eerst op papier uit. Gebruik in je code modulo en Math.floor.
