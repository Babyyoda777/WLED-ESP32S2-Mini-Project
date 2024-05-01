




WLED Smart Light Project - ESP32

Start by plugging in your ESP32 board via USB to your computer. Then in Google Chrome or Microsoft Edge (not Safari or FireFox) visit https://espressif.github.io/esptool-js/ and press Connect under Program:

Next, upload the three files above, bootloader.bin, firmware.bin and partitions.bin. 

bootloader.bin should be assigned flash address 0x1000
partitions.bin should be assigned flash address 0x8000
firmware.bin should be assigned flash address 0x10000


Next, press Program and wait until it says “leaving”. Then unplug and replug your esp32 from usb. Wait a few moments and then check you wifi connections for the network “WLED-AP” and use password “wled1234”.

Wifi Setup To connect your WLED module to your home Wifi:  

1. Click on the Config (gear) icon to edit your WLED module settings and choose "Wifi Setup".  
2. For most home networks, simply enter your Wifi network's name and network password. You can also change the mDNS address for your WLED module here.  
3. Click Save & Connect at the bottom of the page.  
4. Reconnect your device to your home's Wifi network.  


Now, install the WLED app on either iOS on Android from the App Store or on your computer install from here https://github.com/w00000dy/WLED-GUI/releases/tag/v0.7.1
On your laptop, press the top right + and then detect lights. Then return to home page and your light should be there to control! (On phone this should happen automatically.)


Next, go to the settings and press on LED Configuration. Change the drop down that says “WS28XX” to “PWM RGB” from the list, and set the GPIO numbers to be in this order: 2 then 1 then 0. 
Now connect up your bread board like this: 



Once its all connected, unplug and replug the ESP32, then wait for a minute before reconnecting to the app. That’s it, you can now control it wirelessly!
