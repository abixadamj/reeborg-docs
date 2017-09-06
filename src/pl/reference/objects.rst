==============================
 Przedmioty, obrazy tła, itp.
==============================

Oprócz ścian, które blokują ruch Reeborg-owi jest jeszcze pewna liczba
obrazów które są użyte do przedstawienia różnych przedmiotów.


Podstawowe przedmioty
=====================

Reeborg może wchodzić w interakcje z różnymi przedmiotami.
Może je podnosić i opuszczać przy pomocy funkcji ``take()``
i ``put()``. W szczególności |token| **token** jest jego ulubionym przedmiotem.
Żeton (ang. **token**) jest jak moneta, chociaż większość ludzi uważa, że mają
małą wartość, zwłaszcza z uśmiechniętą twarzą; Reeborg uważa inaczej.

Jeśli jest więcej niż jeden przedmiot i Reeborg potrzebuje wybrać jeden z nich
aby podnieść lub opuścić, należy użyć nazwy przedmiotu w apostrofach lub cudzysłowiu
``put("token")`` lub ``take('token')``. Na takie nazwy mówimy łańcuch lub string.
[apostrofy i cudzysłowy muszą być w parach - nie można pisać ``take('token")``]

Oprócz żetonów, Reeborg może przenosić wiele innych geometrycznych kształtów, owoców,
kwiatów, warzyw, itp. [Wiele obrazów pochodzi z http://openclipart.com]


:apple: |apple|
:banana: |banana|
:carrot: |carrot|
:daisy: |daisy|
:dandelion: |dandelion|  Chociaż są ładne, mniszki lekarskie są uważane za chwasty i często należy je usuwać
  ze świata Reeborg-a. 
:leaf: |leaf|  Reeborg nie lubi liści. Obecność liścia (lub liści) w Świecie Reeborg-a
  zwykle oznacza jesień i Reeborg musi je grabić zamiast grać.
  Reeborg zawsze wolałby grać.
:orange: |orange|
:strawberry: |strawberry|
:tulip: |tulip|
:square: |square|
:star: |star|
:triangle: |triangle|  Trójkąt takiego kształtu może istnieć tylko w Świecie Reeborg-a. Tak wygląda
  powiększony trójkąt.

|impossible-triangle|

Przedmioty dekoracyjne
======================

Przedmioty pokazane wyżej mogą być rysowane jako dekoracyjne. Reeborg nie może
ich wtedy przenosić oraz nie mogą być celem zaliczenia zadania.

Ilość "normalnych" przedmiotów w danym miejscu jest wyświetlana jako liczba,
a przedmioty dekoracyjne nie są zliczane.

Tafelki z tłem
==============

:grass: |grass| |pale_grass| Nieszkodliwe dla Reeborga przy chodzeniu.
:gravel: |gravel|  Nieszkodliwe dla Reeborga przy chodzeniu.
:water: |water| Reeborg może się utopić. Na szczęście Reeborg może ją wykryć funkcją
  ``front_is_clear()``.
:mud: |mud| Może skutecznie zablokować Reeborga. Błota (ang. *mud*) Reeborg nie może wykryć.
:brick wall: |bricks|  Reeborg może zderzyć się z murem; może też go wykryć używając funkcji
  ``front_is_clear()``.
:ice: |ice| Lód powoduje, że Reeborg ślizga się do następnego kafelka. Może to być problemem
  gdy znajdzie się tam tafelek z przeszkodą. Reeberg nie może wykryć lodu.

|slip|


Obraz tła
=========

Można wybrać pojedynczy obraz użyty jako tło całego świata wskazując adres (URL)
gdzie plik z obrazem się znajduje.

Podczas edycji świata siatka jest rysowana powyżej obrazu tak, że jest on widzialny;
w trybie wykonywania siatka jest rysowana za obrazem. "Rzeczywiste" ściany
są rysowane powyżej tła i przez to są widoczne.

Obraz tła nie jest skalowany w żadnym kierunku (wyjątkiem jest gdy użyto małego tafelka).
Chcąc wyznaczyć rozmiar wymaganego obrazu, wystarczy obliczyć liczbę kwadratów siatki:
każdy kwadrat ma bok 40 pikseli.


Przedmioty specjalne
====================

Przedmioty specjalne, podobnie jak normalne są rysowane powyżej tła.
Nie mogą być podniesione przez Reeborg-a i mogą zmienić zachowanie tafelka.

:bridge: |bridge|  Pozwala aby Reeborg przeszedł bezpiecznie przez wodę.
  Reeborg powinien zawsze wchodzić na niego chcąc przejść przez wodę.
:fences:  |fence_right| - |fence_left| - |fence_double| - |fence_vertical|
  Może być wykryte przez Reeberga-a. Jeśli Reeborg będzie poproszony o przejście
  przez płot, to mu się nie uda. Do stworzenia zamkniętego obszaru może być
  konieczne użycie kilku rodzajów płotu na niektórych tafelkach. 
:box: |box| Pudełka mogą być przesuwane wzdłuż ścieżki przez Reeborg-a ... pod warunkiem,
  że ściana, inne pudełko, itp. nie zablokuje ruchu. Pudełko przesunięte do wody tworzy most
  pozwalając Reeborg-owi bezpiecznie przejść przez wodę. Zobacz przykład.
  
|box-blocked|

Cele
====

Reeborg musi osiągać pewne cele, jak dojście do określonej pozycji, przeniesienie określonych
przedmiotów na wyznaczone miejsca. Miejsca te są oznaczone kolorem szarym:

|apple_goal| |banana_goal| |carrot_goal|
|daisy_goal| |dandelion_goal| |leaf_goal| |orange_goal|
|strawberry_goal| |tulip_goal| |square_goal| |star_goal|
|triangle_goal| |token_goal|


Gdy Reeborg do zakończenia zadania powinien znaleźć się na określonej pozycji,
to używany jest jeden z obrazów:

|green_home_tile| |house| |racing_flag|

.. |green_home_tile| image:: ../../../src/images/green_home_tile.png
.. |house| image:: ../../../src/images/house.png
.. |racing_flag| image:: ../../../src/images/racing_flag.png

.. |apple| image:: ../../../src/images/apple.png
.. |banana| image:: ../../../src/images/banana.png
.. |carrot| image:: ../../../src/images/carrot.png
.. |daisy| image:: ../../../src/images/daisy.png
.. |dandelion| image:: ../../../src/images/dandelion.png
.. |leaf| image:: ../../../src/images/leaf.png
.. |orange| image:: ../../../src/images/orange.png
.. |strawberry| image:: ../../../src/images/strawberry.png
.. |tulip| image:: ../../../src/images/tulip.png
.. |square| image:: ../../../src/images/square.png
.. |star| image:: ../../../src/images/star.png
.. |triangle| image:: ../../../src/images/triangle.png
.. |impossible-triangle| image:: ../../images/impossible-triangle.png
.. |token| image:: ../../../src/images/token.png

.. |grass| image:: ../../../src/images/grass.png
.. |pale_grass| image:: ../../../src/images/pale_grass.png
.. |gravel| image:: ../../../src/images/gravel.png
.. |ice| image:: ../../../src/images/ice.png
.. |water| image:: ../../../src/images/water.png
.. |mud| image:: ../../../src/images/mud.png
.. |bricks| image:: ../../../src/images/bricks.png
.. |slip| image:: ../../images/ice_slip.gif

.. |bridge| image:: ../../../src/images/bridge.png
.. |box| image:: ../../../src/images/box.png
.. |fence_right| image:: ../../../src/images/fence_right.png
.. |fence_left| image:: ../../../src/images/fence_left.png
.. |fence_double| image:: ../../../src/images/fence_double.png
.. |fence_vertical| image:: ../../../src/images/fence_vertical.png
.. |box-blocked| image:: ../../images/box_blocked.gif

.. |apple_goal| image:: ../../../src/images/apple_goal.png
.. |banana_goal| image:: ../../../src/images/banana_goal.png
.. |carrot_goal| image:: ../../../src/images/carrot_goal.png
.. |daisy_goal| image:: ../../../src/images/daisy_goal.png
.. |dandelion_goal| image:: ../../../src/images/dandelion_goal.png
.. |leaf_goal| image:: ../../../src/images/leaf_goal.png
.. |orange_goal| image:: ../../../src/images/orange_goal.png
.. |strawberry_goal| image:: ../../../src/images/strawberry_goal.png
.. |tulip_goal| image:: ../../../src/images/tulip_goal.png
.. |square_goal| image:: ../../../src/images/square_goal.png
.. |star_goal| image:: ../../../src/images/star_goal.png
.. |triangle_goal| image:: ../../../src/images/triangle_goal.png
.. |token_goal| image:: ../../../src/images/token_goal.png
