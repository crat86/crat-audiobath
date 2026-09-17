# AudioBath

**给 MP3 洗个澡，保留原来的声音。**  
A local MP3 metadata cleaner. Part of the CRAT Tool Series.

[**macOS 下载**](https://github.com/crat86/crat-audiobath/releases/tag/v0.2.0-beta) · [**Windows 下载（未测试 Beta）**](https://github.com/crat86/crat-audiobath/releases/tag/v0.2.0-win.1) · [反馈 / Issues](https://github.com/crat86/crat-audiobath/issues)

## 下载与使用

### Windows 10/11 · Intel / AMD x64

1. 在 Windows Release 的 **Assets** 下载 `CRAT-AudioBath-v0.2.0-win.1-Windows-x64.zip`。
2. **完整解压**后双击 `AudioBath.exe`，保留同目录的 resources 和 DLL 文件，不要在压缩包内直接运行。无需额外安装 Node.js 或 Electron。
3. 选择或拖入 MP3，设置命名规则；清理副本保存在原文件所在文件夹。

> **未经实机测试的 Beta，EXE 未签名。** 本次仅做源码语法和打包检查，没有执行 Windows 启动、功能、音频或实机测试。SmartScreen 或杀毒软件可能提示或拦截。未提供原生 ARM64 或 32 位版。每批最多 500 个文件，单文件最大 512 MB。

### macOS 13+ · Apple Silicon

1. 在 macOS Release 的 **Assets** 下载 `CRAT-AudioBath-v0.2.0-macOS-arm64.zip`。
2. 解压，把 `AudioBath.app` 拖到“应用程序”。
3. 打开 App，设置命名规则，再拖入一个或多个 MP3。

> Mac Beta 为临时签名，尚未经过 Apple Developer ID 签名及公证，macOS 可能阻止首次打开。不包含 Intel Mac 版本。

GitHub 自动生成的 **Source code** 不是安装包。两种系统都需要原文件夹允许写入。

## 它能做什么

- **不转码**：直接清理标签，以保留原 MP3 音频帧为目标，不解码或重新编码。
- **批量处理**：一次处理多个 MP3，统一应用命名规则。
- **清理常见标签**：ID3v2、ID3v1 / ID3v1+、APEv2、Lyrics3，以及这些标签中的封面、标题、作者和备注。
- **自定义名称**：后缀、前缀或完整格式，支持 `{歌名}`、`{原名}`、`{标记}` 占位符。
- **智能歌名**：先读取 ID3 标题用于命名，缺失时回退到原文件名；输出不会保留该标题标签。
- **保留原件**：副本保存在原文件夹，重名自动编号，不覆盖原件或已有结果。
- **本地处理**：不上传音频，不需要账号，命名偏好保存在本机。

## 使用边界

- 仅支持 **MP3**，不处理 WAV、FLAC、M4A 等格式。
- 这是标签清理工具，不是降噪、母带处理或音频水印移除工具。
- Xing、Info、LAME 等位于音频帧内的播放和编码头会保留。
- 损坏的标签尺寸或找不到 MP3 音频帧时，会显示处理错误。
- Windows 首版使用 Electron，下载体积比原生 Mac 版更大；功能和兼容性尚未经过 Windows 实测。

## English

AudioBath creates local MP3 copies without common ID3, APEv2 and Lyrics3 tag metadata and embedded artwork. It does not re-encode audio. Custom naming and ID3 title recognition are supported; outputs are written beside the originals without overwriting existing files.

**Windows:** download the Windows x64 ZIP above, extract the entire archive and run **AudioBath.exe**. Keep all accompanying files together. Targets Windows 10/11 on Intel/AMD x64. No separate Node.js/Electron installation is needed. **Unsigned, UNTESTED pre-release: syntax and packaging checks only; no Windows launch, functional, audio or real-device tests were performed.** Limit: 500 files per batch, 512 MB per file.

**macOS:** download the macOS ZIP above, extract it and move AudioBath.app into Applications. Requires Apple Silicon and macOS 13+. Ad-hoc signed, not Apple-notarized.

**Scope:** MP3 only. Xing/Info/LAME playback headers are retained. Not an audio denoiser or watermark remover. Audio is processed locally without an account or upload.

## 反馈与 CRAT 工具系列

请在 [Issues](https://github.com/crat86/crat-audiobath/issues) 提供操作系统版本、芯片、App 版本和复现步骤。请勿公开上传未授权或未发布的音乐。GitHub 下载和反馈属于 GitHub 在线服务。

也可以试试 [CRAT MIX CHECKER](https://github.com/crat86/crat-mix-checker)：四轨混音对比、RGB 波形、全局 Loop 和响度匹配。

This repository hosts documentation, downloads and feedback. The app source code is not published here; this is not an open-source release.

Copyright © 2026 CRAT.
