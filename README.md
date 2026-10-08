<div align="center">

<img src="https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/icon.png" alt="Erith, an offline translator for Mac: a robin icon" width="128">

# Erith — offline translator for Mac

### Translate anything on your Mac. Send nothing to anyone.

An on-device translator for text, PDF and Word files that works without internet.<br>
The model runs inside the app: no cloud, no account, no upload.

[![Download the offline translator for Mac](https://img.shields.io/badge/Download_for_Mac-free_during_early_access-f2551c?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/KazKozDev/Erith/releases/latest)

Apple Silicon · 230 MB · 16 languages

</div>

https://github.com/user-attachments/assets/9a816f0a-1411-48fc-89e5-5f5604df70be

<sub>Music in the film: 'Life in Silico' by Scott Buckley - released under CC-BY 4.0. www.scottbuckley.com.au</sub>

## A private translator: your text is never uploaded

**What you translate is nobody else's business.** A contract. A medical letter. A message you would not show a stranger. A cloud translator receives every word of it, and you cannot take it back. Erith has no server to send anything to: it runs Google's TranslateGemma on your own Mac, so the translation stays on your device.

That also makes it a translator that works without internet: with the Wi-Fi off, on a plane or behind a company firewall, with no account to create, no subscription to cancel and no character limit to hit.

## Translate text, PDF and Word documents offline

| You have | You do | You get |
|:---|:---|:---|
| **A text** | Paste it and press ⌘↵ | The translation beside the original, paragraph by paragraph |
| **A PDF or Word document** | Drop it on the window | The same document in another language, layout intact, saved next to the original |
| **A web article** | Paste its link into the left pane | The article's text without menus and banners, ready to translate |
| **A line in any app** | Select it and press ⌃⌥T | A card with the translation by the pointer, without leaving Mail, the browser or a chat |
| **Text in a picture or a screenshot** | Press ⌃⌥O and drag over any area of the screen | The translation of a menu, a sign in a photo, a video subtitle or an image |
| **No time to read** | Press Listen | Either side read aloud, by the Mac's voices or a neural voice that also runs on your Mac |

Erith does not just hand you a translation and leave. It keeps the original and the result paired, points at paragraphs that look cut off and at numbers or names that went missing, and lets you choose the tone: formal or informal, natural or literal. Pick Fast for a model that runs on any Apple Silicon Mac, or Quality for a bigger one.

It translates between English, Russian, Ukrainian, Spanish, French, German, Italian, Portuguese, Dutch, Polish, Chinese, Japanese, Korean, Arabic, Hindi and Turkish.

## An offline alternative to Google Translate and DeepL for Mac

Both are good translators, and both do the work on their own servers. Erith is for the text you would rather not send there, and for the places where there is no connection to send it over.

| | Erith | Google Translate | DeepL |
|:---|:---|:---|:---|
| Where your text is translated | On your Mac | On Google's servers | On DeepL's servers |
| Works without internet on a Mac | Yes | No | No |

## A translator for work, study and travel without Wi-Fi

- **Work.** Contracts, reports and e-mail that must not leave the company: translate a whole document and keep its layout, or a line in Mail with one shortcut.
- **Study.** Articles from a link, PDFs of papers, and a Literal style that stays close to the original wording when you are learning a language.
- **Travel.** A plane, a train, a hotel with no Wi-Fi: once the model is on your Mac, the translator needs no connection.

## A native Mac app in five looks

System shortcuts, an interface in 13 languages and five appearances: Pink, Light, Dark, Glass and Forest.

| Pink | Light |
|:---|:---|
| ![Erith offline translator in the Pink appearance](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/theme-pink.png) | ![Erith offline translator in the Light appearance](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/theme-light.png) |
| **Dark** | **Forest** |
| ![Erith offline translator in the Dark appearance](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/theme-dark.png) | ![Erith offline translator in the Forest appearance](https://raw.githubusercontent.com/KazKozDev/Erith/main/assets/theme-forest.png) |

## Download the offline translator and start in three minutes

1. **[Download Erith](https://github.com/KazKozDev/Erith/releases/latest)**, unzip it and drag it into Applications.
2. **Open it.** Erith is not notarized by Apple yet, so macOS stops the first launch: go to System Settings → Privacy & Security, scroll down to the line about Erith and press Open Anyway (on macOS 14 and earlier, right-click the app and choose Open). Or lift the quarantine in Terminal: `xattr -dr com.apple.quarantine /Applications/Erith.app`
3. **Let it download a model** (2.2 GB, once). It works like a language pack, except that one download covers all 16 languages. After that the internet is optional.
4. **Press Translate.**

<details>
<summary><b>Does it work without internet? Is my text uploaded? Is it free? Which Macs?</b></summary>

<br>

**Does the translator work without internet?** Yes. After the one-time model download, translating text and documents, the shortcuts and Listen all work offline.

**Is my text uploaded anywhere?** No. The translation runs on your device. Erith goes online for three things only: to download a model when you ask for one, to fetch a page when you paste its link, and once a day to ask GitHub for the latest version number, which you can turn off. Your text is never part of any of them.

**Is it free?** Yes, during early access. Later versions may be paid; a copy you downloaded stays yours to use.

**Which Macs?** Any Mac with Apple Silicon; Intel is untested. Used daily on macOS 27, and the build passes its self-test on macOS 14. You need about 550 MB for the app, 2.2 GB for the model and about 3 GB of free memory. The Quality model is 6.7 GB and wants 16 GB of memory.

**Why does macOS warn me on the first launch?** Notarization needs a paid Apple developer account, which Erith does not have yet. Until then macOS also asks again for the Accessibility and Screen Recording permissions after each update.

**How good is the translation?** As good as TranslateGemma, an open translation model from Google. It can be wrong: check a translation before relying on it where a mistake matters.

**Does it translate speech or use the camera?** No. Erith translates written text: typed, pasted, in documents, in other apps and in pictures on the screen. Listen reads a text aloud; it does not translate what you say.

**What does not work yet?** PDF layout is kept for languages in Latin, Cyrillic and Greek scripts; for Chinese, Japanese, Korean, Arabic and Hindi a PDF is saved as plain text, and scanned PDFs are not supported. TranslateGemma often ignores glossary terms. The neural voice reads 10 of the 16 languages; the rest are read by a system voice.

**Is it open source?** No. Erith is closed-source freeware. The libraries and models it uses are listed in [NOTICE](NOTICE).

**How do I check the download?** Compare `shasum -a 256 Erith-*-arm64.zip` with the `.sha256` file next to it.

</details>

---

<div align="center">

### Your words. Your Mac. Nobody else.

[![Download the offline translator for Mac](https://img.shields.io/badge/Download_for_Mac-free_during_early_access-f2551c?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/KazKozDev/Erith/releases/latest)

[Issues](https://github.com/KazKozDev/Erith/issues) · [License](LICENSE) · [Third-party notices](NOTICE) · [Changelog](CHANGELOG.md)

</div>
