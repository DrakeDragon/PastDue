# PAST DUE

**A Notice-to-Vacate LitRPG.** A free, single-page, choose-your-own-adventure that plays in your phone's browser.

> The planet missed its rent. Your building is now a dungeon. You are the night maintenance tech, and the whole universe is watching you try to get out.

Play it here: *(paste your GitHub Pages link)*

---

## What it is

Past Due is a long, funny, interactive LitRPG in the tradition of *Dungeon Crawler Carl*. Earth has been served an eviction notice by a cosmic landlord. Your apartment building has turned into a ninety-nine-floor tower of absurd, bureaucratic monsters, and a sarcastic System narrator is livestreaming every move to an audience of billions.

You climb. You fight. You loot. You make friends. And you slowly work out who owns the building, why the rent is overdue, and what it will take to settle the account.

The tone is dark comedy with a real heart. It is a joke about paperwork until, somewhere around the middle, it quietly stops being only a joke.

## Features

- **99 floors of story** told in 23 parts, with a full beginning, middle and ending
- **Branching choices.** Your decisions change scenes, who joins your party, and which of three endings you get
- **Real stat checks.** Four stats (Grit, Wits, Nerve, Tinker) with dice rolls on risky choices
- **Turn-based combat** with attacks, tricks, bracing, items, boss special moves and boss phases
- **Loot and gear.** Hundreds of weapons, armor, trinkets and consumables, with upgrades and a pack screen
- **Loot boxes** at the end of each floor boss
- **A talking smoke detector.** Chirp is your sidekick, with a battery you manage and abilities you can use in a fight
- **A System narrator** who announces everything, from level-ups to evictions, with sarcasm
- **A live audience.** A scrolling viewer count and chat strip react to what you do
- **Over 230 achievements** with funny names and descriptions, plus hidden secret ones
- **Safe rooms** between floors with a shop, a rest, and a quiet scene with a member of your party
- **A party** of memorable characters who join you on the climb
- **Autosave** in your browser, so you can close the page and come back
- **Built for phones.** Large readable text, big touch buttons, and A- / A+ buttons to change the text size
- **Optional sound effects**, off by default

## How to play

1. Open the page and enter a name for your tenant.
2. Tap **Accept Lease** to begin.
3. Read the story, then tap one of the choices to continue.
4. Some choices show a stat check. Your stat plus a die roll must meet the target number.
5. In a fight, use **Attack**, **Trick**, **Chirp**, **Brace** or **Items**. Watch for boss warnings and brace when a big attack is coming.
6. Open **Pack** at the top for your gear, stats, loot boxes, achievements and menu.
7. Losing a fight is called an **eviction**. You restart from the last checkpoint with no real penalty, so take risks.

### Tips

- Try the odd option. The silly or kind choice often works better than the obvious one.
- Boss fights usually have several ways in. A clever approach can make the fight much shorter.
- Talk to everyone in the safe rooms. Those scenes are where the story lives.
- Be kind when you get the chance. The ending notices.
- Spend your scrap on upgrades, and use consumables before a boss, not after.

## Length

A full playthrough runs for many hours. Fights are quick, so most of that time is reading and choosing. Most people play it in short sessions across several days. There are three different endings, and your choices along the way change the epilogue.

## Content notes

Mostly comic fantasy. Contains cartoon violence, workplace and bureaucratic satire, mild language, and some sad and emotional scenes about loss, grief and forgiveness. No graphic content.

## Hosting on GitHub Pages

1. Create a public repository on GitHub.
2. Upload `index.html` to the root of the repository.
3. Go to **Settings > Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute or two your game is live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`.
5. To update the game, upload a new `index.html` over the old one. Players may need to refresh once or twice to see the new version.

Everything runs in the browser. There is no server, no account, and no tracking. Progress is saved only on each player's own device.

## Technical notes

- A single self-contained HTML file with no frameworks and no build step needed to play
- Loads four Google Fonts, and falls back to system fonts offline
- Saves progress to the browser's local storage
- The source is in `source/src` for editing. With Node.js installed, run `node build.js` to rebuild the game and `node validate.js` to check that every story link works

## Credits

Story, design and System narration by Tim, built with Claude.

Inspired by the LitRPG genre, and by every landlord who ever said "I'll get to it this week."

---

*Management would like to remind you that rent is due. Management would also like to remind you that you may pay when able.*
