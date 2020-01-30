# Overview

## Abstract

This documentation defines the integration process with Pruvo's B2B repricing service.

## Service description

Pruvo's repricing service provides you access to Pruvo's powerful price monitoring capabilities.
This will allow you to increase your revenue for already made reservations, by constantly looking for a better rate for them
and replacing them with better priced reservations.

The service consists of 3 parts:
- Automatic import of all your reservations into Pruvo's price monitoring service.
- Continues price monitoring of your reservations, using your own inventory and/or Pruov's inventory.
- Automatic / Manual repricing of reservations with lower  

## Integration Process

In order to integrate with you, Pruvo will need to have an access to your api (and it's docs).
The access should be granted a special permission that allows read access to all of your reservations (for reservations importing and status check).

Most of the integration is performed on Pruvo's side by integrating on our side to your api. 
We will require that you will give us some extended api capabilities on your side, which will be detailed later on in these docs.
