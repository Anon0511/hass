##Home Assistant V0.94.3

So this is my config as of now, most likely updated from time to time.

This costed me approx. 150 hours of work yet, using an RPI 2b which I had laying around since ages now because I never had a usecase here.
It is using the Raspbian Lite Image without a GUI, pure SSH, Docker Setup. 

This config is still pretty small, not having much integrations, devices, automations and functions. Don't consider it as the holy grail since I'm pretty new. 
I didn't even use consistent syntax. God damn. 

Also some things still throw errors which may or may not affect the function.

**NOT WORKING:**
  - ~~ADB seems to be unreliable yet, devices become unavailable and available again like every 10 seconds.~~ moved to adb server
  - ~~ZHA seems to be unreliable yet, sometimes it turn-on turn-off works, sometimes not, throws errors in log / Seems to be fixed with 0.94~~ moved to deconz
  - Xiaomi Gateway (Reset not possible)

**NOT Integrated:**
  - Cheap Hisense 4k TV in bedroom that isn't even online when turned off but idrc anyway
  - Kitchen Yeelight (it actually has no use anyway except I could pair it with a motion detector which I haven't bought yet)

**Docker:**
  - homeassistant/raspberrypi2-homeassistant
  - pihole/pihole
  - portainer/portainer:arm
  - pyouroboros/ouroboros *(deactivated)*
  - codeskyblue/adb *(FORKED)*
  - eclipse-mosquitto
  - linuxserver/letsencrypt:arm32v7-latest
  - linuxserver/duplicati:arm32v7-latest
  - linuxserver/duckdns:arm32v7-latest
  - linuxserver/mariadb
  - marthoc/deconz:armhf
  - nodered

**Monitoring:**
  - Netdata

External reachable! I use the Fail2Ban from Host (protecting SSH) to also read the HASS Logs. 

While the Letsencrypt Container ships with a Fail2Ban it is just dirty to make the HASS Container logs available to letsencrypt, using .htpasswd files within the letsencrypt Container will solve the problem also, you just have to login twice.

Official SSL certificates for sub-sub-domains like hass.subdomain.duckdns.org thx to Linuxserver letsencrypt.

The DuckDNS container will report your IP to the DNS service in a set interval.

MariaDB to prepare for "recorder" which I can't use with the RPI2 image.

Don't forget Duplicati to make regular Backups, keeping a few versions, pushing to the external Desktop HDD and then backup to BackBlaze.

**Devices:**
  - FritzBox 7590
  - Devolo DLAN 1200 ac
  - Netgear GS108eV3
  - 3 Yeelights *(2 2. Gen and 1 1. Gen)*
  - Osram Smart+ Plug
  - Xiaomi Airpurifier Pro
  - Xiaomi Roborock S50
  - LG OLED 55C8
  - Nvidia Sield
  - FireTV
  - Echo Dot V3
  - 2 PC's
  - Xiaomi Gateway *(NOT WORKING)*
  - Xiaomi Humidity Sensor
  - Xiaomi Button
  - 2 Ariela Mobile App

**Need:**
  - ~~Powerline Mesh~~
  - New RPI2 replacement (Keep Pi for PiHole)
  - 6-10TB External Backup HDD
  - ~~8-port managed Switch~~
  - More of these Osram Plugs to kill many of the idle devices when not_home *(look at PiHole how many connections these damn bastards do when you're gone! (And also electricity))*
  - Xiaomi Motion Detectors? Also as iluminance sensor
  - Xiaomi Door-Window Sensors
  - Yeelights everywhere
  - LED Strip for bed
  - Internet Radio or so for wake up?
  - New car

**ToDo:**
  - ~~Connect Xiaomi Zigbee devices via Deconz or ZHA and leave the Gateway standalone~~
  - Further integrations
  - MQTT Topics
  - ~~MariaDB Recorder~~
  - Better automations
  - Scripts
  - Extend Alexa functionality