## iReporter API V1


[![Build Status](https://travis-ci.org/Elisha-Misoi/iReporter_V1.svg?branch=develop)](https://travis-ci.org/Elisha-Misoi/iReporter_V1) [![Coverage Status](https://coveralls.io/repos/github/Elisha-Misoi/iReporter_V1/badge.svg?branch=develop)](https://coveralls.io/github/Elisha-Misoi/iReporter_V1)
[![Maintainability](https://api.codeclimate.com/v1/badges/44e98a10cabd9b6b4d34/maintainability)](https://codeclimate.com/github/Elisha-Misoi/iReporter_V1/maintainability)

Corruption is a huge bane to Africa’s development. African countries must develop novel and localised solutions that will curb this menace, hence the birth of iReporter. iReporter enables any/every citizen to bring any form of corruption to the notice of appropriate authorities and the general public. Users can also report on things that needs government intervention.


## Features
1. Users can create an account and log in.
2. Users can create a ​ red-flag ​ record (An incident linked to corruption)
3. Users can create ​ intervention​​ record​ ​ (a call for a government agency to intervene e.g repair bad road sections, collapsed bridges, flooding e.t.c).
4. Users can edit their ​ red-flag ​ or ​ intervention ​ records.
5. Users can delete their ​ red-flag ​ or ​ intervention ​ records.
6. Users can add geolocation (Lat Long Coordinates) to their ​ red-flag ​ or ​ intervention records​ .
7. Users can change the geolocation (Lat Long Coordinates) attached to their ​ red-flag ​ or intervention ​ records​ .
8. Admin can change the ​ status​​ of a record to either ​ under investigation, rejected ​ (in the event of a false claim)​ ​ or​ resolved ( ​ in the event that the claim has been investigated and resolved)​

## Demo

Project API demo is hosted at [Heroku](https://ireporter-api-v1.herokuapp.com)

### API endpoints

Prefix `api/v1/` to all api endpoints below

| **HTTP METHOD**   | **URI**  | **ACTION** |
|---|---|---|
|  **POST** |  `/red-flags` | post a red-flag |
|  **GET** |  `/red-flags` | get list of all red-flags |
|  **GET** |  `/red-flags/<int:redflag_id>` | fetch red-flag records by `redflag_id` field |
|  **PATCH** |  `/red-flags/<int:redflag_id>/location` | edit redflag location `incident_id` field |
|  **PATCH** |  `/red-flags/<int:redflag_id>/comment` | edit redflag comment `incident_id` field |
| **DELETE**  |  `/red-flags/<int:redflag_id>` | delete redflag record with given `redflag_id` |
|  **POST** |  `/incidents` | post an incident |
|  **GET** |  `/incidents` | get list of all incidents |
|  **GET** |  `/incidents/<int:incident_id>` | fetch incident records by `incident_id` field |
| **DELETE, GET, PUT**  |  `/incidents/<int:incident_id>` | get, delete and update incident records with given `incident_id` |
|  **POST** |  `/users` | create a new user |
|  **DELETE, GET, PUT** |  `/users/<int:user_id>` | get, delete and update user with given `user_id`|
|  **GET** |  `/users` | fetch all users |


### Running Tests
- Install nosetests
- Navigate to project root
- Use `nosetests app/tests/` to run the tests

