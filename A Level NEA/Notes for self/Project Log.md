## 11/03/23

I started working on [[Create OOP Poker Base Game|Creating the base of my game]] with OOP principles.
Instead of implementing the deck like this:
```python
deck = {"Clubs": [2, 3, 4, 5, 6, 7, 8, 9, 10, "Jack", "Queen", "King", "Ace"],  
        "Hearts": [2, 3, 4, 5, 6, 7, 8, 9, 10, "Jack", "Queen", "King", "Ace"],  
        "Diamonds": [2, 3, 4, 5, 6, 7, 8, 9, 10, "Jack", "Queen", "King", "Ace"],  
        "Spades": [2, 3, 4, 5, 6, 7, 8, 9, 10, "Jack", "Queen", "King", "Ace"]  
        }
```
I implemented the deck like this:
```python
class Card:

    def __init__(self, suit, rank):

        self.suit = suit

        self.rank = rank

  

    def __str__(self):

        return f"{self.rank} {self.suit}"

  
  

class Deck:

    def __init__(self):

        self.cards = [Card(rank, suit)

                      for rank in "23456789TJQKA" for suit in ["Clubs", "Diamonds", "Spades", "Hearts"]]
```

## 25/03/23

Today, I made a lot of progress on the GUI of the game.
![[Pasted image 20230325180531.png]]
I did a lot of research on what the best GUI libraries for Python are, and eventually started learning to use PySide6. 

The cards are randomly generated and the respective images are displayed on the screen.

At the moment, the player can't see the amount of chips they have. There is no poker functionality yet such as betting. I plan to implement this the next time I work on the game.
The cards are also shown vertically instead of horizontally, but I really like the way this looks. I might change this later on, just to make the game look more like the original Texas Hold'Em Poker would.  Currently, the players don't actually have their cards go around the table like they would in a real game, but I can implement this in the future.

It could be cool to implement a GUI similar to the one used in this [video](https://www.youtube.com/watch?v=u90TbxK7VEA). Building a fullscreen animated PyQt6 application could be incredible looking. I will definitely look into it, but it isn't my main goal. The AI of the project is my main goal, and as this video explains, it is much harder to make a good poker AI than a good chess AI.
![[Pasted image 20230325181435.png]]
	The aim of the AI when it has a strong hand is to get **as much money** from the enemy players as possible - NOT just to win the round.

# 29/03/23

![[Pasted image 20230329234938.png]]
New UI :))) (made with QT designer and then adapted in PyQt 5)