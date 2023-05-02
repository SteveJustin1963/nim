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

// define a function to get the player's move
int get_player_move(int player, int pieces) {
    int move;
    // loop until a valid move is entered
    do {
        // prompt the player to enter their move
        printf("Player %d, enter your move (1-3): ", player);
        scanf("%d", &move);

        // validate the move
        if (move < 1 || move > 3) {
            printf("Invalid move. Please enter a number between 1 and 3.\n");
        } else if (move > pieces) {
            printf("Invalid move. You cannot remove more pieces than are in the pile.\n");
        } else {
            // the move is valid, return it
            return move;
        }
    } while (1);
}

int main() {
    int pieces = 21;
    int current_player = 1;
    int move;

    // loop until the game is over
    while (pieces > 0) {
        // display the current state of the game
        printf("There are %d pieces remaining in the pile.\n", pieces);

        // get the player's move
        move = get_player_move(current_player, pieces);

        // update the number of pieces in the pile
        pieces -= move;

        // switch to the other player
        if (current_player == 1) {
            current_player = 2;
        } else {
            current_player = 1;
        }
    }

    // display the winner
    if (current_player == 1) {
        printf("Player 2 wins!\n");
    } else {
        printf("Player 1 wins!\n");
    }

    return 0;
}

```
Note that the implementation is slightly different from the pseudocode due to the use of a do-while loop instead of a while loop, and some changes in the syntax for printing and scanning inputs.
