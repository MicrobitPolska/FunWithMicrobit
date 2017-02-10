# Micro:bit czy mnie słyszysz?

## Czego nauczysz się w tym rozdziale?

* Jak używać modułu radio
* Jak używać 2 lub więcej Micro:bitów, żeby stworzyć sieć radiową

## Czym jest moduł radio?

Wewnątrz każdego BBC Micro:bita znajduje się bardzo interesująca funkcjonalność, której możemy użyć, czyli - radio.

Możemy używać modułu radio do wysyłania i otrzymywania wiadomości.

Co dalej?

Dobierzcie się w kilkuosobowe grupy, i wybierzcie jakiś numer, który będzie używany tylko w waszej grupie.

Jeśli członkowie grupy nie siedzą blisko to nic nie szkodzi, ponieważ mamy radio!

Używanie modułu radio jest bardzo proste. Musimy:

1. Zaimportować moduł radio
2. Włączyć radio
3. Ustawić numer grupy
4. Wysyłać albo otrzymywać wiadomości

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
