# TO-DO

- Refine the drawing of the image.
- A switch to toggle between mode 4 and mode 8 before and even after loading the image.
- Add more screen modes taking into account the following information: (1)


__(1) Info by Dilwyn Jones__

As higher resolution screens don't include width and height dimensions, you have to guess the width and height based on file sizes corresponding to common screen dimensions, e.g. 640x480 pixels (76800 bytes), 800x600 pixels (120000 bytes), 1024x768 pixels (196608 bytes).

PIC files have the 10 bytes before the graphics data, holding:

word - ident $4AFC
word - width in pixels
word - height in pixels
word - line increment (number of bytes from start of one line to the next)
byte - mode number
byte - spare, unused