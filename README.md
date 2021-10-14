# GridsMIDITweak
Tweaked firmware for Mutable Instruments Grids with better MIDI support:
- added support for midi stop/continue messages
- the midi clock input now follows the global clock resolution setting
- increaased the trigger duration from ~1ms to ~6ms

## Flashing
I flashed this with avrdude and a cheapo USBASP clone using the following command:

```
avrdude -C "C:\Program Files (x86)\Arduino\hardware\tools\avr/etc/avrdude.conf" -V -p m328p -c usbasp -P usb -B 10 -e -u -U flash:w:grids.hex:i
```
