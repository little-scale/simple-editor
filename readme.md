# Simple Audio Editor

A browser-based audio editor for WAV and AIF files. No installation required - just open `index.html` in your browser.

## Features

### File Operations
- **Import**: Load WAV and AIF audio files
- **Export**: Save as WAV or AIF with configurable bit depth (16-bit, 24-bit, 32-bit float)

### Playback
- Play, pause, and stop controls
- Click anywhere on the waveform to set the playhead position
- Playback starts from the playhead position (or loops back to start if at end)
- Selection-only playback: when audio is selected, only that portion plays

### Waveform Display
- Visual waveform with zoom controls
- Click to position playhead
- Click and drag to create selections
- Double-click or Cmd/Ctrl+A to select all

### Spectrum Analyzer
- Real-time frequency spectrum display during playback
- Static spectrum analysis at playhead position when stopped
- Configurable FFT size (256 to 8192)
- Logarithmic frequency scale with labeled axes

### Audio Metering
- **Peak**: Real-time peak level in dBFS
- **RMS**: Root mean square level in dBFS
- **LUFS**: Short-term loudness (3-second window)
- Color-coded display (green/yellow/red)

### Editing Operations
- **Trim**: Keep only the selected portion
- **Delete**: Remove the selected portion (Delete/Backspace key)
- **Normalize**: Set peak level to target dBFS
- **Fade In/Out**: Apply linear fade to selection
- **Gain**: Apply dB adjustment to selection or entire file
- **Undo/Redo**: Full undo history for all edit operations

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Space | Play/Pause |
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

1. Open `index.html` in your browser
2. Click **Import** to load a WAV or AIF file
3. Use the waveform to navigate and select audio
4. Apply edits using the toolbar buttons
5. Click **Export** to save your edited audio

## License

MIT License
