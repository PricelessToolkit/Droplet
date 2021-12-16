# Droplet
 ALL-IN-ONE Plants growing and monitoring system for ESPHome and Home Assistant.
 
 
 ![DROPLET](https://raw.githubusercontent.com/PricelessToolkit/Droplet/main/img/droplet.jpg)
 
  Main Board
 1. 5 Micro Pumps
 2. 5 Soil Moisture sensors 
 3. Onboard Temperature sensor "DS18B20" https://esphome.io/components/sensor/dallas.html
 4. Onboard Buzzer "Buzzer port can be free up with jumper" https://esphome.io/components/rtttl.html?highlight=buzzer
 5. Breakout pins for connecting "i2c OLED Display" https://esphome.io/components/display/ssd1306.html?highlight=display
 6. 5 Buttons for manual Pumps controll
 7. 1 Button "Short press" for wake-up Oled "Long press" for general purpose. "2x Binary sensors available for HA"
 8. All pumps outputs and moisture sensor inputs have fuses
 9. Free Ports "8xGPIO" "1xi2c" "1xUART" "External port for DS18B20 TMP Sensor"
 
 
 Expansion Board
 1. 8x Outputs "SN74HC595" shift register https://esphome.io/components/sn74hc595.html?highlight=sn74hc595
 2. 2x JST 4pin i2c
 3. 1x JST 4pin UART
 4. 4x JST 4pin Free GPIOs
 
 

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
