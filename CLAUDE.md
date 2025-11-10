# Followly Desktop - Development Instructions

**Project:** Followly Desktop App
**Repository:** `/Users/branko/repos/Followly-Desktop/`
**GitHub:** https://github.com/virtualox/Followly-Desktop
**Purpose:** Cross-platform desktop app for analyzing Instagram CSV exports
**Status:** ✅ Windows Beta Live (v0.9.0-beta)

---

## 🔗 Related Repositories

This is part of the **Followly multi-repository architecture**:

### Desktop Applications

#### 💻 Followly-Desktop ← **YOU ARE HERE**
**Location:** `/Users/branko/repos/Followly-Desktop/`
**GitHub:** https://github.com/virtualox/Followly-Desktop
**Purpose:** Main desktop app repository (documentation, releases)
**Platform:** Cross-platform coordination

#### 🪟 Followly-Windows
**Location:** `/Users/branko/repos/Followly-Windows/`
**GitHub:** https://github.com/virtualox/Followly-Windows (private)
**Purpose:** Windows-specific implementation
**Status:** ✅ v0.9.0-beta Live
**Framework:** WinUI 3, .NET 9

#### 🍎 Followly-MacOS
**Location:** `/Users/branko/repos/Followly-MacOS/`
**Purpose:** macOS-specific implementation
**Status:** 🔨 Not started
**Framework:** .NET MAUI

#### 🐧 Followly-Linux
**Location:** `/Users/branko/repos/Followly-Linux/`
**Purpose:** Linux-specific implementation
**Status:** 🔨 Not started
**Framework:** .NET MAUI

### Other Followly Projects

#### 🌐 Followly-website
**Location:** `/Users/branko/repos/Followly-website/`
**GitHub:** https://github.com/virtualox/Followly-website
**Purpose:** Static marketing website
**URL:** https://followly.app

#### 🔧 Followly-api
**Location:** `/Users/branko/repos/Followly-api/`
**GitHub:** https://github.com/virtualox/Followly-api
**Purpose:** Azure Functions API backend
**URL:** https://api.followly.app

#### 📱 Followly-chromium
**Location:** `/Users/branko/repos/Followly-chromium/`
**Purpose:** Chrome/Edge extension (Manifest V3)
**Status:** ✅ v2.0.1 Production Ready

---

## 📂 Repository Purpose

**This repository (Followly-Desktop) serves as:**
1. **Documentation hub** - README, STATUS, CLAUDE files
2. **Release coordination** - GitHub releases for all platforms
3. **Public repository** - User-facing downloads and info
4. **Cross-platform specs** - Shared requirements and features

**Platform-specific code lives in:**
- `Followly-Windows/` - WinUI 3 app (private repo)
- `Followly-MacOS/` - MAUI macOS app (when started)
- `Followly-Linux/` - MAUI Linux app (when started)

---

## 🎯 Project Overview

### What is Followly Desktop?

A native desktop application that analyzes Instagram follower/following data exported from the Followly browser extension.

**Key Features:**
- Import CSV files from Followly extension
- Compare followers vs following
- Find who doesn't follow back
- Find followers you don't follow back
- Export results to CSV, HTML, Excel, PDF
- Dark/Light theme support
- Offline operation (no cloud required)

### Use Case

1. User exports Instagram data via Followly browser extension
2. User downloads CSV files to their computer
3. User opens Followly Desktop app
4. User imports CSV files (drag & drop or file picker)
5. App analyzes data and shows insights
6. User exports filtered lists or reports

---

## 🚀 Current Status

### Windows ✅ Beta Live
- **Version:** v0.9.0-beta
- **Released:** November 2025
- **Download:** https://github.com/virtualox/Followly-Desktop/releases/tag/v0.9.0-beta
- **Platforms:** Windows 10 22H2+, Windows 11
- **Code Signing:** Sectigo EV (VirtualOx B.V.)

### macOS 🔨 Coming Soon
- **Status:** Not started
- **Target:** Q1 2026
- **Framework:** .NET MAUI

### Linux 🔨 Coming Soon
- **Status:** Not started
- **Target:** Q1 2026
- **Framework:** .NET MAUI
- **Formats:** AppImage, .deb, .rpm

---

## 🛠️ Development Guidelines

### Language Guidelines

#### Communication
- **Dutch** - Preferred for all communication with user
- **English** - Code, documentation, git commits

#### Code
- **ALWAYS English** - Variables, functions, comments, classes
- **ALWAYS English** - Git commits and documentation
- **User-facing content** - Use resource files for localization

### Git Workflow

#### Commit Policy
- ALWAYS commit in English
- DO NOT add any Claude AI attribution lines or co-author tags
- Use conventional commits format:
  - `feat: add new feature`
  - `fix: bug fix`
  - `docs: documentation update`
  - `refactor: code refactoring`
  - `chore: maintenance tasks`

#### Push Policy
**⚠️ CRITICAL: NEVER AUTO-PUSH TO GITHUB ⚠️**

- **ABSOLUTELY NEVER** run `git push` automatically
- **ALWAYS** let user push manually via terminal
- Only use `git add` and `git commit` commands
- User will execute `git push` themselves when ready

**✅ Fetch is allowed:**
- `git fetch` is SAFE and encouraged

---

## 📋 Working with This Repo

### When to Work Here

**Use Followly-Desktop when:**
- Updating README.md (public-facing documentation)
- Creating GitHub releases
- Managing release notes
- Updating STATUS.md or CLAUDE.md
- Coordinating cross-platform features

**DON'T use Followly-Desktop for:**
- Windows app code → Use `Followly-Windows/`
- macOS app code → Use `Followly-MacOS/`
- Linux app code → Use `Followly-Linux/`

### Directory Structure

```
/Users/branko/repos/Followly-Desktop/
├── CLAUDE.md           # ← THIS FILE
├── STATUS.md           # Current status and roadmap
├── README.md           # Public-facing documentation
└── .git/               # Git repository
```

**Note:** No source code in this repo. Code is in platform-specific repos.

---

## 🔐 Code Signing

### Windows (Current)
- **Certificate:** Sectigo EV Code Signing
- **Signed by:** VirtualOx B.V.
- **Type:** Extended Validation (EV)
- **Benefits:**
  - No SmartScreen warnings
  - Instant reputation with Microsoft
  - Trusted by Windows Defender

### macOS (Future)
- **Certificate:** Apple Developer ID
- **Requirement:** Apple Developer Program membership
- **Notarization:** Required for macOS distribution

### Linux (Future)
- **Certificate:** Optional (code signing not required)
- **Verification:** GPG signature for packages

---

## 📦 Releases

### Release Process

**GitHub Releases are created in this repo (Followly-Desktop)**

1. Build platform-specific app in respective repo
2. Sign executable with EV certificate
3. Create installer package
4. Upload to GitHub Releases in Followly-Desktop repo
5. Update STATUS.md with release info
6. Update website downloads page

### Release Naming

- **Windows:** `Followly-Setup-v0.9.0-beta-win-x64.exe`
- **macOS:** `Followly-v0.9.0-beta-macos.dmg` (future)
- **Linux:** `Followly-v0.9.0-beta-linux.AppImage` (future)

### Version Numbering

- **Beta:** v0.x.x-beta
- **Stable:** v1.x.x
- **Format:** vMAJOR.MINOR.PATCH

---

## 🔄 Integration with Website

### Downloads Page

**Website URL:** https://followly.app/downloads.html

**Desktop Apps Section:**
- Windows: Links to GitHub release (v0.9.0-beta)
- macOS: "Coming Soon" button
- Linux: "Coming Soon" button
- All platforms: Link to GitHub repository

**Screenshots:**
- `desktop-import.webp` - Import CSV files
- `desktop-analysis.webp` - Analyze data
- `desktop-export.webp` - Export reports

---

## 📊 Technology Stack

### Framework
- **.NET 9** - Latest .NET runtime
- **WinUI 3** - Windows UI (Windows-specific)
- **MAUI** - Cross-platform (macOS/Linux - planned)

### Libraries
- **CsvHelper** - CSV parsing
- **ClosedXML** - Excel export
- **iTextSharp/QuestPDF** - PDF generation
- **Newtonsoft.Json** - JSON handling

---

## 🔍 Quick Decision Tree

**I need to work on...**

→ **Documentation/Releases:** You're in the right place! (Followly-Desktop)
→ **Windows app code:** Go to `Followly-Windows/`
→ **macOS app code:** Go to `Followly-MacOS/`
→ **Linux app code:** Go to `Followly-Linux/`
→ **Website:** Go to `Followly-website/`
→ **API:** Go to `Followly-api/`
→ **Browser extension:** Go to `Followly-chromium/`

---

## 📝 Documentation Files

- **README.md** - Public-facing documentation (users)
- **STATUS.md** - Current status, roadmap, recent updates
- **CLAUDE.md** - Development instructions (this file)

---

## 📞 Contact

**Developer:** Branko Vucinec
**Company:** VirtualOx B.V.
**Email:** b.vucinec@virtualox.io
**Website:** https://followly.app

---

**Last Updated:** 2025-11-10
**Status:** ✅ Windows Beta Live, macOS/Linux in planning
**Repository Type:** Public (documentation & releases)
