# Cuddle Cards
Cuddle Cards a pure HTML+JS game card game. The name derives from a project, but it's a bit misleading since it can be used to create a generic game based on cards.

## How to play
The original games is designed to be played by a couple. Blue cards are actions performed by "him" and pink cards are actions performed by "her".
There is a set of decks of cards which are used in order. The engine shuffles the first deck, selects a subset of cards (for example half of them) and
starts extracting. Each card has a timing associate so it should be performed for "at least" that time (see below for other options).

When all the cards from a deck have been turned and played, the next deck is used, and so on untile all the cards have been played.

## How a set is made
A "set" is composed by some decks of cards, ordered, and defined in a json. See the assets/base/set.json. At set level card colors can be defined and those
colors referenced from each single card to make it easy to change them.

All assets composing a set (the js, the pictures, ...) must be contained in a folder under the "assets" folder.

A deck is a list of cards with an id (not used right now) and with an optional "max" attribute which is the number of cards the engine should used from that deck during a game.

A card is made if a picture, a text and a duration. The picture path is relative to the set's folder, but absolute URLs can be used. The duration is used by a timer that
starts when the card is turned and it can be used to define a minimum or a maximum time, it depends on the game rules.

## Available sets

* The base set
* The "Cuddles for her" set
* The KS set: it is the base set plus an extra deck

## Configuration
A configuration object is inside the index.html and can be used to set the default card duration (to be moved as a set's property) a some other debug settings.

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
