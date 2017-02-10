# Przyciski & Sensory

## Czego nauczysz się w tym rozdziale?

* Używania przycisków w celu kontrolowania Twojego Micro:bita
* Pokazywania obrazków na Twoim Micro:bicie
* Łączenia teksu i obrazków

## Mamy przyciski

Jak już pewnie zauważyłeś, Micro:bit ma 2 duże przyciski: A i B.
Możesz nimi zrobić wiele ciekawych rzeczy. Zacznijmy od czegoś prostego.

```python
from microbit import *

sleep(10 * 1000)
display.scroll(str(button_a.get_presses()))
```

Poczekaj chwilę przed wyświetleniem kodu!

Wiemy już mniej więcej, co oznacza: `from microbit import *`. (microbit to moduł, gwiazdka oznacza ,,wszystko", czyli wszystkie moduły dostępne do użycia w microbicie). Wiemy też, co oznacza: `sleep(10 * 1000)`.

A co znaczy ten fragment: `display.scroll(str(button_a.get_presses()))`?

Widzimy, że ta linijka składa się z kilku różnych pojedynczych instrukcji.

Od środka mamy:

1. `button_a.get_presses()`

Ten kod zwraca nam liczbę kliknięć przycisku A.

2. `str()`

Ta linijka zamienia ,,value", czyli otrzymaną liczbę, na string. String jest jednym z rodzajów danych, jakie rozumie Python (obok np. liczb). Jest to po prostu fragment znaków, liter, czy wyraz, w odróżnieniu od na przykład liczby.(Liczby można np. dodawać, a stringów już nie, bo to inny typ danych). "1" i 1 to różne wartości w Pythonie. "1" (zapisane w cudzysłowiu) to jest string (czyli wyraz), natomiast 1 to jest liczba, w tym wypadku liczba całkowita, czyli po angielsku integer. Musimy zamienić liczbę na string, ponieważ komenda ,,dispal.scroll()" rozumie tylko stringi.

3. `display.scroll()`

Tej komendy wcześniej już użyliśmy. Wyświetla ona wskazany tekst za pośrednictwem diod.

Podsumowując wszystko razem:

1. Zbieramy ilość kliknięć przycisku A
2. Zmieniamy ten numer na string
3. Wyświetlamy wartość na Micro:bicie

Ok, teraz możesz kliknąć Flash, by wyświetlić swój kod!

### Jak działa ten kod?
### Jak myślisz, jak możemy poprawić ten kod?

### Zadanie

Czy umiesz napisać program, który liczy liczbę kliknięć przycisku B w ciągu 5 sekund?

Masz 10 minut!

## Czas na ulepszenie kodu: część 1

Ten kod działa, ale chcielibyśmy też dodać kilka nowych funkcjonalności:

Chcemy, by przed rozpoczęciem liczenia wyświetlało się odliczanie, np. 3, 2, 1, 0, start! Czyli w skrócie:

* pokaż odliczanie (np. 3, 2, 1, 0)
* pokaż liczbę kliknięć przycisku B
 
```python
from microbit import *

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear() # Tą linijką ,,czyścimy" nasz wyświetlacz :)

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```

## Czas na ulepszenie naszego kodu: część 2

Teraz chcemy jeszcze dodać tekst przed odliczaniem: ,,Naciśnij przycisk A żeby zacząć"

Innymi słowy chcemy, żeby Micro:bit wyświetlał nam informację, że mamy nacisnąć przycisk A, o ile nie jest już wciśnięty.

Jak możemy to zakodować?

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

## Ostatni krok!

Ostatnim krokiem będzie możliwość powtórzenia gry.

To oznacza nieskończone powtrzanie kodu, który napisaliśmy wcześniej.

wskazówka: żeby powtarzać kod w nieskończoność musimy użyć komendy ,,while True" (czyli: dopóki prawda, zrób coś).

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

## Poczuj sensory

Micro:bit ma rózne sensory. Jednym z nich jest akcelerometr, którego możemy użyć do rozpoznawania niektórych ruchów.

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

Możesz otrzymać aktualne położenie Micro:bita używając komendy: ,,accelerometer.current_gesture()". Ta komenda w wyniku zwróci nam string.

Spróbujmy to zobaczyć na prostym przykładzie:

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

Wyświetl ten kod!
