# nim
nim game



### NIM

The game of NIM is played with a number of objects, called pieces. Two players take turns removing objects from the pile. The player who removes the last object loses the game. 

The game can be played with any number of pieces, but the most common number is 21. To play, each player removes 1, 2, or 3 pieces from the pile on their turn. The player who removes the last piece loses the game.

## sudo
```
// set the number of pieces in the pile
pieces = 21

// set the current player to player 1
current_player = 1

// loop until the game is over
while pieces > 0:
    // display the current state of the game
    print "There are", pieces, "pieces remaining in the pile."

    // get the player's move
    move = get_player_move(current_player, pieces)

    // update the number of pieces in the pile
    pieces = pieces - move

    // switch to the other player
    if current_player == 1:
        current_player = 2
    else:
        current_player = 1

// display the winner
if current_player == 1:
    print "Player 2 wins!"
else:
    print "Player 1 wins!"

// define a function to get the player's move
function get_player_move(player, pieces):
    // loop until a valid move is entered
    while True:
        // prompt the player to enter their move
        print "Player", player, "enter your move (1-3):"
        move = input()

        // validate the move
        if move < 1 or move > 3:
            print "Invalid move. Please enter a number between 1 and 3."
        elif move > pieces:
            print "Invalid move. You cannot remove more pieces than are in the pile."
        else:
            // the move is valid, return it
            return move
```

## c code 
```
#include <stdio.h> 
#include <stdlib.h> 

int main() 
{ 
    int n,m,i,j,k; 
    printf("Enter the value of n and m\n"); 
    scanf("%d %d", &n, &m); 
    if (n%2 == 0) 
    { 
        printf("Player 1 wins\n"); 
        return 0; 
    } 
    else
    { 
        printf("Player 2 wins\n"); 
        return 0; 
    } 
}
```
