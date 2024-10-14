# Sparrow

## Arduino-compatible IoT sensor node made from two boards: the Node and the Nest - used for programming and debugging.

<img src="https://github.com/dantudose/Sparrow/blob/main/Node/Images/Sparrow.jpg" height="300"/>

Features include:

* Atmega128RFA1 8-bit AVR low-power microcontroller
* Integrated 2.4GHz radio transceiver
* Precision temperature & humidity sensor
* Barometer/altimeter
* Light sensor (visible, IR and UV spectrum, luxmeter and UV radiation index)
* High capacity CR2450 battery holder
* Fully-compatible with Arduino, with dedicated libraries for easy programming of the sensors and radio.

<img src="https://github.com/dantudose/Sparrow/blob/main/Node/Images/sparrow_diagram.png" height="500"/>

## Repository Contents

* **/Hardware** - Eagle design files (.brd, .sch)
* **/Images** - Board images
* **/bin** - Binaries (board bootloader)

## Programming

### avr-gcc & Makefile

#### Bootloader
The board comes pre-loaded with a bootloader. If you need to re-write it, connect an AVR-ISP or JTAG to the corresponding port and burn the <a href="https://github.com/dantudose/Sparrow/blob/main/Node/bin/">bootloader</a> .hex file with _atmega128rfa1_ as a target and the following fuse settings:

<table>
<thead>
  <tr>
    <th>Fuse</th>
    <th>Value</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>HIGH</td>
    <td>0xD0</td>
  </tr>
  <tr>
    <td>LOW</td>
    <td>0xF7</td>
  </tr>
  <tr>
    <td>EXT</td>
    <td>0XFE</td>
  </tr>
</tbody>
</table>
