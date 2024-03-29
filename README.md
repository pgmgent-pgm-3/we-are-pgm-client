# We are PGM

**PGM evolves.**  
_Dat verdient een stevige introductie, en hoe kunnen we dat beter aanpakken dat data-gewijs een webpage vullen._

## CRUD van studenten

Deze endpoints bestaan in de studenten API van Graduaat Programmeren.

```
API_URL     https://pgm.cmsdevelopment.be/api
  GET /student -> haalt studenten op
  POST /student -> bewaren van een student
  PUT /student/{UUID} -> updaten van een student
  DELETE /student/{UUID} -> verwijderen van een student
```

### Ophalen van studenten (of superhelden)

Ontwikkel een script dat alle studenten ophaalt via een `GET`-request uit de API via volgend endpoint.
Om data op te hamen, kan je tijdelijk met superhelden werken, zolang er nog geen studenten zijn.

```
API_URL     https://pgm.cmsdevelopment.be/api
  GET /superhero -> haalt superhelden op
  GET /student -> haalt studenten op
```
*Ter info, deze superhero API heeft enkel een `GET`-request.*

#### Weergave van studenten

Breng de gegevens van de studenten (of tijdelijk superheroes) in de DOM. Er staat al één voorbeeldje in `index.html` hoe een volledig student-element opgebouwd is.

## Creatie van een student

Maak een script aan dat een `POST`-request uitvoert naar de API. De request moet een JSON-object bevatten met de gegevens van de student. De API zal een `UUID` teruggeven die je kan gebruiken om de student later te updaten of te verwijderen.

Maak een JSON-object aan waarin alle interessante details over jezelf in aanwezig zijn. De JSON moet minstens volgende informatie bevatten

    firstname : string
    lastname : string
    nickname : string
    classname : string // 1PGM-a, 1PGM-b, 1PGM-c
    email : string
    age : number
    avatar : string // link naar de afbeelding, gebruik een service als https://postimg.cc/
    hobbies : array
    motto : string // een motto die jou typeert
    about : string // stel jezelf kort voor

Schrijf een script (welke je later uitvoert via `node.js`) waarbij je deze JSON via een `POST`-request verstuurt naar volgende `API`

### Maak het formulier functioneel

Onderaan de pagina staat een formulier. Maak dit formulier functioneel zodat je via de webpagina een student kan toevoegen. De gegevens van de student moeten via een `POST`-request naar de API gestuurd worden.

## Updaten van een student

Maak een script aan dat een `PUT`-request uitvoert naar de API. De request moet een JSON-object bevatten, en de UUID steek je in de URL.

vb van een mogelijke endpoint
```
PUT /student/{UUID} -> updaten van een student
vb: PUT https://pgm.cmsdevelopment.be/api/student/1234-5678-91011-1213
```

vb van een mogelijk JSON-object
```json
{
  "firstname": "John",
  "lastname": "Doe",
  "nickname": "JD",
}
``` 
## Verwijderen van een student

Maak een script aan dat een `DELETE`-request uitvoert naar de API. De UUID steek je in de URL.

vb van een mogelijke endpoint
```
DELETE /student/{UUID} -> verwijderen van een student
vb: DELETE https://pgm.cmsdevelopment.be/api/student/1234-5678-91011-1213
```
