# esp-xtoys
Scipt to connect your ESP8266 NodeMCU V3 to XToys as a custom HTTP Post Toy

## ESP Set-Up
- The script provide 2 PWM channels on pin 12(D6) and 13(D7)
```c++
const int c1Pin = 12;
const int c2Pin = 13;
```
- Set your Wifi SSID and password
```c++
#define STASSID "your ssid"
#define STAPSK "your password"
```
- Flash the script into your esp
- Connect your motors (or wathever you want to control) to the ESP

## XToys Set-Up
- Go to the side menu > MANAGE YOR DATA > Custom Toys > + sign on bottom right corner > Create a new HTTP Post Toy
- Write the following parameters:

|Parameter|Value|
|-|-|
|NAME|whatever you want|
|TYPE|1/2 Channel Vibrator (based on what you are making)|
|# of Intensity Steps|100|
|URL|https://[your local ESP IP address]/channel/\<\<channel>> (put 1 instead of \<\<channel>> if you use only 1)|
|DATA|\<\<vibrate>>|
- Save
