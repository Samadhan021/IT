# IT DEPARTMENT CRM (Flutter)

This is a ready-to-commit Flutter project scaffold for **IT DEPARTMENT CRM**.

## What's included
- pubspec.yaml
- lib/main.dart (Dashboard + Tickets + Assets + Inventory)
- .github/workflows/build-apk.yml (CI workflow builds APK and uploads artifact)

> Note: The project ZIP intentionally excludes platform folders (android/, ios/) to keep size small. The GitHub Actions workflow will run `flutter create .` before building so the CI can generate android/ios on the runner.

## How to build (locally)
1. Install Flutter & Android SDK.
2. Unzip this project and run `flutter pub get`.
3. Run `flutter run` to test on a device or emulator.
4. Build release APK: `flutter build apk --release`.

## How to build using GitHub Actions (cloud)
1. Create a new GitHub repository and push the contents of this folder to the `main` branch.
2. The included workflow `.github/workflows/build-apk.yml` triggers on push to main and on manual dispatch.
3. After the workflow finishes, download the artifact `it-department-crm-apks` from the Actions run page.

## Change package id
I used `com.itdept.crm` as the default application id. To change, edit `android/app/build.gradle` once the android/ folder exists (or after `flutter create .`) and replace `applicationId`.