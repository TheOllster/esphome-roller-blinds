# esphome-roller-blinds

yaml for use with ESPhome v1.15.0-dev.

Hardware used:
  * Wemos D1 mini, with 12V shield
  * A4988 stepper driver
  * 42SHD0217-24B stepper
  * 3x push-buttons
  
If you are using Homeassistant, this will show up as a "cover" entity, with open/stop/close and also ability to set position 0%(closed) to 100%(open).


Usage:

To set the zero-position(open) of the blind, hold "button1" and release after 3-10s.
To set the closed-position, hold "button3" and release after 3-10s.

To run the blind above/below the limits, hold "button2" while pressing "button1" or "button3" depending on the direction.

Notice that the open/closed positions of the blind is inverted in regards to Homeassistant (0 in esp is 100% in homeassistant).

The set closed position will update if the value of "ms1", "ms2" or "ms3" is changed. This is in regards to the number of steps will be different depending on which driver mode you choose (full-step, half-step etc.).

It is recommended to add an "input number" entity (10-100) to homeassistant, to be able to set the speed.
