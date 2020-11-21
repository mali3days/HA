# Installing Home Assistant Supervised on Raspberry Pi OS

1. Use [pi imager](https://www.raspberrypi.org/blog/raspberry-pi-imager-imaging-utility).

<img width="400" src="https://www.raspberrypi.org/app/uploads/2020/03/RPI_intro-e1583228263677.png" alt="Raspberry Pi Imager.">

2. Enable [remote access to raspberry](https://www.raspberrypi.org/documentation/remote-access/ssh).

3. Connect to it with [`ssh pi@IP_OF_THE_RASPBERRY`](#code) ([How to get IP_OF_THE_RASPBERRY](https://www.raspberrypi.org/documentation/remote-access/ip-address.md)).

4. [Update and upgrade Raspbian](https://www.raspberrypi.org/documentation/raspbian/updating.md).

5. [Configure Raspbian](https://www.raspberrypi.org/documentation/configuration/raspi-config.md).

<img width="400" src="https://www.techcoil.com/blog/wp-content/uploads/Selecting-Advanced-Options-of-raspi-config-on-terminal-in-Raspbian-Buster-20190710.gif" alt="Configure Raspbian.">

6. Setup docker and docker-compose [`sudo apt -y install docker docker-compose`](#code).

7. Install Home Assistant Supervised [link](https://community.home-assistant.io/t/installing-home-assistant-supervised-on-raspberry-pi-os/201836):

- [`sudo apt-get install -y software-properties-common apparmor-utils apt-transport-https avahi-daemon ca-certificates curl dbus jq network-manager`](#code)

- [`systemctl disable ModemManager`](#code)

- [`systemctl stop ModemManager`](#code)

- [`curl -sL "https://raw.githubusercontent.com/Kanga-Who/home-assistant/master/supervised-installer.sh" | bash -s -- -m raspberrypi4`](#code)

8. Open browser at http://IP_OF_THE_RASPBERRY:8123.

9. Restore system from snapshot.

10. Fix Recorder issues.

11. Repo for dscreen dricers: https://github.com/goodtft/LCD-show
