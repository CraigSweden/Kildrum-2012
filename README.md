# ⚽ Kildrum United Matchday Studio

> **CLYFA Division D · Season 26/27**

The **Kildrum United Matchday Studio** is a web application for managing league standings, tracking live matchday events pitch-side, and generating social media graphics. The application features two viewing modes: a public **View-Only Mode** for parents, players, and supporters, and an unlocked **Coach/Admin Mode** for team management and live publishing.

For a full guide with screenshots, see the User Guide:
https://github.com/craigsweden/Kildrum-2012/blob/HEAD/USER_GUIDE.md

---

## 📋 Table of Contents

1. [Access Modes & Navigation](#1-access-modes--navigation)
2. [League Hub (Public & Coach Views)](#2-league-hub-public--coach-views)
3. [Lineup Generator (Coach Mode)](#3-lineup-generator-coach-mode)
4. [Match Day Recorder (Coach Mode)](#4-match-day-recorder-coach-mode)
5. [Result & Match Report Studio (Coach Mode)](#5-result--match-report-studio-coach-mode)
6. [Saving, Cloud Sync & Help](#6-saving-cloud-sync--help)

---

## 1. Access Modes & Navigation

### 👀 Public View-Only Mode (Parents & Supporters)
By default (or when accessed via `?view=league`), the app opens directly to the **League** tab.
* **Available Features:** League Table, This Week's Match, Progression Charts, Head-to-Head Comparisons, Diagnostics, Scorers Leaderboard, League Matrix, and the **Help** guide.
* **Restricted Features:** The **Lineup Generator**, **Result & Match Report**, **Match Recorder**, and **Manage Results** tabs display a lock icon (`🔒`) and cannot be edited without authorization.

### 🔓 Unlocking Coach / Admin Mode
1. Click on any locked tab (**Lineup Generator**, **Result & Match Report**, or **Match Recorder**).
2. Paste your **GitHub Personal Access Token** (configured with `Contents: Read and write` permissions for this repository) into the password field and press **Enter** or click **Unlock**.
3. Once verified, the token is saved locally on your device, the lock icons disappear, and top-bar actions (**Save Locally**, **Reset**, **Print**, **Save Graphic (PNG)**) become visible.

---

## 2. League Hub (Public & Coach Views)

The **League** tab pulls live season data from the repository and organizes it into eight sub-tabs:

| Sub-Tab | Access | Description |
| :--- | :---: | :--- |
| **Table** | Public | Current CLYFA Division D standings. Click any team name to open a pop-up modal showing their past results and upcoming fixtures. |
| **This Week's Match** | Public | Displays the next scheduled Kildrum United fixture along with the published squad announcement graphic. |
| **Progression** | Public | Interactive line charts tracking team points and position changes across the season. |
| **Head to Head** | Public | Side-by-side statistical comparison between Kildrum United and any selected league opponent. |
| **Diagnostics** | Public | Advanced team performance metrics, goal trends, and form analysis. |
| **Scorers** | Public | Season goal-scoring leaderboard. |
| **League Matrix** | Public | Grid overview showing all home and away scorelines between every team in the division. |
| **Manage Results** | Coach Only | Allows editing league results and pushing updated standings and scorer tables online to GitHub. |

---

## 3. Lineup Generator (Coach Mode)

Use this tab to build and publish pre-match squad announcement graphics.

### Step 1: Match Info & Badges
* Enter the **Competition**, **Match Date**, **Kick-off Time**, and **Venue / Pitch**.
* Toggle whether Kildrum Utd are playing **HOME** or **AWAY**.
* Select an **Opposition Club** from the dropdown (which automatically loads their club badge) or enter a custom **Opposition Name** and click **Upload opposition badge** to use a custom image.

### Step 2: Tactics & Kit Customization
* **Starting Formation:** Choose from `4-4-2`, `3-5-2`, `4-3-3`, `4-2-3-1`, `3-4-3`, or `5-3-2`.
* **Graphic View Style:** Switch between **Jerseys Grid (3D Shirt Style)** or **Tactical Pitch View**.
* **Squad Display:** Choose whether to distinguish starters from bench players with `SUB` tags or show all called-up players equally.
* **Kit Style & Colors:** Select the **Home Kit (Red & Black)**, **Away Kit (Green & Patterned)**, or customize the **Kit Body**, **Kit Sleeves**, and **GK Body** colors using the color pickers.

### Step 3: Squad Roster Manager
* Click **Add Player** to add new names to the roster, or edit existing shirt numbers (`#`), names, and positions (`Pos`) directly in the table.
* Set each player's matchday status:
  * **`XI`** — Starting lineup *(included in graphic)*
  * **`SUB`** — Substitute *(included in graphic)*
  * **`NO`** — Not called up *(excluded from graphic)*

### Step 4: Publish or Export
* **Publish Squad Announcement:** Select the upcoming fixture from the dropdown and click **PUBLISH SQUAD ANNOUNCEMENT**. This updates the *This Week's Match* card for parents without altering league scores or standings.
* **Export:** Use the header buttons to **Print** or **Save Graphic (PNG)** for sharing on social media.

---

## 4. Match Day Recorder (Coach Mode)

Designed for pitch-side live tracking on a phone or tablet.

1. **Setup:** Verify the **Match date** and set the **Half length (minutes)** (default is `40` minutes).
2. **Match Clock:** Use **Start first half**, **Stop first half**, **Start second half**, and **Stop second half** to run the live countdown/match timer.
3. **Recording Goals:**
   * Tap the large **KILDRUM UTD** panel when Kildrum scores. A dialog will open prompting you to select the **Scorer** from the matchday squad and confirm the half and elapsed time.
   * Tap the **OPPOSITION** panel to log an opponent goal.
   * Click **Add missed goal** in the **Goal Log** section to manually enter or edit a goal after the fact.
4. **Syncing:** Click **Push details to Match Report** to automatically transfer the final score, match date, and goal scorers into the *Result & Match Report* tab. Click **New match** to clear the timer and log for a fresh game.

---

## 5. Result & Match Report Studio (Coach Mode)

Create a shareable `600×800px` full-time graphic and WhatsApp summary after the final whistle.

1. **Link League Match:** Select the fixture from the **League Match** dropdown to auto-fill the opponent, date, and side.
2. **Scoreline & Details:** Confirm the **Kildrum Utd Score** and **Opposition Score** (or import them from the Match Recorder), select the **Match Status Badge** (`FULL TIME`, `HALF TIME`, `EXTRA TIME`, `PENALTIES`), and enter the **Man of the Match**.
3. **Goals & Assists:** Click **Add Goal** to list scorers, minutes, and assist providers beneath the score boxes.
4. **Match Commentary & Photo:**
   * Type your match summary in the **Match Report & WhatsApp Copy** box.
   * Set **Include team photo?** to **Yes** to upload a post-match squad photo (the layout automatically adjusts badge sizes and text spacing to fit).
5. **Share & Save:**
   * Click **Copy WhatsApp Post** to copy a pre-formatted text summary ready to paste into team group chats.
   * Click **Save Graphic (PNG)** in the top header to download the full-time graphic.

---

## 6. Saving, Cloud Sync & Help

* **Save Locally:** Stores your current lineup, match recorder state, and report draft in your browser's local storage so work is not lost if you refresh the page.
* **Publishing Online:**
  * *Squad lineups* are published via **Publish Squad Announcement** in the Lineup Generator tab.
  * *Official league scores and scorers* are published online via **League > Manage Results > Push current data online**.
* **In-App Help Panel:** Clicking **Help** in the top navigation bar loads this `README.md` directly inside the app for parents and supporters.
