# Flutter Firebase Mobile Template
Template for developing mobile applications with Flutter and Firebase.

## Feature
- Firebase Emulator and Flutter connection (local development)
- Code format for pre-commit

## Required
- Xcode（iOS emulator）

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
- Starting up Firebase Emulator server and Flutter server
    ```
    docker compose up
    ```
- Operation check
    - Firebase Emulator：http://localhost:4000
    - Flutter：iOS Emulator

## Setup（project manager）
- Create Firebase Project
    - Fireabase Authentication
    - Firestore
    - storage 
