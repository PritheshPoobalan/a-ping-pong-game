# Gameplay Guide - Pripro Pong Game

## Overview

Pripro Pong Game is a single-player browser-based pong game. You control the player
paddle and the computer controls the opponent paddle. Score points by getting the ball
past the opponent paddle while preventing the opponent from scoring against you.

## Controls

- Move paddle up: Up arrow or W
- Move paddle down: Down arrow or S
- Pause or resume: P or Esc
- Start game: Spacebar

## Levels and difficulty

The game starts at level 1 and supports up to 10 levels. As you progress, the AI
opponent becomes faster and more accurate, so each successive level is harder.

Score is tracked for both the player and the AI across the session.

## Security

The game enforces a Content Security Policy (CSP) that limits scripts, styles, fonts
and network connections to trusted origins. Client-side checks detect if the page is
embedded in a frame or if developer tools are open, and show a security warning badge
when a potential issue is detected.

## Technologies

- HTML5 for page markup and the loading screen
- CSS for layout, design tokens and animations
- JavaScript for game logic, AI opponent and the Supabase client
- Supabase for leaderboard and session state

## License

MIT License. See LICENSE.
