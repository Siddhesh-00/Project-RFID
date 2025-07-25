# 🔒 RFID Access Control System (Google Sheets Edition)

This repository contains the firmware and setup instructions for an RFID access control system that uses **Google Sheets** as its backend database. This method is easy to set up and is ideal for small-scale projects, demonstrations, or personal use.

---

## ✨ Features
* 🔑 Authenticate users via RFID tags against a Google Sheet.
* 📝 Log all access attempts directly into the spreadsheet.
* 📲 Receive SMS notifications upon successful scan (using SIM800L).
* 📟 Display user feedback on a 16x2 I2C LCD.
* 🔔 Provide audible feedback with a Piezo buzzer.

---

## 🔩 Hardware & 🔌 Connections
The following hardware is required for this project.

#### Required Components:
* PN532 RFID module
* ESP8266 board (NodeMCU or similar)
* Piezo buzzer
* LCD 16x2 with I2C module
* SIM800L GSM Module

➡️ For detailed instructions on how to wire the components together, please refer to our comprehensive **[Wiring Diagram](https://github.com/YOUR_USERNAME/YOUR_REPO/wiki/Wiring-Diagram)**.

---

## 💻 Software & Setup
To get the system running, you'll need to set up Google Sheets, create a Google Apps Script, and configure the Arduino code.

### 1. Google Sheet Setup
1.  Create a new Google Sheet.
2.  Set up two tabs: one named `students` and another named `attendance_logs`.
3.  The `students` sheet should have columns like: `uid`, `name`, `dept`, `year`, `roll_no`, `parent_number`.
4.  The `attendance_logs` sheet should have columns like: `timestamp`, `uid`, `name`, `roll_no`.

### 2. Google Apps Script
1.  In your Google Sheet, go to **Extensions > Apps Script**.
2.  Download the `google-apps-script.gs` file from the [**Releases Page**](https://github.com/YOUR_USERNAME/YOUR_REPO/releases) and paste its content into the script editor.
3.  Deploy the script as a **Web app**.
4.  Set access to **"Anyone"** (or "Anyone, even anonymous").
5.  Copy the generated **Web app URL**. You will need this for the Arduino code.

### 3. Arduino IDE
1.  Install the required libraries: `ESP8266WiFi`, `ESP8266HTTPClient`, `LiquidCrystal_I2C`, `PN532`, and `ArduinoJson`.
2.  Download the latest source code `.zip` from the project's [**Releases Page**](https://github.com/YOUR_USERNAME/YOUR_REPO/releases).
3.  Unzip the file and open the `.ino` sketch in the Arduino IDE.
4.  Update the placeholder values for your WiFi SSID, password, and the Google Apps Script URL you copied earlier.
5.  Upload the code to your ESP8266.

