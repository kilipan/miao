# MIAO (喵) ch552t MCU board

| :zap: **THIS HARDWARE IS UNTESTED** as of 2023-09-28. **Use at your own risk!** |
|---------------------------------------------------------------------------------|

The MIAO is a cheap and hand-solderable drop-in replacement for the Seeeduino Xiao series.
It is fully ESD protected, including reverse current protection and overcurrent protection.
It utilizes wch's ch552t microcontroller, which at the time of writing costs a few dozen cents!

![miaofront](https://github.com/kilipan/miao/blob/main/img/miao_3d_front.png?raw=true)
![miaoback](https://github.com/kilipan/miao/blob/main/img/miao_3d_back.png?raw=true)

# Features
This board should fit onto any pcb that is designed for mounting a XIAO board via through-holes.  
(Castellated holes are expensive, so the MIAO doesn't support them [for now].)

MIAO features:
- Top-mount USB port for maximum drop-in-ability
- 4 additional broken out pins (not pads!) compared to the Xiao boards:
  - 2 free GPIOs (P3.0 and P3.1)
  - reset pin (pull HIGH for reset)
  - boot pin (pull HIGH for entering bootloader)
- Full ESD protection incl. protection against reverse current and overcurrent
- Optional power or user led (on the backside; bridge left and middle jumper for always-on, middle and right for user controllable via P3.3)
- Optional reset and bootloader buttons (on the backside)
- Optional footprint for connecting USB Shield to GND in a way that fits your application


# Firmware
The project is inspired by and designed for usage with [semickolon](https://github.com/semickolon/)'s [FAK firmware](https://github.com/semickolon/fak/), but it's obviously not limited to that! Refer to the ch552t documentation for more details.

# License
The hardware design is licensed under the CERN-OHL-v2-S license, so feel free to look at the sources and remix to your heart's content! :)

# Thanks
- semickolon for creating FAK, inspiring the project and helping with design considerations
- 0xCB for open-sourcing the [Helios](https://github.com/0xCB-dev/0xCB-Helios/) and providing inspiration for the ESD stuff
- the Clacktales community for their continued support, discussion, and interest in the project
