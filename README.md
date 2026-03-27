# PrivGuard
AES-128 encryption Android app built with Kotlin &amp; Jetpack Compose
<!-- HEADER BANNER -->
<div align="center">

```
██████╗ ██████╗ ██╗██╗   ██╗ ██████╗ ██╗   ██╗ █████╗ ██████╗ ██████╗
██╔══██╗██╔══██╗██║██║   ██║██╔════╝ ██║   ██║██╔══██╗██╔══██╗██╔══██╗
██████╔╝██████╔╝██║██║   ██║██║  ███╗██║   ██║███████║██████╔╝██║  ██║
██╔═══╝ ██╔══██╗██║╚██╗ ██╔╝██║   ██║██║   ██║██╔══██║██╔══██╗██║  ██║
██║     ██║  ██║██║ ╚████╔╝ ╚██████╔╝╚██████╔╝██║  ██║██║  ██║██████╔╝
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═══╝   ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝
```

### ⚡ SECURE ENCRYPTION · AES-128 · CYBERPUNK UI ⚡

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://android.com)
[![Kotlin](https://img.shields.io/badge/Kotlin-2.0.21-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-2024.12-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![AES-128](https://img.shields.io/badge/Encryption-AES--128--CBC-FF006E?style=for-the-badge&logo=shield&logoColor=white)](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard)
[![License](https://img.shields.io/badge/License-MIT-BC13FE?style=for-the-badge)](LICENSE)
[![Min SDK](https://img.shields.io/badge/Min_SDK-26_(Android_8.0)-00F0FF?style=for-the-badge&logo=android&logoColor=white)](https://developer.android.com/about/versions/oreo)

<br/>

> *"In a world where data is power — guard yours."*

</div>

---

## 〔 WHAT IS PRIVGUARD? 〕

**PrivGuard** is a sleek, cyberpunk-themed Android encryption app that lets you lock and unlock any text using **AES-128-CBC** — one of the most widely trusted encryption standards in the world. No accounts. No cloud. No tracking. Just pure, local encryption on your device.

Built entirely with **Kotlin** and **Jetpack Compose**, it's fast, minimal, and ruthlessly clean.

---

## 〔 FEATURES 〕

| Feature | Details |
|--------|---------|
| 🔒 **Encrypt** | Convert any plain text into an AES-128 encrypted secret code |
| 🔓 **Decrypt** | Reverse any encrypted code back to its original message |
| 🌙 **Dark / Light Mode** | Cyberpunk neon dark theme + clean electric light theme |
| 📋 **Copy to Clipboard** | One-tap copy of encrypted or decrypted output |
| ⚡ **Instant Processing** | Real-time encryption with zero delay |
| 🛡️ **100% Offline** | No internet required. No data leaves your device |
| 🎨 **Cyberpunk UI** | Neon glows, gradient surfaces, monospace output — built different |

---

## 〔 TECH STACK 〕

```
┌─────────────────────────────────────────────────────────┐
│                     PRIVGUARD STACK                     │
├──────────────────────┬──────────────────────────────────┤
│  Language            │  Kotlin 2.0.21                   │
│  UI Framework        │  Jetpack Compose (BOM 2024.12)   │
│  Architecture        │  MVVM + ViewModel                │
│  Encryption          │  AES-128 / CBC / PKCS5Padding    │
│  Crypto Library      │  javax.crypto (Android built-in) │
│  Encoding            │  Base64                          │
│  Min SDK             │  26 (Android 8.0 Oreo)           │
│  Target SDK          │  35 (Android 15)                 │
│  Build System        │  Gradle with Version Catalogs    │
└──────────────────────┴──────────────────────────────────┘
```

---

## 〔 PROJECT STRUCTURE 〕

```
PrivGuard/
├── app/src/main/
│   ├── java/com/privguard/app/
│   │   ├── MainActivity.kt              # Entry point, theme state
│   │   ├── crypto/
│   │   │   └── EncryptionManager.kt     # AES-128/CBC encrypt & decrypt
│   │   └── ui/
│   │       ├── screens/
│   │       │   └── HomeScreen.kt        # Main UI — all composables
│   │       ├── theme/
│   │       │   ├── Color.kt             # Cyberpunk color palette
│   │       │   └── Theme.kt             # Dark/light theme config
│   │       └── viewmodel/
│   │           └── CryptoViewModel.kt   # State + business logic
│   ├── AndroidManifest.xml
│   └── res/                             # Icons, strings, themes
└── gradle/
    └── libs.versions.toml               # Version catalog
```

---

## 〔 ARCHITECTURE 〕

PrivGuard follows **MVVM (Model-View-ViewModel)** — clean separation of concerns:

```
┌─────────────┐     state      ┌──────────────────┐     logic     ┌───────────────────┐
│  HomeScreen │ ◄────────────► │  CryptoViewModel │ ────────────► │ EncryptionManager │
│  (Compose)  │   user events  │   (ViewModel)    │               │  (AES-128/CBC)    │
└─────────────┘                └──────────────────┘               └───────────────────┘
```

- **HomeScreen** → Pure UI, observes ViewModel state
- **CryptoViewModel** → Holds input/output/mode state, handles clipboard
- **EncryptionManager** → Stateless singleton, handles all crypto operations

---

## 〔 COLOR PALETTE 〕

```
DARK MODE (Cyberpunk Neon)          LIGHT MODE (Electric)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━      ━━━━━━━━━━━━━━━━━━━━━━━━━
Background  #050505  ████           Background  #F0F4F8  ████
Surface     #0A0A0F  ████           Surface     #FFFFFF  ████
Neon Blue   #00F0FF  ████           Electric    #0066CC  ████
Neon Purple #BC13FE  ████           Cyan        #00B4D8  ████
Neon Pink   #FF006E  ████           Dark Text   #0A0A0F  ████
```

---

## 〔 GETTING STARTED 〕

### Prerequisites
- Android Studio **Hedgehog** or later
- JDK 11+
- Android device / emulator running **API 26+**

### Clone & Run

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/PrivGuard.git

# Open in Android Studio
File → Open → select the PrivGuard folder

# Run on device or emulator
Shift + F10  (or hit the ▶ Play button)
```

### Build APK

```bash
# Debug APK
./gradlew assembleDebug

# Output location
app/build/outputs/apk/debug/app-debug.apk
```

---

## 〔 HOW IT WORKS 〕

```
YOUR MESSAGE                          ENCRYPTED OUTPUT
────────────                          ────────────────
"Hello World"  ──► AES-128-CBC ──►  "rBxK9mZ2+Lp...=="
                   (encrypt)

"rBxK9mZ2+Lp...=="  ──► AES-128-CBC ──►  "Hello World"
                         (decrypt)
```

**Algorithm:** AES (Advanced Encryption Standard)  
**Mode:** CBC (Cipher Block Chaining)  
**Padding:** PKCS5  
**Encoding:** Base64 (for safe text transport)

---

## 〔 DEPENDENCIES 〕

```toml
[versions]
kotlin                   = "2.0.21"
compose-bom              = "2024.12.01"
lifecycle-viewmodel      = "2.8.7"
core-ktx                 = "1.15.0"
activity-compose         = "1.9.3"
material-icons-extended  = "1.7.6"
```

---

## 〔 ROADMAP 〕

- [ ] 🔑 Custom key input by user
- [ ] 📁 File encryption support
- [ ] 🔐 Biometric lock for the app
- [ ] 🌐 AES-256 mode toggle
- [ ] 📤 Share encrypted output directly
- [ ] 🎨 More cyberpunk themes (red neon, green matrix)

---

## 〔 CONTRIBUTING 〕

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

```bash
# Fork → Clone → Branch → Code → Push → PR
git checkout -b feature/your-feature-name
git commit -m "feat: add your feature"
git push origin feature/your-feature-name
```

---

## 〔 LICENSE 〕

```
MIT License — use it, fork it, build on it.
Just don't remove the credits. ⚡
```

---

<div align="center">

```
⚡ DEVELOPED BY RAKIB · JASHORE, BANGLADESH ⚡
```

[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github)](https://github.com/mr-10)

*Built with 🖤 and a lot of neon.*

</div>
