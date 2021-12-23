# VUmeter-Arduino
Coding a VU meter to work with an Arduino and a SSD1322 256x64 display.

![video](https://github.com/Sesam31/VUmeter-Arduino/blob/master/vu.mp4)

## Features

- Tunable rise and fall times for the indicators
- Full 60 fps using u8g2 and memcpy_P to make full buffer refreshes
- Bitmap file for the scale is provided so you can edit it any way you want

## Important

If you want to make your own background use a tool like Image2GLCD to create it insted of exporting a .bmp directly from gimp. 
This is very important because allocation in flash memory using PROGMEM has a different ordering of bytes so your image will turn out a mess if it's not done properly. 
This is an example of the configuration used to create the background: 

![image](https://github.com/Sesam31/VUmeter-Arduino/blob/master/i2glcd.png)
