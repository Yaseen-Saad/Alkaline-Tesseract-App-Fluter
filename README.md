# CO₂ Monitor

**CO₂ Monitor** is a Flutter-based mobile and web application designed to track CO₂ concentrations, helping to assess the efficiency of an air purifier. The project connects with a Raspberry Pi Pico, which serves as an IoT device for real-time CO₂ data collection, transmitting data to the app for monitoring and visualization.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Connecting with Raspberry Pi Pico](#connecting-with-raspberry-pi-pico)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [License](#license)

## Overview
This project is designed to track indoor air quality by measuring CO₂ concentration levels over time. The collected data is displayed through the Flutter app interface, providing insights into the effectiveness of an air purifier. The integration with Firebase allows for real-time updates, and the data is visualized using line charts.

## Features
- **User Authentication:** Simple login interface to enter or scan a username using QR.
- **Real-Time CO₂ Monitoring:** Displays the current CO₂ concentration.
- **Historical Data Visualization:** Line chart showing CO₂ levels over time.
- **Filtering Options:** Toggle filtering options to exclude low CO₂ values.
- **Settings Screen:** Configurations for user preferences.
- **Web and Mobile Compatibility:** Runs as a Flutter web app and mobile app.
- **Firebase Integration:** Uses Firestore for real-time data updates.

## Installation

### Prerequisites
- Flutter SDK (latest stable version)
- Firebase account with Firestore enabled
- Raspberry Pi Pico (for CO₂ sensor data collection)
- CO₂ Sensor compatible with Raspberry Pi Pico
- [Syncfusion Flutter Charts](https://pub.dev/packages/syncfusion_flutter_charts) license (for chart visualization)

### Steps
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
   cd YOUR_REPOSITORY
   ```
2. **Install Dependencies:** Run the following command in the project root to install necessary packages:

```bash
flutter pub get
```
3. **Set Up Firebase:**

Register your app on Firebase.
Add google-services.json for Android and GoogleService-Info.plist for iOS.
Copy Firebase configuration details into main.dart in the FirebaseOptions setup.
Run the App: For web:

```bash
flutter run -d chrome
```
For mobile:

```bash
flutter run
```
- Configuration
    - Firebase:
Ensure that Firebase Firestore is set up to receive real-time CO₂ data from the Raspberry Pi Pico. Use Firebase Firestore for storing CO₂ readings with timestamps.

Raspberry Pi Pico CO₂ Sensor Connection
Connect the CO₂ sensor to the Raspberry Pi Pico.
Use the Raspberry Pi Pico to capture CO₂ levels, sending readings to Firebase Firestore via Wi-Fi or a connected computer.
Refer to this tutorial for configuring the CO₂ sensor with Raspberry Pi Pico and pushing data to Firebase