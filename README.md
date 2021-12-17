# Droplet
 ALL-IN-ONE Plants growing and monitoring system for ESPHome and Home Assistant.
 
   Main Board
   
   
 ![DROPLET](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/droplet.jpg)
 

 1. 5x Micro Pump outputs
 2. 5x Soil Moisture sensor inputs
 3. Onboard Temperature sensor "DS18B20" https://esphome.io/components/sensor/dallas.html
 4. Onboard Buzzer "Buzzer port can be free up with jumper" https://esphome.io/components/rtttl.html?highlight=buzzer
 5. Breakout pins for connecting "i2c OLED Display" https://esphome.io/components/display/ssd1306.html?highlight=display
 6. 5x Buttons for manual Pumps controll
 7. 1x Button "Short press" for wake-up Oled "Long press" for general purpose. "2x Binary sensors available for HA"
 8. All pumps outputs and moisture sensor inputs have fuses
 9. Pins Which can be used "GPIO19,5,26,2,15,27,14,12" and "1xi2c GPIO21,22" "1xUART" "GPIO25 External port for DS18B20 TMP Sensor!!"
 
  Expansion Board
  
  
 ![ExpBoard](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/ExpBoard.JPG)
 
 
 1. 1x JST 10pin Outputs for 8 Relays "SN74HC595" shift register used GPIO pns "19, 26, 2, 27" https://esphome.io/components/sn74hc595.html?highlight=sn74hc595
 2. 2x JST 4pin i2c "5v or 3.3v, GND, GPIO21, GPIO22"
 3. 1x 2 Pin Header TX and RX
 4. 4x JST 4pin Free "GPIO5, 15, 14, 12"
 5. 1x JST 3pin for "DS18B20 TMP Sensors" GPIO25 3.3v GND
 6. 1x 1pin Header GPIO23 connected to buzzer "Buzzer port can be free up with jumper"
 
 

 What sensors does it support ? "All sensors supported by ESPHome" https://esphome.io/index.html
 
 
 I connected and tested at the same time.
 5x Pump
 5x Moisture Sensor V2, 
 2x "DS18B20" Temperature, 
 1x BMP280 Temperature and Pressure, 
 1x VL53L0x Distance Sensor, 
 1x DHT Temperature and Humidity, 
 4x Relays. 
 
 
 ![HA](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/HASensors.JPG)
