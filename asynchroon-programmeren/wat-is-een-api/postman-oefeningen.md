# oefeningen

## oefeningen

### oefening 1: basis api request

**leerdoelen**

* Verkenning van het maken van een eenvoudig GET-verzoek naar een openbare API.

**functionele analyse**

1. **API:** [**JSONPlaceholder**](https://jsonplaceholder.typicode.com/)
2. Endpoint: `/posts`
3. Doel: Haal alle berichten op.

**technische analyse**

1. Open Postman.
2. Maak een nieuw verzoek naar de API.
3. Gebruik de endpoint `/posts`.
4. Voer het verzoek uit en bekijk de JSON-respons.

### oefening 2: query parameters

**leerdoelen:**

* Werken met query parameters bij een API-verzoek.

**functionele analyse:**

1. **API:** [**PokeAPI**](https://pokeapi.co)
2. Endpoint: `/generation`
3. Doel: Haal generatie 1 uit Pokémon op.

**technische analyse:**

1. Maak een nieuw verzoek naar de API.
2. Gebruik de endpoint `/generation`.
3. Voeg de query parameter `id` toe voor de eerste generatie.
4. Voer het verzoek uit en analyseer de respons.

### oefening 3: post-verzoek

**leerdoelen:**

* Een POST-verzoek maken.

**functionele analyse:**

1. **API:** [**JSONPlaceholder**](https://jsonplaceholder.typicode.com/)
2. Endpoint: `/posts`
3. Doel: Maak een nieuw bericht aan.

**technische analyse:**

1. Maak een nieuw verzoek naar de API.
2. Gebruik de endpoint `/posts`.
3. Stel de body in als raw JSON met de benodigde gegevens.
4. Voer het verzoek uit en controleer of het nieuwe bericht is toegevoegd.

### oefening 4: authentificatie met api key

**leerdoelen:**

* Gebruik van een API-sleutel voor toegang.

**functionele analyse:**

1. **API:** [**News API**](https://newsapi.org/)
2. Endpoint: `/top-headlines`
3. Doel: Haal nieuws op met een API-sleutel.

**technische analyse:**

1. Maak een nieuw verzoek naar de API.
2. Gebruik de endpoint `/top-headlines`.
3. Voeg een `X-Api-Key` header toe met je API-sleutel.
4. Voer het verzoek uit en bekijk de respons.

### oefening 5: werken met authentication token

**leerdoelen:**

* Gebruik van een authentication token.

**functionele analyse:**

1. **API:** [**Auth0 Management API**](https://auth0.com/docs/api/management/v2)
2. Endpoint: `/users`
3. Doel: Haal alle gebruikers op.

**technische analyse:**

1. Maak een nieuw verzoek naar de API.
2. Gebruik de endpoint `/users`.
3. Voeg een `Authorization` header toe met een Bearer Token.
4. Voer het verzoek uit en bekijk de lijst met gebruikers.

## extra oefeningen

Ga op zoek naar enkele leuke, interessante API's die vrij toegankelijk zijn en onderzoek de werking van deze API's.
