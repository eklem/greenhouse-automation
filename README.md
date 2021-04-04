# greenhouse-automation
Just a hobby project =) Greenhouse automation based on Raspberry Pi, Node-red and Pimoroni Automation Hat

## Functionality to be
* Check soil moisture
* Water once every day if soil is too dry
* Check water level in reservoir
* SMS / email if reservoir needs refilling
* Input to [Justini](https://github.com/eklem/justini) if reservoir needs refilling and filling statistics.

## Software and Modules
* Raspberry Pi OS
* [Node-RED](https://nodered.org/) - [Running on Raspberry Pi](https://nodered.org/docs/getting-started/raspberrypi)
* [Node-RED nodes for Pimoroni Automation HAT/pHAT](https://github.com/shortbloke/node-red-contrib-automation-hat) - [blogpost on using it](https://www.martinrowan.co.uk/2018/09/node-red-support-for-pimoroni-automation-hat-phat/)

## Hardware
* Raspberry Pi
* Automation Hat - [Explanation on ports](https://blog.pimoroni.com/automation-hat-tanya-teardown/)
* [Arduino Soil Moisture Sensor](https://thepihut.com/blogs/raspberry-pi-tutorials/raspberry-pi-plant-pot-moisture-sensor-with-email-notification-tutorial)
* 12V solenoid valve (closed when power off)
* Some USB charger
* 240 AC - 12V DC converter (IKEA) to solenoid
* Water hose
* Hose nipples etc.


## Setup
### Rasperry Pi

* Install Raspberry Pi OS
* `sudo raspi-config` and enable ssh, set hostname to greenhouse, change password, maximise disk space and update raspi-config
* `sudo aptitupde update && sudo aptitude safe-upgrade`
* `sudo apt install build-essential git`
* Install node and node-red - `bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)`
* Make node-red start on boot `sudo systemctl enable nodered.service`
* Reboot
* Go to `http://greenhouse:1880`
* Install node-red-contrib-automation-hat with `menu` > `settings` > `pallete` > `install`
