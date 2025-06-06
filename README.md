# U6143_ssd1306
## Preparation
```bash
sudo raspi-config
```
Choose Interface Options 
Enable i2c

##  Clone U6143_ssd1306 library 
```bash
cd
git clone https://github.com/UCTRONICS/U6143_ssd1306.git
```
## Run `setup_display_service.sh` script
```bash
cd U6143_ssd1306
chmod +x setup_display_service.sh
sudo ./setup_display_service.sh
```
## For older 0.91 inch lcd without mcu 
- For the older version lcd without mcu controller, you can use python demo
- Install the dependent library files
```bash
sudo pip3 install adafruit-circuitpython-ssd1306
sudo apt-get install python3-pip
sudo apt-get install python3-pil
```
- Test demo 
```bash 
cd /home/pi/U6143_ssd1306/python 
sudo python3 ssd1306_stats.py
```

## Custom display temperature type 
- Open the U6143_ssd1306/C/ssd1306_i2c.h file. You can modify the value of the TEMPERATURE_TYPE variable to change the type of temperature displayed. (The default is Fahrenheit)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/OLED/select_temperature.jpg)


## Custom display IPADDRESS_TYPE type 
- Open the U6143_ssd1306/C/ssd1306_i2c.h file. You can modify the value of the IPADDRESS_TYPE variable to change the type of IP displayed. (The default is ETH0)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/OLED/select_ip.jpg)

## Custom display information 
- Open the U6143_ssd1306/C/ssd1306_i2c.h file. You can modify the value of the IP_SWITCH variable to determine whether to display the IP address or custom information. (The custom IP address is displayed by default)
![EasyBehavior](https://github.com/UCTRONICS/pic/blob/master/OLED/custom_display.jpg)





