# Buttons & Sensors

## What will you learn during this chapter ?

* Use the buttons to control your Micro:bit
* Show an image on your BBC Micro:bit
* Combine text and images

## So we do have buttons....

As you probably saw your Micro:bit has 2 big buttons `A` and `B`.
And you can do a lot of things with me, let's start with something easy.


```python
from microbit import *

sleep(10 * 1000)
display.scroll(str(button_a.get_presses()))
```

wait before flashing!

We know what `from microbit import *` does and the same goes for `sleep(10 * 1000)`.

But what about `display.scroll(str(button_a.get_presses()))` ?

We see that this line is formed by many instructions.

From the inside we have:

1. `button_a.get_presses()`

This code returns the number of times you pressed the `A` button.

2. `str()`

This line just conver a `str(value)` to a string.
"1" and 1 are different values in Python, "1" is a string (like a word) weather 1 is a number, an integer in this case. 
We need to convert an integer to a string because `display.scroll()` accept strings.

3. `display.scroll()`

We have already used this command, it displays text using the leds.

So putting everything together we:

1. Collect the number of times we pressed the button `A`
2. Convert that number into a str
3. Display the value on the Micro:bit

Ok, now you can press flash an try this code!

### How is the code working?
### How do you think we can improve this code?

### Quest of the day

Can you write a program to count the total number of times you pressed the button `B` during 5 seconds ?

You have 10 minutes for this quest!

## Time to improve our code: part 1#


The code is working but we would like add some new features:

We want to show a countdown before start _counting_, something like 3, 2, 1, go!

* show a countdown (like 3, 2, 1, 0)
* display the number of time you pressed the button `B`
 
```python
from microbit import *

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear() # With this we just clear the display :)

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```

## Time to improve our code: part 2#

Now we want to have something like `Press button A to start`.

In other words we want to display `Press button A to start` _until_ we pressed the button `A`.

how can we code this ?

__hint: `button_a.was_pressed()` returns True if `A` was pressed or False__

```python
from microbit import *

while button_a.was_pressed() is False:
    display.scroll("Press button A to start")

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear()

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```


## Last step!

The last step is to add the possibility to repeat the game.

This means repeat infinitely all this code we had before.

__hint: to repeat code infinitely you have to use while True__


```python
from microbit import *

while True:
    while button_a.was_pressed() is False:
        display.scroll("Press button A to start")
        
    countdown = ['3','2','1','0']
    display.show(countdown, 1*1000)
    display.clear()
    sleep(10 * 1000)
    display.scroll(str(button_b.get_presses()))
```

## Feel the sensors

Micro:bit has different sensors, one of them is an _accelerometer_ and we can use it to recognize some gestures.

```python
up
down
left
right
face up
face down
freefall
3g
6g
8g
```

You can get the current gesture using `accelerometer.current_gesture()`, this command returns a string.

Let's try a simple example:

```python
from microbit import *


x = Image("90009:"
          "09090:"
          "00900:"
          "09090:"
          "90009")

square = Image("99999:"
               "99999:"
               "99999:"
               "99999:"
               "99999")

while True: 
    gesture = accelerometer.current_gesture()
    if gesture == "face up":
        display.show(square)
    else:
        display.show(x)
```

Flash it!
