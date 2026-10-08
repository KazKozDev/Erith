# Erith — offline translator for Mac with a built-in local model

Translate text, PDF and Word files on your Mac without sending them anywhere.

[Download the latest release](https://github.com/KazKozDev/Erith/releases/latest) · free during early access

![Translating three paragraphs from English to German in Erith](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/demo.gif)

Runs on your Mac · No account · No internet after setup

---

## Quick start

1. Download the `.zip` (about 230 MB) from [Releases](https://github.com/KazKozDev/Erith/releases/latest), unzip it and drag Erith into Applications.
2. Open it. The app is not notarized by Apple yet, so macOS refuses the first launch: open System Settings → Privacy & Security, scroll down to the line about Erith and press Open Anyway. On macOS 14 and earlier, right-click the app and choose Open instead.
3. Erith offers to download a model: keep TranslateGemma 4B (2.2 GB) and press Download and start. This is the only step that needs the internet.
4. Type or paste text and press Translate (⌘↵).

Instead of step 2 you can lift the quarantine in Terminal, once:

```bash
xattr -dr com.apple.quarantine /Applications/Erith.app
```

To check that the download is intact, compare it with the `.sha256` file next to it:

```bash
shasum -a 256 Erith-*-arm64.zip
```

## Translate PDF and Word files and keep their layout

Use File → Translate Files… (⇧⌘O), or drop `.pdf` and `.docx` files on the left pane. A Word file keeps its styles, tables, headers, footnotes and the bold, italic and linked words inside a paragraph. In a PDF the translation is drawn into the place of the original text at the same size and colour; pictures and backgrounds stay.

```
report.docx  →  report.de.docx   (saved next to the original)
report.pdf   →  report.de.pdf
```

The original is never overwritten. Markdown, `.srt` subtitles, `.csv` and plain text are translated too, and the result card lists passages that may be cut off or numbers that went missing.

## Translate selected text in any Mac app with one shortcut

Select text anywhere and press ⌃⌥T. A small card appears by the pointer with the translation, a Copy button and "Open in Erith".

The shortcut copies your selection by sending ⌘C, so macOS asks for access under System Settings → Privacy & Security → Accessibility (named Device Control and Data Access on macOS 27). Settings → General shows whether it is allowed.

## Translate text from any part of the screen

Press ⌃⌥O and drag a rectangle over a menu, a sign, a picture or a video subtitle. The text is read on your Mac with Apple Vision and the translation appears in the same card. The first use asks for Screen Recording permission.

## How it works

Erith runs Google's TranslateGemma inside the app with Apple's [MLX](https://github.com/ml-explore/mlx): there is no server and no account, and your text stays on the Mac. It detects the language, splits the text into paragraphs and translates them one at a time, so line breaks survive and the two panes stay paired. After translating it warns about paragraphs that look cut off and numbers or names that went missing. Listen reads either side aloud with the Mac's voices or with Qwen3-TTS, a neural voice that also runs on the Mac.

```
text or file → detect language → split paragraphs → model on your Mac → checks → side-by-side panes
```

## Configuration

Everything is set in the Settings window.

| Option | Default | What it does |
|---|---|---|
| Appearance | System | Follows macOS, or a fixed Pink, Glass, Forest, Light or Dark theme |
| Language | System | The interface in 13 languages |
| Model | none until downloaded | TranslateGemma 4B (2.2 GB) or 12B (6.7 GB), or another MLX model from Hugging Face |
| Mode | Quality | Fast runs 4B, Quality runs 12B |
| Tone | Default | Formal or informal register |
| Style | Natural | Literal stays close to the original wording, which suits language study |
| Glossary | empty | `term = translation` lines, used when the term appears |
| Voice engine | System voices | The Mac's own voices, or Qwen3-TTS (a 4.5 GB download) |
| Translate selection anywhere | On | The ⌃⌥T shortcut |
| Check for updates | On | Once a day asks GitHub for the latest version number; nothing else is sent |

## Requirements

- A Mac with Apple Silicon (Intel is untested)
- Used daily on macOS 27; the build also passes its self-test on macOS 14
- Internet once, to download a model from Hugging Face
- About 550 MB of disk for the app, plus 2.2 GB for the 4B model or 6.7 GB for 12B
- About 3 GB of free memory for the 4B model; 16 GB of memory or more for 12B
- Accessibility permission for ⌃⌥T and Screen Recording permission for ⌃⌥O

## Limitations

- Not notarized: macOS asks you to confirm the first launch (see Quick start), and after each update it asks again for the Accessibility and Screen Recording permissions.
- Early access. It is free now; later versions may be paid. A copy you downloaded stays yours to use.
- The source code is not published. Erith is closed-source freeware, not open source.
- PDF layout is kept for languages in Latin, Cyrillic and Greek scripts. For Chinese, Japanese, Korean, Arabic and Hindi a PDF is saved as plain text. Scanned PDFs without a text layer are not supported.
- TranslateGemma often ignores glossary terms; a general model such as Gemma 3 follows them.
- Qwen3-TTS reads 10 of the 16 languages; Ukrainian, Dutch, Polish, Arabic, Hindi and Turkish are read by a system voice.
- A translation can be wrong. Check it before relying on it where a mistake matters.

---

<div align="center">

![macOS](https://img.shields.io/badge/macOS-333?style=flat-square&logo=apple&logoColor=fff)

[Issues](https://github.com/KazKozDev/Erith/issues) · [License](LICENSE) · [Third-party notices](NOTICE) · [Changelog](CHANGELOG.md)

</div>
