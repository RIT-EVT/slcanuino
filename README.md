#Slcanuino

NOTE: This project is a fork of
[kahiroka's Slcanuino program](https://github.com/kahiroka/slcanuino).

This Arduino program enables an Arduino with a CAN shield to operate as a
serial can device. The script implements the LAWICEL ASCII protocol for
converting serial communication to CAN. To see the original, see section
2 of the [CAN232](http://www.can232.com/docs/can232_v3.pdf) datasheet.

This project as mentioned is forked. The code was modified to make sure of
a CAN library made by
[Sandeep Mistry](https://github.com/sandeepmistry/arduino-CAN). This allows
the script to be easier to install and run, and also supports multiple
Arduino compatible platforms.

# Supported hardware

* Arduino compatible platform
* MCP2515 Arduino CAN shield

# How to use

Program the Arduino with the contained script and use along side existing
Slcan supported tools. For example, the tool
[python-can](https://python-can.readthedocs.io/en/master/index.html) has
many resources for working with serial CAN devices.

## Deps

1. Sandeep Mistry's arduino-CAN library which can be installed via the
   built in Arduino Library Manager tool

To find Sandeep's CAN library, open the Arduino Library Manager,
search for "MCP2515", and scroll down and look for Sandeep's name.

## Example usage with Python-CAN

```bash
python -m can.viewer -c /dev/tty.usbmodem143301@115200 -i slcan
```

Where `/dev/tty.usbmodem143301` is replaced with the path to the serial
device.

For more information, see [Python-CAN's documentation](https://python-can.readthedocs.io/en/master/interfaces/slcan.html)
on working with Slcan.
