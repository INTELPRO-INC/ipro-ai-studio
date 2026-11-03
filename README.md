# IPRO AI Studio

Desktop tool for the INTELPRO IPRO7AI and the IPRO7AI Reef EVK. It has two parts:

- **IPRO AI Teach**: teach the Reef to recognize images, voices or sensor states without writing code. Collect data with the board's camera, microphone or a sensor, train on your computer, deploy over USB-C, and the IPRO7AI's NPU runs the model.
- **Model tools**: convert a TensorFlow Lite model for the NPU, inspect how its layers are dispatched, and verify it on the board.

The same program contains the `ipro-ai` command line for scripts and automation.

**Download:** [Latest release](https://github.com/INTELPRO-INC/ipro-ai-studio/releases/latest)

| Platform | File |
|---|---|
| macOS 11 or later, Apple silicon | `IPRO-AI-Studio-<version>.dmg` |
| Windows, 64-bit (x64) | `IPRO-AI-Studio-<version>-windows-x64.zip` |

## Install

**macOS**

1. Open the `.dmg` and drag **IPRO AI Studio** into the Applications folder.
2. The app is not notarized by Apple, so open it the first time from Finder: right-click **IPRO AI Studio**, choose **Open**, then **Open** again. Or remove the download quarantine in Terminal:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/IPRO AI Studio.app"
   ```
3. The first time you open the **Teach** page, allow IPRO AI Studio to use the camera.

**Windows**

1. Unzip the `.zip` where you want the program, for example `C:\IPRO\`. The `ipro-ai-studio` folder has `ipro-ai-studio.exe` (the program) and `ipro-ai.exe` (the command line). The Visual C++ runtime is included.
2. Double-click `ipro-ai-studio.exe`. If Windows SmartScreen warns about an unrecognized app, choose **More info**, then **Run anyway**.
3. In **Settings → Privacy & security → Camera**, let desktop apps use the camera.

Check a download against [SHA256SUMS.txt](SHA256SUMS.txt):

```bash
shasum -a 256 -c SHA256SUMS.txt --ignore-missing     # macOS / Linux
```

```powershell
Get-FileHash .\IPRO-AI-Studio-0.4.2-windows-x64.zip -Algorithm SHA256   # Windows
```

## What you need for IPRO AI Teach

- An IPRO7AI Reef EVK V4.0 running the Edge AI firmware (`ipro_reef_teach`). Its source and flashing steps are in the [IPRO SDK](https://github.com/INTELPRO-INC/IPRO-SDK) (V2.2.0 or later).
- A USB-C data cable from the Reef to the computer.
- For image recognition: an OV5640 camera module on the Reef.

Studio finds the board on USB by itself. The **Teach**, **Audio** and **Sensor** pages each drive one tool; when the board is in another mode, the page offers to switch it.

## Documentation

Step-by-step guides for installing Studio, flashing the Edge AI firmware, and each Teach tool:
<https://intelpro-inc.github.io/ipro-sdk-docs/en/teach/> (English) · <https://intelpro-inc.github.io/ipro-sdk-docs/teach/> (繁體中文)

## 中文說明

IPRO AI Studio 是 INTELPRO IPRO7AI 與 IPRO7AI Reef EVK 的桌面工具：

- **IPRO AI Teach**：不用寫程式，就能讓 Reef 學會辨識影像、聲紋或感測器狀態。用板子的相機、麥克風或感測器收集資料，在電腦上訓練，經 USB-C 部署，由 IPRO7AI 的 NPU 執行。
- **模型工具**：把 TensorFlow Lite 模型轉成 NPU 格式、檢視各層分派，並在板上驗證。

下載：[最新版本](https://github.com/INTELPRO-INC/ipro-ai-studio/releases/latest)。macOS 版需 Apple 晶片的 Mac、macOS 11 以上；Windows 版為 64 位元（x64）。

安裝與各工具的操作步驟見文件站的 IPRO AI Teach 章節：<https://intelpro-inc.github.io/ipro-sdk-docs/teach/>

## License

IPRO AI Studio is licensed under the [Apache License 2.0](LICENSE). Third-party components and their licenses are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md); the same notices and license texts are inside the app.

## Release notes

See [RELEASE_NOTES.md](RELEASE_NOTES.md).

© INTELPRO
