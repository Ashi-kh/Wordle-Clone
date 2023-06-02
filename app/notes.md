# Functional Requirements


## gameplay
6 tiles to guess a word

### pick a solution word
store solution word in JSOn object / array
when game is loaded choose random item from array
set solution to that word 

### Making a guess

Detect any keypresses
- If keypress is a letter 
    - update "letters" attribute 
        - update tile markup based on "letters" value
- If keypress is backspace
    - delete last letter in "letters"
        - update tile markup based on "letters"

Don't run update function if "letters" length = 4

Typing in the letter will display the letter in the tile
backspace will delete the letters
### submit guess
Enter will submit guess
    - compare each letter with the corresponding letter in solution word
    - update the stste/color of the letter
    - if all letters are "correct"/green, game is won


Guesses must be a reall world in "word list"
Guess colors (data-state):
- Gray: absent
- green: correct
- yellow: correct but not in the right position

Hard mode:
present or correct letters nust be used in subsequent guesses

Guesses are saved in local storage

## Design
5*6 tiles
Virtual keyboard


## Interactions
- Border of the tile changes to light gray
- Blinking in animation with letter
- Backspace will remove the letter, border changes back to darck gray
- 

When submitting guess:
- Tiles will flip up and background color will change based on guess
- slight delay between each tile flipping 
- background color changes when the tile is flat, i.e. can't see it