Szybkie wprowadzenie do Świata Reeborg-a
========================================

Uruchamianie programu
----------------------

Poniżej uruchomiono przykładowy program. Animacja zawiera numery scen a tu krótki ich opis:

1. Klikając na przycisk "run" (czerwone koło), program w edytorze (zielony prostokąt) zaczyna
   działać i robot (niebieski prostokąt) wykonuje instrukcje. Po zakończeniu okno dialogowe
   (czerwona strzałka) informuje, czy program wykonano pomyślnie czy z błędem. Program
   kończy się dość szybko.
2. Jednorazowe uruchomienie całego programu możemy zastąpić pracą krokową instrukcja po
   instrukcji. Należy użyć przycisku oznaczonego czerwonym kółkiem. Mamy wtedy kontrolę nad szybkością
   wykonywania instrukcji. Wykonywana instrukcja jest podświetlona w edytorze (zwykle jest to jedna linia).
3. Przy podświetlaniu instrukcji jest wykonywany dodatkowy ukryty program. W pewnych rzadkich
   przypadkach, np. bardziej złożonych programach, ten dodatkowy kod może sprawiać problemy.
   Jeśli zajdzie taka konieczność, to jest możliwe wyłączenie podświetlania instrukcji.
4. Domyślny obraz Reeborg-a może być zmieniony przez użytkownika.

|running|

Informacje zwrotne
------------------

Świat Reeborg-a jest zaprojektowany do prostego przekazywania informacji
zwrotnej gdy napotyka problem (np. Reeborg uderza o ścianę, gdy próbuje ruszyć
lub próbuje podnieść przedmiot którego nie ma). Wiele różnych "światów/zadań" może być
stworzonych, które by ukończyć należy pokierować Reeborg-a by znalazł się na określonej
pozycji lub przesunął przedmioty do oznaczonych miejsc. Niżej można zobaczyć cztery
przykłady.

|feedback|


Tworzenie nowych światów i zadań
--------------------------------

Tworzenie nowego świata lub podstawowych zadań jest ułatwione gdy
korzysta się z edytora świata. Światy są przechowywane przez przeglądarkę
i mogą być eksportowane jako pliki formatu json (tylko świat). Światy
i zadania mogą być też otrzymywane jako specjalnie spreparowane adresy URL,
które zawierają także kod zapisany w edytorze i bibliotekach.

|edit-world|

.. |running| image:: ../../images/running_programs.gif
.. |feedback| image:: ../../images/feedback.gif
.. |edit-world| image:: ../../images/edit_world.gif
