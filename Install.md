Raspberry Pi Zero W
```
sudo apt-get update

sudo apt-get install build-essential python-dev python-pip git

git clone https://github.com/fingerskier/RaspberryPi-Joystick

cd RaspberryPi-Joystick/32_Buttons_Joystick/
```

Append to `/boot/config.txt`
```
dtoverlay=dwc2
```

Append to `/etc/modules`
```
dwc2
libcomposite
```

Create this file and make it executable `/usr/bin/32_buttons_rpi_joystick_usb`

Modify `/etc/rc.local`
...add the following before the `exit 0`
```
/usr/bin/32_buttons_rpi_joystick_usb # Raspberry Joystick 32 button libcomposite configuration

```

Copy this file: `32_buttons_rpi_joystick_usb` from the repo `RaspberryPi-Joystick/32_Buttons_Joystick/`
...to `/usr/bin/`
...and make it executable

Reboot
