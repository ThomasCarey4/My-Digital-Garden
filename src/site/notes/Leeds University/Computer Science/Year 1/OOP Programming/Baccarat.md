---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/oop-programming/baccarat/"}
---

Two hands:
- Player
- Banker
*Both hands are unrelated to their namesake*
*The bettor can choose either*
Each round has three outcomes:
(Based on highest score)
- Player
- Banker
- Tie
Points:
- 1–9 Cards have respective points
- 10+ Cards have no points
**Points are valued modulo 10!**
*i.e. only the last digit of the sum is used $\color{lightgreen} (6+7=13\therefore3 \text{ points})$*
Therefore, the highest hand value is 9
**A *shoe* containing 6 or 8 decks of cards is used**
A *cut-card* is placed ***in front*** of the *seventh from last* card, and the drawing of this card indicated the last coup of the shoe

---
The dealer *burns* the first card **face up** and then based on its respective numerical value, with aces worth 1 and face card worth 10, the dealer *burns* that many cards **face down**.

For each coup, two cards are dealt face up to each hand, starting with “player” and alternating between the hands.
The dealer may call the total (*e.g. “five player, three banker”*)
If either the player or banker achieve a total of 8 or 9 at this stage, the coup is finished and the result is announced: a player win, a banker win or a tie.

If neither hand has eight or nine (*This is known as a natural*), the drawing rules are applied to determine whether the player should receive a third card.
Then, *based on the value of **any** card drawn to the player*, the drawing rules are applied to determine whether the banker should receive a third card.

The coup is then finished, the outcome is announced, and the winning bets are paid out.

---
##### Drawing Rules
###### Player’s rules
- If the player has an initial total of 5 or less, they draw a third card.
- Otherwise, they *stand*
###### Banker’s rules
- **If the player *stood***, the banker follows the same rules as the player did.
- Otherwise, 
	- If the banker total is 2 or less, *they draw*
	- If the banker total is 3, *they draw **unless** the player’s third card is an 8*
	- If the banker total is 4, *they draw if the player’s third card is 2,3,4,5,6 or 7*
	- If the banker total is 5, *they draw if the player’s third card is 4,5,6 or 7*
	- If the banker total is 6, *they draw if the player’s third card is 6 or 7*
	- If the banker total is 7, *they **stand***

---
