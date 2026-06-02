# 🚀 Premium Flutter SaaS Boilerplate

A production-ready Flutter starter kit designed to save you 40+ hours of tedious setup. Launch your next cross-platform SaaS, B2B app, or startup this weekend.

## 🛠 Tech Stack
* **Framework:** Flutter 3.x
* **State Management:** Riverpod 2.x
* **Routing:** GoRouter (Deep-link ready & Auth Guarded)
* **Backend:** Firebase (Core & Authentication)

## ✨ Features Out-of-the-Box
* 🔒 **Complete Authentication Flow:** Login, Registration, and automatic Session Persistence.
* 🛡️ **Protected Routing:** Unauthenticated users are automatically kicked to the login screen. Logged-in users are routed straight to the dashboard.
* 📱 **Responsive Dashboard Shell:** A clean, responsive grid layout ready for your metrics and features.
* 🏗️ **Enterprise Architecture:** A clean, feature-first folder structure built for massive scalability.

---

## 🚀 Quick Start Guide

### 1. Install Dependencies
Make sure you are in the project root, then run:
```bash
flutter clean
flutter pub get
```

### 2. Connect Your Firebase Project
We use the official FlutterFire CLI for a seamless, secure setup. Do not manually move JSON files.
```bash
# 1. Log into your Google account
firebase login

# 2. Activate the CLI tools
dart pub global activate flutterfire_cli

# 3. Link your Firebase project (Select Android & iOS)
flutterfire configure
```
***Crucial:** Go to your Firebase Console -> Authentication -> Sign-in Method, and enable **Email/Password**.*

### 3. Launch
```bash
flutter run
```

---

## 📂 Architecture Overview
We use a feature-first modular structure to keep your codebase clean as it scales:
* `/lib/core/` - Routing (`routes.dart`), themes, and global constants.
* `/lib/features/` - Isolated feature modules (e.g., `auth`, `home`).
* `/lib/services/` - 3rd-party integrations and API repositories.
* `/lib/shared/` - Reusable UI components (buttons, text fields, cards).

## 🎨 Customizing Your Brand
To change the primary color and branding, open `lib/main.dart` and modify the `ThemeData` block:
```dart
theme: ThemeData(
  // Change Colors.deepPurple to your brand's primary color:
  colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple), 
  useMaterial3: true,
),
```