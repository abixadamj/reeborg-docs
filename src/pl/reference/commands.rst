Podstawowe instrukcje
=====================

.. topic:: Informacja dla zaawansowanych użytkowników

    Świat Reeborg-a używa składni Python-a 3 (dzięki skryptowi Brython) i
    używa stylu nazewnictwa zalecanego w PEP 8 (z niewielkimi wyjątkami).
    
.. topic:: Informacja dla początkujących użytkowników

   *Mamy problem!* Jako zupełny nowicjusz, jeśli nic nie wiesz o Python-ie
   (i programowaniu), możesz opis używany do zilustrowania jak działają
   podstawowe instrukcje uznać za zagmatwany. Mimo wszystko do wyjaśnienia
   składni Python-a potrzebujesz wiedzieć co podstawowe polecenia robią...

   Moja rada: przeczytaj wszystko raz nie tracąc wiele czasu jeśli coś jest
   skomplikowane. Później przeczytaj dwa rozdziały, pierwszy o obiektach,
   które można znaleźć w świecie Reeborg-a a następnie krótkie wprowadzenie
   do Python-a, gdzie możesz znaleźć wiele przykładów. Później wróć tu ...
   i wszystko będzie prostsze.

W tym podrozdziale przyjżymy się prostym światom i opiszemy polecenia które
Reeborg może wykonać. Polecenia są funkcjami Python-a. W Python funkcja o
nazwie ``my_function`` jest wykonywana gdy jest "wywołana" przez umieszczenie
jej nazwy zakończonej nawiasami: 
``my_function()``.

W całym podrozdziale, za wyjątkiem jednego przykładu na końcu, korzystamy
z funkcji bez argumentów. [Jeśli nie wiesz czym jest *argument* funkcji,
to wyjaśnimy to dalej.]

Będziemy wykorzystywać dwa typy funkcji:

1. Proste akcje które Reeborg ma wykonać, np. ``move()``.

2. Otrzymując informacje, które Reeborg ma uzyskać, np. ``front_is_clear()``
   po wykonaniu funkcji Reeborg będzie wiedział czy przed nim jest przeszkoda.

W przedstawianych przykładach będziemy korzystać z specjalnych słów znanych
Python-owi, np. ``while``, ``True``, i ``not``.


Poruszanie
----------


``move()``
***********

Świat Reeborg-a jest określony na siatce. Reeborg znajduje się w jednej z kratek.
Po otrzymaniu polecenia Reeborg może pozostać w swojej kratce **albo** przejść na inną.
Polecenie ``move()`` powoduje, że Reeborg przesuwa się na sąsiednią kratkę.

=================  =================
Before ``move()``   After ``move()``
-----------------  -----------------
|move_e_before|    |move_e_after|
|move_n_before|    |move_n_after|
|move_w_before|    |move_w_after|
|move_s_before|    |move_s_after|
=================  =================



.. |move_e_before| image:: ../../images/move_e_before.png
.. |move_e_after| image:: ../../images/move_e_after.png
.. |move_n_before| image:: ../../images/move_n_before.png
.. |move_n_after| image:: ../../images/move_n_after.png
.. |move_w_before| image:: ../../images/move_w_before.png
.. |move_w_after| image:: ../../images/move_w_after.png
.. |move_s_before| image:: ../../images/move_s_before.png
.. |move_s_after| image:: ../../images/move_s_after.png

Funkcja ``move()`` może zakończyć się błędem i zatrzymać wykonywanie programu
jeśli na ścieżce Reeborg-a jest przeszkoda.


``turn_left()``
***************

Funkcja ``turn_left()`` obraca Reeborga o 90 stopni w jego lewo (przeciwnie
do ruchu wskazówek zegara).
Funkcja nie może skończyć się z błędem.

|turn_left|

.. |turn_left| image:: ../../images/turn_left.gif

Przenoszenie przedmiotów
------------------------


.. important::

    W tym podrozdziale zakładamy, że świat w którym jest Reeborg
    ma tylko jeden przedmiot w danym momencie.

``take()``
************

Funkcja ``take()`` powoduje, że Reeborg podnosi przedmiot znajdujący
się na tej pozycji. Funkcja może zakończyć się błędem jeśli przedmiotu
tam nie ma lub znajdują się dwa przedmioty i nie wiadomo który
podnieść.

``put()``
************

Funkcja ``put()`` powoduje, że Reeborg opuszcza przedmiot który posiada.
Funkcja może zakończyć się błędem jeśli Reeborg nie niesie przedmiotu lub
posiada więcej niż jeden przedmiot i nie wiadomo który zostawić.

|take_put|

.. |take_put| image:: ../../images/take_put.gif

Odpytywanie Reeborg-a o otoczenie i pozycję
-------------------------------------------

Reeborg ma ograniczone pozstrzeganie jednak wystarczające by pomóc mu
wykonać potrzebne zadania.


``is_facing_north()``
**********************

Reeborg jest proszony o odpowiedź czy jest skierowany na północ
(w górę ekranu komputera).

|is_facing_north|

.. |is_facing_north| image:: ../../images/is_facing_north.gif


``at_goal()``
*************

Reeborg jest proszony o odpowiedź, czy jest w końcowym położeniu czyli
jakie miał osiągnąć w zadaniu.

|at_goal|

.. |at_goal| image:: ../../images/at_goal.gif


``front_is_clear()``
********************

Reeborg jest proszony o odpowiedź, czy przed nim znajduje się przeszkoda
(np. ściana). W przykładzie użyta jest także funkcja ``think()``
która jest opisana na dole tej strony.


|think|


``right_is_clear()``
********************

Reeborg jest proszony o odpowiedź, czy z jego prawej strony jest przeszkoda.
W przykładzie Reeborg podąża wzdłóż ściany po jego prawej stronie dopóki
nie znajdzie przejścia (i ``right_is_clear()`` zwróci ``True``).
W tym miejscu każemy zabudować przejście używając funkcji ``build_wall()``
opisanej na końcu tej strony.

|build_wall|


``object_here()``
******************

Reeborg proszony jest o sprawdzenie czy znajduje się w tym miejscu
co najmniej jeden przedmiot.

``carries_object()``
**********************

Reeborg proszony jest o sprawdzenie czy niesie co najmniej jeden
przedmiot.

W przykładzie używamy obu funkcji ``object_here()`` i
``carries_object()`` aby pomóc Reeberg-owi zebrać wszystkie przedmioty
i zanieść je w jedno miejsce. Gdy jest więcej niż jeden przedmiot
w danej kratce, to pojawiająca się liczba wskazuje ich ilość.


|object_here|

.. |object_here| image:: ../../images/object_here.gif


Przerywanie
-----------

``pause()``
***********

Funkcja zatrzymuje wykonywanie programu Reeborga w tym
miejscu i czeka na kliknięcie przycisku "run" lub "step"
by wykonywać program dalej.


``done()``
***********

Kończy program Reeborga, niekoniecznie wszystkie linie programu
muszą być uruchamiane.

W przykładzie użyto funkcji ``pause()`` i ``done()`` aby przerwać
normalne wykonywanie programu.

|pause|

.. |pause| image:: ../../images/pause.gif



``think()``
***********

Jeśli potrzebujesz aby Reeborg dostał trochę czasu między
instrukcjami, bo musi "pomyśleć" o co go prosisz.
Można wskazać ile czasu ma na "pauzę" przekazując do funkcji
``think()`` argument, tak jak tu:

.. code-block:: python

    think(500)

Liczba ``500`` znajdująca się w nawiasach nazywana jest *argumentem*
funkcji. Mniejsza liczba, mniej czasu na przerwę. Wartość 1000
oznacza jedną sekundę. 

|think|

.. |think| image:: ../../images/think.gif



Zmiana świata
-------------

``build_wall()``
****************

Reeborg może budować ściany, tuż przed miejscem zatrzymania, jak
widzieliśmy wcześniej. Funkcja może skończyć się błędem jeśli
ściana już znajduje się w tym miejscu.

|build_wall|

.. |build_wall| image:: ../../images/build_wall.gif

|build_wall_fail|

.. |build_wall_fail| image:: ../../images/build_wall_fail.gif
