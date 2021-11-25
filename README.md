# lib-6x5RGBMatrix
Arduino compatible library to drive 6x5 arrays of RGB LEDs.

Supports multiple boards with only one object, easing use and addressing.  Board we used and recommend is:
  Adafruit 8x16 LED matrix FeatherWing (ID:3090)

Board based on the Holtek HT16K33, which drives a matrix of LEDs up to 8x16 according to I2C commands:
  https://www.holtek.com/documents/10179/116711/HT16K33v120.pdf

Why is this 6x5 rather than 8x16?  First, red, green, and blue LEDs all count, so 5 RGB LEDs/row use 15 of 16 outputs.
Second, we needed 60 LEDs, so 30/board worked well.  With 5 LEDs per row, we only need 6 of 8 column outputs.
We wrote this to drive the LEDs for a 24" resin clock upcycle. Was cheap AA-powered hands that died, but liked the clock.
It's a large open format with most of the underlying wall showing through and 60 decorative holes around the outside rim.
We just reamed the holes for 10mm "gumdrop" LEDs to heep "open" look, wired to two boards (easier said!), and added NodeMCU.
