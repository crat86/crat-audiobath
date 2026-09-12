# AudioBath

**给 MP3 洗个澡，保留原来的声音。**  
A local MP3 metadata cleaner. Part of the CRAT Tool Series.

[**下载 / Download v0.2.0 Beta**](https://github.com/crat86/crat-audiobath/releases/tag/v0.2.0-beta) · [反馈 / Issues](https://github.com/crat86/crat-audiobath/issues)

> **Apple Silicon · macOS 13+ · Beta**  
> 当前开发包为临时签名，尚未经过 Apple Developer ID 签名及公证；macOS 可能阻止首次打开。Ad-hoc signed and not notarized by Apple; macOS may block launch.

## 它能做什么

把单个或一批 MP3 拖到卡通水龙头下面，生成清理了常见标签和封面的新副本。

- **不转码**：不解码、不重新编码，MP3 音频帧保持字节级不变。
- **批量处理**：一次拖入多个 MP3，统一应用命名规则。
- **清理常见标签**：ID3v2、ID3v1 / ID3v1+、APEv2、Lyrics3，以及这些标签中包含的封面、标题、作者和备注。
- **自定义名称**：后缀、前缀或完整格式；支持 `{歌名}`、`{原名}`、`{标记}` 占位符。
- **智能歌名**：可先读取 ID3 标题用于命名，缺失时回退到原文件名；输出不会保留该标题标签。
- **保留原件**：在原文件所在文件夹创建新 MP3，重名时自动顺延编号，不覆盖源文件或已有结果。
- **全程离线**：不上传音频，不需要账号；命名偏好保存在本机。

## 安装与使用

1. 打开下载页面，在 **Assets** 下载 `CRAT-AudioBath-v0.2.0-macOS-arm64.zip`。自动生成的 **Source code** 不是安装包。
2. 解压，把 **AudioBath.app** 拖到“应用程序”。
3. 打开 App，设置出浴命名规则，再拖入一个或多个 MP3。
4. 在处理结果中查看输出；新文件位于原文件所在文件夹。请确保该文件夹允许写入。

例如，默认清理副本可以命名为 `歌曲_clean.mp3`；如果已存在，则自动使用新的编号。

## 使用边界

- 当前仅支持 **MP3**，不处理 WAV、FLAC、M4A 等格式。
- 这是标签清理工具，不是降噪、母带处理或音频水印移除工具。
- Xing、Info、LAME 等位于音频帧内的播放和编码头会保留，以支持正常播放与定位。
- 遇到损坏的标签尺寸或找不到 MP3 音频帧时，会停止该文件的处理并显示原因。
- 当前提供 Apple Silicon（M 系列）版本，最低 macOS 13；不包含 Intel 或 Windows 版本。更多系统和文件兼容性仍在测试。

## English

Drag one or more MP3 files into AudioBath to create copies without common tag metadata and embedded artwork. AudioBath removes supported ID3, APEv2 and Lyrics3 tags **without re-encoding**: MPEG audio frames remain byte-for-byte unchanged.

Customize output filenames with prefixes, suffixes or a template. Outputs are created beside their originals; existing files are never overwritten. Everything runs locally, without an account or audio upload.

**Install:** download the named ZIP from Release Assets, extract it, and move AudioBath.app into Applications. Requires an Apple Silicon Mac running macOS 13 or later. This beta is ad-hoc signed and not Apple-notarized.

**Scope:** MP3 only. Playback headers such as Xing/Info/LAME are preserved. This is not an audio denoiser or watermark remover. Malformed tags or missing audio frames produce an error instead of an output.

## 反馈与 CRAT 工具系列

请在 [Issues](https://github.com/crat86/crat-audiobath/issues) 提供 macOS 版本、芯片、App 版本和复现步骤。请勿公开上传未授权或未发布的音乐。GitHub 的下载和反馈功能属于 GitHub 在线服务。

也可以试试 [CRAT MIX CHECKER](https://github.com/crat86/crat-mix-checker)：四轨混音对比、RGB 波形、全局 Loop 和响度匹配。

This repository hosts documentation, downloads and feedback. The app source code is not published here; this is not an open-source release.

Copyright © 2026 CRAT.
