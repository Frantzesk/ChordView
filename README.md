# 🎸 ChordView

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)](https://www.android.com/)
[![Kotlin](https://img.shields.io/badge/Kotlin-100%25-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Min SDK](https://img.shields.io/badge/Min%20SDK-26%20(Android%208.0)-brightgreen)](https://developer.android.com/about/dashboards)
[![Target SDK](https://img.shields.io/badge/Target%20SDK-35%20(Android%2015)-blue)](https://developer.android.com/about/versions/15)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](LICENSE)

> **ChordView** is a clean, modern, and distraction-free Android application built for guitarists, worship leaders, and live musicians to view, organize, transpose, and perform song chord charts and lyrics.

---

## ✨ Features

### 🔄 Real-Time Transposition & Capo Calculation
- **Instant Pitch Shift**: Transpose any chord chart up or down semitone-by-semitone (`+1` / `-1`) with single-tap reset.
- **Dynamic Key Context**: Real-time key badge indicators (e.g., `Key: G → A`).
- **Smart Accidental Notation**: Choose between **Auto** (key-aware context), **Sharps (#)**, or **Flats (♭)**.
- **Slash Chord Support**: Full transposition for compound chords and alternate bass notes (e.g., `G/B` → `A/C#`).
- **Capo Selector**: Set capo positions from fret 0 to 11 to match your instrument configuration.

### 🎸 Interactive Guitar Chord Diagrams
- **Song Chords Ribbon**: A scrollable pill ribbon at the top of the song viewer showing all chords used in the song in real time.
- **Visual Fretboard Modal**: Tap any chord pill or chord in the sheet to open a bottom sheet modal showing the exact guitar fretboard diagram, finger placements, and open/muted string indicators in standard tuning (`E A D G B e`).

### 📜 Intelligent Two-Way Song Parser
- **Inline ChordPro Style**: Parses bracketed inline chords (e.g., `[Am]Once upon a [C]time`).
- **Classic Two-Line Format**: Intelligently detects and aligns chords placed directly above lyrics.
- **Automatic Metadata Extraction**: Automatically parses **Title**, **Key**, **Capo**, **Time Signature** (e.g., `4/4`, `6/8`), and **Tempo / BPM** (`♩ = 120`).
- **Section Recognition**: Automatically detects and styles song sections (Verse, Chorus, Bridge, Intro, Outro, Pre-Chorus, Solo).

### ⚡ Live Performance Tools
- **Smooth Auto-Scroll**: Hands-free floating auto-scroll with adjustable playback speed slider (1x – 5x).
- **Keep Screen On**: Prevents your device display from dimming or locking during rehearsals or live stage performances.
- **Quick Font Scaling**: On-the-fly text size adjustment (`+` / `-`) for optimal visibility on music stands or floor monitors.
- **Monospaced Alignment**: High-legibility monospaced alignment so chords always sit accurately above their corresponding lyrics.

### 🔍 Fast Search & Greek Accent Normalization
- **Full Library Search**: Search instantly across song **Titles** and full **Lyrics**.
- **Greek & Multilingual Diacritics Normalizer**: Advanced search normalizer handling Greek vowels with accents/tonoi (`τόνοι`), diacritics, and character variants (e.g., `εκεινος` matches `Εκείνος`, `δοξολογια` matches `Δοξολογία`, and final sigma `ς` → `σ`).

### 📂 Song Library & Offline Management
- **Tabbed Organization**: Switch between **All Songs** and **Favorites** with a single tap.
- **Batch Import**: Import multiple `.txt` or chord chart files at once using the system document picker.
- **Paste / New Song**: Quick-paste lyrics and chords straight from clipboard.
- **Custom Sorting**: Sort your library by Title (A–Z, Z–A), Newest Added, or Oldest Added.
- **Local & Offline**: All songs and custom settings are stored locally on device without requiring cloud connectivity.

### 📤 Sharing & Export
- **Copy Transposed Text**: Copy the transposed lyrics and chords directly to your clipboard.
- **Direct Share**: Export songs straight to other apps (notes, messaging, email).

### 🎨 Clean Material Design
- Available in **Dark Mode**, **Light Mode**, or **Follow System Theme**.
- Minimalist, high-contrast palette highlighting chords, lyrics, and metadata distinctly.

---

## 📝 Supported Song Formats

ChordView supports both standard chord chart formats seamlessly:

### Format A: Inline Bracketed Chords (ChordPro)
```text
Title: Amazing Grace
Key: G
Time: 3/4
Tempo: 75

[Verse 1]
[G]Amazing grace how [C]sweet the [G]sound
That saved a [D]wretch like [G]me
```

### Format B: Two-Line Chords Over Lyrics
```text
Title: Stand By Me
Key: A
Time: 4/4

[Verse 1]
A                       F#m
When the night has come and the land is dark
        D          E                A
And the moon is the only light we'll see
```

---

## 🛠️ Tech Stack & Architecture

- **Language**: Kotlin 100%
- **UI Architecture**: Android Jetpack, ViewBinding, Material Components 3
- **Custom Views**: `ChordDiagramView` (custom Canvas drawing for guitar fretboards)
- **Concurrency**: Kotlin Coroutines (`Dispatchers.IO`, `lifecycleScope`)
- **Persistence**: SharedPreferences with asynchronous JSON serialization (`Gson`)
- **Min SDK**: 26 (Android 8.0 Oreo)
- **Target SDK**: 35 (Android 15)

---


## 📋 Release Notes — V1.0.0

- 🚀 Initial public release of ChordView.
- 🎼 Core song parser supporting inline bracketed and two-line chord formats.
- 🎹 Real-time semitone transposer with key context, accidental preferences, and slash chord support.
- 🎸 Visual guitar chord diagram engine with bottom-sheet viewer.
- 📜 Hands-free auto-scrolling with speed controls and stage screen lock.
- 🔍 Greek diacritics / tonoi-insensitive and lyrics-aware search engine.
- 🗂️ Batch `.txt` file importer and direct song editor.
- 🌗 Light, Dark, and System appearance modes.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — see the LICENSE file for details.
