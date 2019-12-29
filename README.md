##Home Assistant V0.103.5

So this is my config as of now, most likely updated from time to time.

~This costed me approx. 180 hours of work yet, ~~using an RPI 2b which I had laying around since ages now because I never had a usecase here.
It is using the Raspbian Lite Image~~ without a GUI, pure SSH, Docker Setup.
Changed to Deskmini, Ryzen 5 3400G, 16GB DDR4 3200Mhz CL16 Ram, 500GB NVMe SSD x2, Debian 10.

This config is still pretty small, not having much integrations, devices, automations and functions. Don't consider it as the holy grail since I'm pretty new. 
I didn't even use consistent syntax. God damn. 

Also some things still throw errors which may or may not affect the function.

**NOT WORKING:**
  - ~~ADB seems to be unreliable yet, devices become unavailable and available again like every 10 seconds.~~ ~~moved to adb server~~ Moved to custom component via HACS from Jeff
  - ~~ZHA seems to be unreliable yet, sometimes it turn-on turn-off works, sometimes not, throws errors in log / Seems to be fixed with 0.94~~ moved to deconz
  - Xiaomi Gateway (Reset not possible)
  - ~~Duplicati Backups~~

**NOT Integrated:**
  - Cheap Hisense 4k TV in bedroom that isn't even online when turned off but idrc anyway
  - Kitchen Yeelight (it actually has no use anyway except I could pair it with a motion detector which I haven't bought yet)

**Docker:**
  - homeassistant/home-assistant
  - ~~pihole/pihole~~
  - adguard/adguardhome
  - portainer/portainer
  - pyouroboros/ouroboros
  - ~~codeskyblue/adb *(FORKED)*~~
  - ~~eclipse-mosquitto~~
  - linuxserver/letsencrypt
  - linuxserver/duplicati
  - linuxserver/duckdns
  - linuxserver/mariadb
  - marthoc/deconz
  - ~~nodered~~
  - klutchell/unbound
  - linuxserver/unifi-controller
  - linuxserver/nextcloud
  - linuxserver/smokeping
  - linuxserver/taisun
  - jenkins/jenkins
  - linuxserver/plex
  - linuxserver/guacd
  - linuxserver/znc


**Monitoring:**
  - Netdata

External reachable! I use the Fail2Ban from Host (protecting SSH) to also read the HASS Logs. 

Using .htpasswd files within the letsencrypt Container will solve the problem also, you just have to login twice.

Official SSL certificates for sub-sub-domains like hass.subdomain.duckdns.org thx to Linuxserver letsencrypt.

The DuckDNS container will report your IP to the DNS service in a set interval.

Don't forget Duplicati to make regular Backups, keeping a few versions, pushing to the external Desktop HDD and then backup to BackBlaze.

**Devices:**
  - FritzBox 7590 (Yet only as a dumb-made modem, without WIFI or any other feature turned on. Only static routes to my Unifi Network.
  - Unifi USG
  - Unifi NanoHD AP
  - ~~Devolo DLAN 1200 ac~~ Powerline only gave me 20Mbit, terrible electricity here
  - Netgear GS108eV3
  - Seagate Backup Plus Hub 8TB
  - 3 Yeelights *(2 2. Gen and 1 1. Gen)*
  - 4 Osram Smart+ Plug
  - Xiaomi Airpurifier Pro
  - Xiaomi Airpurifier 2S
  - Xiaomi Roborock S50
  - LG OLED 55C8
  - Nvidia Sield
  - FireTV
  - 2 Echo Dot V3
  - 2 PC's
  - Xiaomi Gateway *(NOT WORKING)*
  - Xiaomi Humidity Sensors
  - Xiaomi Button
  - 3 Xiaomi Door- / Window-Sensor
  - 4 Xiaomi Mi Flora Plant Sensor
  - 2 Ariela Mobile App
  - Tradfri 30W Driver @ 11x Ledberg Spots (Zigbee)
  - Medion Alexa WiFi Radio

**Need:**
  - ~~Powerline Mesh~~
  - ~~New RPI2 replacement (Keep Pi for PiHole)~~
  - ~~6-10TB External Backup HDD~~
  - ~~8-port managed Switch~~
  - ~~More of these Osram Plugs to kill many of the idle devices when not_home *(look at PiHole how many connections these damn bastards do when you're gone! (And also electricity))*~~
  - Xiaomi Motion Detectors? Also as iluminance sensor
  - ~~Xiaomi Door-Window Sensors~~
  - Yeelights everywhere
  - ~~LED Strip for bed~~
  - ~~Internet Radio or so for wake up?~~
  - ~~New car~~
  - ~~Unifi Setup~~

**ToDo:**
  - ~~Connect Xiaomi Zigbee devices via Deconz or ZHA and leave the Gateway standalone~~
  - Further integrations
  - (MQTT Topics)
  - ~~MariaDB Recorder~~
  - Better automations
  - Scripts
  - Extend Alexa functionality
  - ~~HACS~~

