# Dropletee

**Liquid distortion effect for After Effects, powered by WebGPU**

[![Buy on aescripts](https://img.shields.io/badge/Buy%20on-aescripts.com-blue)](https://aescripts.com/dropletee/)

---

## What is Dropletee?

Dropletee is a GPU-accelerated plugin that turns any layer into flowing liquid. It accumulates frames over time, pushing pixels along surface normals with iridescent color palettes and specular lighting.

Key features:
- **Frame accumulation** with temporal distortion, noise, and wind
- **Self-distortion** that builds a normal map and pushes pixels along it, creating a fluid look
- **Stylization** with cosine palettes, surface normals, and lighting
- **Real-time GPU rendering** via WebGPU (Metal on macOS)
- **Auto Cache** for seamless timeline scrubbing
- **Multi-Frame Rendering** support
- 6 presets included: Chemtrails, Blue Acid, Dust Devil, Oil Slick, Wave Rush, Soap Burst

---

## How it works

Dropletee is a time-dependent effect - each frame is built from all the previous ones. Parameters are split into two categories:

- **Simulation** - frame accumulation, distortion, noise, wind. Changes require re-caching
- **Stylization** - surface normals, palette, lighting. Applied on top of cached results, updates instantly

### Caching modes

Since the simulation is sequential, there are three caching modes:

1. **Live Preview** - quick feedback for tweaking simulation parameters. Set the number of preview frames; fewer frames means faster response
2. **Compute** - manual caching from the layer's in-point to the current time, with a progress bar shown in the frame
3. **Auto Cache** (recommended) - blocks the current frame until the entire sequence up to that point is computed. Once done, scrub freely

---

## System requirements

| Platform | Status |
|----------|--------|
| macOS 10.15+ (Intel & Apple Silicon) | Available |
| Windows 10+ | Available |

- **After Effects** 2022 and later
- GPU with WebGPU support (Metal on macOS)

---

## Support

### Reporting issues

This repository is for **bug reports** and **feature requests**. Please use the issue templates provided.

Before creating an issue:
- Check [existing issues](../../issues) to avoid duplicates
- Include your After Effects version and OS
- Provide steps to reproduce bugs
- Attach screenshots or videos if possible

### Purchase & licensing

For purchase and licensing questions, please contact [aescripts support](https://aescripts.com/contact/).

---

## Privacy

Dropletee collects anonymous crash reports and usage statistics to improve stability. No personal files or project data is accessed. See our full [Privacy Policy](PRIVACY.md).

---

## Links

- [Buy Dropletee](https://aescripts.com/dropletee/)

---

## Author

Developed by **Tim Constantinov** / [Towards Inner Momentum](https://timomentum.com)

---

*Dropletee is a commercial product distributed through aescripts.com. This repository is for issue tracking and community feedback only.*
