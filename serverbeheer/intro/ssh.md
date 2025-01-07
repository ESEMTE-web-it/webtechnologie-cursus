# SSH

Het gebruik van Secure Shell (SSH) voor het beheer van je website is een modernere en veiligere benadering ten opzichte van FTP. SSH biedt een versleutelde verbinding voor het overbrengen van bestanden en het uitvoeren van commando's op een externe server. Hier zijn enkele voor- en nadelen van het werken met SSH, gevolgd door een uitleg over hoe je SSH kunt gebruiken.

## voordelen van SSH:

### veiligheid

SSH versleutelt de gegevensoverdracht tussen je computer en de server, waardoor het moeilijker wordt voor kwaadwillenden om gevoelige informatie te onderscheppen.

### command line functionaliteit

Met SSH kun je niet alleen bestanden overbrengen, maar ook opdrachten uitvoeren op de server. Dit biedt meer flexibiliteit en controle over serverconfiguraties en -taken.

### sleutelauthenticatie

SSH ondersteunt sleutelauthenticatie, wat betekent dat je geen wachtwoorden hoeft in te voeren bij elke verbinding. Dit verbetert de beveiliging en gebruiksvriendelijkheid.

### poortdoorsturing

SSH maakt het mogelijk om poortdoorsturingen in te stellen, waardoor je veilig specifieke services op de server kunt benaderen.

## nadelen van SSH:

### leercurve

Voor beginners kan de opdrachtregelinterface van SSH intimiderend lijken. Het vergt wat tijd om vertrouwd te raken met de commando's en functionaliteiten.

### toegangsniveau

SSH vereist meestal geavanceerdere toegangsrechten dan FTP. Dit betekent dat je mogelijk de juiste rechten moet verkrijgen van je hostingprovider.

### configuratie vereist

Het opzetten van SSH-toegang vereist configuratie op de server, en sommige hostingproviders hebben standaard geen SSH-toegang ingeschakeld.

## werken met SSH:

Het gebruik van SSH vergt wat initieel werk, maar het biedt een veiligere en krachtigere manier om je website te beheren. Zodra je bekend bent met de basiscommando's, zal SSH je veel controle geven over je serveromgeving.

### verbinden met de server

Open een terminalvenster en gebruik het volgende commando om verbinding te maken met de server:

```bash
ssh gebruikersnaam@jouw-server-ip
```

### bestanden overbrengen

Gebruik het `scp` commando om bestanden naar de server te kopiëren of van de server naar je lokale machine te halen:

```bash
scp jouw-bestand.txt gebruikersnaam@jouw-server-ip:/pad/op/de/server/
```

### commando's uitvoeren op de server

Gebruik de SSH-verbinding om opdrachten direct op de server uit te voeren:

```bash
ssh gebruikersnaam@jouw-server-ip 'commando'
```

### sleutelauthenticatie instellen

Genereer een SSH-sleutelpaar op je lokale machine met het `ssh-keygen` commando en kopieer de openbare sleutel naar de server:

```bash
ssh-copy-id gebruikersnaam@jouw-server-ip
```
