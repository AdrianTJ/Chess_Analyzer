# Chess Analyzer

Some useful functions to analize a or create chess boardstates based on the stockfish AI. The files included are: 
* chess_game_analizer.py: The main script, includes a group of 3 functions useful for creating and analizing chess boardstates. This script has some testing oprions at the end of it for the different functions implemented in it. 
* Board_Positions_Database.csv: A sample game generated from using the function board_generator in chess_game_analizer.py and saving the output dataframe as a csv. In this case, it is a game with 10 moves for each player played with a time constraint of 0.1 seconds per move for each player. 
* Moves_With_Score.csv: The sample result from using the function game_analyzer from the chess_game_analizer.py script on the dataframe of boardstates generated by board_generator. 

Requirements: 
* Stockfish engine (included in this GitHub page), can be downloaded at https://stockfishchess.org/download/. I recommend building from source, since that worked flawlessly for me. 
* Python packages: os, sys, re, csv, pandas, chess.engine, chess
* This was built on python 3.9.2, and we have a venv for it, if anyone wants it, I can be reached by email. 

Usage: As is, the program takes in a FEN position as input and returns the dataframe associated with every possible move and its score along with some other information. An example follows. 

Example Input 

./chess_game_analyzer.py 'rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1'

Example Output

FEN Player Move Piece  Score   Mate
0   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE  Nh3     N  -0.77  False
1   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE  Nf3     N   0.21  False
2   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE  Nc3     N  -0.18  False
3   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE  Na3     N  -0.65  False
4   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   h3     P   0.03  False
5   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   g3     P   0.23  False
6   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   f3     P  -0.78  False
7   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   e3     P   0.23  False
8   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   d3     P  -0.20  False
9   rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   c3     P   0.07  False
10  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   b3     P   0.01  False
11  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   a3     P  -0.06  False
12  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   h4     P  -0.44  False
13  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   g4     P  -1.46  False
14  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   f4     P  -0.35  False
15  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   e4     P   0.42  False
16  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   d4     P   0.24  False
17  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   c4     P   0.34  False
18  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   b4     P  -0.25  False
19  rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/RNBQKBNR w KQkq - 0 1  WHITE   a4     P  -0.10  False%
