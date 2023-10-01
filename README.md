# MIAO (喵) ch552t MCU board

### Changelog
2023-09-29 initial commit  
2023-09-30 fixed pinout to correspond to Xiao, added jumper to choose between RX/CS on pin 8, completely rerouted

| :zap: **THIS HARDWARE IS UNTESTED** as of the latest commit. **Use at your own risk!** |
|----------------------------------------------------------------------------------------|

## About
MIAO is a cheap and hand-solderable drop-in replacement for the Seeeduino Xiao series.  
(Castellated holes are expensive, so MIAO doesn't support them [for now].)

喵 is the Hanzi for "miāo", which is Mandarin for "meow".

## Pictures
<details>
<summary> Front view render </summary>

![miaofront](https://github.com/kilipan/miao/blob/main/img/miao_3d_front.png?raw=true)

</details>
<details>
<summary> Back view render </summary>

![miaoback](https://github.com/kilipan/miao/blob/main/img/miao_3d_back.png?raw=true)

</details>
<details>
<summary> Schematic </summary>

![miaoschematic](https://github.com/kilipan/miao/blob/main/img/miao_schematic.png?raw=true)

</details>

# Features
MIAO features:
- Utilizes wch's ch552t microcontroller, which at the time of writing costs a few dozen cents! 
- SPI and UART pins in the same places as Xiao (use jumper to choose between RX/CS on pin 8)
- 2 Analogue pins
- 4 additional broken out pins (not pads!) compared to the Xiao boards:
  - 2 free GPIOs
  - reset pin (pull HIGH for reset)
  - boot pin (pull HIGH for entering bootloader)
- Full ESD protection incl. protection against reverse current and overcurrent
- Top-mount USB port for maximum drop-in-ability
- Optional power or user led (on the backside; bridge left and middle part of jumper for always-on, middle and right for user controllable via P3.3)
- Optional reset and bootloader buttons (on the backside)
- Optional footprint for connecting USB Shield to GND in a way that fits your application
- Cute pixel cat on the back! 🐱


# Firmware
The project is inspired by and designed for usage with
[semickolon](https://github.com/semickolon/)'s
[FAK firmware](https://github.com/semickolon/fak/), but it's obviously not
limited to that! Refer to the ch552t documentation and the many other ch55x
projects for more details.

# License
The hardware design is licensed under the CERN-OHL-v2-S license, so feel free
to look at the sources and remix to your heart's content! :)

# Thanks
- semickolon for creating FAK, inspiring the project and helping with design considerations
- 0xCB for open-sourcing the [Helios](https://github.com/0xCB-dev/0xCB-Helios/) and providing inspiration for the ESD stuff
- the Clacktales community for their continued support, discussion, and interest in the project
- Pete Johanson for noticing and pointing out the pinout mix-up in the initially commited version
