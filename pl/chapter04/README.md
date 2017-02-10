# Animacje

## Czego nauczysz się w tym rozdziale?

* Wyświetlać tekst na swoim BBC Micro:bicie
* Wyświetlać obrazki na swoim BBC Micro:bicie
* Łączyć tekst z obrazkami

## Wyświetlanie obrazów

Wyświetlanie tekstu jest fajne, ale spróbujmy teraz powyświetlać obrazki!

Zacznijmy z czymś...wesołym :)

```python
from microbit import *

display.show(Image.HAPPY)
```

Czy przesłałeś kod do swojego Micro:bita?


To jest lista obrazków, które możesz użyć:

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

Spróbuj wypróbować kilka z nich.

Spróbuj również wyświetlić więcej niż jeden obrazek!

```python
from microbit import *

display.show(Image.HAPPY)
display.show(Image.HOUSE)
```

Podyskutujmy teraz o rezultacie tego kodu:)

# Wyświetlanie 2 obrazków

Nie widzimy pierwszego obrazka, ponieważ...Micro:bit wykonuje wyświetlenie drugiego obrazka tak szybko, że nie widzimy tego pierwszego.

Poprośmy Micro:bita, żeby na trochę...zasnął.

Jest specjalna komenda, która nazywa się sleep(seconds*1000), która przenosi Twojego Micro:bita w specjalny rodzaj snu.

Spróbujmy wpisać tą komendę, a wewnątrz ,,(seconds*1000)" powinieneś zastąpić słowo ,,seconds" liczbą sekund, w czasie których chcesz, żeby Twój Micro:bit spał.

```python
from microbit import *

display.show(Image.HAPPY)
sleep(10*1000)
display.show(Image.HOUSE)
```
Wyświetl ten kod i zobacz jak działa!

# Stwórz swój własny obrazek!

Micro:bit zna wiele różnych obrazków, ale możemy też stworzyć nowe.

To działa tak:


```python
new_image = Image(
             "11111:"
             "19991:"
             "19991:"
             "19991:"
             "11111")
display.show(new_image)
```
Właśnie stworzyliśmy nowy obrazek!

Ale czym są te numery?

Mamy 5 linijek i 5 numerów w każdej linijce.

To są nasze diody!

Każdy numer oznacza jedną diodę na naszym Micro:bicie, począwszy od lewego górnego rogu.

Mamy tutaj 1 i 9.

Czy możesz powiedzieć co się zmienia, jak używamy 0, 1 lub 9?

Wskazówka: możemy tu używać numerów od 0 do 9.

Poeksperymentuj!
