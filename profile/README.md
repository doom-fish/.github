<div align="center">

<img src="https://raw.githubusercontent.com/doom-fish/.github/main/profile/pentagram.svg" alt="doom-fish" width="180"/>

# doom-fish

**Safe, idiomatic Rust bindings for Apple's macOS frameworks.**
*Zero‑Swift. One crate per framework. All the power, none of the ceremony.*

[doom.fish](https://doom.fish) · [open an issue](https://github.com/doom-fish/.github/issues) · [per@doom.fish](mailto:per@doom.fish)

</div>

---

## What is this?

A Stockholm-based shop building the Rust crates we wished existed when we started writing macOS apps in Rust. Each crate wraps a single Apple framework with a focused, safe API — no Swift toolchain in your build, no half-baked FFI, no surprises at runtime.

If you've ever wanted to drive Apple's screen capture, on-device LLMs, computer vision, accessibility, or HID input from Rust without rolling your own bindings, you're in the right place.

## The suite

### 🎥 Capture & video
- [`screencapturekit-rs`](https://github.com/doom-fish/screencapturekit-rs) — High-performance screen, window and audio capture (ScreenCaptureKit).
- [`videotoolbox-rs`](https://github.com/doom-fish/videotoolbox-rs) — Hardware-accelerated video encode / decode (VideoToolbox).
- [`avassetwriter-rs`](https://github.com/doom-fish/avassetwriter-rs) — Mux encoded video / audio into `.mp4` and `.mov`.
- [`gst-screencapturekit`](https://github.com/doom-fish/gst-screencapturekit) — GStreamer source element backed by ScreenCaptureKit.

### 🧠 On-device ML
- [`foundation-models-rs`](https://github.com/doom-fish/foundation-models-rs) — Apple's on-device LLM (macOS 26+).
- [`vision-rs`](https://github.com/doom-fish/vision-rs) — OCR, object detection, face landmarks.
- [`speech-rs`](https://github.com/doom-fish/speech-rs) — `SFSpeechRecognizer` speech-to-text.
- [`naturallanguage-rs`](https://github.com/doom-fish/naturallanguage-rs) — Language detection, tokenisation, named-entity recognition.
- [`soundanalysis-rs`](https://github.com/doom-fish/soundanalysis-rs) — On-device sound classification.

### 🎨 Graphics & media I/O
- [`apple-metal-rs`](https://github.com/doom-fish/apple-metal-rs) — Apple's Metal framework.
- [`imageio-rs`](https://github.com/doom-fish/imageio-rs) — Read / write / convert PNG, JPEG, HEIC, TIFF, GIF, RAW.
- [`uti-rs`](https://github.com/doom-fish/uti-rs) — UniformTypeIdentifiers, for file-type / MIME identification.

### ⌨️ Input, HID & automation
- [`cgevents-rs`](https://github.com/doom-fish/cgevents-rs) — Synthesise and intercept keyboard, mouse and scroll events globally.
- [`carbonhotkey-rs`](https://github.com/doom-fish/carbonhotkey-rs) — Global keyboard shortcuts. No Accessibility permission required.
- [`iohidmanager-rs`](https://github.com/doom-fish/iohidmanager-rs) — Enumerate connected mice, keyboards, gamepads via IOKit HID.
- [`gamecontroller-rs`](https://github.com/doom-fish/gamecontroller-rs) — Gamepad enumeration and state snapshots.
- [`axuielement-rs`](https://github.com/doom-fish/axuielement-rs) — Drive other apps' UIs via the Accessibility API.

### 🧱 Foundations
- [`cidre`](https://github.com/doom-fish/cidre) — Umbrella Apple-framework bindings used across the suite.
- [`apple-cf-rs`](https://github.com/doom-fish/apple-cf-rs) — Shared Core\* frameworks (CoreGraphics, IOSurface, Dispatch, …).
- [`core-frameworks`](https://github.com/doom-fish/core-frameworks) — Lower-level Apple core wrappers.
- [`networkframework-rs`](https://github.com/doom-fish/networkframework-rs) — Apple's `Network.framework`.
- [`apple-log-rs`](https://github.com/doom-fish/apple-log-rs) — `os_log`, with Console.app and the `log` CLI integration.

### 🐟 See it all together
- [`doom-fish-examples`](https://github.com/doom-fish/doom-fish-examples) — Cross-crate examples that wire the suite up end-to-end.

## Design principles

- **Zero-Swift.** Pure Objective‑C runtime calls. No Swift toolchain in your build.
- **One crate, one framework.** Pull in only what you need.
- **Safe by default.** Lifetimes, ownership and `Send` / `Sync` modelled honestly.
- **macOS-first, honest about it.** We target current macOS releases and say so up front.

## Contributing

Issues and PRs are welcome on any crate. If you're missing a wrapper for an Apple framework you need, open an issue — there's a decent chance we want it too.

---

<div align="center">
<sub>made with ☠️ in Stockholm · <a href="https://doom.fish">doom.fish</a></sub>
</div>
