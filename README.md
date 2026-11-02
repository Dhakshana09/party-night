# Party Night 🎭
 
A free browser game for playing **Imposter**, **Werewolf** and **Mafia** with friends. The app deals each player a secret role on their own phone. Everything else, the talking, the nights and the voting, happens in person.
 
**Play now:** https://dhakshana09.github.io/party-night/
 
No accounts, no installs, nothing to pay. One person creates a room; shares the link and everyone joins from their phone.
 
## How to play
 
1. One person opens the link, types a name and taps **Create a room**.
2. Tap **Invite** to share the link, or give friends the 4 letter room code. They tap **Join room**.
3. The host picks a game and its settings, then taps **Start game**.
4. Everyone taps **Show** to see their secret card, and keeps it hidden.
5. Play in person.
6. At the end the host taps **Reveal roles**, then chooses **Play again** or **End game**.
## The games
 
**Imposter** (3 or more players)
Everyone gets the same secret word, except the imposter, who only sees the category and an optional one word hint. There are 80 words across 8 categories, and the host can choose which categories to use and how many imposters there are.
 
**Werewolf** (4 or more players, 5 with a narrator)
Villagers hunt the hidden werewolves. Roles you can switch on or off: Seer, Doctor, Witch, Hunter, Cupid, Masons and Tanner. Werewolves are shown who their pack is.
 
**Mafia** (4 or more players, 5 with a narrator)
Town hunts the hidden mafia. Roles you can switch on or off: Detective, Doctor, Godfather, Vigilante, Bodyguard, Escort and Jester. The mafia are shown who their family is.
 
In Werewolf and Mafia the host can act as the **narrator**. The narrator gets no role, but sees everyone's role, a short script for each night that only covers the roles in play, and can cross out players who are out.
 
## Why only roles?
 
The first version had typed clues and in app voting. Playing it in person made it clear the app was getting in the way, so those parts were removed. Now the app does the one thing a phone is good at, keeping secrets, and people do the rest face to face.
 
## How it works
 
* The whole game is a single `index.html` file, written in plain HTML, CSS and JavaScript with no framework.
* It is hosted for free with **GitHub Pages**.
* Players connect directly to each other with **PeerJS** (WebRTC). The free PeerJS server only introduces the phones to each other. After that, game data goes straight between them.
* The host's browser acts as the game server and holds the roles. Each player is only ever sent their own role.
* There is no database and no tracking. Names exist only while a game is running.
## Testing
 
* Automated browser tests with simulated players cover dealing roles, secrecy of roles, reconnecting after a refresh, ending a game and room recovery.
* The live site has been tested with several browser tabs on the real network.
## Known limits
 
* If the host closes or refreshes their page, the game ends. The host should keep the page open.
* Some school, office or mobile networks block direct connections. Wi-Fi usually works.
* It has been tested with browser tabs and on real phones.
## About this project
 
Designed, tested and directed by Dhakhana (me) . The code was written with AI assistance (Claude). The game design, the decision to focus on roles only, and the feedback from testing are mine.
 
## Ideas for later
 
* Custom word lists for Imposter
* More roles and more game modes, such as Undercover, Spyfall and Avalon
* Keeping a room alive if the host refreshes
