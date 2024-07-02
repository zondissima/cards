# Cuddle Cards
Cuddle Cards a pure HTML+JS game card game initially created to extract random cards with cuddles for couples and with increasing intensity. 

Annyway, it can be used to create a generic game based on cards, even with more than two players.

## Demo

https://zondissima.free.nf/cards/index.html

## How to play
The original games is designed to be played by a couple. Blue cards are actions performed by "him" and pink cards are actions performed by "her".
There is a set of decks of cards which are used in order. The engine shuffles the first deck, selects a subset of cards (for example half of them) and
starts extracting. Each card has a timing associate so it should be performed for "at least" that time (see below for other options).

When all the cards from a deck have been turned and played, the next deck is used, and so on until all the cards have been played.

## How a set is made
A "set" is composed by one or more decks of cards, ordered, and defined as JSON. See the assets/base/set.js for a complete example. The set contains some
general configurations, like the name, instructions, colors and images references, and so on.

All assets composing a set (the js, the pictures, ...) must be contained in a folder under the "assets" folder. The folder name is how a set is referenced.

A deck is a list of cards with an id (not used right now) with a few attributes:

* max - indicvated how many cards of that deck should be used, extracting them randomly. If it's a number less than 1 (like 0.5) a proportional number of cards are extracted. If missing, all cards are used.
* shuffle (true|false) - indicated if the extracted cards should be shuffled or used in the original order. This is important when the cards should played in the defined sequence. 

A card is made of a picture, a text and a duration. The picture path is relative to the set's folder, but absolute URLs can be used. The duration is used by a timer that
starts when the card is turned and it can be used to define a minimum or a maximum time, it depends on the game rules.

## Available sets

* The "base" set, loaded by default, is the original game. Demo: https://zondissima.free.nf/cards/index.html
* The "her" set or "Cuddles for her" is a simple sequence of cuddles for her. Demo: https://zondissima.free.nf/cards/index.html?set=her

## Configuration
A configuration object is inside the index.html and can be used to set the default card duration (to be moved as a set's property) a some other debug settings.

## Debug mode
Adding the parameter debug to the URL you can use the debug mode, which mainly shorten the timer. Example: https://zondissima.free.nf/cards/index.html?debug. To play a specific set in debug more, use https://zondissima.free.nf/cards/index.html?set=her&debug

## Help needed
* A better organization of the code
* Choose the right method to load a game set
* A lot of professional design
* Add the option to extract the cards changeing everytime the color (so every player do something in a round)
* Move the default card duration at set level or deck level (or both)
* Move instruction to set definition
 
## Notes
The commited pictures are samples, you must change them with your own if you want to publish the game "as-is".
Of course, if you create your own game you'll add you own pictures.

## Contacts
I'm on Discord as "zondissima": let's chat!
