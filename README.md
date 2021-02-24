# Chess Analizer

Some useful functions to analize a or create chess boardstates based on the stockfish AI. The files included are: 
* chess_game_analizer.py: The main script, includes a group of 3 functions useful for creating and analizing chess boardstates. 
* Board_Positions_Database.csv: A sample game generated from using the function board_generator in chess_game_analizer.py and saving the output dataframe as a csv. In this case, it is a game with 10 moves for each player played with a time constraint of 0.1 seconds per move for each player. 
* Moves_With_Score.csv: The sample result from using the function game_analyzer from the chess_game_analizer.py script on the dataframe of boardstates generated by board_generator. 

Requirements: 
* Stockfish engine (included in this GitHub page), can be downloaded at https://stockfishchess.org/download/. I recommend building from source, since that worked flawlessly for me. 
* Python packages: os, sys, re, csv, pandas, chess.engine, chess
* This was built on python 3.9.2, and we have a venv for it, if anyone wants it, I can be reached by email. 
