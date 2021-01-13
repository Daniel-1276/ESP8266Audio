# ESP32 SPDIF digital audio Webradio project
## Goals
This project aims to create the most cheapest hifi quality webradio, elimating buzzing sounds and ground loop issues by using SPDIF and TOSLINK connections to hifi amplifieres. 
This project will output an http mp3 internetradio webstream via [S/PDIF](https://de.wikipedia.org/wiki/Sony/Philips_Digital_Interface) digital audio interface.
Basic information about Artist and Song can be shown via SPI port, using an ST7735 128x160 pixel TFT display (optional).

## Current state of development
Audio output is working stable. Oscilloscope measurements of S/PDIF output showed no relevant jitter at all, even after adding ST7735 display drivers and some scrolling text  . Optical digital audio quality is exceptionally well, compared to traditional 3.5mm Headphone jack connections. Currently one http webradio link can be compiled into the source code and is playing flawlessly. 
### Next steps
I am planning to add a webconfig page that does stop playing the stream as soon as somebody is connected. Else ESP32 webserver is interfering with the audio stream which causes unpleasant noise (currently the case in webserver example of ESP8266 example).

## Credits
All code forked and based on the excellent work of [ESP8266Audio project](https://github.com/earlephilhower/ESP8266Audio) :) I only throwed code snippets together, understanding only half of the stuff whats going on under the hood ;-)

1.8" ST7735 128x160 display connected via SPI (I2C is way to slow).
![WebRadio Display](https://github.com/Daniel-1276/ESP8266Audio/blob/master/SPDIF_WebRadio.gif)

![WebRadio](https://github.com/Daniel-1276/ESP8266Audio/blob/master/SPDIF_WebRadio.jpg?raw=true)
