# rpi-NAS

#Setting headless rpi
1) Write image to the SD card. It has 2 partitions rootf and boot
2) Under boot :
- create an empty file ssh (this will allow rpi to have ssh server and it can be accessed using ssh or via putty)
- create a file wpa_supplicant.conf 
country=IN
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
scan_ssid=1
ssid="your_wifi_ssid"
psk="your_wifi_password"
}

3) Load the SD card in rpi and power it on.
4) On Router admin page, you can check the Dynamic IP allocated to the rpi.

