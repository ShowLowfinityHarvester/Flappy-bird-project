# 1. Start
Initialize game screen
Initialize roadrunner position (starting at default height)
Initialize score = 0
Set game state = "Main Menu"
Set gravity = constant value
Set flap strength = constant upward value
Set game running = False

# 2. Player interactions
Player taps or clicks to make the roadrunner flap
Game starts when player selects "Start Game" from the main menu

# 3. Running Process
While game is running:
    # Update roadrunner position
    Apply gravity to roadrunner's vertical position
    If player taps/clicks:
        Apply flap strength to move the roadrunner upward
    
    # Check for collisions
    If roadrunner collides with a building:
        Set game state = "Game Over"
    
    If roadrunner flies out of the screen (top or bottom):
        Set game state = "Game Over"
    
    # Scoring logic
    If roadrunner successfully passes a building:
        Increase score by 1

    # Check for victory
    If score >= 100:
        Set game state = "Victory"

    # Render the game's state
    Update the screen with:
        - Background (mountains, sunset)
        - Roadrunner position
        - Buildings/obstacles
        - Current score

# Game states
If game state = "Main Menu":
    Display start menu with options:
        - "Start Game"
        - "View High Score"
        - "Quit Game"

If game state = "Game Over":
    Display "Game Over" screen with:
        - Final score
        - Option to restart or return to main menu

If game state = "Victory":
    Display "Victory" screen with:
        - Congratulations message
        - Final score
        - Credits
        - Option to restart or return to main menu

# 4. Output
Display the current score on the gameplay screen
Display final score when game ends (Game Over or Victory)
Save high score locally if the current score exceeds the previous high score

# 5. End
If player chooses to quit:
    End the game and close the application
If player chooses to restart:
    Reset all variables (roadrunner position, score, game state) and restart the game loop