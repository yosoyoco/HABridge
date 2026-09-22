# HABridge 1.1.1

First public release of HABridge.

## Features

- Preamp Gain and +48 V control from eMotion LV1
- Behringer WING support
- Behringer X32 support
- Midas M32 support
- AES50 preamp control
- Multiple device associations
- Session save/recall
- HABridge Control for Windows and macOS

## Known limitations

- On some inactive LV1 channels, PREAMP may remain visible temporarily after hardware disconnect. HABridge disables hardware control immediately.
- Some WING AES50 preamps use wider analog gain steps than the values LV1 can display. Intermediate displayed values do not add digital gain.
- The macOS build is not signed or notarized with Apple Developer ID.

Before enabling or recalling +48 V, verify the microphone, source and cabling connected to the preamp.
