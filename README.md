# Marlin 2.1.x on Ender 3 with a SKR 1.3 and TMC 2130 (SPI) (Sensorless and silent) (Bigtree)
<img align="right" src="../../raw/1.1.x/buildroot/share/pixmaps/logo/marlin-250.png" />

<img align="right" src="https://www.hta3d.com/image/cache/cache/1-1000/386/main/9d54-SKR-1.3-01-0-4-550x550.jpg" alt="Image" height="200" width="200" />

Marlin is the world's most popular open source firmware for 3D printers. [Marlin 2.0](https://github.com/MarlinFirmware/Marlin/tree/bugfix-2.0.x). The SKR 1.3's processor is LPB 1768. But the rest of the things are what the Ender 3 brings from the factory.

I'm owner of this configuration, I did it following some videos and foros. I had some problems along the way, they was the hot of the motors, the hotend, it burns twice, and I change it to a V6 by trianglelab.
If you haven't V6 by trianglelab, in thermistor configuration you have to put "1" instead of "5".

I use Sensorless except in Z, for that you may have to weld somethings, but I hadn't, the TMC 2130 SPI come ready to connect and ready, but it's more expensive. To end stop in Z, have to remove the red switch, near LCD conection. .The Sensorless could be changed in the Firmware or in the LCD, if you change in LCD, you have to save in EEPROM, or when you turn off the printer, it'll lose. 

The file that you have to put in the SD Card is "firmware.bin", you MUST to move it, or copy&paste and later delete it. "firmware.bin" can't be in the folder before you compile. The firmware is in "C:...\Marlin\.pio\build\LPC1768\".

After do all this, you must to do a step calibration, and a PID again. 

Here you have some tutorials that could helps you. 

How to connect and configurate:
https://medium.com/@damien.martin.guillerez/skr-1-3-tmc2130-on-a-creality-ender-3-b4ec4abfdfd1 (by: Damien Martin-Guillerez)

When you connect the LCD, the pins go upside down.

To configure Marlin, you need Platform.io in a code editor, it could be Visual Studio Code or ATOM, I did all in ATOM.
https://youtu.be/kLTaNh301AE?t=158 

PID 
https://reprap.org/wiki/PID_Tuning
