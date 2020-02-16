# Overview

## Abstract

This documentation defines the integration process with Pruvo's repricing service.  

## Service description
Pruvo developed an AI-Driven hotel price monitoring service that helps you increase your profitability by re-booking when the market price drops.
The solution was developed while focusing on creating a simple to integrate solution which lowers the required development efforts from your end to the minimum.  

The service consists of the following steps:

 1. **Import**: Automatic import of all your reservations into Pruvo's price monitoring service.
 2. **Price Monitoring**: Continues price monitoring of your reservations, using your own inventory and/or Pruov's inventory.
 3. **Rebooking (Automatic / Semi-Automatic)**: Once Pruvo finds a lower price for the exact room, the re-booking can be made automatically by Pruvo or semi-automatically by allowing you to verify the proposed change on Pruvo's platform (once the change is approved by you, the re-booking takes place automatically).
 4. **Back-office Booking Update**: After re-booking the exact same room using Pruvo's platform, the only thing
  left is to update the original reservation with the new reservation data (It's important to allow a *silent* replacement so
   the end customer won't be aware of the changes that were made).
 
By completing the above steps, you can increase your profitability for already made reservations, by constantly looking for a better rate 
and replacing them with a better priced reservations.


## Integration Process

Pruvo's solution is a SAAS solution that can be integrated with any platform.  
In order to complete such an integration, Pruvo requires access to your API endpoints and documentation as well as special permissions to gain access to all hotel reservations.  
Such permission will be used in order to allow Pruvo to import existing reservations, check status and monitor the market prices.

Most of the integration is performed on Pruvo's side by integrating to your existing api.  
The ONLY requirement of integration on your end is extending your api capabilities to support the re-booking process.
