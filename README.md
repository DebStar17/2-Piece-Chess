# Aim
This project is an attempt at making a kind of primitive yet twisted unsupervised learning chess bot. 
Unlike traditional bots, which feed on human data, I wondered if it was possible to make something wherein 2 bots would fight and in the process train each other.
And, as usual, I made it all in VANILLA python (no external AI-related libraries used, only used random and libs for the UI)
Although, I didn't make a whole chess bot in vanilla python, I simplified my study down to where only 2 chess pieces fight for the win in a customizable chess-like-board

# What the Game is...
So, in my game, called 2 Piece Chess - there are 2 players
- P1 - controlling a Knight
- P2 - controlling a King

The game is simple, the player who eats up the other player wins!
But, if the game exceeds 50 total moves (totalling both players' moves), then it's a draw.

Now, the board - it's of a special kind! The board is not totally blank, but filled with walls (which are randomly placed, more in next section). These walls restrict the movement of both players and are fixed throughout the game. This makes the game even more interesting and more tight!

PS: P1 plays first.

# What do YOU do?
Now you provide inputs.

**Main1**
- First it asks for the size of the chessboard/grid. Since the grid is square - one dimension will suffice. (give an integer input)
- Next, it will ask for "Bias for space and wall". This is essential to know the ratio of empty squares to walls. (give two integers space separated)
- Now it will show you your custom made chess-board.
  <img width="665" height="589" alt="image" src="https://github.com/user-attachments/assets/921bd213-feff-434d-9a6f-d356a524107a" />


**Main2**
- Next, you provide the positions of P1 (Knight) and P2 (King) as space separated integers.
- Now, it asks for training threshold... this is how many games you will let the bots play with each other to train themselves. (single integer)
- Finally after training is complete... the real showdown begins! Press enter and watch an epic fight unravel between two bots! If you like - make it more crazy by betting at each stage where the bot might move!
<img width="655" height="603" alt="image" src="https://github.com/user-attachments/assets/da44d4af-98d3-43ca-98ca-d5a0bc972d1f" />

# The Algorithm
Now, how did I do that? HEHE
Well, in training stage, I let the bots move on randomly and fight each other. And noted down who wins and who loses.
This data is then used by the bots in the final showdown... wherein they will make their moves based on which moves in the training stage lead to either a draw or their win.
This decision is also not fixed. It randomly selects from all possible moves that it had seen when it was in that position in some previous training games.
If allowed to train for like 500-1000 games, this creates a bias in the random algorithm and thus - AI (I guess)!

# To Play
Open the "Copy of 2-pieceChess.ipynb" file and press run all.
<img width="173" height="86" alt="image" src="https://github.com/user-attachments/assets/61d9f44e-edd0-45f4-a39b-e960bb0781f4" />

Then give the inputs as directed. And, ENJOY!
