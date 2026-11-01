# Install on Mobile - 3 Ways (No PC coding needed)

## WAY 1: One-Click Cloud Build (EASIEST - 5 min, NO Flutter install)
1. Create GitHub account (github.com)
2. Create NEW repo: construction-calculator-pk -> Upload this folder (drag & drop zip -> extract)
3. Go to Actions tab -> See "Build APK" running -> Wait 4-5 min (green check)
4. Click Build -> Artifacts -> Download app-release-apk -> Unzip
5. Send app-release.apk to your phone via WhatsApp/Telegram/Google Drive
6. On phone: Open file -> Allow "Install unknown apps" -> Install -> Open!
   APK size ~18 MB, works 100% offline.

## WAY 2: Build on your PC (Windows)
1. Install Flutter: https://docs.flutter.dev/get-started/install/windows
   Extract to C:\flutter, add C:\flutter\bin to Path, restart CMD, run: flutter doctor
2. Install Android Studio -> SDK Manager -> install SDK
3. Enable phone: Settings -> About Phone -> Tap "Build Number" 7 times -> Developer Options -> Enable USB Debugging
4. Connect phone via USB -> Allow debugging popup on phone
5. CMD:
   cd "g:\Niche GPT\construction_calculator_pk"
   flutter pub get
   flutter install  <- installs directly to phone!
   or: flutter build apk --release
   Find APK at: build\app\outputs\flutter-apk\app-release.apk -> copy to phone

## WAY 3: Codemagic (Alternative Cloud)
1. codemagic.io -> Sign up free -> Connect GitHub repo
2. Select Flutter -> Android -> Build -> Download APK

## After Install - Test These:
- Open app -> Home shows 9 tiles with Urdu
- Tap Concrete -> 10 ft x 10 ft x 0.5 ft 1:2:4 -> Calculate -> 6.16 bags
- Tap Steel -> 12mm 40ft x4 -> 42.67 kg / 1.07 maund
- Airplane mode ON -> still works (offline proof)
- Cost Estimator -> PDF -> Share on WhatsApp

Troubleshooting:
- "App not installed": Uninstall old version first
- "Blocked by Play Protect": Tap "Install anyway"
- White screen: Run flutter doctor, ensure Android SDK installed
