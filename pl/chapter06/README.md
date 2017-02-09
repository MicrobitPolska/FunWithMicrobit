# Micro:bit czy mnie s³yszysz?

## Czego nauczysz siê w tym rozdziale?

* Jak u¿ywaæ modu³u radio
* Jak u¿ywaæ 2 lub wiêcej Micro:bitów, ¿eby stworzyæ sieæ radiow¹

## Czym jest modu³ radio?

Wewn¹trz ka¿dego BBC Micro:bita znajduje siê bardzo interesuj¹ca funkcjonalnoœæ, której mo¿emy u¿yæ, czyli - radio.

Mo¿emy u¿ywaæ modu³u radio do wysy³ania i otrzymywania wiadomoœci.

Co dalej?

Dobierzcie siê w kilkuosobowe grupy, i wybierzcie jakiœ numer, który bêdzie u¿ywany tylko w waszej grupie.

Jeœli cz³onkowie grupy nie siedz¹ blisko to nic nie szkodzi, poniewa¿ mamy radio!

U¿ywanie modu³u radio jest bardzo proste. Musimy:

1. Zaimportowaæ modu³ radio
2. W³¹czyæ radio
3. Ustawiæ numer grupy
4. Wysy³aæ albo otrzymywaæ wiadomoœci

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
