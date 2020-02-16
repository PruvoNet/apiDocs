# Repricing Flow Example

Please find an example of the typical flow used by most of our customers 
(in case of special integration request, the current flow can be modified according to the desired scenario)

1. An agent makes a reservation on your system
2. Pruvo automatically imports that reservation
3. Pruvo price monitoring starts
4. Pruvo checks the status of the reservation to make sure it is still valid
5. Pruvo checks the current price of the reservation using your api
6. A better price is found - Pruvo validates the rate
7. Pruvo makes a new reservation using your book api
8. Pruvo notifies your back office on the change using the back office endpoint
9. You change the reservation data with the newly crated reservation
10. You silently cancel the original reservation
11. You have the same exact reservation, with a lower price
