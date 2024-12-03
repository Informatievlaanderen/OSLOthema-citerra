# Notes

This track is a combination of public services (offering access to a zone and handing out permits) and
legal documents and actions (requests and permits).
The latter is described in 
the [application profile](https://data.vlaanderen.be/doc/applicatieprofiel/omgevingsvergunning/) of 
OSLO Omgevingsvergunning.

## Aanvraag

We use https://data.vlaanderen.be/ns/omgevingsvergunning#Aanvraag 
because it matches what we need for this track.

## Activiteit

We use https://data.vlaanderen.be/ns/omgevingsvergunning#Activiteit
because it can be used with Aanvraag en Vergunning.
In Omgevingsvergunning they probably didn't use an existing class representing an activity because
they needed a very specific legal definition. I didn't verify this with the authors of that application profile.

The property "tijdsbestek" has as range Periode.
In Omgevingsvergunning this was Tijdsduur
but this is probably wrong.
See https://github.com/Informatievlaanderen/OSLOthema-omgevingsvergunning/issues/52

## Bewijs

We use http://data.europa.eu/m8g/Evidence
because it works with the public services as definied by the Core Public Service Vocabulary.
In our case we Evidence as a concrete evidence and not an abstract description of what the characteristics are of 
an evidence.

## Bewijstype

Nothing to mention.

## Dossier

We use this class to group all evidences that are related to a single request.
A single request is linked to single case and a single case is linked to a single Dossier.

## Procedure

Nothing to mention.

## Project

We use this class to group cases (and their corresponding requests) together.
For example, when a company those multiple requests for multiple vehicles for a specific event.
There will be multiple cases and they all belong to the same project.

# Publiekedienstverlening

We use this class to model the act of giving access to a zone and the act of giving a permit as public service.

## Stuk

Nothing to mention.

## Toegang

You can at most link only one vehicle to a Toegang because you want to be able to add metadata about this specific
vehicle in the future. 
If there would be more vehicles linked and you want to say something about a specific one, then you don't have a way
to do that.

## Vergunning

We use http://data.vlaanderen.be/ns/besluit#Vergunning
because it matches what we need for this track.

## Voertuig

Nothing to mention.

## Voorwaarde

Nothing to mention.

## Voorwaardecollectie

See also https://github.com/Informatievlaanderen/OSLOthema-citerra/issues/16.

## Weigering

Nothing to mention.

## Zaak

This class links a request, permit, and denial.
It also links to a Dossier which has all the evidences.

## Zone

Nothing to mention.

