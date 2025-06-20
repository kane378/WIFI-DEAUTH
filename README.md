The ESP8266 Wi-Fi Deauthentication Project is an open-source initiative that repurposes the ESP8266 microcontroller to perform deauthentication attacks on
802.11 wireless networks. By exploiting the unprotected nature of Wi-Fi management frames, particularly deauthentication frames, the device can send forged packets to disconnect clients from their access points. This functionality is facilitated through a user-friendly web interface hosted directly on the ESP8266, eliminating the need for additional software.

Beyond deauthentication, the firmware also supports beacon flooding and probe request attacks, enabling users to simulate multiple fake networks and mimic client devices searching for networks. These features are accessible via a web interface hosted on the ESP8266, eliminating the need for additional software.

 Main Aim:
The primary objective of this project is to serve as an educational tool, demonstrating the vulnerabilities inherent in the Wi-Fi protocol and emphasizing the importance of implementing security measures such as Protected Management Frames (PMF). While the project provides a practical demonstration of these vulnerabilities, it is crucial to note that it is intended solely for authorized testing and educational purposes. Unauthorized use on networks without explicit permission is illegal and unethical. Users are encouraged to utilize this tool responsibly to understand network vulnerabilities and advocate for stronger security measures in wireless communications.

steps to be followed:

1)sudo apt install python3-pip git unzip 
2)pip3 install esptool(for this tool to work we need to work with virtual environment)
By adding espenv, you are automating the configuration process for the ESP8266/ESP32 environment, so you don’t have to manually set environment variables like PATH, ESPPORT, ESPTOOL, etc., each time you work with the microcontroller. It helps make the development process more seamles            
3) Download deauther firmware
   https://github.com/SpacehuhnTech/esp8266_deauther
   Download the .bin file for your board,
   for example: ESP8266_DEAUTHER-1.6.5-NodeMCU.bin
   
4)Connect and Use the Deauther
Unplug and replug the ESP8266.
It will create a Wi-Fi access point, usually called pwned or Deauther. Connect to it from another device (phone/laptop).
Open a browser and go to: http://192.168.4.1
Use the interface to:
Scan for networks Select a target
Start Deauth, Beacon spam, or Probe attack
