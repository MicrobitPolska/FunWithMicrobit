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
