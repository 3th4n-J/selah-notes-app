<div align="center">

<img src="docs/screenshots/icon.png" width="120" alt="Selah Notes icon" />

# Selah Notes

**Capture sermon notes and personal spiritual trackers — with a full Bible reader (MKJV, KJV & WEB) built right in.**

[![Version](https://img.shields.io/badge/version-6.1.0-6750A4)](https://github.com/3th4n-J/selah-notes-app/releases)
[![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white)](https://github.com/3th4n-J/selah-notes-app/releases)
[![Built with Flet](https://img.shields.io/badge/built%20with-Flet-00C8FF)](https://flet.dev)
[![Python](https://img.shields.io/badge/python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org)
[![Offline](https://img.shields.io/badge/offline-first-2E7D32)](#-privacy)

<em>“Be still, and know that I am God.” — Psalm 46:10</em>

</div>

---

## ✨ Overview

**Selah Notes** is a calm, offline-first note-taking app for the everyday church-goer and Bible-college student. Jot sermon notes, keep personal spiritual trackers (prayers, dreams, visions), and study lecture notes — all with the **Bible** (MKJV, KJV and WEB) a tap away for pulling verses straight into your notes.

No accounts. No servers. No tracking. Your notes live on your device.

> 🕊️ Built with the prayer that it's a blessing — a quiet place to hear, reflect, and remember.

---

## 📸 Screenshots

<div align="center">

| Home | Note editor | Verse index | Lock screen |
|:---:|:---:|:---:|:---:|
| <img src="docs/screenshots/home.png" width="180"/> | <img src="docs/screenshots/editor.png" width="180"/> | <img src="docs/screenshots/verses.png" width="180"/> | <img src="docs/screenshots/lock.png" width="180"/> |

</div>

---

## 🚀 Features

### 📝 Your Notes, Your Way
- **Three note types** — Sermon **Notes**, personal **Trackers** (Prayer, Dream, Vision, Testimony…), and **Bible College** lecture notes.
- **Templates at creation** — start from a Sermon outline or Lecture skeleton, or a blank page.
- **Context fields** — Minister (sermon notes) with autocomplete, Course + Lesson (college notes).
- **Folders** you can create, rename, recolour and re-icon; **pin** notes to the top.

### ✍️ Writing Experience
- **Auto verse chips** - type `John 3:16` or `1 Cor 13:4-7` and it becomes a chip; tap one for a sheet with prev/next verse and the full chapter, your passage highlighted.
- **`[[Note links]]` + backlinks**, **focus mode** (distraction-free, screen stays on), live word count and **draft autosave** with restore.
- **Continue writing** card on the home screen.

### 📖 Scripture, Woven In
- **Three Bible translations** bundled offline (66 books each): **MKJV**, **KJV** and **WEB**. Pick your default in *Settings → Bible*; the reader and every verse sheet can switch on the spot.
- **Bible reader** (home → *Bible*) — book/chapter navigator (type a reference like `john 3` to jump), prev/next chapter, remembers where you stopped. Tap a verse to **highlight** it (4 colours), **bookmark** it, **copy**, **share**, or **add it to a note** as a verse chip. A **Bookmarks** page lists your bookmarks and highlights; both are included in backups.
- **Verse picker** — search a book, pick chapter & verse (or a range like `JHN 3:16-18`), preview, and drop it in as a chip.
- **Reference-aware search** — `PSA23:1`, `psa 23.1-3`, `1 cor 13`, `psalms` all just work.
- **Verse of the day** on the home screen.
- **Verse cross-references** — tap a verse chip to see every other note that cites it, plus a dedicated **Verse Index** of your most-referenced scriptures.

### 📚 Series, Prayer & Insights
- **Series** view: every sermon in a series in preaching order.
- **Prayer timeline**: trackers by month, mark prayers *answered* (with date) and see how long it took.
- **Insights**: notes per month, who you hear from, a 66-book scripture heatmap, writing streak.

### 🏷️ Organise & Find
- **Series** field for sermon series, and **colour + icon Tags** you can create and manage.
- **Full-text search** across notes *and* the entire Bible (in your default translation), with **filters** (type, tag, minister, prayer status, date range) and **saved searches**.
- **Multi-select** to bulk move / pin / trash / **export & share** (Selah bundle `.snn`, **PDF** or readable `.md`). **Trash** keeps deletions for 30 days with one-tap undo.

### 📎 Rich Content
- **Photo attachments** — snap a slide or handout; auto-downscaled to keep things lean (5 MB / file, 25 MB / note caps).
- **Reminders** — recurring, with due banners (and OS notifications where supported).

### 🔒 Private & Secure
- **PIN app-lock** with a keypad, filling dots, and a custom unlock animation. PINs are PBKDF2-hashed, never stored in plaintext. Auto-locks after time in the background.
- **Local-first** — all your data stays on-device. 

### 💾 Portable
- **Backup & restore** to a JSON file (includes photos, tag styling, bookmarks and highlights).
- **`.snn` note files** — share a single note (all metadata + photos) and import it on another device with full fidelity.
- **PDF export** — one styled note, or a bundle with cover page, contents grouped by series and PDF bookmarks. Multi-select notes (or use the export icon in the editor) → **Selah bundle / PDF / text**.

### ♿ Accessibility
- **Reading text size** (100-170%) for notes and scripture, on top of your phone's font size.
- **High contrast**, **reduce motion**, **haptics on/off**, configurable **auto-lock timing**.
- Bundled **Atkinson Hyperlegible** font (SIL OFL) designed for low-vision readers; labelled controls for TalkBack.

### 🎨 Polished
- Light / Dark / System themes (plus **pure-black AMOLED**), **accent palettes** (+ custom colour), app & scripture fonts.
- Collapsible detail panes, smooth route transitions, tasteful animations, a personal birthday greeting, and an in-app **update checker**.

---

## 🛠️ Tech stack

| | |
|---|---|
| **Language** | Python 3.10+ |
| **UI** | [Flet](https://flet.dev) 1.0.4 (Flutter under the hood) |
| **Storage** | SQLite — `MKJV.db`, `KJV.db`, `WEB.db` (read-only scripture, same schema) + `userDB.db` (your data) |
| **Imaging** | Pillow (photo downscale/re-encode) |
| **Tooling** | [uv](https://github.com/astral-sh/uv) for env & builds |
| **Extensions** | `flet-local-notifications` (vendored) for OS reminders |

---

## 🏁 Getting Started (development)

```bash
# 1. Install uv (https://github.com/astral-sh/uv), then sync deps
uv sync

# 2. Run on desktop for quick iteration
uv run flet run

# 3. Build a signed Android APK (see Release workflow below)
uv run flet build apk
```

> **Note:** Android release builds use a **vendored build template** (`flet-build-template/`) that carries a core-library-desugaring patch — keep it committed.

---

## 📦 Release Workflow

Two helper scripts (git-ignored, since they hold local paths/secrets) make releases a two-step affair:

```powershell
# Build a signed APK — prompts for the keystore password, auto-increments versionCode
.\build-release.ps1

# Commit, tag (vX.Y.Z), push, and publish the GitHub release
.\create-release.ps1            # prompts once for a message used as commit + release notes
.\create-release.ps1 -Build     # chain both: build then release
```

Signing uses **Play App Signing-ready** release keys (your `.jks` is the upload key). Releases are published to the public downloads repo.

📥 **Download The Latest APK here:** [github.com/3th4n-J/selah-notes-app/releases](https://github.com/3th4n-J/selah-notes-app/releases)

---

## 🗂️ Project Structure

```
src/
├─ main.py                # entry point: theming, routing, app-lock gate, lifecycle
├─ assets/                # MKJV.db / KJV.db / WEB.db, fonts, icon, splash, unlock animation
└─ app/
   ├─ config.py           # constants, palettes, templates, version
   ├─ db.py               # SQLite data layer (notes, tags, photos, backup, .snn)
   ├─ prefs.py            # JSON preferences + transient nav state
   ├─ a11y.py             # accessibility prefs: reading size, contrast, motion, haptics
   ├─ drafts.py           # unsaved-edit drafts (crash safety net)
   ├─ searches.py         # search filters + saved searches
   ├─ security.py         # PIN hashing (PBKDF2)
   ├─ media.py            # photo downscale/re-encode
   ├─ theme.py            # Material 3 theming + accent handling
   ├─ ui.py               # shared components (cards, chips, dialogs, pickers)
   ├─ updates.py          # in-app GitHub release check
   ├─ verse_picker.py     # MKJV verse picker
   └─ views/              # home, editor, folder, search, settings, reminders,
                          # trash, verses, lock, series, timeline, insights, bible, bookmarks
extensions/               # vendored flet-local-notifications
flet-build-template/      # vendored build template (desugaring patch)
```

---

## 🔐 Privacy

Selah Notes is **offline-first and account-free**. Your notes, photos and reminders never leave your device. The only network request is an optional check to GitHub for app updates. Backups and shared `.snn` files are created **only when you choose to export them**.

---

## 🙏 Acknowledgements & Author

Made with care by **Ethan Johnston**.

Scripture text:
- **Modern King James Version (MKJV)**.
- **King James Version (KJV)**, 1769 text — public domain in most of the world; in the United Kingdom the Crown holds letters patent over the KJV (administered through Cambridge University Press). Sourced from [scrollmapper/bible_databases](https://github.com/scrollmapper/bible_databases) (MIT).
- **World English Bible (WEB)**, 2020 stable text from [eBible.org](https://ebible.org/web/) — public domain. *"World English Bible"* is a trademark of eBible.org; the text is bundled unmodified (verses the WEB omits are simply absent).

> May this app be as much of a blessing to you as it was building it.
> Jesus loves you and wants a deeper relationship with you.
> Be blessed.❤️

---

<div align="center">
<sub>© 2025–2026 Ethan Johnston · Selah Notes</sub>
</div>
