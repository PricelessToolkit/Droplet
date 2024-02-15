🤗 Please consider subscribing to my [YouTube channel](https://www.youtube.com/@PricelessToolkit/videos)
Your subscription goes a long way in backing my work.


[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/U6U2QLAF8)

# Droplet
 ALL-IN-ONE Irrigation and monitoring system for ESPHome and Home Assistant.
 * Youtube How-To https://youtu.be/mCXTqONmpZk
 * Shop https://www.pricelesstoolkit.com
 

 
 ![DROPLETFull](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/dropletfull.JPEG)
 
 
 
   ### Main Board
   
   
 ![DROPLET](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/droplet.jpg)
 

 1. 5x Micro Pump outputs "5v"
 2. 5x Soil Moisture sensor inputs "Data-5v-GND" 'Data line pulled down with 1M ohm resistor' ( Data line MAX 3.3v !!!!! )
 3. Onboard Temperature sensor "DS18B20" https://esphome.io/components/sensor/dallas.html
 4. Onboard Buzzer "Buzzer port can be free up with jumper" https://esphome.io/components/rtttl.html?highlight=buzzer
 5. Breakout pins for connecting "i2c OLED Display" https://esphome.io/components/display/ssd1306.html?highlight=display
 6. 5x Buttons for manual Pumps controll
 7. 1x Button "Short press" for wake-up Oled "Long press" for general purpose. "2x Binary sensors available for HA"
 8. All pumps outputs and moisture sensor inputs have fuses
 9. Pins Which can be used "GPIO 19,5,26,2,15,27,14,12" and "1xi2c GPIO 21,22" "1xUART" "GPIO25 External port for DS18B20 TMP Sensor!!"
 
  ### Expansion Board v3
  
  
 ![ExpBoard](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/ExpaBoard.JPG)
 
 
 1. 1x JST 10pin connector Outputs for 8 Relays  "MCP23017" Expander  https://esphome.io/components/mcp230xx.html
 2. 1x 8 Pin Header "MCP23017" Expander  https://esphome.io/components/mcp230xx.html
 3. 2x XH 4pin i2c (V, GPIO 21, GPIO 22 GND)
 4. 7x XH 3pin GPIO 19,5,26,2,15,27,14
 5. 1x XH 3pin for "DS18B20 TMP Sensors" (3.3v, GPIO 25, GND)
 6. 1x 1pin Header GPIO23 connected to buzzer. Buzzer port can be free up, "remove jumper JP"
 
 

 ## What sensors Droplet support ?
 ### Droplet support "Almost all sensors supported by ESPHome" https://esphome.io/index.html
 
 I connected and tested at the same time.
* 5x Pump
* 5x Moisture Sensor V2, 
* 2x "DS18B20" Temperature, 
* 1x BMP280 Temperature and Pressure, 
* 1x VL53L0x Distance Sensor, 
* 1x DHT Temperature and Humidity, 
* 8x Relays. 
 
 
 
 ![HA](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/HASensors.JPG)
 
 
## First time setup

### WIFI Captive Portal

The captive portal component in ESPHome is a fallback mechanism for when connecting to the configured WiFi fails.
After 1 minute of unsuccessful WiFi connection attempts, the ESP will start a WiFi hotspot with the credentials
```
SSID: "Droplet Fallback Hotspot"
password: "password"
```

When you connect to the fallback network, the web interface should open automatically (see also login to network notifications).
If that does not work, you can also navigate to http://192.168.4.1/ manually in your browser.
In this web interface, you can manually override the WiFi settings of the device.
Additionally, you can upload a new firmware file to your node without having to use a USB cable for uploads.

<img src="https://esphome.io/_images/captive_portal-ui.png" width="390" height="400" />


### Reflashing via USB-UART adapter

First, you need to create in the ESPhome new device using the Droplet Config file "don't forget to change it to your needs" then compile it and download the ".bin" file. To upload it to the Droplet, we also need  "ESPHome Flasher" software

* Connect your USB-UART adapter to your PC
* Push the "PROG" button on the Droplet Mainboard "don't release it"
* Plug the power adapter and wait for a second, then release the button
* Connect your USB-UART cables TX, RX, and GND to "J1"
* Upload firmware via ESPHome Flasher
 



## Setting the onboard DS18b20 temperature sensor

First of all we need to find out the address of the Onboard temperature sensor.
For example with this configuration: "which is already in the default config"

```
dallas:  # Integrated Temperature Sensor. https://esphome.io/components/sensor/dallas.html
  - pin: 25
    update_interval: 5s
```

In the log output (the log level must be set to at least debug!) you will find something like this


<img src="https://esphome.io/_images/dallas-log.png" width="634" height="321" />


Now that we know the address of temperature sensor, we can add it to the config as an example shown below

```
sensor:
  - platform: dallas
    address: 0xA40000031F055028
    name: "Droplet Onboard TMP Sensor"
```
after adding it to the config "install" the new firmware one more time.
 

## Part List

!!! Sellers very often change the type of pump to air "Link may not be relevant" !!!

* Power adapter 5v 2-3.5Ah Connector DC-005 2.0 - https://s.click.aliexpress.com/e/_DEsuOdV
* Oled Display - https://s.click.aliexpress.com/e/_DlkmoXv
* Pump 1 - https://s.click.aliexpress.com/e/_DdjCmgL
* Pump 2 - https://s.click.aliexpress.com/e/_DF3tloX
* Silicone tube " inner diameters 3 and 4mm" - https://s.click.aliexpress.com/e/_DBnM9qL
* Heat Set Insert M3 X D4.6 X L4.5 - https://s.click.aliexpress.com/e/_9xbSZC
* Capacitive Soil Moisture Sensor "lottery may be working or defective" - https://s.click.aliexpress.com/e/_9Qz84W
* Cables with connectors for sensors and relays "pin pitch XH 2.54MM" - https://s.click.aliexpress.com/e/_DDpn7iB
* 3D Case "For those who live in France" you can order here - https://www.facebook.com/Upin3d
* Cable for soil moisture sensor https://s.click.aliexpress.com/e/_DDGNx5h
