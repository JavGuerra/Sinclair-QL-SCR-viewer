# TO-DO

- A routine that tries to guess if a screen is in mode 4 or mode 8.

    __Info by Dilwyn Jones__

    It can be done by looking at the flash bits. If very few or no flash bits are set, it is most likely mode 8. In mode 4, the 'flash' bits within the color word would be green pixel bits, so unless there is no green on the mode 4 screen, this is a fairly accurate way (although not foolproof!) to check the way.


- Add more screen modes considering the following information:

    __Info by Dilwyn Jones__

    As higher resolution screens don't include width and height dimensions, you have to guess the width and height based on file sizes corresponding to common screen dimensions, e.g. 640x480 pixels (76800 bytes), 800x600 pixels (120000 bytes), 1024x768 pixels (196608 bytes).

    PIC files have the 10 bytes before the graphics data, holding:

    word - ident $4AFC
    word - width in pixels
    word - height in pixels
    word - line increment (number of bytes from start of one line to the next)
    byte - mode number
    byte - spare, unused
    