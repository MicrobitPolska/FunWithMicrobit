# Micro:bit do you copy ?

## What will you learn during this chapter ?

* How to use the radio module
* Use 2 or more Micro:bits to create a radio network 

## What is the radio module ?

Inside each BBC Micro:bit there is a very interesting feature that you can use: a radio.

You can use the radio module to send and receive messages.

What's next ?

Create a group with some of your friends a decide a number, it should be used only inside your group.
If your friends are close or not it doesn't matter, we have a radio!

Use the radio module is very easy:

1. Import the radio module
2. Turn the radio on
3. Set a group number
4. Send or receive messages

```python
import radio
import random
from microbit import display, Image, button_a, sleep

# Create the "flash" animation frames. Can you work out how it's done?
flash = [Image().invert()*(i/9) for i in range(9, -1, -1)]

# The radio won't work unless it's switched on.
radio.on()

# The radio won't work unless it's switched on.
radio.config(group=NumberThatYouChose)
# A micro:bit Firefly.

# Event loop.
while True:
    # Button A sends a "flash" message.
    if button_a.was_pressed():
        radio.send('flash')  # a-ha
    # Read any incoming messages.
    incoming = radio.receive()
    if incoming == 'flash':
        # If there's an incoming "flash" message display
        # the firefly flash animation after a random short
        # pause.
        sleep(random.randint(50, 350))
        display.show(flash, delay=100, wait=False)
        # Randomly re-broadcast the flash message after a
        # slight delay.
        if random.randint(0, 9) == 0:
            sleep(500)
            radio.send('flash')  # a-ha
```
