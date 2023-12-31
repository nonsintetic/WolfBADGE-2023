![WolfBADGE-2023](https://github.com/nonsintetic/WolfBADGE-2023/blob/main/res/wolfbadge-live.png?raw=true)

# WolfBADGE-2023
 This is the Official Wolf-e Robotics end of year badge. Every year we create something to celebrate the end of the year. This year it's an ornament / fridge magnet / desktop toy thing with a ton of addressable LEDs and WiFi connectivity. Feel free to remix it into your own fun design and poke us on social media if you do, we'd love to see it.

# Hardware
 We used an ESP32 microcontroller module as the main processor. 
 
 The touch IC is connected to GPIO36 and will output HIGH when the decorative triangle pad is touched. There are two solder bridges you can link to configure the button to be a toggle switch and change it from active HIGH to active LOW.

 There is a PDM microphone on board connected to the ESP32 GPIO that can be configured in WLED. PDM DATA is on GPIO32 and PDM CLK is on GPIO15.

 The board as a battery charger build-in, just plug in USB and the battery will be charged. Default current is 200mA, change R3 to adjust the charge current.

# Firmware
 We used the MoonModules fork of WLED to support sound reactivity. You can find our config file 

# Power consumption
 We limited the leds to 250mA in WLED (the minimum allowed setting in WLED), but these particular pixels use a lot less power. We measured around 140mA at full blast with WiFi on and connected (with the WLED limit in place). So a 250mA battery should be more than enough to give you over an hour battery life (and will generally fit on the back without issues).

# 3D printed case
 We included a 3D printed case to hide the battery on the back of the module, it's a bit of a fast and dirty design since we ran out of time.
