<!DOCTYPE html>
<html lang="en">
<body>

<h1>🔒 RFID Access Control System</h1>
<p><span class="badge">Technology: RFID</span> <span class="badge">License: MIT</span></p>

<h2 id="overview">📌 Overview</h2>
<p>This project implements an <strong>RFID-based access control system</strong> using an ESP8266 and RFID reader modules. It allows authorized users to unlock doors or access secure areas by scanning RFID tags/cards.</p>

<h2 id="team">👨‍💻 Team</h2>
<ul>
  <li><strong>Team Name:</strong> Team Pioneer</li>
  <li><strong>Lead:</strong> Siddhesh Godage</li>
  <li><strong>Programming:</strong> Om Joshi, Siddhesh Godage</li>
  <li><strong>Electronics:</strong> Aveek Ganguly, Siddhesh Godage</li>
  <li><strong>Designed by:</strong> Avinash Malusare, Shubham Jaiswal</li>
  <li><strong>This Repo Created By:</strong> Siddhesh Bhole</li></ul>
    
<h2 id="features">✨ Features</h2>
<ul>
  <li>🔑 Authenticate users via RFID tags</li>
  <li>📀 Log access events to Google Sheets</li>
  <li>📲 Receive SMS notifications (SIM800L)</li>
  <li>📟 Display feedback on 16x2 LCD (I2C)</li>
  <li>🔔 Piezo buzzer feedback</li>
</ul>

<h2 id="system-architecture">🧠 System Architecture</h2>
<div class="code">
[RFID Reader] ---> [ESP8266] ---> [Lock Control]<br>
                         |<br>
                         +--> [LCD, SIM800L, Google Sheets]
</div>

<h2 id="hardware-requirements">🔩 Hardware Requirements</h2>
<ul>
  <li>📶 PN532 RFID module (UART mode)</li>
  <li>📡 ESP8266 board (NodeMCU or Wemos D1 Mini)</li>
  <li>🔊 Piezo buzzer</li>
  <li>📟 LCD 16x2 with I2C module</li>
  <li>📲 SIM800L GSM Module</li>
</ul>

<h2 id="software-requirements">💻 Software Requirements</h2>
<ul>
  <li>Arduino IDE or PlatformIO</li>
  <li>ESP8266 Board JSON URL:<br> <code>http://arduino.esp8266.com/stable/package_esp8266com_index.json</code></li>
</ul>

<h2 id="libraries-included">📚 Libraries Included</h2>
<ul>
  <li><strong>ESP8266 Arduino Core</strong> - <code>ESP8266WiFi</code>, <code>SoftwareSerial</code>, <a href="https://github.com/esp8266/Arduino">GitHub</a></li>
  <li><strong>Adafruit PN532</strong> - <code>PN532_SWHSU</code>, <a href="https://github.com/adafruit/Adafruit-PN532">GitHub</a></li>
  <li><strong>LiquidCrystal_I2C</strong> - <code>LiquidCrystal_I2C</code>, <a href="https://github.com/marcoschwartz/LiquidCrystal_I2C">GitHub</a></li>
  <li><strong>ArduinoJson</strong> (v6) - <code>deserializeJson()</code>, <a href="https://github.com/bblanchon/ArduinoJson">GitHub</a></li>
</ul>

<h2 id="installation">🛠️ Installation</h2>

<h3>🔌 Hardware Setup</h3>
<ul>
  <li>Connect all components as shown in the wiring diagram.</li>
  <li>Ensure proper voltage levels for PN532 and SIM800L.</li>
  <li>Use the document provided here: <a href="<link-to-instructions>">Wiring Instructions</a></li>
</ul>

<h3>💻 Software Setup</h3>
<ul>
  <li>Follow the instructions in this <a href="<link-to-google-sheet>">Setup Guide</a>.</li>
  <li>Install the required libraries via Library Manager.</li>
  <li>Configure <code>WiFi</code>, <code>SIM800L</code>, and hardware pins in <code>config.json</code>.</li>
  <li>Upload the code to your ESP8266 using Arduino IDE.</li>
</ul>

<h3>🧪 Testing</h3>
<ul>
  <li>Power up the circuit.</li>
  <li>Scan an RFID card. LCD should show details.</li>
  <li>You’ll hear a beep and receive an SMS if set up.</li>
  <li>If something doesn’t work, recheck wiring or script settings.</li>
</ul>

<h2 id="usage">📦 Usage</h2>
<ul>
  <li>Open the Arduino IDE and flash your board.</li>
  <li>Tap an RFID tag to authenticate.</li>
  <li>System will handle display, logging, and alert automatically.</li>
</ul>

<h2 id="configuration">⚙️ Configuration</h2>
<p>Edit <code>config.json</code> with your credentials and settings.</p>
<div class="code">
{<br>
&nbsp;&nbsp;"wifi_ssid": "yourSSID",<br>
&nbsp;&nbsp;"wifi_pass": "yourPASS",<br>
&nbsp;&nbsp;"gsm_number": "+91XXXXXXXXXX",<br>
&nbsp;&nbsp;"lcd_address": "0x27"<br>
}
</div>

<h2 id="contributing">🤝 Contributing</h2>
<p>Feel free to fork this repo, report bugs, and create pull requests.</p>

<h2 id="license">📄 License</h2>
<p>This project is licensed under the MIT License. See the <code>LICENSE</code> file for more details.</p>

<h2 id="contact">📬 Contact</h2>
<p>Made with ❤️ by <strong>Team Pioneer</strong>. Reach out via GitHub issues or email Siddhesh Godage for support.</p>

</body>
</html>
