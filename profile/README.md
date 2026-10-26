<div align="center">

<img src="https://raw.githubusercontent.com/doom-fish/.github/main/profile/pentagram.svg" alt="doom-fish" width="180"/>

# doom-fish

**Safe, idiomatic Rust bindings for macOS and Windows system frameworks.**
*One crate per framework. All the power, none of the ceremony.*

[doom.fish](https://doom.fish) · [open an issue](https://github.com/doom-fish/.github/issues) · [per@doom.fish](mailto:per@doom.fish)

</div>

---

## What is this?

The Rust crates we wished existed when we started writing macOS and Windows apps in Rust. Each crate wraps a single system framework with a focused, safe API — no half-baked FFI, no surprises at runtime. The Windows crates are small, owned subsets that use no other binding crates.

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
- [`apple-cf-rs`](https://github.com/doom-fish/apple-cf-rs) — Shared Core\* frameworks (CoreGraphics, IOSurface, Dispatch, …).
- [`networkframework-rs`](https://github.com/doom-fish/networkframework-rs) — Apple's `Network.framework`.
- [`tls-rs`](https://github.com/doom-fish/tls-rs) — Blocking TLS client streams on the TLS of the operating system: SecureTransport on macOS and Schannel on Windows.
- [`commoncrypto-rs`](https://github.com/doom-fish/commoncrypto-rs) — SHA-256 and SHA-1 through CommonCrypto on macOS.
- [`apple-log-rs`](https://github.com/doom-fish/apple-log-rs) — `os_log`, with Console.app and the `log` CLI integration.

### WebRTC

These public repositories provide WebRTC protocols and an Opus codec. Some crates are not available on crates.io.

- [`rtc-rs`](https://github.com/doom-fish/rtc-rs) — A WebRTC connection that combines ICE, DTLS, SRTP and RTP.
- [`ice-rs`](https://github.com/doom-fish/ice-rs) — ICE candidate collection and connection checks.
- [`sdp-rs`](https://github.com/doom-fish/sdp-rs) — Parse and build SDP session descriptions.
- [`rtp-rs`](https://github.com/doom-fish/rtp-rs) — RTP and RTCP packets, feedback messages and media payloads.
- [`stun-rs`](https://github.com/doom-fish/stun-rs) — STUN messages and attributes.
- [`turn-rs`](https://github.com/doom-fish/turn-rs) — TURN allocations, permissions and channel bindings.
- [`dtls-rs`](https://github.com/doom-fish/dtls-rs) — DTLS 1.2 handshakes and secure datagrams.
- [`srtp-rs`](https://github.com/doom-fish/srtp-rs) — SRTP and SRTCP packet protection.
- [`opus-rs`](https://github.com/doom-fish/opus-rs) — Encode and decode audio with Opus.

### 🪟 Windows
- [`win-com-rs`](https://github.com/doom-fish/win-com-rs) — The COM core: GUIDs, HRESULT errors, interface pointers, apartments, server objects, BSTR, VARIANT and PROPVARIANT.
- [`win-kernel-rs`](https://github.com/doom-fish/win-kernel-rs) — kernel32: handles, named pipes, overlapped I/O, events, processes, threads, the thread pool, memory, time and locale.
- [`win-user-rs`](https://github.com/doom-fish/win-user-rs) — user32: windows, input, monitors, DPI, IME, DWM, the clipboard and the OS version.
- [`win-shell-rs`](https://github.com/doom-fish/win-shell-rs) — The shell: known folders, shell links, property stores, dialogs, jump lists and drag and drop.
- [`win-security-rs`](https://github.com/doom-fish/win-security-rs) — Process tokens, SIDs, security descriptors, credentials, system random numbers, SHA-256 and SHA-1.
- [`win-registry-rs`](https://github.com/doom-fish/win-registry-rs) — String values under predefined and opened registry keys.
- [`winrt-desktop-rs`](https://github.com/doom-fish/winrt-desktop-rs) — WinRT for desktop apps: HSTRING, activation, UI settings, XML documents and toast notifications.
- [`directx11-rs`](https://github.com/doom-fish/directx11-rs) — Direct3D 11, DXGI and DirectComposition: devices, pipelines, swap chains and run-time shader compilation.
- [`directwrite-rs`](https://github.com/doom-fish/directwrite-rs) — DirectWrite: fonts, fallback, text layout, glyph rasterization and renderer callbacks.
- [`directmanipulation-rs`](https://github.com/doom-fish/directmanipulation-rs) — DirectManipulation: the manager, viewports, their content and the viewport event handler.
- [`graphicscapture-rs`](https://github.com/doom-fish/graphicscapture-rs) — Windows.Graphics.Capture: monitor capture items, Direct3D 11 frame pools and capture sessions.
- [`mediafoundation-rs`](https://github.com/doom-fish/mediafoundation-rs) — The media engine, loaded at run time: playback into Direct3D 11 textures.
- [`xaudio2-rs`](https://github.com/doom-fish/xaudio2-rs) — XAudio2 2.9, loaded at run time: the engine, mastering and source voices, owned buffers and the engine and voice callbacks.
- [`uiautomation-rs`](https://github.com/doom-fish/uiautomation-rs) — UI Automation providers: provider interfaces, events and identifiers.
- [`accesskit-windows-rs`](https://github.com/doom-fish/accesskit-windows-rs) — An AccessKit adapter for UI Automation, built on the crates above.
- [`xinput-rs`](https://github.com/doom-fish/xinput-rs) — XInput gamepads: state, buttons, triggers and sticks.
- [`win-icu-rs`](https://github.com/doom-fish/win-icu-rs) — Unicode conversion and text properties with the ICU library that Windows provides.

### 🐟 See it all together
- [`doom-fish-examples`](https://github.com/doom-fish/doom-fish-examples) — Cross-crate examples that wire the suite up end-to-end.

## Design principles

- **One crate, one framework.** Pull in only what you need.
- **Safe by default.** Lifetimes, ownership and `Send` / `Sync` modelled honestly.
- **Current releases, honest about it.** We target current macOS and Windows releases and say so up front.

## Contributing

Issues and PRs are welcome on any crate. If you're missing a wrapper for an Apple or Windows framework you need, open an issue — there's a decent chance we want it too.

---

<div align="center">
<sub>made with ☠️ · <a href="https://doom.fish">doom.fish</a></sub>
</div>
