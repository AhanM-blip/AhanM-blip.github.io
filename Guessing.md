```mermaid
flowchart TD
    Start([Start]) --> Generate[Generate random number]
    Generate --> Player_Input[Prompt player to guess]
    Player_Input --> Validate{Is input valid?}
    Validate -- No --> Error[Show error, prompt retry]
    Validate -- Yes --> Check{Guess against Answer}
    Check -- Too High --> High[Display too High]
    Check -- Too Low --> Low[Display too low]
    Check -- Correct --> Win[Display you win]
    Win --> End([End])
    Error --> Player_Input
    High --> Player_Input
    Low --> Player_Input
```
Start: Where the game begins.
Generate: Generates a random number(maybe 1-100).
Player Input: The game asks player to guess the number.
Validate: Number is checked to see if its a valid input(1-100 or just a numerical value)
Error: If given input is out or range or is not a numerical value, they are shown an error message and sent back to the guess screen in order to try again.
Check: Compares number inputted to number chosen. If the guess is correct then a "win" message is displayed.
If number is too high or low it shows up on the screen. Then the player is redirected to the guess to screen in order to retry.
If player guesses number correctly the game will end.
