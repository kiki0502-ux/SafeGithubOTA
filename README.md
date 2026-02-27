# 📡 SafeGithubOTA - Secure ESP32 Firmware Updates Easily

[![Download Releases](https://img.shields.io/badge/Download-SafeGithubOTA-blue?style=for-the-badge)](https://github.com/kiki0502-ux/SafeGithubOTA/releases)

---

SafeGithubOTA is a tool designed to update firmware on ESP32 devices safely and easily. You do not need to be a programmer or have technical skills to use it. This guide will help you download and run the software step-by-step.

---

## 📖 What is SafeGithubOTA?

SafeGithubOTA is an Arduino library that allows your ESP32 device to update its firmware over the air (OTA). It connects to private GitHub repositories to get the latest updates. It includes important protections so your device stays safe and works correctly after each update.

Key points:

- Works with ESP32 microcontroller devices  
- Supports private GitHub repositories  
- Protects against faulty firmware with rollback safety  
- Lets you set up updates easily using a local Wi-Fi portal  
- Compares version numbers clearly before updating  
- No need for any extra external software  
- Supports ESP32 and its variants like ESP32-C3 and ESP32-S3  

You can think of SafeGithubOTA as a way to keep your ESP32 device’s software fresh and secure without needing to plug it into your computer. Everything happens through Wi-Fi, and updates come from your private GitHub projects.

---

## 🖥️ System Requirements

Before you start, make sure your system meets these requirements:

- A computer running Windows 10 or later, MacOS, or Linux.  
- An ESP32 device connected to your network.  
- Stable Wi-Fi connection for both your ESP32 device and your computer.  
- A web browser like Chrome, Firefox, Safari, or Edge.  
- Access to the internet to connect to GitHub for firmware updates.  
- Arduino IDE or PlatformIO installed if you plan to customize or upload firmware yourself. (Not required just to run the update process.)

---

## 🚀 Getting Started

This section walks you through the steps of downloading and running SafeGithubOTA on your ESP32 device. You don’t have to write code or handle complex setups. Just follow each step carefully.

### Step 1: Download SafeGithubOTA

To download the software package, click the big blue button below. It will take you to the GitHub release page for SafeGithubOTA:

[![Download SafeGithubOTA](https://img.shields.io/badge/Download-SafeGithubOTA-blue?style=for-the-badge)](https://github.com/kiki0502-ux/SafeGithubOTA/releases)

On the release page, locate the latest release version. You will find download files such as firmware images and installation instructions.

### Step 2: Prepare Your ESP32 Device

1. Make sure your ESP32 device is powered and connected to your Wi-Fi network.  
2. If your device is new or has never been set up for OTA updates, perform an initial setup using the Arduino IDE or PlatformIO. This may require loading the SafeGithubOTA library onto your device following instructions in the project documents on GitHub.  
3. Connect your computer and ESP32 to the same Wi-Fi network to allow communication.

### Step 3: Access the Captive Portal

SafeGithubOTA includes a captive portal – a kind of small web page hosted by your ESP32. This portal will help you configure and start updates.

- On your device’s Wi-Fi, look for a new network named something like `SafeGithubOTA_Setup`.  
- Connect to this Wi-Fi network from your computer or smartphone.  
- A web browser should open automatically to the captive portal page. If not, open a browser and enter the IP address `192.168.4.1`.

### Step 4: Configure GitHub Access

On the captive portal page, enter your private GitHub repository details so the device can check for firmware updates.

- You will need your GitHub username and a personal access token (PAT) with permission to read private repositories. You can generate a PAT on GitHub under your account settings.  
- Enter the repository name exactly.  
- Submit the details on the portal.

### Step 5: Initiate the Firmware Update

Once configured, SafeGithubOTA will compare the currently installed firmware version with the version stored in your GitHub repository. If a newer version exists, the device will download and apply the update automatically.

The system protects your device with rollback safety, so if an update fails, your ESP32 will keep running the last stable version. You will see progress and status messages on the captive portal page.

---

## 💾 Download & Install

You can visit the SafeGithubOTA release page here:

[Download SafeGithubOTA Releases](https://github.com/kiki0502-ux/SafeGithubOTA/releases)

From this page:

- Find the latest stable release version.  
- Download the version files compatible with your device variant (ESP32, ESP32-C3, or ESP32-S3).  
- Read any included notes or installation instructions.  

If you are not familiar with uploading firmware using Arduino IDE or PlatformIO, the project README on GitHub has guides on how to load the initial library onto your device.

---

## 🔧 How It Works

SafeGithubOTA updates your ESP32 devices wirelessly by checking for new firmware files in your GitHub private repository.

1. Your device contacts your GitHub repo using the access token you set.  
2. It compares the version of installed firmware to the semver tags in GitHub releases.  
3. If there is a newer version, it downloads the update in the background.  
4. The device installs the update and restarts on the new firmware.  
5. If anything goes wrong, the device rolls back to the last safe version automatically.

This means you don’t have to physically connect your device to a computer or manually download updates every time. You maintain control through your private code repository on GitHub.

---

## 📡 Features

- Over-the-air updates with no physical connection.  
- Secure access to private GitHub repositories using personal access tokens.  
- Captive portal for simple provisioning and configuration.  
- Rollback protection ensures device stability after failed updates.  
- Semantic versioning (semver) helps system pick the correct update.  
- Lightweight with zero external dependencies—runs fully on your ESP32.  
- Supports multiple ESP32 models including ESP32-C3 and ESP32-S3 variants.  

---

## 🔍 Troubleshooting

If you run into trouble, try these steps:

- Confirm ESP32 and your computer are on the same Wi-Fi network.  
- If captive portal does not appear, reconnect to the device network and try again.  
- Double-check your GitHub personal access token is valid and has correct permissions.  
- Verify the repository name and paths are typed correctly in the portal.  
- Restart your ESP32 device and try the update process again.  
- Consult the project documentation or open an issue on the GitHub page for support.

---

## 🌐 Supported Devices

- ESP32 (Standard models)  
- ESP32-C3  
- ESP32-S3

All these variants are supported by SafeGithubOTA with the same update and protection mechanisms.

---

## 📁 Repository Topics

This project relates to these areas:

arduino, arduino-library, captive-portal, embedded, esp-idf, esp32, esp32-arduino, esp32-c3, esp32-s3, firmware-update, github-releases, iot, ota, ota-updates, over-the-air, platformio, private-repo, rollback, semver, wifi

---

## 📞 Contact & Support

For more information, visit the GitHub repository:

https://github.com/kiki0502-ux/SafeGithubOTA

If you find issues or want to request help, you can open a GitHub issue there.

---

Thank you for using SafeGithubOTA to keep your ESP32 device secure and up to date.