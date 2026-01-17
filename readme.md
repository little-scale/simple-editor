# Simple Audio Editor

A browser-based audio editor for WAV and AIF files. No installation required - just open `index.html` in your browser.

**Key Features:**
- 🎵 Multi-file workflow with drag & drop support
- 📊 Real-time spectrum analyzer with FFT visualization
- 📈 Professional metering (Peak, RMS, True Peak, LUFS)
- ✂️ Essential editing tools (Trim, Normalize, Fade, Gain, Reverse)
- 🔄 Full undo/redo history
- 🎚️ Master output volume control
- ⌨️ Keyboard shortcuts for efficient workflow

## Features

### File Operations
- **Import**: Load WAV and AIF audio files (single or multiple)
- **Drag & Drop**: Drag multiple audio files onto the waveform to add them to the queue
- **File Queue**: Manage multiple files in a list; click to switch between files, delete with X button
- **Export**: Save as WAV or AIF with configurable bit depth (16-bit, 24-bit, 32-bit float)

### Playback
- Play, pause, and stop controls
- Click anywhere on the waveform to set the playhead position
- Playback starts from the playhead position (or loops back to start if at end)
- Selection-only playback: when audio is selected, only that portion plays
- Loop selection: toggle looping to continuously replay the selected region
- Master output volume control (-60 dB to +6 dB)

### Waveform Display
- Visual waveform with zoom controls
- Click to position playhead
- Click and drag to create selections
- Double-click or Cmd/Ctrl+A to select all
- Clear file end indicator (dashed orange line with shaded area beyond)

### Spectrum Analyzer
- Real-time frequency spectrum display during playback (blue)
- Static spectrum analysis at playhead position when stopped
- Configurable FFT size (256 to 8192) - control located in bottom-right of spectrum view
- Logarithmic frequency scale with labeled axes
- Smooth animated visualization with glow effects

### Audio Metering
- **Real-time Peak Meter**: Live peak level display during playback (dBFS)
- **File Statistics**: Calculated across entire file
  - RMS Peak: Root mean square peak level
  - True Peak: Inter-sample peak detection
  - LUFS: Integrated loudness measurement
- Color-coded peak display (green/yellow/red)

### Editing Operations
- **Trim**: Keep only the selected portion
- **Delete**: Remove the selected portion (Delete/Backspace key)
- **Normalize**: Set peak level to target dBFS
- **Fade In/Out**: Apply linear fade to selection
- **Gain**: Apply dB adjustment to selection or entire file
- **Reverse**: Reverse audio (selection or entire file)
- **Undo/Redo**: Full undo history for all edit operations

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Space | Play/Pause |
| L | Toggle loop |
| R | Reverse |
| + / = | Zoom in |
| - | Zoom out |
| Delete / Backspace | Delete selection |
| Cmd/Ctrl + A | Select all |
| Cmd/Ctrl + Z | Undo |
| Cmd/Ctrl + Shift + Z | Redo |
| Cmd/Ctrl + Y | Redo (alternative) |

## Mouse Controls

| Action | Result |
|--------|--------|
| Click | Move playhead to position |
| Click + Drag | Create selection |
| Double-click | Select all |
| Scroll up/down | Zoom in/out |
| Scroll left/right | Pan waveform |

## Technical Details

- Built with vanilla HTML, CSS, and JavaScript
- Uses Web Audio API for playback and analysis
- Canvas-based waveform and spectrum visualization
- No external dependencies
- Works offline after initial load

## Browser Compatibility

Works in modern browsers that support:
- Web Audio API
- Canvas 2D
- ES6+ JavaScript

Tested in Chrome, Firefox, Safari, and Edge.

## Usage

### Getting Started
1. Open `index.html` in your browser
2. Load audio files:
   - Click **Import** to select one or more WAV/AIF files, or
   - Drag and drop multiple audio files directly onto the waveform

### Working with Files
- Multiple files appear in the file list on the right sidebar
- Click any file in the list to load and work on it
- Active file is highlighted in blue
- Remove files from the queue using the X button

### Editing Audio
1. Use the waveform to navigate and select audio
   - Click to position playhead
   - Click and drag to select regions
   - Use zoom controls (+/-) or mouse scroll
2. Adjust playback volume with the output volume slider (right sidebar)
3. Monitor levels with the real-time peak meter during playback
4. Apply edits using the toolbar buttons (Trim, Normalize, Fade, Gain, Reverse)
5. Use Undo/Redo (Cmd/Ctrl+Z) as needed
6. Click **Export** to save your edited audio

### Tips
- Press **L** to toggle loop mode for selected regions
- Press **R** to reverse audio quickly
- Use **Space** to play/pause
- Check the spectrum analyzer to view frequency content
- File statistics (RMS Peak, True Peak, LUFS) update automatically when files are loaded or edited

## License

MIT License
