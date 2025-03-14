Intro
Welcome to the NBA Team Match game! Test your NBA knowledge by filling in a grid with players who have played on both teams shown. Use your skills and insights to find matching players. One goal: complete the grid!

Inspired by: https://www.hoopgrids.com/

Table of Contents
Game Overview

Required Libraries

How to Play

Project Structure

main_game.py

test_game.py

dependencies.txt

Game Overview
This Python script implements the "NBA Team Match" game. The game presents a 3x3 grid with NBA teams as row and column headers. The objective is to guess players who have played for both teams specified by their numeric positions in the grid.

The game utilizes the NBA API to fetch information about teams and players. It features an interactive, terminal-based interface with colorful formatting.

Required Libraries
nba_api

numpy

os

pandas

pyfiglet

random

re

sys

tabulate

termcolor

time

typing

The required modules which not come with Python itself can be installed using the following command:

bash
pip install nba_api numpy pandas pyfiglet tabulate termcolor
How to Play
To play the game, follow these steps:

Run the script.

Follow the instructions displayed in the terminal.

Guess players by typing their name and the corresponding number from the grid, as shown in the instructions.

To quit, press CTRL+C or CTRL+D.

Project Structure
main_game.py
This is the main file, composed of the following elements:

Imports: The first part of the code consists of importing various libraries and modules needed for the program's functionality, including libraries for working with NBA data, numerical computations, operating system interactions, data manipulation, text formatting, and more. The typing module is also imported to support type hinting.

Global variables:

nba_teams_dict: A dictionary containing information from the 30 NBA franchises.

score_emojis: A dictionary that translates numbers into emoji.

Class TeamMatchGame: The TeamMatchGame class represents the core logic of the NBA Team Match game and is responsible for managing game state information. The class includes methods and properties that allow interaction with the game.

Attributes:

row_teams_list: A list of team names for the grid rows.

col_teams_list: A list of team names for the grid columns.

game_grid: The game grid represented as a Pandas DataFrame.

guessed_players_count: The number of players who have been guessed so far.

Methods:

__init__: The constructor of the class that initializes the attributes.

__str__: Returns a printable representation of the TeamMatchGame object, printing a welcome banner and the grid.

get_banner: Returns a string representing the welcome banner and instructions for the game.

is_game_over: Checks if the game is finished by checking if all players have been guessed.

validate_user_response: Checks whether the response given by the user is correct according to the rules of the game.

check_player_guessed: Checks whether a player has been guessed based on the location and name provided by the user.

update_game_grid: Updates the grid with the name of the guessed player based on the location and name provided by the user.

Properties:

game_grid: A property that returns the DataFrame object representing the game grid.

guessed_players_count: A property that returns the number of guessed players.

main function: This function serves as the primary entry point for program execution when the file is run as a script. The main function contains all the function calls that handle the progress of the game and the implementation logic for it.

get_teams_played_by_player function: This function receives as input the name of an NBA player and returns a list of abbreviations of the teams on which that player played during their career. get_teams_played_by_player performs an online search of the "stats.nba.com" database, using the players module included in the imported API. If the name provided does not match a valid player, the exception is handled and an error message is printed. In this case, the function returns an empty list, as well as in the case where a player also played for teams prior to the founding of the NBA.

create_game_grid function: This function aims to create and initialize a game grid using a Pandas DataFrame object. The grid represents three NBA teams organized into rows and columns. create_game_grid takes as input two lists: row (list of team names for rows) and col (list of team names for columns) and associates each pair of the elements in these lists with an identifying number. The latter will be used by the user to indicate which cell of the table he/she intends to complete, providing precise and unambiguous input.

parse_user_response function: This function handles the process of extracting the grid position and player name from a user-provided response. The function relies on regular expressions to parse the response by extracting the necessary information. parse_user_response receives as input a string representing the response provided by the user. Two scenarios can occur at this point: If the user's response matches the pattern defined in the regular expression, the function will return a tuple containing two elements: pos (the position in the grid) and name (the player's name). If there is no match in the regular expression, the function will return None.

test_game.py
This file was created specifically for use with the pytest testing library, with the goal of automating and simplifying the process of testing the functions defined in the main_game.py file.

dependencies.txt
This file reports the command lines that must be run from the terminal in order to install, via pip, the modules necessary for NBA Team Match to work.
