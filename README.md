# Pomodoro

A minimal single-page Pomodoro timer with cat GIFs. No build step, no dependencies: one `index.html`.

## Run

Serve the folder on localhost and open it in a browser:

```bash
python3 -m http.server 8765
```

Then visit http://localhost:8765.

## Features

- Pick a focus length and a relax length in minutes (defaults 15 / 5), and optionally a number of cycles (focus sessions). Leave cycles empty to keep going; with a number, the last focus ends in a FINISHED screen with the relax sound and gifs, no timer.
- **Start** runs the cycle focus → relax → focus … with a minimalistic counter. Space also starts/pauses. **Skip** asks for confirmation, then ends the current period and starts the next one at once.
- A sound plays when a period ends: "yippie" after focus, "faaah" after relax (both from myinstants.com). Each is a URL you can change, or clear for a built-in soft bell.
- GIFs pop up in random places on the screen during both phases; focus and relax have their own sets.
- The cog in the top-right corner opens settings: add/remove GIF (or short mp4/webm) URLs per phase, tune how long each GIF stays and how soon the next one appears, set the end-of-focus and end-of-relax sounds, restore defaults.
- Under the counter: completed focus sessions, overall running time and focus-only time.
- Settings are saved in the browser's local storage.
