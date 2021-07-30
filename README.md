# Extremely Simple Chess AI

Had originally started out this project to play against my brother and beat him in it. (I'm a beginner noob at chess)

I'll admit that I didn't manage to put in as much effort as I could into the enhancement of the project. But I did learn quite abit. So here are some references, a summary and codes.

## How To Play
You can try it out if you want to. But just a note that going to a depth of 4 or 5 would greatly slow the playing speed. So, choose wisely, at your own risk.

## Structure
* Board Visualisation
* Legal Gameplay
* Evaluation
* Search

### Board Visualisation
Used [Chessboard.js](https://github.com/oakmac/chessboardjs/), a standalone JS Chess Board. Just the board and no codes with it.

### Legal Gameplay
Connected Chessboard.js with [Chess.js](https://github.com/jhlywa/chess.js). Chess.js is the code that would help us to make valid moves, instead of being able to go to every and any square.
- Uses Node.js
  - Install npm first
  - Restart computer
  - Install chess.js

### Evaluation
Used the [Simplified Evaluation Function] (https://www.chessprogramming.org/Simplified_Evaluation_Function) from ChessProgramming Wiki. 

### Search
**Minimax & Alpha-Beta Pruning**
This is the search algorithm used in this program, and where the AI part comes in. Though, honestly this is like a glorified version of decision tree.
Here's a really good explanation on the algorithm - https://www.youtube.com/watch?v=l-hh51ncgDI

**Negamax**
This is another algo but it wasn't used here because I felt like it was just the same as the Minimax & Alpha-Beta Pruning (the one before this). The only difference was that instead of keeping track of 2 score variables: Black & White, it only keeps track of 1.

An example:
    int negaMax( int depth ) { 
        if ( depth == 0 ) return evaluate(); 
        int max = -oo; 
        for ( all moves)  { 
            score = -negaMax( depth - 1 ); 
            if( score > max ) 
                max = score; 
        } 
        return max; 
    }

## Tools
- VScode
- HTML/CSS/JS

## Things Tried
When I first started out, I had close to 0 knowledge in Chess play and how I could structure the project. So here are some experimentations I did:
* [Simple Neural Chess AI Walkthrough - George Hotz](https://www.youtube.com/watch?v=RFaFmkCEGEs)
  * This would be a great walkthrough for those who are a little more experienced. (I got so lost 1 hour into the tutorial LOL)
* [Deep Learning for... Chess](https://erikbern.com/2014/11/29/deep-learning-for-chess)
  * I couldn't understand the structure of the program and any resources that I could further look into. This project makes use of external datasets to train the model.

## Troubleshooting
- Google Collab
  - "IOPub data rate exceeded." 
    - Happened when printing out large chunks of data 
    - Solution - Print it out in smaller chunks OR increase the iopub data rate limit configuration 

## Possible Future Enhancements
* Evaluation
  * [PESTO's Evaluation Function](https://www.chessprogramming.org/PeSTO%27s_Evaluation_Function)
* Search
  * Alpha-Beta Enhancements
  * Quiescence Search
  * Monte Carlo Tree Search (MCTS)

## Common Chess Jargon
Jargon | Definition | Example
------ | ---------- | -------
[Chess Standard Algebraic Notation (SAN)](http://cfajohnson.com/chess/SAN/) | A system for recording chess moves. Moves are represented by the name of the piece and the square to which it is being moved. | Nf3, Qb7, Bb5

## References
Title | Link
----- | ----
**A step-by-step guide to building a simple chess AI** (Based-off this project) | https://www.freecodecamp.org/news/simple-chess-ai-step-by-step-1d55a9266977/ 
Simple Chess AI Guide | https://github.com/lhartikk/simple-chess-ai/blob/master/script.js 
Chess programming Wiki | https://www.chessprogramming.org/Search 
"How My Chess Engine Works" Blog | https://www.naftaliharris.com/blog/chess/ 
AlphaZero - A Novel Reinforcement Learning Algorithm | https://towardsdatascience.com/alphazero-a-novel-reinforcement-learning-algorithm-deployed-in-javascript-56018503ad18 
Converting Keras / Tensorflow onto JS | https://towardsdatascience.com/deploying-a-simple-machine-learning-model-into-a-webapp-using-tensorflow-js-3609c297fb04 
Creating A Chess AI using Deep Learning | https://towardsdatascience.com/creating-a-chess-ai-using-deep-learning-d5278ea7dcf 
Python Chess Library Documentation | https://python-chess.readthedocs.io/en/latest/ 
Extracting PGN | https://github.com/pmerg/ExtractPGN 
