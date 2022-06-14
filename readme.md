<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/klor-font-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/klor-font-logo-bright.svg">
  <img alt="KLOR logo font" src="/docs/images/klor-font-logo-bright.svg">
</picture>

# THE QMK CONFIG FOR THE KLOR SPLIT KEYBOARD

[Here](https://github.com/GEIGEIGEIST/zmk-config-klor) you can find the ZMK config for the KLOR. You need to create your own fork to use it.\
[Here](https://github.com/GEIGEIGEIST/klor) you can find the hardware files and build guide.

KLOR is 42 keys column-staggered split keyboard. It supports a per key RGB matrix, encoders, OLED displays, haptic feedback, audio, a Pixart Paw3204 trackball and four different layouts, through brake off parts.

![KLOR layouts](/docs/images/klor-layouts.svg)



## AVR MCU
**Sparkfun Pro Micro / Elite-C / Puchi-C**

You'll need to setup a local build environment of QMK. [Here](https://docs.qmk.fm/) you can find the instructions.\
Place the klor folder from this repository in the keyboards folder of your qmk installation.\
Use this command to compile the firmware for the KLOR.

`qmk compile -kb klor -km default`




## RP2040 MCU
**Adafruit KB2040 / Sparkfun Pro Micro RP2040 / Boardsource Blok**

Currently you need to use [this PR](https://github.com/KarlK90/qmk_firmware/tree/feature/raspberry-pi-rp2040-support) instead of the official QMK Repo, if you plan to use the RP2040.\
Place the klor folder from this repository in the keyboards folder of your qmk installation.\
Use this command to compile the RP2040 firmware for the KLOR.

`qmk compile -kb klor/kb2040 -km default`
