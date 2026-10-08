<div align="center">

<img src="https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/icon.png" alt="Erith icon: a robin" width="128">

# Erith — offline translator for Mac

**Translate text, PDF and Word files without sending a single word anywhere.**

The model runs inside the app, on your Mac. No cloud. No account. No internet needed.

[![Download for Mac](https://img.shields.io/badge/Download_for_Mac-free_during_early_access-f2551c?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/KazKozDev/Erith/releases/latest)

Apple Silicon · 230 MB · 16 languages

</div>

![Translating three paragraphs from English to German in Erith](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/demo.gif)

---

## Your text stays on your Mac

A contract, a medical letter, a message you would not show a stranger: an online translator receives every word of it. Erith does not. It runs Google's TranslateGemma on your own Mac, so there is no server to send anything to.

- **Nothing leaves the computer.** Not the text, not the files, not usage data.
- **Works offline.** After the one-time model download you can turn the Wi-Fi off: on a plane, on a train, behind a company firewall.
- **No account, no subscription, no character limits.** Translate one line or a long document.

| | Erith | An online translator |
|---|---|---|
| Where your text goes | Nowhere | To someone's server |
| Works without internet | Yes | No |
| Account | None | Often needed for documents |
| Character limits | None | Common on free plans |

## Whole documents, layout intact

Drop a PDF or a Word file on the window and get the same document in another language, saved next to the original.

```
report.docx  →  report.de.docx
report.pdf   →  report.de.pdf
```

- **Word** keeps styles, tables, headers, footnotes, and the bold, italic and linked words inside a sentence.
- **PDF** gets the translation drawn in place of the original text, at the same size and colour; pictures and backgrounds stay.
- **Subtitles, Markdown and CSV** keep their timings, headings and columns.
- **Your original is never overwritten.**

## Translate any area of the screen

**Press ⌃⌥O and drag a rectangle over anything you see.** A menu in a foreign app, a sign in a photo, a subtitle in a video, text inside a picture: Erith reads it with Apple Vision and shows the translation on the spot. If it is on your screen, it can be translated.

## Translate anywhere on your Mac

**Select text in any app and press ⌃⌥T.** A small card appears by the pointer with the translation: in Mail, in a browser, in a PDF viewer, in a chat.

## Paste a link, get the article

**Paste a web address straight into the left pane.** Erith fetches the page, drops the menus and banners, and puts the text of the article in the pane, ready to translate. No copying paragraph by paragraph.

## Checked, not just translated

- **Side by side.** The original and the translation stay paired paragraph by paragraph.
- **Things to check.** After each translation Erith points at paragraphs that look cut off and numbers or names that went missing.
- **Your tone.** Formal or informal, natural or literal (useful when you study a language).
- **Fast or Quality.** A 2.2 GB model that runs on any Apple Silicon Mac, or a 6.7 GB one for better quality.
- **Listen.** Hear either side read aloud by the Mac's voices or by a neural voice that also runs on your Mac.

## Made for the Mac

A native window, system shortcuts, and five looks: Pink, Light, Dark, and two kinds of glass, clear and forest green. The interface speaks 13 languages.

![Erith in the Pink, Light, Dark and Forest appearances](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/themes.png)

**Translates between:** English, Russian, Ukrainian, Spanish, French, German, Italian, Portuguese, Dutch, Polish, Chinese, Japanese, Korean, Arabic, Hindi and Turkish.

## Get it in three minutes

1. **[Download the latest release](https://github.com/KazKozDev/Erith/releases/latest)**, unzip it and drag Erith into Applications.
2. **Open it.** Erith is not notarized by Apple yet, so macOS stops the first launch: go to System Settings → Privacy & Security, scroll down to the line about Erith and press Open Anyway. On macOS 14 and earlier, right-click the app and choose Open.
3. **Download a model** when Erith offers: keep TranslateGemma 4B (2.2 GB). This is the only step that needs the internet.
4. **Press Translate (⌘↵).**

Prefer Terminal? This replaces step 2:

```bash
xattr -dr com.apple.quarantine /Applications/Erith.app
```

To check that the download is intact, compare it with the `.sha256` file next to it:

```bash
shasum -a 256 Erith-*-arm64.zip
```

## Questions

**Is it really free?**
Yes, during early access. Later versions may be paid; a copy you downloaded stays yours to use.

**Which Macs?**
Any Mac with Apple Silicon. Used daily on macOS 27; the build also passes its self-test on macOS 14. Intel Macs are untested. You need about 550 MB for the app, 2.2 GB for the model and about 3 GB of free memory.

**Why does macOS warn me on the first launch?**
Apple's notarization needs a paid developer account, which Erith does not have yet. Until then macOS also asks again for the Accessibility and Screen Recording permissions after each update.

**Does it ever go online?**
Only for three things: to download a model when you ask for one, to fetch a page when you paste its link, and once a day to ask GitHub for the latest version number, which you can turn off in Settings. Your text is never part of any of them.

**Is it open source?**
No. Erith is closed-source freeware. The libraries and models it uses are listed in [NOTICE](NOTICE).

**How good is the translation?**
As good as TranslateGemma, an open translation model from Google. It can be wrong: check a translation before relying on it where a mistake matters.

**What does not work yet?**
PDF layout is kept for languages in Latin, Cyrillic and Greek scripts; for Chinese, Japanese, Korean, Arabic and Hindi a PDF is saved as plain text, and scanned PDFs are not supported. TranslateGemma often ignores glossary terms. The neural voice reads 10 of the 16 languages; the rest are read by a system voice.

---

<div align="center">

**[Download Erith for Mac](https://github.com/KazKozDev/Erith/releases/latest)**

![macOS](https://img.shields.io/badge/macOS-333?style=flat-square&logo=apple&logoColor=fff)

[Issues](https://github.com/KazKozDev/Erith/issues) · [License](LICENSE) · [Third-party notices](NOTICE) · [Changelog](CHANGELOG.md)

</div>
