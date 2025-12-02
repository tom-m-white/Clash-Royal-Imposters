# Clash Imposters 👑

**Clash Imposters** is a real-time, multiplayer social deduction game (similar to *Spyfall* or *Among Us*) themed around **Clash Royale** cards. Players are assigned roles, undergo a turn-based interrogation, and vote to eject the Imposter.

Built as a lightweight, single-file web application using **HTML, CSS, JavaScript, and Firebase**.

## 🎮 Game Overview

-   **The Goal:**
    -   **Innocents:** Everyone sees a specific Clash Royale card (e.g., "Mega Knight"). Their goal is to prove they know the card without revealing it too obviously to the Imposter.
    -   **The Imposter:** Sees "IMPOSTER" instead of the card. Their goal is to blend in, figure out what the card is, and avoid being voted out.
-   **Phases:**
    1.  **Lobby:** Create a room and wait for friends.
    2.  **Reveal:** Players see their secret role/card.
    3.  **Interrogation:** Players take turns sending one message to prove their innocence.
    4.  **Voting:** Players vote to eject a suspect or skip to another round of questioning.
    5.  **Results:** The truth is revealed!

## ✨ Features

-   ⚡ **Real-time Multiplayer:** Instant updates using Firebase Realtime Database.
-   📱 **Mobile First Design:** Responsive UI optimized for phones and tablets.
-   🃏 **Huge Card Database:** Includes Commons, Rares, Epics, Legendaries, and Champions.
-   ⏳ **Turn-Based Chat:** Structured interrogation phase with a countdown timer.
-   🗳️ **Voting System:** Dynamic voting logic with skip functionality.
-   🎨 **Clash Themed UI:** Visuals and rarity colors inspired by the game.

## 🚀 Setup & Installation

This project uses **Firebase** for the backend. You must configure it for the game to work.

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/clash-imposters.git
cd clash-imposters
```

### 2. Create a Firebase Project
1.  Go to the [Firebase Console](https://console.firebase.google.com/).
2.  Click **Add project** and give it a name.
3.  Disable Google Analytics (not needed for this).
4.  Click **Create Project**.

### 3. Setup Realtime Database
1.  In your Firebase project dashboard, go to **Build** > **Realtime Database**.
2.  Click **Create Database**.
3.  Select a location (e.g., United States) and click **Next**.
4.  Select **Start in Test Mode** (allows read/write access during development) and click **Enable**.

### 4. Get Your API Keys
1.  Click the **Settings Gear** icon (Project Settings).
2.  Scroll down to the **Your apps** section.
3.  Click the **</> (Web)** icon.
4.  Register the app (any nickname works).
5.  You will see a code block named `const firebaseConfig = { ... }`.

### 5. Update the Code
1.  Open `index.html` in your code editor.
2.  Locate the section labeled `CONFIGURATION - PASTE KEYS HERE` ( line 250 ).
3.  Replace the placeholder values with the keys from your Firebase console:

```javascript
// IN index.html
const firebaseConfig = {
    apiKey: "YOUR_ACTUAL_API_KEY", 
    authDomain: "your-project.firebaseapp.com",
    databaseURL: "https://your-project-default-rtdb.firebaseio.com",
    projectId: "your-project-id",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "123456789",
    appId: "1:12345:web:abcdef"
};
```

### 6. Run the Game
Simply open `index.html` in any modern web browser. 
*Note: Since this is a browser-based game, you can host it for free on GitHub Pages, Netlify, or Vercel.*

## 🕹️ How to Play

1.  **Start:** Enter your name and click **Create Room**.
2.  **Invite:** Share the 4-letter **Room Code** with friends.
3.  **Settings:** The host selects the number of Imposters (1-3).
4.  **Reveal:** Memorize your card! If you are the Imposter, pay attention to the chat.
5.  **Discuss:** When it is your turn, the bar turns blue. Type a hint about the card.
    *   *Good Hint:* "It costs 7 elixir."
    *   *Bad Hint:* "It's the P.E.K.K.A." (The Imposter will win immediately if they know exactly what it is).
6.  **Vote:** Decide who the faker is.

## 🛠️ Technologies Used

-   **HTML5 / CSS3** (CSS Variables for theming)
-   **Vanilla JavaScript** (ES6+)
-   **Firebase Realtime Database** (v8.10.1)

## 🤝 Contributing

Feel free to fork this project and submit pull requests.
*   **Add Cards:** You can add new cards to the `allCards` array in the JavaScript section.
*   **Themes:** Change the CSS variables in `:root` to create new themes.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

*Disclaimer: This project is a fan-made game and is not affiliated with, endorsed, sponsored, or specifically approved by Supercell. Clash Royale and its logos are trademarks of Supercell.*
