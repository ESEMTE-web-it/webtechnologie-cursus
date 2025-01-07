# FTP

Om je statische website online te zetten, kun je gebruikmaken van het File Transfer Protocol (FTP), een standaardmethode voor het overbrengen van bestanden naar een webserver. FileZilla is een populaire, gratis FTP-client die een intuïtieve interface biedt. Hier is een stapsgewijze handleiding voor het gebruik van FileZilla om je website naar een server te uploaden.

## stap 1: download en installeer FileZilla

Ga naar de officiële [FileZilla-website](https://filezilla-project.org/) en download de client. Installeer de software op je computer volgens de instructies op de website.

## stap 2: verzamel FTP-inloggegevens

Voordat je begint, verzamel de FTP-inloggegevens van je webhostingprovider. Deze gegevens omvatten meestal:

* **Hostnaam (of IP-adres):** Dit is het adres van je webserver.
* **Gebruikersnaam en Wachtwoord:** De inloggegevens voor je FTP-account.

## stap 3: open FileZilla en configureer de verbinding

1. Start FileZilla en ga naar `File > Site Manager`.
2. Klik op "New Site" en geef je site een naam.
3. Voer de hostnaam, gebruikersnaam, wachtwoord en poort in onder de "General" tab.
4. Klik op "Connect" om de verbinding te testen. Als het lukt, kun je doorgaan naar de volgende stap.

## stap 4: navigeer naar de lokale en serverbestanden

1. In de linkerhelft van FileZilla zie je de lokale bestanden op je computer. Navigeer naar de map waarin je websitebestanden zich bevinden.
2. In de rechterhelft zie je de bestanden op de server. Dit zijn waarschijnlijk lege of standaardmappen.

## stap 5: upload je bestanden

1. Selecteer de bestanden en mappen op je lokale computer die je wilt uploaden.
2. Sleep deze bestanden naar de gewenste locatie op de server of gebruik de uploadknop in de toolbar.

## stap 6: wacht tot het uploaden voltooid is

FileZilla geeft de voortgang weer terwijl het je bestanden naar de server uploadt. Wacht tot alle bestanden zijn overgezet.

## stap 7: controleer je website online

Open een webbrowser en ga naar de URL van je website. Als alles correct is geüpload, zou je je website online moeten zien.

## extra tips:

* **mapstructuur behouden:** Zorg ervoor dat je de mapstructuur op de server behoudt om links en verwijzingen binnen je website goed te laten werken.
* **index bestand:** Zorg ervoor dat je hoofdpagina (bijv. `index.html`) aanwezig is, zodat dit automatisch wordt geladen wanneer iemand jouw domein bezoekt.
