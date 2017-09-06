Sokoban
=======

.. figure:: ../../images/sokoban_ani.gif
   :figwidth: 55%
   :align: left

   "Sokoban ani" by Carloseow at English Wikipedia.
   Licensed under CC BY 3.0 via Wikimedia Commons -
   http://en.wikipedia.org/wiki/Sokoban#/media/File:Sokoban_ani.gif

Cytat z http://pl.wikipedia.org/wiki/Sokoban

*Plansza składa się z układu kwadratów, część z nich to ściany przez które
nie może przechodzić gracz ani skrzynia. Sokoban jest grą, w której dozorca
w hurtowni musi przesuwać przedmioty (zwykle paczki, piłki lub skrzynie) na
odpowiednie miejsca, przy jak najmniejszej liczbie wykonanych ruchów
(lub pchnięć, w zależności od kryteriów punktowania). Dozorca może pchać
tylko jedną paczkę, nie można ich ciągnąć, ani przez nie przechodzić.*


Sokoban i Świat Reeborg-a
-------------------------

Świat Reeborg-a umożliwia rozwiązywanie łamigłówek Sokoban.
Kontrola ruchów Reeborg-a jest możliwa przez wydawanie poleceń, klawisze
strzałek nie są używane. Tak jak w Sokoban pudełka nie można przesunąć na drugie
pudełko czy ścianę. Odwrotnie niż w Sokoban taka próba kończy
się błędem.

|sokoban_wiki|

Łamigłówkę można rozwiązywać używając funkcji ``move()`` i ``turn_left()`` ...
lecz jest to monotonne. Mogłoby to spowodować wyciek oleju z Reeborg-a.
Dużo łatwiejsze jest zaimportowanie funkcji ``up()``, ``down()``, ``left()``
i ``right()`` z biblioteki **sokoban** i ich użycie. Ponadto można używać
wtedy klawiszy strzałek. Zaimportowane funkcje mogą mieć opcjonalnie argument
liczbowy mówiący ile kratek w danym kierunku należy się przemieścić. Pozwala
to pisać krótszy program.

Użycie biblioteki **sokoban** zatrzymuje też wycieki oleju z Reeborg-a.

Kolejne wyzwania
----------------

Ponieważ pudełka spychane do wody automatycznie tworzą most, to
pozwala na tworzenie zadań, których w oryginalnym Sokoban nie spotykamy.

|sokoban2|

.. |sokoban_wiki| image:: ../../images/sokoban_wiki.gif
.. |sokoban2| image:: ../../images/sokoban2.gif


Ponadto dodanie tafelek z lodem (**ice**) podnosi poziom wyzwań.

Dlaczego Sokoban?
-----------------

Zadania logiczne w Sokoban mogą stanowić duże wyzwanie. Z moich obserwacji wynika,
że dużo trudniej jest je rozwiązać pisząc program niż przy pomocy klawiszy strzałek.
[**Notatka osobista**: *zaimplementuj tryb ze strzałkami i zapisem ruchów.*]

Pozwala także początkującym użytkownikom na zapoznanie się z instrukcjami sterującymi
(``if/elif/else/while/...``) wykonywaniem funkcji do przemieszczania robota.

Gdy łamigłówka zostanie rozwiązana przy pomocy funkcji ``up(), down(), left(), right()``,
można spróbować przełożyć rozwiązanie, by używać tylko ``move()`` i ``turn_left()``.

Sokoban dla zaawansowanych
--------------------------

.. Topic:: Tylko ekspertom

   **Tekst nie będzie miał sensu, chyba że jesteś zaawansowanym programistą.**

    Łamigłówka Sokoban może być rozwiązana poprzez techniki wyszukiwania
    znane zaawansowanym użytkownikom. Do skorzystania z tego sposobu
    potrzebna jest wiedza jak przekazać informacje o świecie do programu.
    Świat jest reprezentowany przez obiekt (tylko właściwości, bez metod)
    w języku javascript. Obiekt ten jako tekst json należy zapisać do
    słownika w Python. Program niżej wykonuje to zadanie.

    .. code-block:: python

        import json  # very incomplete Brython module
        from browser import window

        # First, use the builtin JSON Javascript function as it can
        # show a nicely formatted representation of the world;
        # this should have been implemented in the Brython json module
        # but is currently missing.
        world_str = window.JSON.stringify(RUR.current_world, None, 2);
        print(world_str)

        # Convert the json world representation into a Python dict
        # using Brython's json module.
        world_dict = json.loads(world_str)

        # We can now use Python's standard notation for dicts and lists
        # to extract the required information.
        print(world_dict["robots"][0]["orientation"] == RUR.EAST)


