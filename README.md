# Construction Calculator Pakistan - Flutter App

## Run
1. Install Flutter: https://docs.flutter.dev/get-started/install
2. `cd construction_calculator_pk`
3. `flutter pub get`
4. `flutter run`  (connect Android phone with USB debugging or emulator)
5. Build APK: `flutter build apk --release` -> `build/app/outputs/flutter-apk/app-release.apk`

## What's Built (ALL 8 Working ✅)
- Home grid 9 calculators wired - no more "coming soon"
- Concrete: LxWxH feet+inch, 1:2:4/1:1.5:3, PKR cost lakh/crore
- Brick: 4.5"/9" wall, bricks+motor
- Steel/Sariya: 8-25mm, kg/ton/maund
- Plaster: area sqft, 12/15mm, 1:4/1:5/1:6
- Paint: area, 1-3 coats, liters/gallons/drums + cost
- Tiles: room LxW, 12x12/24x12/24x24 +10% wastage
- Excavation: LxWxD cft, trolley trips, mazdoor-days
- Water/Septic Tank: liters, US/UK gallons, m³
- All: city multiplier (7 cities), WhatsApp share, offline

## To Add Next
- Plaster, Paint, Tiles screens (copy concrete pattern, use PakFormulas.plaster/paintLiters/tilesQty)
- PDF generation (add `pdf` package)
- AdMob (add `google_mobile_ads`, add banner in result screens)
- Firebase Remote Config for live rates
- History with shared_preferences (save calculations)
- Urdu localization with easy_localization

## Upload to Play Store
- Package: com.pakbuild.constructioncalculator (set in android/app/build.gradle)
- Version: 1.0.0+1 in pubspec.yaml
- See ../construction-calculator/TECH_STACK.md for ASO checklist

## Test Calculations
Concrete 10x10x0.5 ft, 1:2:4 => ~6.16 bags, 13.4 cft sand, 26.9 cft crush
Brick 20x10 ft, 4.5" => ~1050 bricks
Steel 12mm x 40ft x 4 bars => ~42.67 kg (1.07 maund)

Questions? See formulas in lib/core/utils/formulas.dart
