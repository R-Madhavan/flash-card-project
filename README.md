# Flash-Card_Project (Flashy)

Flashy is a language-learning flashcard app built with Python's Tkinter GUI toolkit. It displays a French word on a flashcard, then flips to reveal its English translation after a short delay. Users can mark if they know the word, and the app saves words that the user still needs to learn.

## Features

- Randomly displays a French word and flips to show its English translation after 3 seconds.
- Users can mark if they know a word; known words are removed from the review list.
- Progress is saved automatically, so only unfamiliar words will appear next time.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/flashy.git
   cd flashy
   ```

2. Install the required libraries:
   ```bash
   pip install pandas
   ```

3. Place your word data files and images:
   - `french_words.csv` (French-English word list) in the `data` folder.
   - `card_front.png`, `card_back.png`, `right.png`, and `wrong.png` in the `images` folder.

## File Structure

```
flashy/
├── data/
│   ├── french_words.csv       # The original French-English word list
│   └── words_to_learn.csv     # Tracks remaining words to learn (This file will be created once the program start's running)
├── images/
│   ├── card_front.png         # Front of the flashcard
│   ├── card_back.png          # Back of the flashcard
│   ├── right.png              # Checkmark icon for "I know this word"
│   └── wrong.png              # Cross icon for "I don't know this word"
└── main.py                    # The main Python script for Flashy
```
### How It Works

- **Flashcards**: Each card displays a French word initially and flips after 3 seconds to reveal the English translation.
- **Buttons**: 
  - **Right Button**: Mark a word as known, which removes it from the review list.
  - **Wrong Button**: Move to the next card without marking the current word as known.

### Data Persistence

- Known words are saved to `words_to_learn.csv`, allowing progress to continue from where you left off next time.

## Dependencies

- Python 3.x
- `pandas` library for data management
- `tkinter` for the graphical interface (included in Python standard library)

## Contributing

Contributions are welcome! Feel free to submit pull requests for new features, improvements, or bug fixes.
