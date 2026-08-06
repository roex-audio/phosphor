# Phosphor -- Getting Started Guide

## What is Phosphor?

Phosphor is a spectrogram-based audio synthesis tool. You paint images on a canvas, and Phosphor turns them into sound. The X-axis is time, the Y-axis is frequency, and brightness controls volume. You can also import any image and hear what it sounds like.

Phosphor is inspired by MetaSynth and designed for sound designers, musicians, and anyone curious about the relationship between images and sound.

---

## Your First Sound in 60 Seconds

1. **Open Phosphor** -- you'll see a dark canvas with a toolbar on the left and parameters on the right.
2. **Select the Brush tool** -- press **B** or click the brush button in the toolbar.
3. **Paint on the canvas** -- click and drag to draw. Higher on the canvas = higher pitch. Further right = later in time.
4. **Press Space** to play what you've painted.
5. That's it -- you've just created a sound from an image.

Try painting a diagonal line from bottom-left to top-right -- you'll hear a rising pitch sweep.

---

## Understanding the Canvas

The canvas is a spectrogram -- a visual representation of sound:

- **X-axis (horizontal)**: Time. Left is the start, right is the end.
- **Y-axis (vertical)**: Frequency. Bottom is low pitch, top is high pitch.
- **Brightness**: Louder sounds are brighter. Black = silence.
- **Colour**: When using the timbre palette, colour represents the harmonic content (timbre) of the sound.

### Overlays

Toggle these with keyboard shortcuts to help you paint:

- **Piano Roll** (P): Shows note lines overlaid on the canvas, so you can paint at specific pitches.
- **Beat Grid** (G): Shows vertical time divisions for rhythmic alignment.
- **Snap to Grid** (S): Snaps your brush to the nearest grid line.

---

## Tools

### Brush (B)
The main painting tool. Click and drag to add sound to the canvas. Use **[** and **]** to decrease and increase brush size.

### Eraser (E)
Remove painted content. Works like the brush but clears instead of adding.

### Line (L)
Draw straight spectral lines. Click to set the start point, then click again to complete the line. Great for precise tonal content.

### Harmonic Brush (H)
Like the brush, but automatically generates overtones above the fundamental frequency you paint. Creates richer, more natural tones.

### Select (R)
Draw a selection rectangle on the canvas. Selected regions can be:
- **Copied** (Cmd+C) and **Pasted** (Cmd+V)
- **Cleared** (Delete)
- **Inverted** (Edit menu)
- **Blurred** (Cmd+B) -- smooths the spectral content

---

## Colour and Timbre

The timbre palette in the toolbar lets you paint with different tonal qualities:

- **None** (grey): Pure sine tone -- just the fundamental frequency, no overtones.
- **Saw** (red): Sawtooth wave -- bright and buzzy, all harmonics present.
- **Square** (green): Square wave -- hollow sound, only odd harmonics.
- **Warm** (blue): Soft and round -- just the first few harmonics.

When you paint with a colour, the Harmonic Brush automatically generates the corresponding overtone pattern. The hue controls which harmonic profile is used, and the saturation controls how strong the overtones are.

---

## Working with Images

### Importing Images
Go to **File > Import Image** (Cmd+I) or drag and drop an image onto the canvas.

Any image works -- photos, drawings, text, abstract art. Phosphor maps:
- Brightness to volume
- Colour (hue) to harmonic content / timbre
- The image is stretched to fill the spectrogram's time and frequency range

### Exporting Images
Go to **File > Export Image** (Cmd+Shift+E) to save your spectrogram as a PNG.

---

## Working with Audio

### Importing Audio
Go to **File > Import Audio** (Cmd+Shift+I) to load a WAV or AIFF file.

Phosphor analyses the audio using an FFT and displays its spectrogram. You can then edit the spectrogram and re-synthesize the modified audio.

### Exporting Audio
Go to **File > Export Audio** (Cmd+E) to render your spectrogram to a WAV file.

---

## Parameters Panel

The right-hand panel controls the spectrogram's properties:

- **Duration**: Length of the sound in seconds.
- **Sample Rate**: Audio sample rate (44100 Hz is standard).
- **FFT Size**: Frequency resolution. Larger = more precise frequencies but less time precision.
- **Frequency Range**: The minimum and maximum frequencies displayed and synthesized.
- **Beat Grid / Snap to Grid**: Toggle rhythmic overlays and snapping.

---

## Keyboard Shortcuts

### Tools
| Action | Shortcut |
|---|---|
| Brush | B |
| Eraser | E |
| Line | L |
| Harmonic Brush | H |
| Select | R |

### Playback
| Action | Shortcut |
|---|---|
| Play / Stop | Space |

### Painting
| Action | Shortcut |
|---|---|
| Brush size down | [ |
| Brush size up | ] |

### Overlays
| Action | Shortcut |
|---|---|
| Piano roll | P |
| Beat grid | G |
| Snap to grid | S |

### View
| Action | Shortcut |
|---|---|
| Zoom in | + |
| Zoom out | - |
| Reset zoom | Cmd+0 |

### Editing
| Action | Shortcut |
|---|---|
| Undo | Cmd+Z |
| Redo | Cmd+Shift+Z |
| Select all | Cmd+A |
| Copy | Cmd+C |
| Paste | Cmd+V |
| Clear selection | Delete |
| Blur selection | Cmd+B |

### File
| Action | Shortcut |
|---|---|
| New project | Cmd+N |
| Open project | Cmd+O |
| Save | Cmd+S |
| Save as | Cmd+Shift+S |
| Import image | Cmd+I |
| Import audio | Cmd+Shift+I |
| Export audio | Cmd+E |
| Export image | Cmd+Shift+E |
| Quit | Cmd+Q |

---

## Tips and Tricks

- **Start simple**: A single horizontal line is a pure tone. A vertical line is a click/impulse. Build from there.
- **Use the piano roll overlay** (P) to paint at specific musical notes.
- **Zoom in** (+) for detail work on small frequency ranges.
- **Undo is generous** -- Cmd+Z supports up to 30 levels of undo.
- **Try importing photos** -- landscapes often make interesting drones, text creates rhythmic patterns.
- **Blur** (Cmd+B on a selection) smooths harsh edges and creates evolving textures.

---

## Getting Help

- **Report bugs**: Help > Report a Bug, or visit [GitHub Issues](https://github.com/roex-audio/phosphor/issues)
- **Suggest features**: Help > Suggest a Feature, or visit [GitHub Discussions](https://github.com/roex-audio/phosphor/discussions)
- **Join the community**: [Discord](https://discord.gg/k5ky5apBrd) or Help > Join Discord
- **Website**: [roexaudio.com/phosphor](https://www.roexaudio.com/phosphor)
