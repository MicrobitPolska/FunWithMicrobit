# Pick&Mix

## What will you learn during this chapter ?

* Mixing the lectures to create something new!

Form some groups and try to work together, if you need any help don't be afraid to ask!

## Python Programmers
If you need any help don't forget to check the [Micro:bit Micropython docs](https://microbit-micropython.readthedocs.io).


## Quest  n.1 - Display a Christmas Tree
Yeah.... Christmas is over, but a Christmas tree is always nice.
Try to display a Christmas tree on you Micro:bit.

Hints:
* Remember you have to use Image()

## Quest n.2 - Display the button you pressed
The goal of this quest is to write a program that display the name of the button you pressed.

Hints:
* You only have 2 buttons __A__ and __B__
* try to use `if`
* use `is_pressed()`

## Quest n.3 - Shack and display messages!
The goal of this quest is to write a program that display different messages everytime you shack you Micro:bit.

Some hints:
* you can put all your messages inside a list
* use `accelerometer.was_gesture("shake")`
* pick a random message using random.choice(messages)

But what does it mean ?

## Quest n.4 - Show the direction of you Micro:bit
Micro:bit comes with an _accelorometer_, a sensor that gives you the direction of the Micro:bit.
Build a program that shows the direction of the Micro:bit with an arrow.

Hints:
* Consider only `up`, `down`, `left` and `right`
* Build the arrows using Image()
* Use `accelerometer.current_gesture()` to get the current direction
* Don't forget about `while True:`

## Quest n.5 - Use the radio
Try to build a simple text-walkie-talkie with your friends.
Choose a message and send the message to your friend every time you push a button (A or B).

Hints:
* Remember to call `radio.on()`
* When you receive a radio-message scroll the message
* To simplify the program consider that only one Micro:bit at time will send a message
