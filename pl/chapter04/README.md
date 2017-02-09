# Animacje

## Czego nauczysz siê w tym rozdziale?

* Wyœwietlaæ tekst na swoim BBC Micro:bicie
* Wyœwietlaæ obrazki na swoim BBC Micro:bicie
* £¹czyæ tekst z obrazkami

## Wyœwietlanie obrazów

Wyœwietlanie tekstu jest fajne, ale spróbujmy teraz powyœwietlaæ obrazki!

Zacznijmy z czymœ...weso³ym:)

```python
from microbit import *

display.show(Image.HAPPY)
```

Czy przes³a³eœ kod do swojego Micro:bita?


To jest lista obrazków, które mo¿esz u¿yæ:

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

Spróbuj wypróbowaæ kilka z nich.

Spróbuj równie¿ wyœwietliæ wiêcej ni¿ jeden obrazek!

```python
from microbit import *

display.show(Image.HAPPY)
display.show(Image.HOUSE)
```

Podyskutujmy teraz o rezultacie tego kodu:)

# Wyœwietlanie 2 obrazków

Nie widzimy pierwszego obrazka, poniewa¿...Micro:bit wykonuje wyœwietlenie drugiego obrazka tak szybko, ¿e nie widzimy tego pierwszego.

Poproœmy Micro:bita, ¿eby na trochê...zasn¹³.

Jest specjalna komenda, która nazywa siê sleep(seconds*1000), która przenosi Twojego Micro:bita w specjalny rodzaj snu.

Spróbujmy wpisaæ t¹ komendê, a wewn¹trz ,,(seconds*1000)" powinieneœ zast¹piæ s³owo ,,seconds" liczb¹ sekund, w czasie których chcesz, ¿eby Twój Micro:bit spa³.

```python
from microbit import *

display.show(Image.HAPPY)
sleep(10*1000)
display.show(Image.HOUSE)
```

Wyœwietl ten kod i zobacz jak dzia³a!

# Stwórz swój w³asny obrazek!

Micro:bit zna wiele ró¿nych obrazków, ale mo¿emy te¿ stworzyæ nowe.

To dzia³a tak:


```python
new_image = Image(
             "11111:"
             "19991:"
             "19991:"
             "19991:"
             "11111")
display.show(new_image)
```
W³aœnie stworzyliœmy nowy obrazek!

Ale czym s¹ te numery?

Mamy 5 linijek i 5 numerów w ka¿dej linijce.

To s¹ nasze diody! 

Ka¿dy numer oznacza jedn¹ diodê na naszym Micro:bicie, pocz¹wszy od lewego górnego rogu.

Mamy tutaj 1 i 9.

Czy mo¿esz powiedzieæ co siê zmienia, jak u¿ywamy 0, 1 lub 9 ?

Wskazówka: mo¿emy tu u¿ywaæ numerów od 0 do 9.

Poeksperymentuj!
