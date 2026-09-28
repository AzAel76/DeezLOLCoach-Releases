# LoL Coach

LoL Coach is a free pre-game coach for League of Legends on Windows.

- **Champ select:** as soon as you lock in your champion, it gets a rune page ready and imports it into the client, together with summoner spells and starting items.
- **Game plan:** it builds a plan for your matchup covering the laning phase, objectives, mid game and late game.
- **In game:** small see-through overlays show what matters in the current phase of the game, track your CS against a target, and remind you of key timings. Reminders can be read aloud.
- **After the game:** it reviews your game against the plan and gives you one thing to focus on next time, and tracks your trends across games.

It uses Google's Gemini free tier by default, so it costs nothing to run.

## Download

Get **LoLCoach_x.y.z_x64-setup.exe** from the **[latest release](https://github.com/AzAel76/DeezLOLCoach-Releases/releases/latest)** and run it. It installs for your Windows user only, without administrator rights, and keeps itself up to date.

- **Needs** Windows 10 or 11, a free Gemini API key (setup shows you how), and League set to **Borderless** window mode.
- **Windows may warn you** with "Windows protected your PC", because the app isn't signed with a paid certificate. Click **More info**, then **Run anyway**.

## How to use it

Read the **[quick start guide](https://azael76.github.io/DeezLOLCoach-Releases/)**. It covers setup, what you'll see during a game, hotkeys, tips and troubleshooting. It's also [here as text](docs/QUICKSTART.md), and each release includes `LoLCoach-QuickStart.html` to open offline.

## Riot's rules

- **Made before the game:** your rune page and game plan are made before the game and never change during it.
- **In game, it reads only two things:** the game clock and your own CS. It never reads game memory, tracks enemies or cooldowns, or reacts to kills, objectives or turrets.
- **Official data only:** it uses Riot's own local client and game APIs, and the public Data Dragon data.
- **Your rune pages are safe:** it only creates or replaces a page called "LoL Coach".

LoL Coach isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games and all associated properties are trademarks or registered trademarks of Riot Games, Inc.

## Privacy

- **Stored on your PC:** your API key, settings, game history and log are saved in `%APPDATA%\LoLCoach` and never uploaded anywhere.
- **Sent to the AI provider:** only the champion draft, your notes and your post-game stats. On Gemini's free tier, Google may use those requests to improve its products.
- **Sent only when you choose:** the log goes to the developer's Discord only when you choose **Send log to Discord**. It never contains your API key.

## Problems or ideas

Right-click the tray icon and choose **Send log to Discord**, or tell whoever shared LoL Coach with you.
