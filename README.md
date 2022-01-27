# Droplet
 ALL-IN-ONE Irrigation and monitoring system for ESPHome and Home Assistant.
 
 !!!!! I will upload the Gerber files when I receive the new expansion boards. I want to make sure everything works. !!!!
 
 
 ![DROPLETFull](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/dropletfull.JPEG)
 
 
 
   Main Board
   
   
 ![DROPLET](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/droplet.jpg)
 

 1. 5x Micro Pump outputs
 2. 5x Soil Moisture sensor inputs 'Pulled down with 1M ohm resistor'
 3. Onboard Temperature sensor "DS18B20" https://esphome.io/components/sensor/dallas.html
 4. Onboard Buzzer "Buzzer port can be free up with jumper" https://esphome.io/components/rtttl.html?highlight=buzzer
 5. Breakout pins for connecting "i2c OLED Display" https://esphome.io/components/display/ssd1306.html?highlight=display
 6. 5x Buttons for manual Pumps controll
 7. 1x Button "Short press" for wake-up Oled "Long press" for general purpose. "2x Binary sensors available for HA"
 8. All pumps outputs and moisture sensor inputs have fuses
 9. Pins Which can be used "GPIO 19,5,26,2,15,27,14,12" and "1xi2c GPIO 21,22" "1xUART" "GPIO25 External port for DS18B20 TMP Sensor!!"
 
  Expansion Board v3
  
  
 ![ExpBoard](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/ExpaBoard.JPG)
 
 
 1. 1x JST 10pin connector Outputs for 8 Relays  "MCP23017" Expander  https://esphome.io/components/mcp230xx.html
 2. 1x 8 Pin Header "MCP23017" Expander  https://esphome.io/components/mcp230xx.html
 3. 2x JST 4pin i2c (V, GPIO 21, GPIO 22 GND)
 4. 7x JST 3pin GPIO 19,5,26,2,15,27,14
 5. 1x JST 3pin for "DS18B20 TMP Sensors" (3.3v, GPIO 25, GND)
 6. 1x 1pin Header GPIO23 connected to buzzer. Buzzer port can be free up, "remove jumper JP"
 
 

 What sensors Droplet support ? "All sensors supported by ESPHome" https://esphome.io/index.html
 
 
 I connected and tested at the same time.
 5x Pump
 5x Moisture Sensor V2, 
 2x "DS18B20" Temperature, 
 1x BMP280 Temperature and Pressure, 
 1x VL53L0x Distance Sensor, 
 1x DHT Temperature and Humidity, 
 8x Relays. 
 
 
 ![HA](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/HASensors.JPG)
