# Algorhythm
- Generate algorithmically music at the click of a button.

## How it works
- Using nothing but raw math/algorithms to generate music.
  - Simpling typing words or letters and pressing a button you can generate music:
    - Alphabet
      - We assign every letter a number. (Ex. a = 1, c = 3, z = 26)
      - Convert those values to the correct name files in [Piano Samples](Piano%20Samples) folder.
      - For note types (Ex. [Crochet, Minim]) we take the length of the word, for example ("bear") is 4 letters in lenght and 4 is closest to the value "Crochet" in our `note_types` dictionary in `main.py`
  - Use provided algorithm methods to generate music:
    - Step (+)
      - Pick three random numbers (starting number, ending number, and length)
      - Lets say starting number is 3, ending number is 7, and lenght is 8
      - Then we evenly increase from 3 to 7 using only 8 numbers.
        - Ex. [3, 4, 4, 5, 5, 6, 6, 7]
      - Convert those values to the correct name files in [Piano Samples](Piano%20Samples) folder.
      - Do the exact same method but for note types. Ex. [Crochet, Minim]
    - Step (-)
      - Pick three random numbers (starting number, ending number, and length)
      - Lets say starting number is 3, ending number is 7, and lenght is 8
      - Then we evenly decrease from 7 to 3 using only 8 numbers.
        - Ex. [7, 6, 6, 5, 5, 4, 4, 3]
      - Convert those values to the correct name files in [Piano Samples](Piano%20Samples) folder.
      - Do the exact same method but for note types. Ex. [Crochet, Minim]
      - TL;DR, we simply do the exact same thing as we did in `Step (+)` except we reverse the lists.
    - Step (Random)
      - Pick three random numbers (starting number, ending number, and length)
      - Lets say starting number is 3, ending number is 7, and lenght is 8
      - Then we evenly increase from 7 to 3 using only 8 numbers.
        - Ex. [3, 6, 5, 4, 6, 5, 4, 7]
      - Convert those values to the correct name files in [Piano Samples](Piano%20Samples) folder.
      - Do the exact same method but for note types. Ex. [Crochet, Minim]
      - TL;DR, we simply do the exact same thing as we did in `Step (+)` except we randomize the lists.
    - Random
      - Pick notes at random.


## Plans
- [ ] Make pre-configured genres.
- [x] Text to music
- [ ] Image to music
- [x] Possibly make the generation process faster.
- [x] Better visual GUI
- [ ] Better quality sounds.
- [ ] More than just piano sounds.
  - For the time being you can change the sounds yourself by going to the [Piano Samples](Piano%20Samples) folder and edit them yourself. ***DO NOT CHANGE THE FILE NAMES! If you do the program will not work and it will crash.***
- Better generating algorithms.
## ToDo 
- [x] Convert Audio to Video
  - [ ] Implement conversion to `main.py`.
- [ ] Refactor `Step` Algorithm

## Known Bugs
- [ ] Audio clipping with `demisemiquaver` & `semiquaver` notes.
  - Possible needs a longer fade, or better quality sounds.
- [x] Fix `Step` Algorithm.
- [x] Fix crashes with `QThread`
