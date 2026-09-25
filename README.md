# HABridge 1.2.1

HABridge controls preamp gain and +48 V for compatible preamps directly from the **PREAMP** section of eMotion LV1.

It supports compatible Behringer WING, X32 and Midas M32 systems using SoundGrid WING, X-WSG or DN32-WSG interfaces.

## Compatibility

- SoundGrid WING, X-WSG and DN32-WSG
- Compatible Behringer WING, X32 and Midas M32 systems
- Windows
- macOS 12 or later on Intel and Apple Silicon

The corresponding original Waves SoundGrid module must already be installed. HABridge does not include or redistribute Waves modules.

See the [user guide](GUIDE.md) and [supported versions](SUPPORTED_VERSIONS.md).

## Installation

1. Install the Waves module required by the SoundGrid interface and confirm it works in LV1.
2. Close eMotion LV1.
3. Windows: open `HABridge-1.2.1-Windows.exe` and click **Installer HABridge**. macOS: unzip `HABridge-1.2.1-macOS.zip`, move HABridge Control to Applications, open it and click **Installer HABridge**.
4. In LV1, assign the SoundGrid devices and patch their inputs to the required channels.
5. With LV1 running, associate each SoundGrid device with its console in HABridge Control.

Download HABridge from [Releases](../../releases).

## Updating

Close eMotion LV1 and HABridge Control, then open the new version (Windows: the new `.exe`; macOS: replace the app in Applications). When HABridge Control shows « Mise à jour nécessaire », click **Installer cette version**. Associations are kept; there is no need to uninstall first.

## +48 V

Before enabling or recalling +48 V, verify the microphone, source and cabling connected to the preamp.

## Support HABridge

HABridge is free. If you appreciate the project, you can support its development at [Ko-fi](https://ko-fi.com/yosoyoco). Support is entirely optional and unlocks no feature.

## Licence

HABridge is proprietary freeware. Copyright © 2026 YoSoYoCo. See [LICENSE.txt](LICENSE.txt).
