# Third-party notices — IPRO AI Studio

IPRO AI Studio is Copyright 2026 INTELPRO and licensed under the Apache License 2.0
(`LICENSE`). The packaged application (macOS `.app`, Windows folder) also contains the
third-party software listed below, each under its own licence. The licence texts are in
the `licenses/` folder next to this file: in a macOS app that is
`IPRO AI Studio.app/Contents/Resources/`, on Windows the folder that holds
`ipro-ai-studio.exe`. Versions are those of the 0.4 builds.

## 1. Runtime and user interface

| Component | Version | Licence (SPDX) | Text |
|---|---|---|---|
| Python | 3.14 | PSF-2.0 (Windows build: with the notices of the libraries python.org bundles) | `licenses/python/Python/LICENSE.txt` |
| Qt (Core, Gui, Widgets, Multimedia, Network, OpenGL, Svg, DBus, Concurrent and their plugins) | 6.11.2 | LGPL-3.0-only | `licenses/LGPL-3.0.txt`, `licenses/GPL-3.0.txt` |
| PySide6 and Shiboken6 | 6.11.2 | LGPL-3.0-only | `licenses/LGPL-3.0.txt`, `licenses/GPL-3.0.txt` |
| FFmpeg (libavcodec, libavformat, libavutil, libswresample, libswscale; Qt Multimedia's FFmpeg back end) | 7.1.5 | LGPL-2.1-or-later | `licenses/LGPL-2.1.txt` |
| OpenSSL (macOS; on Windows part of the Python build above) | 3.6 | Apache-2.0 | `licenses/runtime/openssl@3/` |
| mpdecimal (macOS) | 4.0 | BSD-2-Clause | `licenses/runtime/mpdecimal/` |
| Zstandard (macOS) | 1.5 | BSD-3-Clause | `licenses/runtime/zstd/` |
| PyInstaller bootloader | 6.22 | GPL-2.0-or-later WITH the PyInstaller bootloader exception | `licenses/python/pyinstaller/` |

Qt, PySide6, Shiboken6 and FFmpeg are shared libraries in the application
(`Contents/Frameworks/` on macOS, `_internal/PySide6/` on Windows) and can be replaced
with other builds of the same versions. Their source code is published by the Qt
Project (<https://download.qt.io/official_releases/>) and the FFmpeg project
(<https://ffmpeg.org/download.html>); INTELPRO will also provide it on request. The
build leaves out every Qt module whose open-source licence is the GPL only (Qt Virtual
Keyboard among them) and the Qt Quick, QML and PDF modules, which the application does
not use.

## 2. Python packages

| Component | Version | Licence (SPDX) | Text |
|---|---|---|---|
| NumPy (Windows: with OpenBLAS and its runtime) | 2.5 | BSD-3-Clause and the licences of its bundled parts | `licenses/python/numpy/` |
| Pillow (with libjpeg-turbo, libpng, libtiff, libwebp, OpenJPEG, LittleCMS, libavif, FreeType, HarfBuzz, Brotli, XZ, zlib-ng, libxcb and others) | 12.3 | MIT-CMU and the licences of its bundled libraries | `licenses/python/pillow/` |
| pySerial | 3.5 | BSD-3-Clause | `licenses/pyserial.txt` |
| LiteRT (ai-edge-litert) | 2.2 | Apache-2.0 | `licenses/Apache-2.0.txt` |
| FlatBuffers (Python) | 25.12 | Apache-2.0 | `licenses/Apache-2.0.txt` |
| Protocol Buffers (Python) | 7.36 | BSD-3-Clause | `licenses/python/protobuf/` |
| ml_dtypes | 0.6 | Apache-2.0; Eigen parts MPL-2.0 | `licenses/python/ml_dtypes/` |

## 3. Tools inside the application

The model converter (`ips_aitool`), the host simulator (`ipro_ai_sim`), the flashing
tool (IntelProCube) and `ipro_probe_ctl.py` are INTELPRO software provided under your
license agreement with INTELPRO; they are not covered by the Apache License of IPRO AI
Studio. On Windows the Microsoft Visual C++ runtime (`msvcp140.dll`,
`vcruntime140.dll`, `vcruntime140_1.dll`, `concrt140.dll`) is next to them,
redistributed under the Microsoft Visual Studio licence terms.

The converter contains, statically linked:

| Component | Version | Licence (SPDX) | Text |
|---|---|---|---|
| TensorFlow Lite | 2.16.1 | Apache-2.0 | `licenses/converter/tensorflow.txt` |
| Abseil | as pinned by TensorFlow 2.16.1 | Apache-2.0 | `licenses/converter/abseil-cpp.txt` |
| ruy | as pinned | Apache-2.0 | `licenses/converter/ruy.txt` |
| gemmlowp | as pinned | Apache-2.0 | `licenses/converter/gemmlowp.txt` |
| FlatBuffers | as pinned | Apache-2.0 | `licenses/converter/flatbuffers.txt` |
| cpuinfo | as pinned | BSD-2-Clause | `licenses/converter/cpuinfo.txt` |
| pthreadpool | as pinned | BSD-2-Clause | `licenses/converter/pthreadpool.txt` |
| FXdiv | as pinned | MIT | `licenses/converter/FXdiv.txt` |
| FarmHash | as pinned | MIT | `licenses/converter/farmhash.txt` |
| fft2d (Ooura) | as pinned | the fft2d licence | `licenses/converter/fft2d.txt` |
| Eigen (headers) | as pinned | MPL-2.0 (source: <https://gitlab.com/libeigen/eigen>) | `licenses/MPL-2.0.txt`, `licenses/converter/eigen-README.txt` |
| OpenCV (core, imgproc, imgcodecs, dnn) | 4.9.0 | Apache-2.0 | `licenses/converter/opencv.txt` |
| libjpeg-turbo (in OpenCV) | 4.9.0's copy | IJG AND BSD-3-Clause AND Zlib | `licenses/converter/libjpeg-turbo.md`, `licenses/converter/libjpeg-turbo-README.ijg` |
| libpng (in OpenCV) | 4.9.0's copy | Libpng | `licenses/converter/libpng.txt` |
| LibTIFF (in OpenCV) | 4.9.0's copy | libtiff | `licenses/converter/libtiff.txt` |
| libwebp (in OpenCV) | 4.9.0's copy | BSD-3-Clause | `licenses/converter/libwebp.txt` |
| OpenJPEG (in OpenCV) | 4.9.0's copy | BSD-2-Clause | `licenses/converter/openjpeg.txt` |
| Protocol Buffers (in OpenCV dnn) | 4.9.0's copy | BSD-3-Clause | `licenses/converter/protobuf.txt` |
| ittnotify (in OpenCV) | 4.9.0's copy | BSD-3-Clause OR GPL-2.0-only (used under BSD-3-Clause) | `licenses/converter/ittnotify.txt` |
| carotene (in OpenCV; macOS Arm build) | 4.9.0's copy | BSD-3-Clause | `licenses/converter/carotene.txt` |
| OpenEXR (in OpenCV; Windows build) | 4.9.0's copy | BSD-3-Clause | `licenses/converter/openexr.txt` |
| zlib (in OpenCV; Windows build) | 4.9.0's copy | Zlib | `licenses/converter/zlib.txt` |

## 4. Licence texts

`licenses/Apache-2.0.txt` is the Apache License 2.0, which also covers IPRO AI Studio
itself. The GNU licences are `licenses/LGPL-3.0.txt` (with `licenses/GPL-3.0.txt`,
which it incorporates) and `licenses/LGPL-2.1.txt`; the Mozilla Public License 2.0 is
`licenses/MPL-2.0.txt`.
