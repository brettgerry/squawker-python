# Squawker REST API

The Squawker [REST API][REST] allows you to get and interact aviation data
including TFRs, Pireps, Notams. You can also create alerts that send
notifications to your users, such as sending an SMS message when a TFR pops up
near an airport.

Because the API is based on [REST Principles][REST], it is very easy to write
applications in the language of your choice using most any HTTP client. By
usng Squawker, you can concentrate on building your aviation app instead of
spending time aggregating and translating data from all the different sources
out there. We have done the heavy lifting for you.


## API Resources

### Alerts and Notifications
* [TFR Alert Requests][alertrequests]

### Flight Data
* **TFRs** Coming soon!
* **Notams** Coming soon!
* **Pireps** Coming soon!


## Client Libraries

To make it easy, we have created some open source libraries that interact with
the Squawker REST API in several programming languages. If the language you use
is not listed, you can use your own HTTP client library that is common for that
language to make requests to the API resources using the proper paramters.


### Python
* [squawker-python][python]

### Java
* **squawker-java** coming soon!

## Using the REST API

### API HTTP Requests

Requests to the Squawker API require [HTTP Basic Authentication][basic-auth].

### API HTTP Response Formats

Squawker responds to HTTP requests in the [JSON][json] format.

[REST]: http://rest.elkstein.org/ "Learn REST"
[python]: https://github.com/brettgerry/squawker-python "Squawker Python client"
[alertrequests]: alert-requests
[json]: http://www.w3schools.com/json/
[basic-auth]: http://en.wikipedia.org/wiki/Basic_access_authentication
