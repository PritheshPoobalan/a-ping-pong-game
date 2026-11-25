Pripro Pong Game
================

A browser-based pong game built with HTML, CSS and JavaScript. Play against an AI opponent across multiple levels with score tracking.

Features
--------
- Player versus AI pong gameplay
- Multiple levels with increasing AI difficulty
- Score tracking for player and AI
- Responsive layout
- Content Security Policy headers
- Supabase integration for leaderboard data

Controls
--------
Move your paddle: Up and Down arrow keys (or W and S)
Pause / unpause: P or Esc
Start game: Spacebar
See Controls.txt for the full control reference.

How to run
----------
No installation or build step is required. Open index.html in a modern web browser.

To run a local server (optional):
    python3 -m http.server 8000
    # then open http://localhost:8000

Configuration
-------------
game.js exposes a config object with the following fields:

- supabaseUrl: Supabase project URL used by the leaderboard client.
- supabaseKey: public Supabase anon key used by the leaderboard client.
- gameSettings.initialLevel: starting level (default 1).
- gameSettings.maxLevel: maximum level cap (default 10).
- gameSettings.aiDifficultyCurve: AI difficulty scaling factor (default 0.5).

The Supabase URL and anon key in game.js are placeholders. Replace them with
values from your own Supabase project settings before connecting to a real
leaderboard. See docs/CONFIG.md for details.

Project structure
-----------------
- index.html   - main page
- game.js      - game logic
- style.css    - styles
- Controls.txt - game controls
- CNAME        - GitHub Pages custom domain (priprostudios.js.org)
- leaderboard.html - scoreboard page
- docs/        - project documentation (GAMEPLAY.md, PROJECT-STRUCTURE.md, CONFIG.md)

The repository also contains several self-contained subprojects, including
DuckOS-main, v86-master, chilibowlflash-main and games-gh-pages. Each one has
its own index.html and can be opened directly in a browser.

Deployment
----------
This site is published on GitHub Pages with the custom domain priprostudios.js.org.

License
-------
MIT

Contributing
------------
Fork the repository, make changes on a feature branch and open a pull request
against the main branch. Please keep changes additive where the original
project markers are preserved, for example the placeholder sections in
game.js.
