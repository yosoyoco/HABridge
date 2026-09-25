# Changelog

## 1.2.1 — 2026-09-25

- Gain knobs in LV1 keep a correct scale when the console, S32 or SoundGrid card is detected after LV1 starts (no more needle stuck at the bottom).
- Smooth, regular knob rotation: one step equals one real gain step.
- An unavailable port keeps its last value and receives no command.
- An S32 is still recognised when another console is chained on its port B.
- DN32-WSG uses HABridge Control associations on Windows and is recognised on macOS.
- HABridge Control: new icon, Start menu shortcut on Windows, single window, SoundGrid devices listed with type, MAC address and console, clearer install and update flow, fixed search and manual connection in Advanced, update and uninstall work whatever the installed version.

## 1.2.0 — 2026-09-24

- Added DN32-WSG support for compatible X32/M32 systems on Windows and macOS.
- Improved compatibility with Waves v17 SoundGrid control modules.
- Added universal macOS DN32 support for Intel and Apple Silicon.

## 1.1.1 — 2026-09-22

- Added the optional “Soutenir HABridge…” action in HABridge Control.
- The action opens YoSoYoCo’s Ko-fi page in the system browser.
- No audio, Gain, +48 V, AES50 or recall engine changes.

## 1.1.0 — 2026-09-22

First public release of HABridge.

- Preamp gain and +48 V control from eMotion LV1.
- Support for Behringer WING, Behringer X32 and Midas M32.
- AES50 preamp control, multiple device associations and session save/recall.
- HABridge Control for Windows and macOS.
