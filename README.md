# Basketball Substitution Manager

A simple web app for managing basketball team substitutions during games.

## Live App

**https://wlicamele.github.io/basketball-subs/**

## Features

- **Player Management**: Track players with jersey numbers and skill ratings (handling, shooting, defense)
- **Game Management**: Start games, track quarters, and manage who's on court
- **Smart Substitutions**: AI-powered suggestions for balanced rotations
- **Playing Time Rules**: Ensures each player gets ≥1/2 of each quarter
- **Win/Loss Tracking**: Record game outcomes for analysis
- **CSV Roster Management**: Update your roster from a CSV file

## Managing Your Roster with CSV

You can manage your team roster using the `players.csv` file. This is useful for bulk updates or managing your roster from your computer.

### CSV Format

```csv
number,name,handling,shooting,defense
1,Player One,3,4,3
2,Player Two,4,3,4
```

- **number**: Jersey number (0-99)
- **name**: Player name
- **handling**: Ball handling skill (1-5)
- **shooting**: Shooting skill (1-5)
- **defense**: Defense skill (1-5)

### How to Update Roster via CSV

1. Edit `players.csv` in this repository (click the file, then click the pencil icon to edit)
2. Update player information following the format above
3. Commit your changes to the main branch
4. Open the app and click the "🔄 Load from CSV" button on the Roster tab
5. Your roster will be updated!

**Note**:
- If a player number already exists, their information will be updated
- New player numbers will be added to the roster
- Players not in the CSV won't be deleted (delete them manually in the app if needed)

## Privacy

All game data (roster, games, stats) is stored in your browser's localStorage - it never leaves your device. The app hosted on GitHub Pages only contains the code, not your data.

## Substitution Rules

Based on standard youth basketball rules:
- All players must play at least 1/2 of each quarter (unless arriving late)
- Players arriving late must play at least 1/2 of remaining quarters
- Substitutions occur at mid-quarter or between quarters
- Free substitutions in overtime

## How to Use

1. **Add Players**: Go to Roster tab and add your team
2. **Start a Game**: Go to Game tab, select available players, and start
3. **Make Substitutions**:
   - Click players on court to sub them out
   - Click bench players to sub them in
   - Use "Suggest Subs" for smart recommendations
4. **Track Time**: App automatically tracks playing time per quarter
5. **End Game**: Record win/loss when game is complete

## Local Development

This is a single-page HTML app with no build step required:

```bash
# Just open the file in a browser
open index.html
```

Or serve it locally:

```bash
python -m http.server 8000
# Then visit http://localhost:8000
```
