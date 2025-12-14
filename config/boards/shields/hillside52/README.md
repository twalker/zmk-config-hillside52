Hillside 52 is a split ergonomic keyboard with 3x6+3+5 choc-spaced keys.
It has the aggressive stagger of the Ferris but a longer thumb arc and a break-off outer pinkie column.
More information is at [github/mmccoyd](https://github.com/mmccoyd/hillside/).

The default keymap is described in
  [QMK](https://github.com/qmk/qmk_firmware/tree/master/keyboards/handwired/hillside/52).
  
For ZMK, the adjust layer has a few differences from the QMK version:

- Extra keys for bluetooth, reset and output.
- No swap Alt GUI keys.
- No RGB controls as RGB eats power.
- Bluetooth clear is deliberately in an inconvenient spot to avoid unpairing.

If used, the following must be manually enabled in hillside52.conf:

- Encoders
- Underglow

If desired, you could hardwire a display to the I2C header,
  which is arranged for a haptic feedback board.
  
  
---
## Trackpoint integration
## r61 trackpoint (oldest)
https://github.com/alonswartz/trackpoint/blob/master/pinouts/r61.jpg

First on the pins: Kim's trackpoint driver strictly only needs 2 pins, data (SDA) and clock (SCL), with an optional third pin for the trackpoint's reset.
1 DATA *
2 RST *optional
3 BTN1
4 BTN2
5 BTN3
6 CLOCK *
7 GND *
8 VCC *

## 28050? trackpoint (new)

https://github.com/alonswartz/trackpoint/blob/master/pinouts/28050.jpg

1 RST * (optional)
2 VCC *
3 CLK * 
4 GND *
5 MB0
6 MB1
7 DTA *
8 MB2

Nice nano pinout:
https://github.com/infused-kim/kb_zmk_ps2_mouse_trackpoint_driver-zmk_config
RST: D9/P1.06
SCL D16/P0.10
SDA D10/P0.09
  


 
---
## Trackpoint integration
## r61 trackpoint (oldest)
https://github.com/alonswartz/trackpoint/blob/master/pinouts/r61.jpg

First on the pins: Kim's trackpoint driver strictly only needs 2 pins, data (SDA) and clock (SCL), with an optional third pin for the trackpoint's reset.
1 DATA *
2 RST *optional
3 BTN1
4 BTN2
5 BTN3
6 CLOCK *
7 GND *
8 VCC *

## 28050? trackpoint (new)

https://github.com/alonswartz/trackpoint/blob/master/pinouts/28050.jpg

1 RST * yellow (optional) 
2 VCC * red
3 CLK * green
4 GND * black
5 MB0
6 MB1
7 DTA * blue
8 MB2
