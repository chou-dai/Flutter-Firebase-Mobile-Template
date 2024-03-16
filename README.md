# Flutter Firebase Mobile Template
Template for developing mobile applications with Flutter and Firebase.

This flutter project is cloned from https://github.com/mitesh77/Best-Flutter-UI-Templates

## Feature
- Firebase Emulator and Flutter connection (local development)
- Code format for pre-commit

## Required
- Xcode（iOS emulator）
    - Check if iOS emulator is available.
        ```
        flutter emulators
        ```
        > apple_ios_simulator • iOS Simulator   • Apple  • ios

## Setup
- Create `.firebaserc` by cpying `./firebase.sample` in the `./firebase`, and fill in the firebase project name.
- Build Docker Compose
    ```
    docker compose build
    ```
- Login to GCP：Execute the following command to log in with your google account.
    ```
    docker compose run --rm firebase firebase login --no-localhost
    ```
- Starting up Firebase Emulator server
    ```
    docker compose up
    ```
    Firebase Emulator：http://localhost:4000
- Starting up Flutter Emulator
    ```
    cd flutter
    ```
    vscode > execution > Start Debugging > Start iOS Simulator

## Setup（project manager）
- Create Firebase Project
    - Fireabase Authentication
    - Firestore
    - storage 


## Appendix
- Dart Format command
    ```
    dart format
    ```