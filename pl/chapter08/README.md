# Free your creativity

## What will you learn during this chapter ?

* You will apply what you have learned before
* You will work with your team to prepare a project
* Combine text and images

## Let works together

It's time to form some group, you will have around 30 minutes to prepare a project using Python and BBC Micro:bit.
After you prepared your project you will present your project.

If you need

```python
# This is a COMMENT
from microbit import display
```

STOP !

Let's think about this first 2 lines.
The first one starts with # and it means is a comment.
A comment is a part of code in Python used...just to comment and it starts with #.

The second line is much more important. We are asking Python to import the _display_ module from microbit.

But what is a module ?
Think about a _module_ as a collection of Python code that will help us using the _display__.


now we can ask Micro:bit to display our text

```python
# This is a AGAIN a COMMENT
from microbit import display

display.show("Hello PutYourNameHere, I am your Micro:bit")
```

What we have here now ?

First and second line are nothing new.

But what about the third line ?

Well we are using a part of the code, described inside _display_, called _show_.

And we are jut putting text after it.

Let's try with a different text:

```python
# This is a AGAIN a COMMENT
from microbit import display

display.show("Helloo Poland!)
```

copy this text in your Mu editor and flash it !

Mmmm.... why are we receiving an error ?

* The exclamation mark at the end of the text is causing a problem
* The text is too short
* We need a __"__ at the end of the text
* Helloo (should be Hello) is not grammatically correct

## But why only one time ?

We put __showed__ our text inside the Micro:bit...but it shows our text only for one timeself.
What if we want to keep our Micro:bit showing the text ?

We need to introduce the concept of __loop__

With a __loop_ we are saying to the Micro:bit to _do something until some condition is respected_

In Python we have different __loops__, we can start using __while__.

While literally means _do something until the condition is true_

```python
from microbit import display

while 1>0:
  display.show("Hello Poland!")
```

Let's try again with this code:

```python
from microbit import display

while 1<0:
  display.show("Hello Poland!")
```

We just changed the condition with something that is always _False_

## What is the difference between these codes ?


## Why display is not exactly under while ?
