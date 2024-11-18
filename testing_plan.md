## Part 1: Unit Testing the Game Mechanics
**Description**: Testing isolated features of the game to ensure mechanics function correctly.

| Test Case                          | Test Data                            | Expected Outcome                                                                 |
|------------------------------------|--------------------------------------|---------------------------------------------------------------------------------|
| Player movement (flap)             | Player taps/clicks                   | Roadrunner moves upward in response to each tap/click.                          |
| Gravity application                | No player input                      | Roadrunner gradually descends due to gravity.                                   |
| Collision detection with obstacles | Roadrunner hits a building           | Game transitions to “Game Over” state.                                          |
| Boundary detection (top/bottom)    | Roadrunner flies above screen/below  | Roadrunner is restricted within screen boundaries or triggers “Game Over.”      |

---

## Part 2: Logic Testing the Game Rules and Calculations
**Description**: Verifying the game rules and score logic are functioning as intended.

| Test Case                          | Test Data                            | Expected Outcome                                                                 |
|------------------------------------|--------------------------------------|---------------------------------------------------------------------------------|
| Scoring per building passed        | Roadrunner passes 1, 5, 100 buildings| Score increases by 1 per building; score = number of buildings passed.          |
| Win condition                      | Roadrunner passes 100 buildings      | Game transitions to “Victory” screen when score reaches 100.                    |
| Game over condition                | Roadrunner collides with a building  | Game displays “Game Over” screen and prompts restart or return to menu.         |

---

## Part 3: Boundary Testing: Edge Cases and Limits
**Description**: Testing edge cases to ensure the game handles extreme scenarios.

| Test Case                          | Test Data                            | Expected Outcome                                                                 |
|------------------------------------|--------------------------------------|---------------------------------------------------------------------------------|
| Maximum score                      | Player scores 9999 points            | Game continues to run; score remains constant at 9999 if maximum is reached.    |
| Minimum position                   | Roadrunner reaches bottom of screen  | Game triggers “Game Over” if roadrunner moves beyond the bottom boundary.        |
| Maximum position                   | Roadrunner reaches top of screen     | Roadrunner cannot move past the top of the screen.                              |
| Fast-paced gameplay                | Player taps repeatedly at high speed | Roadrunner responds consistently without lag or missed inputs.                  |

---

## Part 4: Integration Testing: System Interaction
**Description**: Ensuring smooth interaction between components, like mechanics and scoring.

| Test Case                          | Test Data                            | Expected Outcome                                                                 |
|------------------------------------|--------------------------------------|---------------------------------------------------------------------------------|
| Collision + Scoring                | Roadrunner passes 10 buildings, then hits one | Game updates score to 10 and transitions to “Game Over” without delay.          |
| Menu and gameplay interaction      | Player pauses the game               | Game pauses all movement and displays menu options.                             |
| High score saving                  | Player scores higher than current high score | New high score is saved and displayed on the main menu.                         |

---

## Part 5: Handling Bad Input and Run-Time Errors
**Description**: Testing for unexpected inputs or error conditions to prevent crashes.

| Test Case                          | Test Data                            | Expected Outcome                                                                 |
|------------------------------------|--------------------------------------|---------------------------------------------------------------------------------|
| Invalid input                      | Keypresses like “#@!”                | Game ignores input; no crash or unintended behavior occurs.                     |
| Conflicting inputs                 | Player presses multiple conflicting keys | Game prioritizes valid inputs and ignores invalid ones without crashing.        |
| Error during save/load             | Corrupt save file                    | Game displays error message and allows player to restart without crashing.      |
| Infinite loop prevention           | Roadrunner gets stuck at a boundary  | Game handles state correctly and triggers appropriate end state or restriction. |

---

## Part 6: Test Plan Summary in Table Form

| **Test Case**                    | **Test Data**                          | **Expected Outcome**                                                             |
|----------------------------------|----------------------------------------|---------------------------------------------------------------------------------|
| Player movement                  | Player taps/clicks                     | Roadrunner moves upward in response to input.                                   |
| Gravity application              | No player input                        | Roadrunner descends gradually.                                                  |
| Collision detection              | Roadrunner hits a building             | Game displays “Game Over” screen.                                               |
| Scoring                          | Roadrunner passes buildings            | Score increases by 1 for each building passed.                                  |
| Maximum score boundary           | Score reaches 9999                     | Game continues; score capped at 9999.                                           |
| Pause menu interaction           | Player pauses during gameplay          | Gameplay pauses, menu appears; resumes smoothly after unpausing.                |
| Invalid input handling           | Player presses invalid keys            | Invalid keys are ignored; game continues without errors.                        |
| High score saving                | Player achieves a new high score       | New high score is saved and displayed on main menu.                             |
| Victory condition                | Player passes 100 buildings            | Game transitions to “Victory” screen.                                           |
| Game over condition              | Player hits an obstacle                | Game transitions to “Game Over” screen.                                         |
| Restart functionality            | Player selects restart from menu       | Game resets all variables and restarts gameplay loop.                           |

---

