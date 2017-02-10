# Pick&Mix

## Czego nauczysz się w tym rozdziale?

* Łączenia tego, co się nauczyłeś, do tworzenia czegoś zupełnie nowego!

Dobierzcie się w kilkuosobowe grupy i pracujcie teraz razem. Jeśli będziecie potrzebować pomocy, to mówcie

## Programiści Pythona
Jeśli potrzebujecie pomocy, możescie zajrzeć do [Micro:bit Micropython docs](https://microbit-micropython.readthedocs.io).


## Ćwiczenie nr 1 - Wyświetl choinkę
Święta się skończyły, ale choinki są zawsze fajne.
Spróbuj stworzyć choinkę i wyświetlić ją na Micro:bicie.

Wskazówka:
* Pamiętaj, żeby użyć Image()

## Ćwiczenie nr 2 - Wyświetl przycisk, który nacisnąłeś
W tym ćwiczeniu spróbuj napisać program, który wyświetli nazwę przycisku, który wcześniej naciśniesz.

Wskazówka:
* Masz tylko 2 przycisku __A__ i __B__
* spróbuj użyć "if"
* użyj "is_pressed()""

## Ćwiczenie nr 3 - Wstrząśnij i wyświetl wiadomość!
Celem tego ćwiczenia jest napisanie programu, który wyświetla inną wiadomość za każdym razem, jak wstrząśniesz swoim Micro:bitem.

Wskazówki:
* możesz umieścić wszystkie swoje wiadomości wewnątrz listy (stworzyć listę wiadomości)
* użyj `accelerometer.was_gesture("shake")`
* wybierz przypadkową wiadomość za pomocą komendy random.choice(messages)

## Ćwiczenie nr 4 - Pokaż pozycję swojego Micro:bita
W Micro:bicie znajduje się akcelerometr, czyli czujnik, który pokazuje pozycję, w jakiej znajduje się Micro:bit.
Spróbuj stworzyć program, który pokazuje pozycję Twojego Micro:bita za pomocą strzałki.

Wskazówki:
* Weź pod uwagę tylko pozycje takie jak `up`, `down`, `left` and `right`
* Zbuduj strzałki, używając komendy Image()
* Użyj `accelerometer.current_gesture()` żeby uzyskać informację o położeniu Micro:bita
* Nie zapomnij o użyciu `while True:`

## Ćwiczenie nr 5 - Użyj radia
Spróbuj zbudować proste tekstowe walkie-talkie z kilkoma osobami.
Wybierz wiadomość i wyślij ją za każdym razem, kiedy naciśniesz przycisk (A lub B).

Wskazówki:
* Pamiętaj, żeby wywołać radio: `radio.on()`
* Kiedy otrzymasz wiadomość, wyświetl ją na ekranie diodowym
* Upraszczając załóżmy, że tylko jeden Micro:bit naraz będzie wysyłał wiadomość