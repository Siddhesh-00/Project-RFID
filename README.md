# 🔒 RFID Access Control System (Firebase Edition)

This repository contains the firmware and setup instructions for a high-performance RFID access control system that uses **Firebase Realtime Database** as its backend. This method provides a fast, scalable, and low-latency solution suitable for larger projects or applications requiring real-time data synchronization.

---

## ✨ Features
* 🔑 Authenticate users via RFID tags against a secure Firebase database.
* ⚡ Log access events in **real-time**.
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
To get the system running, you'll need to set up a Firebase project and configure the Arduino code.

### 1. Firebase Project Setup
1.  Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
2.  In the project dashboard, go to **Build > Realtime Database**. Create a new database, starting in **test mode** for now.
3.  Go to **Build > Authentication**. Click "Get started" and enable the **Email/Password** sign-in provider.
4.  In the Authentication "Users" tab, add a new user for your device (e.g., `device@example.com` with a strong password).
5.  Go to **Project Settings** (gear icon) and copy your **Web API Key** and **Database URL**.

### 2. Database Structure
In the Realtime Database, you will need to structure your data. A recommended structure is:
```json
{
  "students": {
    "YOUR_CARD_UID_1": {
      "name": "John Doe",
      "dept": "Engineering",
      "roll": "E101",
      "year": "4",
      "parent_number": "+1234567890"
    }
  },
  "attendance_logs": {}
}
