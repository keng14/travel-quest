# Travel Quest

A Thai-first (with English) travel checklist game. Plan a trip day by day, pack and complete daily missions, and earn a coin for every finished day. Finish every day to unlock the champion trophy.

**Repo description (short):** Thai/English travel checklist game: daily missions, coins, budgets, infographic export, and a champion trophy.

## Features

- **Language first**: choose Thai or English on open, then a short how-to, then the app.
- **Trip setup**: enter the trip name and start and end dates. Each trip gets a pack stage plus one stage per day, and the last day is the goal.
- **Daily missions**: add items by category (travel, eat, shop, sight, temple, nature, rest, pack, other), or start from a template. Each stage can hold a place, a memo, and photos.
- **Per-day budget**: set a budget per day and log spending against it.
- **Coins and trophy**: completing a day earns a coin. Completing every day unlocks the champion trophy, with a celebration popup.
- **Infographic**: view the trip as a game-style infographic, then save it as an A4 PNG or an HTML file.
- **Backup**: copy your trip data as text. The app reminds you to back up regularly.
- **Sound and effects**: sound effects and confetti, with a toggle to turn effects off.
- **Installable**: a PWA manifest, so it can be added to the home screen on phones and tablets.

## Run it

No build step is needed. The app is one HTML file.

1. Open `index.html` in a browser, or
2. Serve the folder with any static server, for example:

   ```bash
   python3 -m http.server 8000
   ```

   Then open `http://localhost:8000`.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles, and script |
| `manifest.webmanifest` | PWA manifest (name, colors, icon) |
| `icon.svg` | App icon |

## Data and privacy

All data stays in the browser's `localStorage` on the device that made it. Nothing is sent to a server. Clearing site data erases the trip, so use the backup feature to keep a copy.

Storage keys used by the app:

- `travelquest.v3`: trip data
- `travelquest.lang`: chosen language
- `travelquest.fx`: effects on or off
- `travelquest.backupAt`: time of the last backup

## Testing

Tested in a headless Chrome with scripted checks for navigation, the infographic export, popups, templates, and budgets. Not yet tested on a range of real phones.

## License

Add a license before publishing if you want others to reuse the code.
