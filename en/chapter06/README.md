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

very_small_square = Image(
             "00000:"
             "00000:"
             "00900:"
             "00000:"
             "00000")

small_square = Image(
             "00000:"
             "09990:"
             "09990:"
             "09990:"
             "00000")

square = Image(
             "99999:"
             "99999:"
             "99999:"
             "99999:"
             "99999")

radio.on()
radio.config(group=YourGroupNumber)

while True:
    display.show([very_small_square, small_square, square], delay=200)
    
    if button_a.was_pressed():
        radio.send('flash')

    incoming = radio.receive()
    
    if incoming == 'flash':
        sleep(random.randint(50, 350))
        display.show(Image.HAPPY)
        sleep(random.randint(1, 10)*1000)
```
