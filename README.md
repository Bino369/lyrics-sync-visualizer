# 🎵 Lyrics Sync Visualizer

A premium, interactive, Apple Music-style lyrics visualizer web app built with **vanilla HTML, CSS, and JavaScript**.

Check out the live demo on [GitHub Pages](https://bino369.github.io/lyrics-sync-visualizer/) *(after enabling Pages)*.

---

## ✨ Features

- **Fluid Ambient Background:** Dynamic, animated colored gradients that morph smoothly in the background, drawing inspiration from Apple Music's lyrics interface.
- **Glassmorphic UI:** Modern translucent frosted-glass panels with subtle borders and shadows that adjust to light and dark angles.
- **Precision Karaoke Sync:** Smooth highlight transitions. Active lines glow and scale up while inactive lines dim and blur out.
- **Interactive Seeking:** Click on any lyric line to instantly jump the audio playback to that specific line's timestamp.
- **Custom Player Controls:** Styled Play/Pause, Restart, dynamic Seeker progress slider, volume controls, and track detail displays.
- **Local File Importer:** Drag and drop or browse to load your own `.mp3` audio files and `.json` lyric sheets directly in the browser.
- **Fully Responsive:** Optimizes beautifully for desktop, tablets, and mobile devices.

---

## 🛠️ How to Use Your Own Song & Lyrics

You can load songs dynamically in the UI or hardcode them directly into the file.

### Option 1: Dynamic Loading (Directly in UI)
1. Open the visualizer in your browser.
2. Click **Load Song** in the top right.
3. Select or drag-and-drop your audio file (`.mp3`, `.wav`, etc.).
4. Select or drag-and-drop your lyrics file (`.json`). The app will automatically sync them and close the importer.

### Option 2: Hardcoding Your Default Song
If you want the page to load your song by default when it opens:
1. Place your audio file at `audio/song.mp3` relative to `index.html`.
2. Open `index.html` in a text editor.
3. Locate the `DEFAULT_LYRICS` array in the `<script>` tag:
   ```javascript
   const DEFAULT_LYRICS = [
     { "time": 0.0, "text": "🎵 (Intro Instrumental) 🎵" },
     { "time": 4.5, "text": "First line of the song" },
     { "time": 8.5, "text": "Second line of the song" }
   ];
   ```
4. Modify the timestamps (in seconds) and text lines to match your audio track.

---

## 📄 Lyrics JSON Schema

The lyrics file must be a standard JSON array containing objects with `time` (in seconds) and `text` (the lyric line to display):

```json
[
  { "time": 0.0, "text": "🎵 (Intro Instrumental) 🎵" },
  { "time": 5.2, "text": "Welcome to the show" },
  { "time": 10.8, "text": "This is the second line of lyrics" },
  { "time": 15.0, "text": "🎵 (Instrumental Break) 🎵" }
]
```

---

## 🚀 Deployment to GitHub Pages

1. Push this repository to GitHub.
2. Go to your repository on GitHub.
3. Click the **Settings** tab.
4. On the left sidebar under *Code and automation*, click **Pages**.
5. Under *Build and deployment*, set the Source to **Deploy from a branch**.
6. Select the **`main`** branch and the **`/ (root)`** folder, then click **Save**.
7. Your page will be live at `https://<your-username>.github.io/<repository-name>/` in a minute!
