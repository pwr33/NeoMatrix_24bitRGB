NeoMatrix_24bitRGB
==================
6/1/15 by Paul W. Rogers

Display 24 bit RGB bitmaps from PROGMEM
Adafruit_GFX, Adafruit_NeoPixel and Adafruit_Neomatrix libraries modified for 24bit RGB and RGB bitmap draw function
and pixel level brightness

Copy the 3 Adafruit directories to your libraries folder
Copy pwr_matrix_24bittest to your code folder, this is the example sketch

NOTE: As I only have the neomatrix panels, all the other display specific classes/libraries will
      need a change to functions in .h and .cpp files
      so this currently only works with my version of Adafruit_NeoMatrix provided here

.h
    drawPixel(int16_t x, int16_t y, uint16_t color, int16_t bright = -1)
    drawPixelRGB(int16_t x, int16_t y, uint8_t r, uint8_t g, uint8_t b, int16_t bright = -1)

.c
   void Adafruit_NeoMatrix::drawPixel(int16_t x, int16_t y, uint16_t color, int16_t bright)
   void Adafruit_NeoMatrix::drawPixelRGB(int16_t x, int16_t y, uint8_t r, uint8_t g, uint8_t b, int16_t bright)

WORK IN PROGRESS - Still got to split out the duplicated code in drawpixel functions to a new
                   common calc_pixel function, use the brightness parameter with drawpixelrgb
                   and some other improvements like gamma correction.

