# Bluedot demo

## Hardware - ESP32 based board

It is a Wemos Lolin32 device - https://wiki.wemos.cc/products:lolin32:lolin32  
There is a circuit diagram there.

Can be powered by the +5V and GND pins next to the Lipo battery connector.

It has been configured that both GPIO pins have internal pull up resistors and best used with an open drain or relay to GND.

_WARNING_: All of the IO pins run at 3.3V. Good chance the device will be destroyed if a voltage outside +3.3V and 0V is applied to the pins.

## Software Events

The demo software displays the following events or notifications when the cooresponding pins are driven to ground.

- pin 16: Arc Detected - Potential fire risk!
- pin 17: Unexpected Event - Bedroom a/c left running

### Notifications

Notifications are only diplayed when application is running in the background.  
Notifications are delayed by 5 seconds, giving time to go to the Home screen and waiting to show the event.  
Notifications are also displayed even if the screen has turned off - as long as the application is still running.

### Status Line

On the app screen the bluetooth status is displayed at the bottom.  
When everything is ok it will display "Listening for Events..."
