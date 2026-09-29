# LoL Coach quick start

LoL Coach gets your rune page ready as soon as you lock in your champion, builds a game plan for your matchup, and shows it in small overlays while you play. It reminds you of key timings, tracks your CS, and reviews your game afterwards. Setup takes about five minutes.

## 1. Install

1. Download **LoLCoach_x.y.z_x64-setup.exe** from the [releases page](https://github.com/AzAel76/DeezLOLCoach-Releases/releases/latest).
2. Run it. It installs for your Windows user only, so it doesn't need administrator rights. Windows may show "Windows protected your PC", because the app isn't signed with a paid certificate. Click **More info**, then **Run anyway**.
3. LoL Coach starts when the installer finishes. You'll find it in the Start menu afterwards.

You need Windows 10 or 11. If nothing opens on an older Windows 10 PC, install Microsoft's free [WebView2 Runtime](https://developer.microsoft.com/microsoft-edge/webview2/) and try again.

**Updates:** the app checks for a new version when it starts and asks before installing it, never during a game. To check yourself, open Settings → **Updates**, or right-click the tray icon and choose **Check for updates**.

## 2. Add a free AI key

The Settings window opens the first time you run the app.

1. On the **Setup** tab, keep **Gemini (free tier)** selected.
2. Click **Get a free Gemini key**, sign in with a Google account and create a key. You don't need a credit card.
3. Paste the key into **API key**, then click **Test connection**. You should see "Connected".
4. Click **Save**.

The app now runs in the system tray, as a blue "C" icon near the clock. You may need to click the **^** arrow to see it.

## 3. Set up League

In League, go to **Settings → Video → Window Mode** and choose **Borderless**. The overlays can't draw over Fullscreen mode.

## 4. Play

| When | What you see |
|---|---|
| **Champ select** | As soon as you lock in your champion, a **runes window** shows the client's recommended rune page. A few seconds later it switches to a page tuned for your matchup. Each page is imported into the client as a page called **LoL Coach**, ready before the game loads. The window also lists summoner spells and starting items. |
| **Loading screen** | Your game plan is built while the game loads. |
| **In game** | The **game plan** overlay shows only what matters now: laning until 14:00 (when turret plating ends), then mid game until 25:00, then late game. It changes on the game clock. The plan is written for your role: junglers get a first clear, gank timing and ward spots; laners get a trade pattern, wave plan and all-in window; supports get a lane pattern, vision plan and roam windows. A small **CS tracker** shows your CS, CS per minute and how you're doing against a target. Pop-ups at the top of the screen, read aloud, remind you of gank windows, objectives, power spikes and more. |
| **After the game** | About a minute after the game ends, a **Review** appears: your key stats, what went well and what to fix, and **one focus for next game**. |

The in-game overlays are see-through and click-through, so they never block your clicks.

**Runes:** the app never changes or deletes your own rune pages. It only creates or replaces the page called "LoL Coach". If you already have as many pages as your account allows, delete one or rename one to "LoL Coach", and the app will use it.

## 5. Hotkeys

| Keys | What it does |
|---|---|
| **Ctrl+Shift+O** | Show or hide the in-game overlays |
| **Ctrl+Shift+L** | Switch the game plan between **Now**, **Build** (items and skill order) and **Matchup** (both teams' strengths and threats, and mechanics tips for your matchup) |
| **Ctrl+Shift+P** | Build the game plan now, or rebuild it |
| **Ctrl+Shift+M** | Move overlays on or off: drag the game plan and CS tracker where you want them, then press again to lock them |

You can change these in Settings, under **Hotkeys**.

## 6. The tray menu

Right-click the tray icon for these options:
- **Show / hide overlay**, **Next page**, **Build / rebuild plan**, **Move overlays**
- **Review last game**, to review a game that ended while the app wasn't running
- **Game history & improvement…**, which lists your past games with their reviews. Its second tab shows your trends and can build an **improvement plan** after 5–10 games.
- **Settings…**, **Check for updates**, **Open log file**, **Send log to Discord**, **Quit**

## Tips

- **Make the overlays more or less see-through.** Settings → **Overlay** has sliders for the background and text opacity.
- **Set your own CS target.** Settings → **Coaching** → **Target CS per minute**. Leave it at 0 to use a default for your role. The tracker hides its target for supports.
- **Tell it what you know.** Settings → **Coaching** → **Standing notes** is sent with every plan. You could write, for example, "I struggle against poke" or "Patch 26.19 removed item X".
- **Get a natural-sounding voice.** Settings → **Notifications** → **Voice type: Natural** → **Download voice** (about 85 MB, once). Choose Ryan or HFC, then click **Test voice**. Until it's downloaded, the built-in Windows voice is used.
- **Too chatty?** In Settings → **Notifications** you can turn off reminder types, change the voice or its speed, or switch voice off and use a beep instead.
- **Your focus carries over.** The focus from your last review, and your improvement plan's top priority, are added to your next game plan.
- **Gank warnings are predictions** based on typical jungle paths. Read them as "be ready", not "it's happening".

## Troubleshooting

| Problem | Fix |
|---|---|
| The overlay says "Waiting for the League client…" | Open the League client. If League is installed somewhere other than `C:\Riot Games`, go to Settings → **Coaching** → **Client lockfile** and choose the `lockfile` file in your League folder. |
| No overlays in game | Set League to **Borderless** (step 3). Press **Ctrl+Shift+O** in case you hid them. |
| The runes window didn't appear | It appears once you've locked in your champion. If you closed it, it comes back in the next champ select. |
| "No free rune page" | Delete one of your rune pages, or rename one to "LoL Coach". |
| Hotkeys don't work while League is focused | Update to version 0.3.1 or later, where hotkeys work without tabbing out. If they still don't, right-click LoL Coach in the Start menu, choose **Run as administrator**, and try again. |
| "Couldn't build the plan" | Check your key with **Test connection** in Settings, then press **Ctrl+Shift+P** to retry. |
| "High demand", "limiting requests" or "daily limit … used up" | Gemini's free tier allows only a few requests per model each day (as few as 20), and it's often busy. The app automatically tries the backup models in Settings → **Setup**, which each have their own quota, and daily limits reset at midnight Pacific time. For more headroom, set up an **Other provider** in the same tab: Groq, OpenRouter and Mistral have their own free tiers, and a model on your own PC (Ollama or LM Studio) has no limits. Tick "try my other providers" to use it as a backup. |
| No review after a game | Reviews skip remakes and modes other than Summoner's Rift. Otherwise, choose **Review last game** from the tray menu. |
| Windows or your antivirus blocks the app | The app is unsigned, not harmful. Choose **More info → Run anyway**, or add an exception for LoL Coach in your antivirus. |

## Reporting a problem

The app keeps a log of what it did and any errors in `lolcoach.log`. It contains no API keys. Your settings, history and log are in `%APPDATA%\LoLCoach`, and Settings → **Updates** shows the exact folder.

If something goes wrong, right-click the tray icon and choose **Send log to Discord**. A message appears on the overlay when the log has been sent. If it says no Discord link is set, paste the link you were given into Settings → **Coaching** → **Discord link for logs**.

## Good to know

- **It follows Riot's rules.** Your rune page and game plan are made before the game and never change during it. In game, the app reads only the game clock and your own CS. It never reads game memory, tracks enemies or cooldowns, or reacts to kills, objectives or turrets. It is not a Riot-endorsed app.
- **Your data stays with you.** Your key, settings and history are saved on your PC. Only the draft, your notes and your post-game stats are sent to the AI provider. On Gemini's free tier, Google may use those requests to improve its products.
- **Don't share `config.json`.** It contains your API key.
- **Moving from the portable version?** Copy `config.json` and the `history` folder from your old LoL Coach folder into `%APPDATA%\LoLCoach` to keep your settings and game history.
