# PuttLab — Real-Time Putting Tracker

Track your putter's face angle, speed, and acceleration in real-time using your iPhone camera and two colored stickers.

## Setup in 5 Minutes

### Step 1: Physical Setup
- Stick a **RED sticker** on the **heel** (grip end) of your putter face
- Stick a **BLUE sticker** on the **toe** (far end) of your putter face
- Use bright, fluorescent stickers — at least 2cm diameter works best

### Step 2: Create the GitHub Repo
1. Go to [github.com/new](https://github.com/new)
2. Name it `putting-tracker` (or whatever you want)
3. Make it **Public**
4. Click **Create repository**
5. Upload all files from this folder (`index.html`, `manifest.json`, `icon-180.png`, `icon-192.png`, `icon-512.png`)

### Step 3: Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under "Source", select **Deploy from a branch**
3. Pick **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait ~60 seconds, then your site is live at:
   ```
   https://YOUR-USERNAME.github.io/putting-tracker/
   ```

### Step 4: Open on iPhone
1. Open the link above in **Safari** on your iPhone
2. Tap **Start Tracking** → enter sticker spacing → **Open Camera**
3. Point your camera straight down at the putter from ~60-100cm above
4. When both markers are detected, the status shows **TRACKING** in green

## How to Use

| Button | What it does |
|--------|-------------|
| **● REC** | Start recording a stroke |
| **■ STOP** | Stop recording |
| **Save Trial** | Save the recorded stroke as a trial |
| **History** | View all trials with charts and stats |

### Live Metrics (shown during tracking)
- **Face Angle** — degrees open/closed (green = within ±1°)
- **Speed** — club head speed in mph
- **Accel** — acceleration (green = accelerating through impact)
- **Tempo** — backswing:downswing ratio (ideal ≈ 2:1)

### Workflow
1. Tap **● REC**
2. Make your putting stroke
3. Tap **■ STOP**
4. Tap **Save Trial**
5. Repeat for multiple putts
6. Tap **History** to see averages, margin of error, and trend charts

## Technical Details

- **Processing resolution**: 640×480 (optimized for iPhone 16's A18 chip)
- **Frame rate**: 30fps with ~3-7ms processing per frame
- **Color tracking**: Custom HSV pixel scanning (zero dependencies)
- **Self-calibrating**: Uses sticker spacing to convert pixels → real-world units
- **No server needed**: Runs entirely in the browser, all processing on-device
