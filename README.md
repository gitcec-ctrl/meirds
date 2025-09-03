# Tuition App Full (Offline - Flutter + SQLite + PDF + Export)

This upgraded project includes:
- Student admission (add/edit/delete)
- Fee Plans (create/delete)
- Payment entry -> Invoice created
- PDF receipt generator (saved to app documents)
- Export all data to CSV
- GitHub Actions workflow to build APK (see .github/workflows)

## How to run locally
1. Install Flutter & Android SDK.
2. From project root:
   ```bash
   flutter pub get
   flutter run
   ```

## Generate release APK locally
1. Create keystore using keytool (see earlier instructions).
2. Add `android/key.properties` with passwords and path.
3. Build:
   ```bash
   flutter build apk --release
   ```
4. APK: `build/app/outputs/flutter-apk/app-release.apk`

## CI (GitHub Actions)
- Push repo to GitHub and create secrets for keystore (if signing).
- The workflow `.github/workflows/flutter-build.yml` will build and upload the APK artifact.

## Notes
- This is a starter full feature app. You can expand reports, backup UI, and add more validations.
- PDF receipts are generated in app document folder (see receipt_generator.dart).
