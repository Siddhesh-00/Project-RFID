# 🔒 RFID Access Control System

  

## 📌 Overview

This master repository is the central hub for an RFID-based access control system built with the ESP8266. It provides two distinct data logging implementations (Google Sheets and Firebase), allowing authorized users to gain access by scanning registered RFID tags/cards.

-----

## 👨‍💻 Team

  * **Team Name:** Team Pioneer
  * **Lead:** Siddhesh Godage
  * **Programming:** Om Joshi, Siddhesh Godage
  * **Electronics:** Aveek Ganguly, Siddhesh Godage
  * **Designed by:** Avinash Malusare, Shubham Jaiswal
  * **Repository & Documentation:** Siddhesh Bhole

-----

## ✨ Core Features

  * 🔑 Authenticate users via RFID tags.
  * 📲 Receive SMS notifications upon successful scan (using SIM800L).
  * 📟 Display user feedback on a 16x2 I2C LCD.
  * 🔔 Provide audible feedback with a Piezo buzzer.
  * 💾 **Choose between two powerful backends for data logging.**

-----

## 🔩 Hardware & 🔌 Connections

The core hardware is consistent across both versions of the project.

#### Required Components:

  * PN532 RFID module
  * ESP8266 board (NodeMCU)
  * Piezo buzzer
  * LCD 16x2 with I2C module
  * SIM800L GSM Module

➡️ For detailed instructions on how to wire the components together, please refer to our comprehensive **[Wiring Diagram](https://www.google.com/search?q=https://github.com/YOUR_USERNAME/YOUR_REPO/wiki/Wiring-Diagram)**.

-----

## 💾 Data Logging Methods

Choose the method that best fits the scale and technical requirements of your project.

### Method 1: Google Sheets (Easy Integration)

Uses Google Sheets as a lightweight database. Perfect for getting started quickly or for smaller-scale projects.

  * **Pros:** Easy setup, no cost, data is easily viewable.
  * **Cons:** Higher latency, not ideal for real-time updates.
  * **Best for:** Small-scale operations, personal projects, or quick demos.

➡️ [**View the Google Sheets Version Repository**](https://github.com/Siddhesh-00/Project-RFID/tree/GoogleSheets-Editon?tab=readme-ov-file)

### Method 2: Firebase (Fast & Scalable)

Integrates with Google's Firebase Realtime Database, offering a professional, scalable, and low-latency solution.

  * **Pros:** Extremely fast, highly scalable, robust security.
  * **Cons:** Moderately more complex setup.
  * **Best for:** Larger-scale deployments or projects requiring instant data logging.

➡️ [**View the Firebase Version Repository**](https://github.com/Siddhesh-00/Project-RFID/tree/Firebase-Edition?tab=readme-ov-file)

-----

## 🤝 Contributing

Feel free to fork this master repo or any of the specific implementation repos. Bug reports and pull requests are always welcome\!

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
