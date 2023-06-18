 



### NIM

TNIM is a simple yet intriguing game of strategy and reasoning. It's played with a pile of objects, usually referred to as "pieces" or "stones." The game follows the rules you described:

The game begins with a predetermined number of pieces in a pile. In the case of the most common version, there are 21 pieces.

Two players take turns removing objects from the pile. Each player has the option to remove 1, 2, or 3 pieces from the pile on their turn.

Players alternate turns until there are no pieces left in the pile.

The player who removes the last remaining piece is considered the loser, while the other player is the winner.

The strategic aspect of NIM lies in trying to force your opponent into a situation where they must take the last piece, leading to their defeat. Players must carefully consider their moves and anticipate their opponent's actions to gain an advantage.

NIM has been studied in the field of combinatorial game theory and has various mathematical properties and winning strategies depending on the initial number of pieces. It's a popular game to study and analyze due to its simplicity and interesting gameplay dynamics.

## code

```
# Helper function to get input from the user
def getInput(prompt):
    while True:
        try:
            return int(input(prompt))
        except ValueError:
            print("Invalid input! Please enter a valid integer.")

def nimGame():
    heaps = [3, 4, 5]  # Initial heap sizes
    currentPlayer = 1  # 1 represents player 1, 2 represents player 2

    while True:
        print("Current state:", heaps)
        print("Player", currentPlayer, "turn:")

        # Get the player's move
        heapIndex = getInput("Enter the index of the heap (0-2): ")
        objectsToRemove = getInput("Enter the number of objects to remove: ")

        # Validate the move
        if heapIndex < 0 or heapIndex >= len(heaps) or objectsToRemove <= 0 or objectsToRemove > heaps[heapIndex]:
            print("Invalid move! Please try again.")
            continue

        # Update the heap
        heaps[heapIndex] -= objectsToRemove

        # Check for the winning condition
        if sum(heaps) == 0:
            print("Player", currentPlayer, "wins!")
            break

        # Switch to the next player
        currentPlayer = 3 - currentPlayer  # Alternate between players 1 and 2

nimGame()
```




## iterate
- 

## ref
- https://en.wikipedia.org/wiki/Nim
