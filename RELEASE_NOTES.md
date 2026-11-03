# IPRO AI Studio release notes

## 0.4.2 — 2026-11-02

The first public release.

- IPRO AI Studio is licensed under the Apache License 2.0. The third-party notices and license texts ship inside the app (`THIRD_PARTY_NOTICES.md`, `licenses/`).
- Qt modules available only under the GPL are no longer bundled.

Included from the 0.4 series:

- **IPRO AI Teach** for the IPRO7AI Reef EVK running the Edge AI firmware: the **Teach** page (image recognition from the Reef's camera), the **Audio** page (voiceprint recognition: enroll people, then see who is speaking) and the **Sensor** page (sensor recognition, with an unknown-state answer). Collect, train on the computer and deploy over USB-C; the pages find the board on USB and switch its mode when needed.
- **Model tools**: **Convert** (TensorFlow Lite to the NPU format), **Inspect** (per-layer dispatch and geometry), **Verify** (layer-by-layer comparison against the reference), **Board** (run a model on the board).
- The `ipro-ai` command line in the same program: `device`, `model`, `deploy` and `verify` commands with `--json` output.
- Windows build (x64). Pages fit any window size and display scaling.

Requirements: macOS 11 or later on Apple silicon, or 64-bit Windows (x64). For IPRO AI Teach, an IPRO7AI Reef EVK V4.0 with the Edge AI firmware (`ipro_reef_teach`, IPRO SDK V2.2.0 or later).

Known issues:

- The apps are not signed by Apple or Microsoft: on macOS open the app from Finder with right-click **Open** the first time; on Windows SmartScreen may ask you to confirm.
- Flash the Edge AI firmware with the steps in the documentation (its own partition table and mfg payload). The **Board** page's flash button writes a standard partition table without the mfg payload and is not meant for the Edge AI firmware.
