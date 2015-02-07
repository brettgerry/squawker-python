# AlertRequests

You can create TFR Alert Requests to register a phone number to receive text and picture messages (SMS and MMS) when restricted airspace pops up near a certain airport. Optionally, you can specify a radius and/or destination and alerts will be sent if the restricted airsapce is within a certain range along that path.

Squawker checks for new TFR's every 10 minutes and sends an MMS message with the type of TFR, a link to the FAA description of the TFR, and an image of the diagram on a VFR sectional map.


To create a new alert request you make an HTTP **POST** request to the list resource url,
~~~/Accounts/{Account SID}/AlertRequests

#### Example: Register the number 555-867-5309 to receive an alert if a TFR pops up within a 200 nm radius of Montgomery Field

    curl -XPOST -u "username:password" https://api.squawker.io/Accounts/ACC1234567/AlertRequests /
        -d "origin=KMYF"
        -d "phone_number=4155551212"

## Required Parameters

| Parameter    | Description                                   | Example |   |   |
|--------------|-----------------------------------------------|---------|---|---|
| origin       | ICAO identifier of a US airport               | KMYF    |   |   |
| phone_number | Ten digigit US phone number in the format of xxxxxxxxxx |         |   |   |
|              |                                               |         |   |   |

## Optional Parameters

| Parameter    | Description                                   | Example | Default  |   |
|--------------|-----------------------------------------------|---------|---|---|
| destination       | ICAO identifier of a US airport               | KOAK    |   |   |
| radius | Radius in NM from specified origin, destination, or cross-track distance from the flight path |    100     |  200 |   |
|              |                                               |         |   |   |





