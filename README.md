The ESP8266 Wi-Fi Deauthentication Project is an open-source initiative that repurposes the ESP8266 microcontroller to perform deauthentication attacks on
802.11 wireless networks. By exploiting the unprotected nature of Wi-Fi management frames, particularly deauthentication frames, the device can send forged packets to disconnect clients from their access points. This functionality is facilitated through a user-friendly web interface hosted directly on the ESP8266, eliminating the need for additional software.

Beyond deauthentication, the firmware also supports beacon flooding and probe request attacks, enabling users to simulate multiple fake networks and mimic client devices searching for networks. These features are accessible via a web interface hosted on the ESP8266, eliminating the need for additional software.

 __Main Aim:__
The primary objective of this project is to serve as an educational tool, demonstrating the vulnerabilities inherent in the Wi-Fi protocol and emphasizing the importance of implementing security measures such as Protected Management Frames (PMF). While the project provides a practical demonstration of these vulnerabilities, it is crucial to note that it is intended solely for authorized testing and educational purposes. Unauthorized use on networks without explicit permission is illegal and unethical. Users are encouraged to utilize this tool responsibly to understand network vulnerabilities and advocate for stronger security measures in wireless communications.

## 🔧 Install Dependencies

# ⚙️ ESP8266 Deauther Setup Guide

This guide walks you through installing necessary tools, downloading firmware, and using the ESP8266 Deauther.

---

## 🔧 Step 1: Install Required Packages

```
sudo apt install python3-pip git unzip
```

## Step 2: Install esptool (Recommended in Virtual Environment)
# Create and activate a virtual environment
```python3 -m venv espenv ```
Activate it:
```
source espenv/bin/activate
```

# Install esptool
```
pip install esptool
```
Using a virtual environment like espenv helps manage the ESP8266/ESP32 toolchain without polluting your system. It avoids the need to manually configure environment variables like PATH, ESPPORT, and ESPTOOL each time.
## Step 3: Download Deauther Firmware
Go to the official repository:

🔗 https://github.com/SpacehuhnTech/esp8266_deauther

Navigate to the Releases section.

Download the appropriate .bin file for your board.

Example:

text
Copy
Edit
```
ESP8266_DEAUTHER-1.6.5-NodeMCU.bin
```
📡 Step 4: Connect and Use the Deauther
Flash the downloaded .bin file to your ESP8266 using esptool.py:

```
esptool.py --port /dev/ttyUSB0 write_flash 0x00000 ESP8266_DEAUTHER-1.6.5-NodeMCU.bin
```
Unplug and replug the ESP8266 board.

A new Wi-Fi access point will appear, usually named pwned or Deauther.

Connect to that Wi-Fi network from another device (phone/laptop).

Open a browser and go to:

```
http://192.168.4.1
```
Use the web interface to:

🔍 Scan for networks

🎯 Select a target

💥 Start Deauth, Beacon spam, or Probe attack

🧠 Note: This tool is meant for educational and authorized testing only. Unauthorized use on other networks is illegal.












