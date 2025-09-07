# Hangman Game  классическая игра палач

A classic, browser-based Hangman word-guessing game built with vanilla HTML, CSS, and JavaScript. This project features dynamic word and hint generation, an interactive on-screen keyboard, and a clean, responsive interface.



---

## ✨ Features

* **Dynamic Word Selection:** Randomly selects a word and a corresponding hint from a predefined list for endless replayability.
* **Interactive Keyboard:** A dynamically generated on-screen keyboard that tracks used letters.
* **Visual Feedback:** The hangman drawing is updated with each incorrect guess, providing clear visual progress.
* **Win/Loss Conditions:** A popup modal clearly indicates whether you've won or lost, showing the correct word at the end.
* **Play Again:** A simple "Play Again" button allows the user to restart the game with a new word instantly.
* **Responsive Design:** The layout adjusts seamlessly for a great experience on both desktop and mobile devices.

---

## 🛠️ Technologies Used

* **HTML5:** For the core structure and content of the game.
* **CSS3:** For all styling, layout (using Flexbox), and responsive design (`@media` queries).
* **JavaScript (ES6):** For all game logic, DOM manipulation, and event handling.

---

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You only need a modern web browser like Google Chrome, Firefox, or Safari.

### Installation

1.  Clone the repository:
    ```sh
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```
2.  Navigate to the project directory:
    ```sh
    cd your-repository-name
    ```
3.  Open the `index.html` file in your web browser.

That's it! You're ready to play.

---

## 📂 Project Structure

The project is organized into clear and distinct files, separating structure, style, and logic.

```
/
├── index.html          # The main HTML file containing the game's structure and modals.
├── style.css           # The stylesheet responsible for all visuals and responsiveness.
├── images/             # Contains all static assets.
│   ├── hangman-0.svg
│   ├── hangman-1.svg
│   ├── ...
│   ├── victory.gif
│   └── lost.gif
└── scripts/
    ├── word-list.js    # The "word bank" containing the array of words and hints.
    └── script.js       # The "brain" of the game, handling all functionality and logic.

```

* **`index.html`**: Defines the skeleton of the application, including the hangman display area, the game box for hints and guesses, the word display placeholders, the keyboard container, and the hidden "Game Over" modal.
* **`style.css`**: Provides the visual presentation. It styles the layout, typography (using the "Open Sans" Google Font), keyboard buttons, and the game-over modal. A media query ensures the game is playable on smaller screens by adjusting the layout to a single column.
* **`scripts/word-list.js`**: Contains a single JavaScript array, `wordList`. Each element is an object with two properties: `word` (the secret word) and `hint` (the corresponding hint).
* **`scripts/script.js`**: This file contains all the game's logic. It handles selecting a random word, generating the keyboard, processing player guesses, updating the hangman image, checking for win/loss conditions, and resetting the game.

---

## 🧠 How It Works

The game's logic is driven entirely by client-side JavaScript in `script.js`.

1.  **Initialization:** When the page loads, the `getRandomWord()` function is called. It selects a random word object from the `wordList` array and calls `resetGame()` to set up the new round.
2.  **Game Setup:** The `resetGame()` function initializes the game state: it clears previous guesses, resets the wrong guess count, updates the hint text, and dynamically creates the letter underscores in the word display.
3.  **Player Interaction:** The script generates a button for each letter of the alphabet. An event listener is attached to each button.
4.  **Guess Processing:** When a player clicks a letter, the `initGame()` function is triggered.
    * If the guessed letter is **in** the secret word, all matching letters are revealed on the screen.
    * If the guessed letter is **not** in the word, the `wrongGuessCount` is incremented, and the hangman image is updated to the next stage (e.g., from `hangman-1.svg` to `hangman-2.svg`).
5.  **Game Over:** After each guess, the script checks for a win (all letters revealed) or a loss (6 incorrect guesses). If either condition is met, the `gameOver()` function is called.
6.  **End State:** The `gameOver()` function displays the modal popup with the appropriate message ("Congrats!" or "Game Over!"), a celebratory or defeat GIF, and the correct word.
7.  **Restarting:** Clicking the "Play Again" button inside the modal simply calls `getRandomWord()` again, starting the entire cycle over with a new word.