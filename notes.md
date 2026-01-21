Calculations for snubber RC:

  https://youtu.be/wgNMepGIrTk?t=319

ECO:

 - Reduce hole size on stakes
 - Reduce solder paste on TO-252 footprint
 - Move cutout on south edge of board (but watch copper on bottom)
 - Reduce hole widths on mains stake pins
 - Remove via under R2.
 - Increase slot widths and lengths underneath resistors
 - The SW3, SW4 and SW5 discrete switches are swapped.  SW3 should be S, and is W.  SW4 is W and should be E.  SW5 should be E and is S.
 - Move multidirectional switch south
 - Mod so 3-pin header can be switched by pads to either thermistor or DS18B20.  (Is there any difference anyway?)
 - Add +/- to top of board where PSU module sits
 - Add earth clip pad
 - Add 2N7002 to drive opto output
 - Mod opto drive resistor to be 90R.
 - Add 4k7 I2C resistors
 - Better SH connnector/footprint
 - Make C1 and C2 X2 capacitors
 - Update fuse footprint and 3d model
 

04 SW5
05 BUZZ2
14 SW4
15 MOTOR
18 BUZZ1
19 SW2
21 SDA
22 SCL
23 SW1
25 SW3
26 HEATER
27 DS18B20
32 THERM
33 LED

