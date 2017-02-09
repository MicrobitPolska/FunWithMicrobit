# Przyciski & Sensory

## Czego nauczysz siê w tym rozdziale?

* U¿ywania przycisków w celu kontrolowania Twojego Micro:bita
* Pokazywania obrazków na Twoim Micro:bicie
* £¹czenia teksu i obrazków

## Mamy przyciski

Jak ju¿ pewnie zauwa¿y³eœ, Micro:bit ma 2 du¿e przyciski: A i B.
Mo¿esz nimi zrobiæ wiele ciekawych rzeczy. Zacznijmy od czegoœ prostego.


```python
from microbit import *

sleep(10 * 1000)
display.scroll(str(button_a.get_presses()))
```

Poczekaj chwilê przed wyœwietleniem kodu!

Wiemy ju¿ mniej wiêcej, co oznacza: ,,from microbit import *". (microbit to modu³, gwiazdka oznacza ,,wszystko", czyli wszystkie modu³y dostêpne do u¿ycia w microbicie). Wiemy te¿, co oznacza: `sleep(10 * 1000)`.

A co znaczy ten fragment: ,,display.scroll(str(button_a.get_presses()))"?

Widzimy, ¿e ta linijka sk³ada siê z kilku ró¿nych pojedynczych instrukcji.

Od œrodka mamy:

1. `button_a.get_presses()`

Ten kod zwraca nam liczbê klikniêæ przycisku A.

2. `str()`

Ta linijka zamienia ,,value", czyli otrzyman¹ liczbê, na string.
String jest jednym z rodzajów danych, jakie rozumie Python (obok np. liczb). Jest to po prostu fragment znaków, liter, czy wyraz, w odró¿nieniu od na przyk³ad liczby.(Liczby mo¿na np. dodawaæ, a stringów ju¿ nie, bo to inny typ danych).
"1" i 1 to ró¿ne wartoœci w Pythonie.  "1" (zapisane w cudzys³owiu) to jest string (czyli wyraz), natomiast 1 to jest liczba, w tym wypadku liczba ca³kowita, czyli po angielsku integer.
Musimy zamieniæ liczbê na string, poniewa¿ komenda ,,dispal.scroll()" rozumie tylko stringi.

3. `display.scroll()`

Tej komendy wczeœniej ju¿ u¿yliœmy. Wyœwietla ona wskazany tekst za poœrednictwem diod.

Podsumowuj¹c wszystko razem:

1. Zbieramy iloœæ klikniêæ przycisku A
2. Zmieniamy ten numer na string
3. Wyœwietlamy wartoœæ na Micro:bicie

Ok, teraz mo¿esz klikn¹æ Flash, by wyœwietliæ swój kod!

### Jak dzia³a ten kod?
### Jak myœlisz, jak mo¿emy poprawiæ ten kod?

### Zadanie

Czy umiesz napisaæ program, który liczy liczbê klikniêæ przycisku B w ci¹gu 5 sekund?

Masz 10 minut!

## Czas na ulepszenie kodu: czêœæ 1#

Ten kod dzia³a, ale chcielibyœmy te¿ dodaæ kilka nowych funkcjonalnoœci:

Chcemy, by przed rozpoczêciem liczenia wyœwietla³o siê odliczanie, np. 3, 2, 1, 0, start! Czyli w skrócie:

* poka¿ odliczanie (np. 3, 2, 1, 0)
* poka¿ liczbê klikniêæ przycisku B
 
```python
from microbit import *

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear() # T¹ linijk¹ ,,czyœcimy" nasz wyœwietlacz :)

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```

## Czas na ulepszenie naszego kodu: czêœæ 2#

Teraz chcemy jeszcze dodaæ tekst przed odliczaniem: ,,Naciœnij przycisk A ¿eby zacz¹æ"

Innymi s³owy chcemy, ¿eby Micro:bit wyœwietla³ nam informacjê, ¿e mamy nacisn¹æ przycisk A, o ile nie jest ju¿ wciœniêty.

Jak mo¿emy to zakodowaæ?

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

Ostatnim krokiem bêdzie mo¿liwoœæ powtórzenia gry.

To oznacza nieskoñczone powtrzanie kodu, który napisaliœmy wczeœniej.

wskazówka: ¿eby powtarzaæ kod w nieskoñczonoœæ musimy u¿yæ komendy ,,while True" (czyli: dopóki prawda, zrób coœ)

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

Micro:bit ma rózne sensory. Jednym z nich jest akcelerometr, którego mo¿emy u¿yæ do rozpoznawania niektórych ruchów.

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

Mo¿esz otrzymaæ aktualne po³o¿enie Micro:bita u¿ywaj¹c komendy: ,,accelerometer.current_gesture()". Ta komenda w wyniku zwróci nam string.

Spróbujmy to zobaczyæ na prostym przyk³adzie:

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

Wyœwietl ten kod!
