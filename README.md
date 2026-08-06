# Phosphor

A spectrogram-based audio synthesis tool for macOS. Paint images that become sound.

Phosphor lets you draw directly on a spectrogram canvas -- the X-axis is time, the Y-axis is frequency, and brightness controls volume. Import any image and hear what it sounds like, or paint spectral sounds from scratch using a variety of tools and timbres.

Inspired by [MetaSynth](https://uisoftware.com/metasynth/) by U&I Software.

## Features

- **Paint sounds**: Brush, eraser, line, and harmonic brush tools
- **Timbre palette**: Paint with different tonal colours (saw, square, warm)
- **Image import**: Drop any image onto the canvas and hear it
- **Audio import**: Load audio files for spectral editing
- **Piano roll overlay**: See note lines while you paint
- **Beat grid and snap**: Rhythmic alignment tools
- **Undo/redo**: Up to 30 levels with intelligent memory management
- **Project files**: Save and load your work in `.phosphor` format
- **Export**: Render to WAV or export as PNG

## Download

Download the latest release from the [Releases](https://github.com/roex-audio/phosphor/releases) page.

**System requirements**: macOS 12 (Monterey) or later. Apple Silicon and Intel supported.

## Getting Started

See the [Getting Started Guide](docs/getting-started.md) for a walkthrough of Phosphor's features and keyboard shortcuts.

## Building from Source

### Prerequisites

- macOS 12+
- Xcode Command Line Tools (`xcode-select --install`)
- CMake 3.15+ (`brew install cmake`)
- libsndfile (`brew install libsndfile`)

### Build

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --target PhosphorGUI -j$(sysctl -n hw.logicalcpu)
```

The app bundle will be at `build/PhosphorGUI_artefacts/Release/Phosphor.app`.

### Run Tests

```bash
cmake --build build --target phosphor_tests -j$(sysctl -n hw.logicalcpu)
./build/phosphor_tests
```

## Feedback and Community

- **Report a bug**: [GitHub Issues](https://github.com/roex-audio/phosphor/issues)
- **Suggest a feature**: [GitHub Discussions](https://github.com/roex-audio/phosphor/discussions)
- **Discord**: [Join the community](https://discord.gg/k5ky5apBrd)
- **Website**: [roexaudio.com](https://www.roexaudio.com)

## License

Phosphor is freeware. See [LICENSES/](LICENSES/) for third-party attribution.

## Author

**RoEx** -- [roexaudio.com](https://www.roexaudio.com)
