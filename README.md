##Home Assistant 2021.9.6

So this is my config as of now, most likely updated from time to time.


**Docker:** (This changes rather often so I limit it to HA relevant containers)
  - homeassistant/home-assistant
  - portainer/portainer
  - pyouroboros/ouroboros
  - eclipse-mosquitto
  - linuxserver/letsencrypt
  - linuxserver/duplicati
  - linuxserver/mariadb
  - nodered


**Monitoring:**
  - Netdata
  - CheckMK
  - OpsGenie
  - NewRelic


External reachable! I use the Fail2Ban from Host (protecting SSH) to also read the HASS Logs. 

Official SSL certificates from Linuxserver letsencrypt. Now with static IP, paid Domain and secured with Cloudflare as well.

Don't forget Duplicati to make regular Backups, I keep all backups on my unlimited Cloud so no need to remove older backups.


**Devices:**
  - FritzBox 7583 (Yet only as a dumb-made modem, without WIFI or any other feature turned on. Only static routes to my Unifi Network.
  - Unifi UDM Pro
  - Unifi NanoHD AP
  - Seagate Backup Plus Hub 8TB connected to the Deskmini
  - Conbee II stick connected to the Deskmini for Zigbee
  - Some Bluetooth stick connected to the Deskmini for room-assistant
  - 2 Yeelights *(2 2. Gen)*
  - 1 Ikea Tradfri E27 bulb 1000lm
  - 1 frient Motion Sensor Pro
  - 4 Blitzwolf BW-SHP13 (more are on the way)
  - Xiaomi Airpurifier Pro
  - Xiaomi Airpurifier 2S
  - Xiaomi Roborock S50
  - LG OLED 55C8
  - Nvidia Sield
  - Xbox Series X
  - FireTV Cube
  - 1 Echo Dot V3
  - 2 PC's
  - 1 Xiaomi Humidity Sensor
  - 3 Xiaomi Door- / Window-Sensor
  - Tradfri 30W Driver @ 11x Ledberg Spots (Zigbee)
  - Medion Alexa WiFi Radio
  - 2 Raspberry Zero W with room-assistant


**Integrations:**
  - Moved from Deconz to ZHA
  - Moved from external ADB to internal
  - room-assistant
  - Alexa Smarthome
  - Energy (With the Blitzwolf smart plugs)
  - MQTT
  - HACS
  - NodeRed
  - Telegram


**ToDo:**
  - Further integrations
  - Better automations
  - Scripts
  - Extend Alexa functionality

