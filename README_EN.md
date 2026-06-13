<img width="200px" src="public/icon.svg" align="left"/>

# Pot (A cute translator)

> A translator application for Windows and macOS ([Telegram Group](https://t.me/pot_app))

![License](https://img.shields.io/github/license/douxy1994/pot-desktop.svg)
![Tauri](https://img.shields.io/badge/Tauri-1.6.8-blue?logo=tauri)
![JavaScript](https://img.shields.io/badge/-JavaScript-yellow?logo=javascript&logoColor=white)
![Rust](https://img.shields.io/badge/-Rust-orange?logo=rust&logoColor=white)
![Windows](https://img.shields.io/badge/-Windows-blue?logo=windows&logoColor=white)
![MacOS](https://img.shields.io/badge/-macOS-black?&logo=apple&logoColor=white)

<br/>
<hr/>
<div align="center">

<h3><a href='./README.md'>中文</a> | English | <a href='./README_KR.md'> 한글 </a></h3>

<table>
<tr>
    <td> <img src="asset/1.png">
    <td> <img src="asset/2.png">
    <td> <img src="asset/3.png">
</table>

# Table of Contents

</div>

-   [Usage](#usage)
-   [Features](#features)
-   [Supported Services](#supported-services)
-   [Plugin System](#plugin-system)
-   [Installation](#installation)
-   [External Calls](#external-calls)
-   [Thanks](#thanks)

<div align="center">

# Usage

</div>

| Translation by selection                        | Translate by input                                                    | External calls                                                                           |
| ----------------------------------------------- | --------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| Select text and press the shortcut to translate | Press shortcut to open translation window, translate by hitting Enter | More efficient workflow by integrating other apps, see [External Calls](#external-calls) |
| <img src="asset/eg1.gif"/>                      | <img src="asset/eg2.gif"/>                                            | <img src="asset/eg3.gif"/>                                                               |

| Clipboard Listening                                                                                                          | Screenshot OCR                     | Screenshot Translation                   |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- | ---------------------------------------- |
| Click the top left icon on any translation panel to start clipboard listening. Copied text will be translated automatically. | Press shortcut, select area to OCR | Press shortcut, select area to translate |
| <img src="asset/eg4.gif"/>                                                                                                   | <img src="asset/eg5.gif"/>         | <img src="asset/eg6.gif"/>               |

<div align="center">

# Features

</div>

-   [x] Parallel translations with multiple services ([Supported Services](#supported-services))
-   [x] OCR with multiple services ([Supported Services](#supported-services))
-   [x] Text-to-Speech with multiple services ([Supported Services](#supported-services))
-   [x] Export to vocabulary apps ([Supported Services](#supported-services))
-   [x] External calls ([External Calls](#external-calls))
-   [x] Plugin system ([Plugin System](#plugin-system))
-   [x] Support Windows and macOS
-   [x] Support Dock minimize/restore and standard window controls on macOS Apple Silicon
-   [x] Multi-language support

<div align="center">

# Supported Services

</div>

## Translation

-   [x] [OpenAI](https://platform.openai.com/)
-   [x] [ChatGLM](https://www.zhipuai.cn/)
-   [x] [Gemini Pro](https://gemini.google.com/)
-   [x] [Ollama](https://www.ollama.com/) (Offline)
-   [x] [Ali Translate](https://www.aliyun.com/product/ai/alimt)
-   [x] [Baidu Translate](https://fanyi.baidu.com/)
-   [x] [Caiyun](https://fanyi.caiyunapp.com/)
-   [x] [Tencent Transmart](https://fanyi.qq.com/)
-   [x] [Tencent Interactive Translate](https://transmart.qq.com/)
-   [x] [Volcengine Translate](https://translate.volcengine.com/)
-   [x] [NiuTrans](https://niutrans.com/)
-   [x] [Google Translate](https://translate.google.com)
-   [x] [Bing Translate](https://learn.microsoft.com/zh-cn/azure/cognitive-services/translator/)
-   [x] [Bing Dictionary](https://www.bing.com/dict)
-   [x] [DeepL](https://www.deepl.com/)
-   [x] [Youdao](https://ai.youdao.com/)
-   [x] [Cambridge Dictionary](https://dictionary.cambridge.org/)
-   [x] [Yandex](https://translate.yandex.com/)
-   [x] [Lingva](https://github.com/TheDavidDelta/lingva-translate) ([Plugin](https://github.com/pot-app/pot-app-translate-plugin-template))
-   [x] [Tatoeba](https://tatoeba.org/) ([Plugin](https://github.com/pot-app/pot-app-translate-plugin-tatoeba))
-   [x] [ECDICT](https://github.com/skywind3000/ECDICT) ([Plugin](https://github.com/pot-app/pot-app-translate-plugin-ecdict))

More Services see [Plugin System](#plugin-system)

## Text Recognize

-   [x] System OCR (Offline)
    -   [x] [Windows.Media.OCR](https://learn.microsoft.com/en-us/uwp/api/windows.media.ocr.ocrengine?view=winrt-22621) on Windows
    -   [x] [Apple Vision Framework](https://developer.apple.com/documentation/vision/recognizing_text_in_images) on MacOS
-   [x] [Tesseract.js](https://tesseract.projectnaptha.com/) (Offline)
-   [x] [Baidu](https://ai.baidu.com/tech/ocr/general)
-   [x] [Tencent](https://cloud.tencent.com/product/ocr-catalog)
-   [x] [Volcengine](https://www.volcengine.com/product/OCR)
-   [x] [iflytek](https://www.xfyun.cn/services/common-ocr)
-   [x] [Tencent Image Translate](https://cloud.tencent.com/document/product/551/17232)
-   [x] [Baidu Image Translate](https://fanyi-api.baidu.com/product/22)
-   [x] [Simple LaTeX](https://simpletex.cn/)
-   [x] [OCRSpace](https://ocr.space/) ([Plugin](https://github.com/pot-app/pot-app-recognize-plugin-template))
-   [x] [Rapid](https://github.com/RapidAI/RapidOcrOnnx) (Offline [Plugin](https://github.com/pot-app/pot-app-recognize-plugin-rapid))
-   [x] [Paddle](https://github.com/hiroi-sora/PaddleOCR-json) (Offline [Plugin](https://github.com/pot-app/pot-app-recognize-plugin-paddle))

More Services see [Plugin System](#plugin-system)

## Text-to-Speech

-   [x] [Lingva](https://github.com/thedaviddelta/lingva-translate)

More Services see [Plugin System](#plugin-system)

## Collection

-   [x] [Anki](https://apps.ankiweb.net/)
-   [x] [Eudic](https://dict.eudic.net/)
-   [x] [Youdao](https://www.youdao.com/) ([Plugin](https://github.com/pot-app/pot-app-collection-plugin-youdao))
-   [x] [ShanBay](https://web.shanbay.com/web/main) ([Plugin](https://github.com/pot-app/pot-app-collection-plugin-shanbay))

More Services see [Plugin System](#plugin-system)

<div align="center">

# Plugin System

</div>

The built-in services are limited. But you can expand the app's functionality through the plugin system.

## Install Plugin

You can find plugins you need in the [Plugin List](https://pot-app.com/plugin.html), and then go to the plugin repo to download it.

The file extension of pot plugin is `.potext`. After downloading the `.potext` file, go to Preferences - Service Settings - Add External Plugin - Install External Plugin to select the corresponding `.potext` to install it. It will then be added to the service list and can be used like a built-in service.

### Troubleshooting

-   The specified module could not be found (Windows)

    Errors like this occur because the system lacks C++ libraries，Go to [here](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#visual-studio-2015-2017-2019-and-2022) download and install it.

-   Not a valid Win32 application (Windows)

    An error like this indicates that you did not download the plugin for the corresponding system or architecture. Go to the plugin repository and download the correct plugin to solve the problem.

## Develop Plugin

The [Template](https://pot-app.com/en/plugin.html#template) section in the [Plugin List](https://pot-app.com/en/plugin.html) provides plugin development templates for various plugins. Please check the corresponding template repo for specific documentation.

<div align="center">

# Installation

</div>

## Windows

### Install Manually

1. Download the installation package ending in `.exe` from the Latest [Release](https://github.com/douxy1994/pot-desktop/releases/latest) page.

    - 64-bit machine download `pot_{version}_x64-setup.exe`
    - 32-bit machine download `pot_{version}_x86-setup.exe`
    - arm64 machine download `pot_{version}_arm64-setup.exe`

2. Double click the downloaded file to install it.

### 故障排除

-   There is no interface after startup, and there is no response when clicking the tray icon.

    Check if WebView2 is uninstalled/disabled, if so, install WebView2 manually or restore it.

    If the enterprise edition system is inconvenient to install or cannot install WebView2, please try to download the fix WebView2 version `pot_{version} at [Release](https://github.com/douxy1994/pot-desktop/releases/latest) _{arch}_fix_webview2_runtime-setup.exe`

    If the issue persists, please try starting in Windows 7 compatibility mode.

## MacOS

### Install Manually

1. Download the installation package ending in `.dmg` from the Latest [Release](https://github.com/douxy1994/pot-desktop/releases/latest) page. (If you are using M1, please download the installation package named `pot_{version}_aarch64.dmg`, otherwise download the installation package named `pot_{version}_x64.dmg`)
2. Double click the downloaded file to install it.

### Troubleshooting

-   "pot" can’t be opened because the developer cannot be verified.

    Click the Cancel button, then go to the Settings -> Privacy and Security page, click the Still Open button, and then click the Open button in the pop-up window. After that, there will be no more pop-up warnings when opening pot.

    If you cannot find the above options in Privacy & Security, or get error prompts such as broken files with Apple Silicon machines. Open Terminal.app and enter the following command (you may need to enter a password halfway through), then restart pot:

    ```bash
    sudo xattr -d com.apple.quarantine /Applications/pot.app
    ```

-   If you encounter a permission prompt every time you open it, or if you cannot perform a shortcut translation, please go to Settings -> Privacy & Security -> Supporting Features to remove pot, and then re-add pot.

<div align="center">

# External Calls

</div>

Pot provides a complete HTTP interface for integration with other software. You can call pot by sending HTTP requests to `127.0.0.1:port`, where `port` is the listening port of pot, default to `60828`, and can be changed in the app settings.

## API Docs:

```bash
POST "/" => Translate given text (body is text to translate)
GET "/config" => Open settings
POST "/translate" => Translate given text (same as "/")
GET "/selection_translate" => Translate selected text
GET "/input_translate" => Open input translation
GET "/ocr_recognize" => Perform OCR on screenshot
GET "/ocr_translate" => Perform translation on screenshot
GET "/ocr_recognize?screenshot=false" => OCR without taking screenshot
GET "/ocr_translate?screenshot=false" => Translate screenshot without taking screenshot
GET "/ocr_recognize?screenshot=true" => OCR with screenshot
GET "/ocr_translate?screenshot=true" => Translate screenshot
```

## Example:

-   Call translation by selection:

    To call pot's translation by selection, simply send a request to `127.0.0.1:port`:

    E.g. using curl:

    ```bash
    curl "127.0.0.1:60828/selection_translate"
    ```

## OCR without internal screenshot

This allows you to perform OCR/translation without using pot's internal screenshot, so you can use your own screenshot tools.

### Workflow:

1. Take screenshot using other tool
2. Save screenshot to `$CACHE/com.pot-app.desktop/pot_screenshot_cut.png`
3. Send request to `127.0.0.1:port/ocr_recognize?screenshot=false` to call

> `$CACHE` is the system cache dir, e.g. `C:\Users\{username}\AppData\Local\com.pot-app.desktop\pot_screenshot_cut.png` on Windows.

## Existing Usages (Quick selection translation)

### SnipDo (Windows)

1. Download and install SnipDo in the [Microsoft Store](https://apps.microsoft.com/store/detail/snipdo/9NPZ2TVKJVT7)
2. Download the SnipDo extension of pot from the Latest [Release](https://github.com/douxy1994/pot-desktop/releases/latest) (pot.pbar)
3. Double click the downloaded file to install it.
4. Selection some text, you can see the pot icon in the upper right corner of the selection, click the icon to translate.

### PopClip (MacOS)

1. Download and install PopClip in the [App Store](https://apps.apple.com/us/app/popclip/id445189367?mt=12)
2. Download the PopClip extension of pot from the Latest [Release](https://github.com/douxy1994/pot-desktop/releases/latest) (pot.popclipextz)
3. Double click the downloaded file to install it.
4. Enable the pot extension in PopClip settings, and then you can translate by selecting text.

## Manual compilation

### Requirements

Node.js >= 18.0.0

pnpm >= 8.5.0

Rust >= 1.80.0

### Start compilation

1. Clone the repository

    ```bash
    git clone https://github.com/douxy1994/pot-desktop.git
    ```

2. Install dependencies

    ```bash
    cd pot-desktop
    pnpm install
    ```

3. Development (Optional)

    ```bash
    pnpm tauri dev # Run the app in development mode
    ```

4. Build
    ```bash
    pnpm tauri build # Build into installation package
    ```

<div align="center">

# Acknowledgement

</div>

-   [Bob](https://github.com/ripperhe/Bob) Inspiration
-   [bob-plugin-openai-translator](https://github.com/yetone/bob-plugin-openai-translator) OpenAI API Reference
-   [@uiYzzi](https://github.com/uiYzzi) Implementation ideas
-   [Tauri](https://github.com/tauri-apps/tauri) A user-friendly GUI framework.
