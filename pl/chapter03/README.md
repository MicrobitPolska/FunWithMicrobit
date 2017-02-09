# Hello Micro:bit

## Czeg nauczysz siê w tym rozdziale?

* Pokazywaæ tekst na swoim Micro:bicie
* Pêtli

## Jak poprosiæ swojego Micro:bita, ¿eby powiedzia³ ,,Hello!"

Twój Micro:bit mo¿e robiæ wiele róznych rzeczy, ale musisz mu wytlumaczyæ, jak ma je robiæ.
To tak jakbyœ coœ czyta³, uczy³ siê, i musia³ ,,zaimportowaæ" to, co przeczyta³eœ do mózgu.

A teraz czas, by otworzyæ **MuEditor** i wpisaæ kilka pierwszych linijek kodu:

```python
# This is a COMMENT
from microbit import display
```

STOP !

Pomyœlmy o 2 pierwszych linijkach.
Pierwsza linijka zaczyna siê znakiem # i oznacza, ¿e to, co jest za tym znakiem, jest komentarzem.
Komentarz jest ,,niewidoczn¹" dla komputera czêœci¹ kodu, która jest przydatna tylko dla cz³owieka, bo tylko on j¹ widzi. Komentarz to taka notatka dla nas, albo dla innych ludzi, opisuj¹ca co dzieje siê w danym fragmencie kodu.

Kolejna linijka jest ju¿ du¿o wa¿niejsza. Prosimy w niej Pythona, ¿eby zimportowa³ nam modu³ __display__ z modu³u microbit.

Czym jest modu³?
Pomyœlmy o nim jako pewnym konkretnym fragmencie kodu Pythona, napisanym ju¿ wczeœniej przez twórców jêzyka Python, który mo¿emy œci¹gn¹æ (zaimportowaæ), i który pomaga nam w naszej dalszej pracy. 
Czyli ktoœ kiedyœ napisa³ pewne komendy w Pythonie, którymi mo¿emy teraz pos³ugiwaæ siê by nasza zabawa z programowaniem by³a ³atwiejsza.

Teraz mo¿emy poprosiæ Micro:bita, by wyœwietli³ nam poni¿szy tekst:

```python
# To jest ZNÓW komentarz, moglibyœmy tu wpisaæ jak¹œ notatkê, albo cokolwiek innego, to widzi tylko cz³owiek
from microbit import display

display.show("Hello WpiszSwojeImie, I am your Micro:bit")
```

Co tym razem tutaj siê dzieje?

Pierwsza i druga linijka nie s¹ niczym nowym.

A o co chodzi w trzeciej linijce kodu?

U¿ywamy fragmentu kodu, którym jest s³owo _show_ wystêpuj¹ce wewn¹trz kodu, fragemntu kodu, jakim jest s³owo _display_.

Display po angielsku oznacza: wyœwietl, lub te¿ wyœwietlacz, a s³owo show = poka¿.

Spróbujmy teraz napisaæ podobny kod, ale z innym tekstem:

```python

from microbit import display

display.show("Helloo Poland!)
```

Skopiuj ten tekst do swojego edytora Mu i naciœnij Flash!

Mmmm.... czemu otrzymujemy Error, czyli b³¹d?

* Wykrzyknik na koñcu zdania powoduje problem?
* Tekst jest za krótki?
* Potrzebujemy znaku " na koñcu tekstu?
* Helloo (po angielsku powinno byæ ,,Hello") nie jest zapisane poprawnie?

## Ale czemu robiæ to tylko jeden raz?

W naszym kodzie przes³aliœmy Micro:bitowi tekt, który ma wyœwietlaæ. Micro:bit wyœwietla ten tekst tylko raz.
Co zrobiæ, jeœli chceby, by nasz Micro:bit wyœwietla³ nasz tekst ca³y czas?
Musimy przedstawiæ Wam koncepcjê pêtli (pêtla po angielsku to ,,loop").

Za pomoc¹ ,,pêtli" mówimy Micro:bitowi, ¿eby robi³ coœ dopóki jakiœ warunek jest spe³niony.

W Pythonie mamy ró¿ne rodzaje pêtli (czyli ró¿ne loops). Teraz zaczniemy u¿ywaæ jednej z tych pêtli. Pêtla ta nazywa siê: while.

Komenda ,,while" jest komunikatem, który brzmi dok³adnie tak: rób coœ, dopóki warunek, czy te¿ inaczej nasze za³o¿enia s¹ prawdziwe.

```python
from microbit import display

while 1>0:
  display.show("Hello Poland!")
```

Teraz spróbujmy w takim kodem:

```python
from microbit import display

while 1<0:
  display.show("Hello Poland!")
```

W³aœnie zmieniliœmy warunek na coœ, co jest zawsze nieprawdziwe.

## Jaka jest ró¿nica miêdzy tymi dwoma fragmentami kodu?

## Czemu komenda ,,display" nie jest napisana tu¿ pod s³owem ,,while"?
