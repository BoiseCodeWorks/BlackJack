## Black Jack Instructions

---

#### User Interface

1. When the page loads, only a 'Play' button should be visible.
2. After the deal, 2 rows of cards should be visible, the dealers above the players. One of the dealer's cards should be face down. All of the players cards should be face up.
3. After the deal, the 'Play' button should be replaced by a 'Hit' button and a 'Stand' button.
4. When the hand is over, an alert should indicate who the winner is.
5. After the hand is over, the 'Hit' and 'Stand' buttons should be replaced by the 'Play Again' button.

<br>

#### Game Logic

When the 'Play' or 'Play Again' button is clicked:

1. Shuffle the deck.
2. Deal the first card up to the player's hand & the first card down to the dealer's hand.
3. Deal the second card up to the player's hand & the second card up to the dealer's hand.
4. If the dealer has an Ace or 10 point card showing:
	* If the dealer has Black Jack and the player doesn't, the dealer wins.
	* If both hands have Black Jack the hand is a push.
	* If the dealer does not have Black Jack play continues.
5. Enter the player hit phase.
	* If player hits, deal another card and calculate total. End hand if the player busts.
	* If the player stands, exit the player hit phase.
6. Enter the dealer hit phase.
	* The dealer must hit on 16 or less.
	* If dealer hits, deal another card and calculate total. End hand if the dealer busts.
	* When the dealer stands (total is over 16 and under 22) determine winner or push and end the hand.

<br>

#### Dealing/Hitting

A deck array containing 52 cards is provided.

A dealer hand array and player hand array is provided.

A shuffle function is provided. 

After the shuffle, dealing should consist of taking cards from the front of the shuffled deck array and putting them in the dealer/player hand array.

Hitting would also pull cards from the front of the shuffled deck array.

<br>

#### Required Functions

* deal
	* Call the shuffle function.
	* Deal cards to the player and dealer.
	* Calculate the hand values for both hands.
	* Determine a Black Jack as described in #4 above.
	* If either hand is a Black Jack call showWinner.

* hit
	* Add another card to the player hand.
	* Calculate the player's hand value.
	* If the value is greater than 21 call showWinner.

* stand
	* Enter the dealer hit phase as described in #6 above.

* getHandValue(hand)
	* Return a numeric value for the cards in a hand.

* getCardValue(card)
	* Return a numeric value for a single card.

* showWinner()
	* Display the hand winner.
	* Display the 'Play Again' button.

* playAgain()
	* Clear the dealer and player hands.
	* Call the deal function.

<br>

#### Some Coding Standards

All code should be in an IIFE

All event handlers should be bound within app.js

All DOM manipulation should be done within app.js

<br>

#### Notes

Don't forget an Ace can be a 1 or 11 when calculating a hand value.

There are card PNG images in the 'img' folder with filenames that match the card text. For example, the Ace of Spades card text is 'AS' and the card image is 'AS.png'.

There is also a card back image file named 'back.png'.

Links to Bootstrap and Font Awesome are already in index.html.

<br>

#### Bonus Challenge

Start the player with a bankroll and enable betting. Adjust the players bankroll with each win/loss.


## Legal Overview

The content under the CodeWorks®, LLC Organization and all of the individual repos are soley intended for use by CodeWorks Instruction to deliver Educational content to CodeWorks Students.

---

## Copyright

© CodeWorks® LLC, 2021. Unauthorized use and/or duplication of this material without express and written permission from CodeWorks, LLC is strictly prohibited.


<img src="https://bcw.blob.core.windows.net/public/img/7815839041305055" width="125">
