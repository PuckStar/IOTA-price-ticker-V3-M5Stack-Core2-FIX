<p><img src="https://github.com/oxinon/IOTA-price-ticker-V2-TTGO-T-Display/blob/master/picture/IOTA-Price-Ticker.png" alt="Cover" width="400"></p>

<p><img src="https://github.com/oxinon/IOTA-price-ticker-V3-M5Stack-Core2/blob/main/picture/pt3v2.png" alt="Cover" width="600"></p>

<br>
IOTA ticker V3 on Youtube: https://www.youtube.com/watch?v=CBe5YHJxLos
<br>
<br>

* * *

<b>Index of this project</b>

+ [Add M5Stack to Arduino IDE](#ESP32)
+ [Libraries for Arduino IDE](#libraries)
+ [How to use](#info)

* * *
<br>
<h2>Changelog</h2>

02.03.2024 PuckStar fork</p>
- Changed in the .ino file "MIOTA" to "IOTA" because it's not called MIOTA anymore</p>
- Added the file iota1.h because it was missing from the source package</p>
   <br>

30.12.2021</p>
- Fix issue with USD/EUR select in Webconfig</p>
- Add light theme select in Webconfig</p>
- NEW is a .bin file for esptool, this can be easy flash on the M5Stack Core2</p>
   <br>

23.06.2021</p>
- Add Baterry Indicator</p>
- Add USD/EUR select in Webconfig</p>
- Dark Theme</p>

<br>
<a name="ESP32"></a><h2>Add M5Stack in Arduino IDE</h2>

Before we can start compiling, the Arduino IDE must have the M5Stack Core2 board, based on an ESP32 in the board selection available.
The instruction on https://docs.m5stack.com/#/en/arduino/arduino_core2_development
In board selector you can select "M5Stack Core2" for M5Stack Core2.
<br>
<br>
For MAC users install the "CP210x USB to UART Bridge VCP Drivers" from Silicon Labs, the port to select is /dev/cu.SLAB_USBtoUART in Arduino IDE under tools-->Port
<br>
https://www.silabs.com/community/interface/knowledge-base.entry.html/2017/01/10/legacy_os_softwarea-bgvU
<br>

<a name="libraries"></a><h2>Libraries for Arduino IDE</h2>
Now we add libraries for Arduino IDE 1.8.13:<br>
The new api requires a developer key, so you must apply for a key to use https://pro.coinmarketcap.com/account
<br>

+ [CoinMarketCapApi.h](https://github.com/lewisxhe/CoinMarketCapApi2) 
+ [ArduinoJSON](https://github.com/bblanchon/ArduinoJson) version 6.x is testet 
   
The genaral instruction for the "M5Stack Core2" can be found here https://docs.m5stack.com/#/en/core/core2<br>
If you are have problem with the "wifi.h" delete the arduino/libraries/wiFi directory, you can use the esp32 WiFi.h
<br>
<br>
<a name="info"></a><h2>How to use</h2>

First start shows no Wifi or CMC key in the display. The first start open a Wifi AP, connect to this Wifi <b>Price-Ticker_SETUP</b> and open a web browser enter the following IP address "192.168.4.1". Please enter your data here, after submitting this data will be saved and it is not necessary to enter it again.
<br>
After the automatic restart, the price ticker connects to your wifi and shows your setting on the display, to check that everything is saved. If the price ticker is connected to the internet, it retrieves data from Coinmarketcap and shows it on the display, every 260sec. the data will be updated.

<p><img src="https://github.com/oxinon/IOTA-price-ticker-V3-M5Stack-Core2/blob/main/picture/Wen-settings.png" alt="Cover" width="600"></p>
<br>
<br>
<a name="esptool"></a><h2>Install and flash via esptool</h2>
<br>
PuckStar: I deleted this .bin file because it didn't include the necessary fix of MIOTA => IOTA
<br>
<br>
<a name="reset"></a><h2>Reset stored config</h2>
There are two ways to reset the setting, first if no wifi connection is established, only the wifi setting is reset after 30sec., the CMC API key remains stored.
second possibility, if the price ticker is connected to the wifi, the setting can be reset via the assigned ip address (in my case is this 192.168.1.227), and the CMC API key is also deleted. Then the price ticker starts again in Wifi AP mode.
<br>

<p><img src="https://github.com/oxinon/IOTA-price-ticker-V3-M5Stack-Core2/blob/main/picture/reset-settings.png" alt="Cover" width="600"></p>
<br>
<a name="lighting"></a><h2>Display lighting</h2>
The lower 3 soft touch buttons set the brightness of the street in 3 steps. Button A = low, button B = middle, button C = high


* * *

If you like my work, you can give me a tip for a beer :)<br><br>
<b>IOTA Donate address:</b> 
iota1qz4uqyauz486zvrm2jjn4gurq5dzcmhezr0d6smykgaferx6madmzj2rzxr <br>

<p><img src="https://github.com/oxinon/IOTA-price-ticker-V2-TTGO-T-Display/blob/master/picture/qrcode3.png" alt="Cover" width="200"></p>
