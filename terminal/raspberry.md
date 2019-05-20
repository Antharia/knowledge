# Raspberry Pi
## Headless installation
Copy your OS iso on your SD card
> dd if=your.iso of=/dev/yourSDcard bs=4M conv=fsync
To know the name of your SD card : 
> lsblk
Once your OS installed, create a /boot/ssh file to access your Pi via ssh later.
### Wifi
> ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
> update_config=1
> country=«your_ISO-3166-1_two-letter_country_code»
> 
> network={
    > ssid="«your_SSID»"
    > psk="«your_PSK»"
    > key_mgmt=WPA-PSK
> }

