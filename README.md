# HazardHulen.IO

## The software

HazardHulen.io is a multiplayer blackjack table, where players can bet virtual
currency to participate in a round of blackjack. The game uses the same ruleset as
regular blackjack played in casinos, with a few details left out for simplicity.
Players play against an artificial intelligence which acts as the dealer, and win
double their bet if they beat the AI. If a player loses, his bet is lost.
All players get a set amount of virtual money when they join the table, and have
to place a bet of at least a minimum amount to play. If a player does not place
a bet within a certain time period in between rounds, he is labeled as inactive,
and cannot take part in the next round.

## Technology
The client is written in HTML and jQuery, which uses socket.io to connect to the server.

The server is written in JavaScript and uses socket.io to communicate with the clients.

https is used to ensure a safe connection between the host and the clients.

## UML Sequence Diagram
![UML Sequence Diagram](https://github.com/DrBumlehund/off_the_books/blob/master/Documentation/sequence.png "UML Sequence Diagram")
The sequence diagram, shown above, shows all calls made between the server and the client.

The server is responsible for synchronizing the table across all clients. It uses the table object _(as seen in the object diagram below)_ for this, in the updateTable method.

## UML Object Diagram
![UML Class Diagram](https://github.com/DrBumlehund/off_the_books/blob/master/Documentation/ClassDiag.png "UML Class Diagram")
The object diagram contains the two key objects used un this project, _Table_ and _Player_.

\* The types set in the fields in the objects, are not according to UML standards. 
