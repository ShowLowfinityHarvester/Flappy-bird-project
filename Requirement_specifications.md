Requirements Specification: Flappy bird

Game Name: Rising Roadruner
Team Members: Jayson doutree, David Avila
Client: Ms. Kenndey
Date: 11/14/2024

Game Overview
	Just flappy bird but with a New Mexico skin\retexturing 



Functional Requirements
	•	Core Features:

The game must feature a simple, fast-paced environment where the player controls a bird.
The bird should be able to flap upwards when the player interacts (e.g., by tapping or pressing a button).
The bird must fall due to gravity when not flapping.
The game should include randomly generated obstacles (pipes) that the bird must navigate through.
The game must track and display the player's score, which increases as the bird successfully passes through pipes.
The game should end when the bird collides with a pipe or the ground.
The game must display a restart option after the game ends.
High scores should be saved (locally, if necessary).



**	•	What must the game do? (E.g., login, save progress, track scores, level progression)**

Track the score, updating it as the bird successfully navigates through obstacles.
Detect collisions with obstacles or the ground to trigger the end of the game.
Reset the game when the player chooses to restart after a game over.
Optionally, save high scores locally.


	**•	How does the player interact with the game?  **
    The player interacts with the game by tapping the screen (or pressing a key) to make the bird flap and move upward.
    When the player releases the tap (or key), the bird begins to fall due to gravity.
    Players can restart the game by tapping the screen (or pressing a button) after the game ends.



Non-Functional Requirements
	•	Usability:
	•	How should the game be designed for the player? (E.g., easy to understand, intuitive controls)
It should be real simple to play and learn but is very difficult


	•	Performance:
	•	How should the game perform? (E.g., frame rate, load time, number of players supported)
It should run at least 60fps load quick and is single player only


	•	Cross-Platform Compatibility:
	•	Does the game need to work on multiple devices or platforms? (E.g., PC, mobile, tablet)
Computer and mobile 

Design Requirements
	•	Graphics and Visuals:
	•	Style of the game graphics (e.g., retro, pixelated, smooth animations)
Basic art style or real images 


	•	Audio:
	•	What kind of sound effects or music will be used?
basic flapping and point sounds


Data Requirements
	•	What data needs to be saved or tracked? (E.g., high scores, player progress, achievements)
	•	How will the data be stored? (e.g., in-game memory, online storage)
The high score will be stored with in-game memory



Collaboration with Client
	•	How will you gather feedback from the client in each sprint? (E.g., through surveys, playtesting, direct meetings)
	•	How will you ensure the game is developing according to the client's needs?
Playtesting to make sure it works