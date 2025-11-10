# Followly Desktop - Project Status

**Last Updated:** 2025-11-10
**Repository:** https://github.com/virtualox/Followly-Desktop
**Platform:** Cross-platform (.NET 9)

---

## 🚀 Current Status

### Windows
- **Version:** v0.9.0-beta
- **Status:** ✅ Beta Released
- **Release:** https://github.com/virtualox/Followly-Desktop/releases/tag/v0.9.0-beta
- **Repository:** https://github.com/virtualox/Followly-Windows (private)
- **Code Signing:** Sectigo EV Code Signing (VirtualOx B.V.)

### macOS
- **Version:** Not started
- **Status:** 🔨 Coming Soon
- **Repository:** https://github.com/virtualox/Followly-MacOS
- **Code Signing:** To be configured

### Linux
- **Version:** Not started
- **Status:** 🔨 Coming Soon
- **Repository:** https://github.com/virtualox/Followly-Linux
- **Package Formats:** AppImage, .deb, .rpm

---

## 📋 Windows Beta Status (v0.9.0-beta)

### Release Information
- **Released:** November 2025
- **Download:** https://github.com/virtualox/Followly-Desktop/releases/tag/v0.9.0-beta
- **Platforms:** Windows 10 22H2+, Windows 11
- **File Size:** ~150 MB (includes .NET 9 runtime)
- **Format:** Self-contained EXE installer

### Features Implemented ✅
1. ✅ **CSV Import**
   - Import Instagram followers/following CSV files
   - Support for Followly extension exports
   - Drag & drop support

2. ✅ **Data Analysis**
   - Compare followers vs following
   - Find who doesn't follow back
   - Find followers you don't follow back
   - Export filtered lists

3. ✅ **Multi-format Export**
   - CSV export
   - HTML report generation
   - Excel (.xlsx) export
   - PDF report generation

4. ✅ **User Interface**
   - Modern WinUI 3 interface
   - Dark/Light theme support
   - Responsive design
   - Data grid with sorting/filtering

### Known Issues 🐛
- None reported yet (beta testing phase)

---

## 🎯 Roadmap

### Short-term (Q4 2025)
- [ ] macOS version development
- [ ] Linux version development
- [ ] Beta testing feedback implementation
- [ ] Performance improvements
- [ ] Bug fixes from beta feedback

### Medium-term (Q1 2026)
- [ ] Windows stable release (v1.0.0)
- [ ] macOS beta release
- [ ] Linux beta release
- [ ] Cloud sync functionality
- [ ] Multi-account support

### Long-term (Q2 2026+)
- [ ] Auto-update functionality
- [ ] Advanced analytics
- [ ] Historical snapshots comparison
- [ ] API integration with Followly backend
- [ ] Premium features

---

## 🔗 Related Repositories

### Platform-Specific Repos
- **Windows:** https://github.com/virtualox/Followly-Windows (private)
- **macOS:** https://github.com/virtualox/Followly-MacOS
- **Linux:** https://github.com/virtualox/Followly-Linux

### Other Followly Projects
- **Website:** https://github.com/virtualox/Followly-website
- **API:** https://github.com/virtualox/Followly-api
- **Chrome/Edge Extension:** https://github.com/virtualox/Followly-chromium
- **Firefox Extension:** https://github.com/virtualox/Followly-firefox
- **Safari Extension:** https://github.com/virtualox/Followly-safari

---

## 📝 Recent Updates

### November 9, 2025
- ✅ Updated README.md with Sectigo EV code signing info
- ✅ Removed DigiCert references
- ✅ Published to website downloads page

### November 10, 2025
- ✅ Added to website downloads.html
- ✅ Screenshots added to website (import, analysis, export)
- ✅ Created STATUS.md documentation

---

## 🔐 Code Signing

### Windows
- **Certificate:** Sectigo EV Code Signing
- **Signed by:** VirtualOx B.V.
- **Valid:** Current
- **Status:** ✅ Active

All Windows executables and installers are digitally signed with EV certificate to ensure authenticity and prevent SmartScreen warnings.

---

## 📊 Technology Stack

### Framework
- **.NET 9** - Latest .NET runtime
- **WinUI 3** - Modern Windows UI framework (Windows only)
- **MAUI** - Cross-platform UI (macOS/Linux - planned)

### Libraries
- **CsvHelper** - CSV parsing
- **ClosedXML** - Excel export
- **iTextSharp/QuestPDF** - PDF generation
- **Newtonsoft.Json** - JSON handling

### Build & Deploy
- **MSBuild** - Build system
- **GitHub Actions** - CI/CD (planned)
- **Sectigo EV** - Code signing

---

## 🔄 Build Information

### Prerequisites
- .NET 9 SDK
- Visual Studio 2022 (Windows)
- Windows SDK 10.0.22621.0 or higher

### Build Commands
```bash
# Restore dependencies
dotnet restore

# Build (Debug)
dotnet build

# Build (Release)
dotnet build -c Release

# Publish self-contained
dotnet publish -c Release -r win-x64 --self-contained
```

---

## 📞 Support

### For Users
- **Website:** https://followly.app
- **Downloads:** https://followly.app/downloads.html
- **FAQ:** https://followly.app/faq.html
- **Email:** support@virtualox.io

### For Developers
- **Issues:** https://github.com/virtualox/Followly-Desktop/issues
- **Discussions:** https://github.com/virtualox/Followly-Desktop/discussions
- **Email:** b.vucinec@virtualox.io

---

**Status:** 🟢 Active Development (Windows Beta Live)
**Team:** VirtualOx B.V.
**License:** Proprietary
