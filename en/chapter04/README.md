# Animations

## What will you learn during this chapter ?

* Show a text on your BBC Micro:bit
* Show an image on your BBC Micro:bit
* Combine text and images

## Showing images

Showing text is ok....but what about images ?!?!

Let's start with something...happy :)

```python
from microbit import *

display.show(Image.HAPPY)
```

Did you flash the code inside your Micro:bit ?

Show us the happy faces!

This is a list of images that you can use:

```python
Image.HEART
Image.HEART_SMALL
Image.HAPPY
Image.SMILE
Image.SAD
Image.CONFUSED
Image.ANGRY
Image.ASLEEP
Image.SURPRISED
Image.ROLLERSKATE
Image.DUCK
Image.HOUSE
Image.TORTOISE
Image.BUTTERFLY
Image.STICKFIGURE
Image.GHOST
Image.SWORD
Image.GIRAFFE
Image.SKULL
Image.UMBRELLA
Image.SNAKE
```

__Take 5 minutes and play with these images.__

Try also to put more then one image together!

```python
from microbit import *

display.show(Image.HAPPY)
display.show(Image.HOUSE)
```

Let's discuss about the result together :)

# Showing 2 images

We don't see the first image because....Micro:bit execute the second display so fast that we cannot see the first.

Let's ask the Micro:bit to...sleep.

There is special command called sleep(seconds*1000) that literally put your Micro:bit under a special kind of sleep.

Let's try this command, inside (seconds*1000) you should substitute _seconds_ with the number of seconds you want your Micro:bit to sleep 

```python
from microbit import *

display.show(Image.HAPPY)
sleep(10*1000)
display.show(Image.HOUSE)
```

Flash this code and tell us about the result!

# Build your image!

Micro:bit knows already a lot of images but we can build also new images.

This is how it works


```python
from microbit import *

new_image = Image(
             "11111:"
             "19991:"
             "19991:"
             "19991:"
             "11111")
display.show(new_image)
```
We have just create a new image!

But what are those numbers ?

We have five lines and five numbers in each line....

They are our leds! 

Each number represent a led on our Micro:bit from, from the left top.

But we have 0, 1 and 9.

Can you say what does it change between putting 0, 1 or 9 ?

hint: you can use numbers between 0 and 9.

Experiment!
