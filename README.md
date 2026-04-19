# Flamme Rouge: Grand Tour - Solo Bot App

An unofficial web application designed to simulate Specialist Riders (Bots) for a Single Race or a multi-stage Grand Tour in the board game *Flamme Rouge*.

## About this Project

This application is based on a fan-made [solo version published on BoardGameGeek](https://boardgamegeek.com/filepage/288985/flamme-rouge-grand-tour-solo-rules) by Fredrik Stahre. The original aim of his variant was to enable Flamme Rouge Bots to utilize all the new rules and specialist powers introduced in the *Grand Tour* expansion.

Playing this solo variant physically requires printing, cutting, and managing a substantial amount of custom cards, which increases table space requirements and administrative overhead. This app digitizes the process. It simulates the drawing, playing, and shuffling of Energy Cards for Specialist Riders, allowing a human player to compete against up to five independent Bot Teams.

**Disclaimer:** This project is a fan creation and is not commercially associated with the game's author, Lautapelit.fi, or any other publisher.

## Features

* **Digital Deck Management:** Automatically handles the draw, recycle, and discard piles for all Specialist Riders.
* **Race Modes:** * *Single Race:* Standard race where everything resets after crossing the finish line.
  * *Grand Tour:* Multi-stage mode where half of each Bot's accumulated Exhaustion Cards are carried over to the subsequent stage.
* **Team Setup:** Manage 1 to 5 Bot Teams. Each team must consist of exactly one Rouleur and one Sprinteur.
* **Exhaustion Handling:** Centralized phase at the end of each round to distribute Exhaustion Cards to affected Riders efficiently.
* **Persistent State:** The app uses your browser's local storage to save the current state automatically. You can close the browser and resume your game later. No login is required, and no data is transmitted to external databases.

## How to Use the App

### 1. Setup
* On the setup screen, select your preferred **Race Mode** (Single Race or Grand Tour).
* Choose the **Number of Bot Teams** you wish to compete against.
* Assign a unique color to each team and recruit their Specialist Riders from the available roles.
* Click **Start Race** to begin the first round.

### 2. Gameplay Loop
* During the race, select a Rider in turn order (starting from the front of the peloton) to open their dedicated action panel.
* Click **Draw Card** to reveal an Energy Card from the Rider's deck.
* If the rules require a second card to be drawn, click **+ 2nd Card?**.
* Select the card to be played by clicking on it and move the physical Rider on your game board according to the Movement Points.
* Click **Done** to close the panel and proceed to the next Rider in turn order.

### 3. Exhaustion Management
* **During a turn:** After playing an Energy Card, a Rider may discard one Exhaustion Card from the game. You can adjust the total number of Exhaustion Cards manually using the **(+/-)** buttons in the Rider's panel.
* **End of round:** Do not manually add Exhaustion Cards for Riders who become exhausted at the end of the movement phase. Once all Riders have completed their turns, a centralized panel will appear, prompting you to distribute Exhaustion Cards to the affected Riders before proceeding to the next round.

### 4. Finishing the Race
* If a Rider crosses the finish line during the round, check the **Race finished?** box in their action panel. This marks them with a flag icon and excludes them from the card draw in all future rounds of the current stage.

## Credits

* **Solo Rules Design:** Fredrik Stahre
* **App Development:** Oliver Baentsch ([Brettspielelust](https://www.brettspielelust.de))

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
