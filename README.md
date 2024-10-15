# Sparrow

## Arduino-compatible IoT sensor node made from two boards: the Node and the Nest - used for programming and debugging.

<img src="https://github.com/dantudose/Sparrow/blob/main/Node/Images/Sparrow.jpg" height="350"/>

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

### Installing Arduino Libraries and Boad Configs

1. Open the Arduino IDE
2. Go to File → Preferences
3. In the Additional Boards Manager URLs textbox add the following link: http://clkdiv8.com/download/package_clkdiv8pre_index.json
4. Close the window by pressing OK
5. Go to Tools → Board → Boards Manager
6. Search “sparrow”
7. Hit Install
8. You're done!

#### Tutorials

Most tutorials for using the on-board sensors or radio are available <a href="https://clkdiv8.com/wiki/doku.php/tutorials">here</a>.

#### Bootloader
The board comes pre-loaded with a bootloader. Should you need to re-write it, connect an AVR-ISP or JTAG to the corresponding port and burn the <a href="https://github.com/dantudose/Sparrow/blob/main/Node/bin/">bootloader</a> .hex file with _atmega128rfa1_ as a target and the following fuse settings:

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

## License Information

This product is _**open source**_! 

