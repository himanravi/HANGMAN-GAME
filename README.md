# 🎯 Hangman Game

*Modern take on the classic word-guessing game built with HTML, CSS & Vanilla JavaScript.*

<p align="center">
  <img src="https://img.shields.io/badge/Made%20with-HTML5-orange?style=for-the-badge&logo=html5" alt="HTML5"/>
  <img src="https://img.shields.io/badge/Styled%20with-CSS3-blue?style=for-the-badge&logo=css3" alt="CSS3"/>
  <img src="https://img.shields.io/badge/Powered%20by-JavaScript-yellow?style=for-the-badge&logo=javascript" alt="JavaScript"/>
  <img src="https://img.shields.io/github/license/himanravi/HANGMAN-GAME?style=for-the-badge" alt="License"/>
  <img src="https://img.shields.io/github/stars/himanravi/HANGMAN-GAME?style=for-the-badge&logo=github" alt="Stars"/>
  <img src="https://img.shields.io/github/forks/himanravi/HANGMAN-GAME?style=for-the-badge&logo=git" alt="Forks"/>
</p>

---

## 🌑 About

A lightweight, client-side **Hangman** game. Guess the hidden word one letter at a time using the on-screen keyboard.  
Each wrong guess advances the hangman illustration — guess the full word before the man is complete!  
Every word has a hint to help the player. Designed to be responsive and mobile-friendly.

---

## 📂 Project Structure

```text
📦 HANGMAN-GAME
├── index.html                     # Game UI / markup (modal, container, keyboard)
├── style.css                      # Styling, layout, responsiveness
├── scripts/
│   ├── word-list.js               # Word bank (array of { word, hint })
│   └── script.js                  # Game logic: selection, input, win/lose, UI updates
├── assets/
│   ├── hangman-0.svg … hangman-6.svg  # Hangman stage images (SVG)
│   ├── victory.gif / lost.gif      # Game over animations
│   └── screenshots/                # optional preview images
└── hangman-game-word-list.txt      # optional backup of word list
⚡ Features
🎨 Clean, dark-friendly UI layout

🧩 Random word selection with helpful hints

🎮 Interactive on-screen keyboard (A–Z)

🔄 Play Again resets the game with a new word

📱 Responsive for mobile & desktop

🚀 Getting Started
1. Clone
bash
Copy code
git clone https://github.com/himanravi/HANGMAN-GAME.git
cd HANGMAN-GAME
2. Run
Open index.html in your browser or serve the folder with Live Server in VS Code.

📸 Screenshots
<p align="center"> <!-- replace with real images in /assets --> <img src="./assets/gameplay.png" alt="Gameplay Screenshot" width="420"/> <img src="./assets/gameover.png" alt="Game Over Screenshot" width="420"/> </p>
If images don’t show, make sure ./assets/ contains the named files (gameplay.png, gameover.png).

🛠️ Built With
HTML5 — structure and semantic markup

CSS3 — styling and responsive layout

JavaScript (ES6) — game logic, event handling, DOM updates

🤝 Contributing
Contributions are welcome! Suggested workflow:

Fork the repo

Create a feature branch: git checkout -b feat/my-feature

Commit changes: git commit -m "feat: add …"

Push and open a PR

Please keep changes small & focused. Add new words to scripts/word-list.js as objects:

js
Copy code
{ word: "guitar", hint: "A string instrument" }
📜 License
This project is licensed under the MIT License — see LICENSE for details.

<p align="center">Made with ❤️ using <b>HTML, CSS & JavaScript</b></p> ```