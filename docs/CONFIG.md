# Configuration — Pripro Pong Game

## Runtime configuration (game.js)

game.js exposes a config object read when the game starts:

```js
const config = {
  supabaseUrl: 'https://xvdeijzqjumkvchxabwc.supabase.co',
  supabaseKey: '<your-supabase-anon-key>',
  gameSettings: {
    initialLevel: 1,
    maxLevel: 10,
    aiDifficultyCurve: 0.5
  }
};
```

- supabaseUrl: Supabase project URL used by the leaderboard client.
- supabaseKey: public Supabase anon key used by the leaderboard client.
- gameSettings.initialLevel: starting level (default 1).
- gameSettings.maxLevel: maximum level cap (default 10).
- gameSettings.aiDifficultyCurve: AI difficulty scaling factor (default 0.5).

## Using your own Supabase project

The Supabase URL and anon key in game.js are placeholders from the original
project. Before connecting to a real leaderboard, replace them with values
from your own Supabase project settings (API > URL, and Project API keys >
anon / public key).

These values are client-side credentials by design: the Supabase client runs
in the browser. Protect leaderboard data with Supabase Row Level Security
(RLS) policies rather than by hiding the anon key.

## Game settings

Adjust gameSettings to change the difficulty progression:

- Raise aiDifficultyCurve to make the AI harder at higher levels.
- Lower maxLevel to shorten the progression.
- Change initialLevel to start at a different level.

No build step is required: edit game.js and refresh the browser to test.
