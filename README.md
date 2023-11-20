# MIAO (喵) ch552t MCU board

### Changelog
2023-09-29 initial commit  
2023-09-30 fixed pinout to correspond to Xiao, added jumper to choose between RX/CS on pin 8, completely rerouted

| :zap: The hardware design is tested and confirmed working as of the latest commit. Nevertheless I cannot guarantee anything. **Use at your own risk!** |
|---|

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

# BOM
| Amount | Part | LCSC part number |
| ------:|:-----|:-----------------|
|      1 | ch552t microcontroller | [C111367](https://www.lcsc.com/product-detail/USB-ICs_WCH-Jiangsu-Qin-Heng-CH552T_C111367.html) |
|      1 | top-mount USB-C receptacle | [C2765186](https://www.lcsc.com/product-detail/_SHOU-HAN-_C2765186.html) |
|      1 | SOT-23 ESD protection diode | [C6807798](https://www.lcsc.com/product-detail/_FUXINSEMI-_C6807798.html) |
|      1 | SOD-323 Schottky diode | [C193668](https://www.lcsc.com/product-detail/_Nexperia-_C193668.html) |
|      1 | 0603 Fuse | [C311055](https://www.lcsc.com/product-detail/_AEM-_C311055.html) |
|      1 | 0603 10kΩ Resistor | [C25804](https://www.lcsc.com/product-detail/_UNI-ROYAL-Uniroyal-Elec-_C25804.html) |
|      2 | 0603 5.1kΩ Resistor | [C23186](https://www.lcsc.com/product-detail/_UNI-ROYAL-Uniroyal-Elec-_C23186.html) |
|      2 | 0603 100nF Capacitors | [C384773](https://www.lcsc.com/product-detail/Multilayer-Ceramic-Capacitors-MLCC-SMD-SMT_Walsin-Tech-Corp-0603X334K100CT_C384773.html) |
|    [1] | [optional] 1kΩ Resistor | [C21190](https://www.lcsc.com/product-detail/_UNI-ROYAL-Uniroyal-Elec-_C21190.html) |
|    [2] | [optional] push buttons | [C115357](https://www.lcsc.com/product-detail/_ALPSALPINE-_C115357.html) |
|    [1] | [optional] LED | [C434442](https://www.lcsc.com/product-detail/_Yongyu-Photoelectric-_C434442.html) |

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
