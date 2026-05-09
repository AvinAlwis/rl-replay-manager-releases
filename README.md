# RL Replay Manager

A desktop application for organising, browsing, and analysing your Rocket League replay files.

**[Download the latest installer →](../../releases/latest)**

---

## Features

### Replay Library

- **Automatic scanning** — finds all `.replay` files in your Steam and/or Epic Games replay folders on startup
- **Card-based browser** — every replay shows its map, score, date, duration, and match type at a glance
- **Card title** — choose whether each card displays the replay's filename or its in-game replay name (configurable in Settings)
- **Live search and filters** — narrow your library instantly by:
  - Text (map name, player name)
  - Map
  - Team size (1v1 through 4v4)
  - Date range
  - Season
  - Casual / competitive toggle
  - Hide-grouped (hide replays already assigned to a group)
- **Bulk selection** — `Ctrl+A` selects all, `Ctrl+click` toggles individual cards, `Ctrl+Shift+click` range-selects

---

### Expanded Replay Detail

Click any replay card to expand it and reveal three collapsible sections.

#### Players
A table showing every player in the match with their **Score, Goals, Assists, Saves, and Shots**.
Click a player's name to open their **camera settings and car loadout** (decals, wheels, boost, trail, goal explosion — with item names if the item database is downloaded).

#### Game Timeline
A per-player swimlane chart visualising the full match.
- **Goals** and **assists** are plotted as coloured markers
- **Demo kills** and **demo deaths** appear on the correct player's lane
- Demo events load automatically in the background from the replay's network data

#### Notes
A rich-text notepad attached to each replay.
- **Bold**, *italic*, underline, font size, and hyperlinks supported
- Notes save automatically as you type and persist between sessions

---

### Section Customisation

- Each section (**Players**, **Game Timeline**, **Notes**) has a clickable header — click to collapse or expand
- **Drag** a section header up or down to reorder all three sections; the new order is saved and applies to every replay
- In **Settings**, toggle "Always show Players / Game Timeline / Notes" to control which sections open by default when you expand a card

---

### Right-Click Context Menu

Right-click any card (or a multi-selection) to access:

| Action | Description |
|--------|-------------|
| **Rename** | Rename the replay file on disk |
| **Edit In-Game Name** | Change the name shown inside Rocket League without re-recording |
| **Open in Folder** | Open the containing folder in Explorer |
| **Upload to ballchasing.com** | Upload selected replays (requires API key) |
| **Assign to Group** | Add replays to one or more groups |
| **Hide / Unhide** | Remove replays from the main view without deleting them |
| **Delete** | Permanently delete replay files |

---

### In-Game Name Editing

The **Edit In-Game Name** action writes a new name directly into the replay file — no third-party tool required. It works on replays that were never named in-game, and is automatically blocked while Rocket League is running to prevent file conflicts.

---

### Player Lookup

- **Click** a player name in the Players table (or on the card summary) to view their **camera settings and loadout**
- **Alt+click** a player name on the card summary to open their **[Rocket League Tracker](https://rocketleague.tracker.network)** profile in your browser

---

### ballchasing.com Integration

- **Upload** — send any replay (or a bulk selection) to [ballchasing.com](https://ballchasing.com) with one click
- **Visibility** — choose Public, Unlisted, or Private for uploads
- **Sync** — check which of your local replays are already on ballchasing.com and mark them in the UI
- **Badge** — uploaded replays show an `↑ ballchasing` badge; click it to open the replay on the website
- **Rate limiting** — requests are automatically paced to your patron tier:

  | Tier | Rate |
  |------|------|
  | Grand Champion | 16 req/s |
  | Champion | 8 req/s |
  | Diamond | 4 req/s |
  | Gold / Free | 2 req/s |

- **API key security** — your key is encrypted with Windows DPAPI, tied to your Windows user account

---

### Groups

- Create named groups to organise replays (e.g. "Ranked", "Clips", "Review")
- **Drag** replays from the main list onto a group to assign them
- **Drag** groups to reorder them in the sidebar
- Filter the list to show only replays in a specific group
- Assign replays to multiple groups via the right-click menu

---

### Themes

Four built-in themes plus a fully customizable option, all switchable live with an instant preview before you confirm:

| Theme | Description |
|-------|-------------|
| **Dark** | Default dark grey |
| **Dark Purple** | Dark with electric violet accents |
| **Midnight** | Deep blue-black |
| **Slate** | Cool blue-grey |
| **Custom** | Fully customizable — pick any colors you like |

#### Custom Theme

Select **Custom** in the theme dropdown to reveal a color picker panel with seven editable color slots:

| Slot | What it affects |
|------|----------------|
| **Background** | Main window background |
| **Surface** | Input fields and list backgrounds |
| **Text** | Primary text |
| **Accent** | Highlights, active buttons, badges, and links |
| **Button** | Standard button backgrounds |
| **Border** | Panel and input borders |
| **Card** | Replay card background |

- Colors apply **live as you pick** — the whole app updates in real time while the color picker is open
- Click **Save as…** to give your color set a name and add it to the theme dropdown as a saved theme
- Saved themes appear alongside the built-in themes in the dropdown; switching to one loads its colors instantly
- Selecting a saved theme still shows the color picker panel so you can continue tweaking
- **Delete theme** removes a saved theme — built-in themes (Dark, Dark Purple, Midnight, Slate) cannot be deleted
- **Reset to defaults** returns all seven slots to the Custom theme baseline colors

---

### Auto-Update

The app silently checks for new releases on startup. If an update is available, a banner appears with a one-click download and install.

---

### Item Names Database

Download the community item database (~2 MB) from Settings so car loadouts show readable names (e.g. "Fennec", "Titanium White Octane") instead of raw item IDs.

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+A` | Select all visible replays |
| `Ctrl+click` | Toggle selection of a single card |
| `Ctrl+Shift+click` | Range-select from last selected to clicked card |
| `Delete` | Delete selected replay(s) |

---

## Installation

1. Download `RLReplayManagerSetup.exe` from the **[Releases](../../releases/latest)** tab
2. Run the installer — no Python or additional dependencies required
3. On first launch, open **Settings** from the toolbar to configure your replay folder and optional ballchasing.com API key

---

## First Launch

Open **Settings** from the toolbar after installing:

1. **Replay folder** — the app will attempt to auto-detect your Steam and Epic replay folders; set it manually if needed
2. **Card title** — choose whether cards show the filename or the in-game replay name
3. **ballchasing API key** — paste your key to enable upload and sync features (get one at [ballchasing.com/upload](https://ballchasing.com/upload))
4. **Item Names Database** — click **Download Item Names** for human-readable loadout display in the player info panel

---

## Source Code

The full source is available at [AvinAlwis/rl-replay-manager](https://github.com/AvinAlwis/rl-replay-manager).

---

## License

MIT
