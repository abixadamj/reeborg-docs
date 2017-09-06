Zagadnienia zaawansowane
========================

Świat Reeborg-a zaprojektowano by ułatwić tworzenie zadań programistycznych
oraz dostarczać informację o postępach uczniowi.
Czasem jednak dodatkowe ustawienia mogą być potrzebne.
Ten podrozdział zawiera opisy ustawień, które być może już
pojawiły się w innych miejscach.

Proste zadanie
--------------

Rozważmy na początek proste zadanie. Wykonaj następujące::

    World("Demo 1")

Zadanie przed wykonaniem wygląda tak:

|simple_demo1|

.. |simple_demo1| image:: ../../images/simple_demo1.png

i po wykonaniu:

|simple_demo1f|

.. |simple_demo1f| image:: ../../images/simple_demo1f.png

Zadanie jest zapisane jako odnośnik bezpośredni, włączając kod w edytorze i bibliotece;
jest możliwe do wybrania na liście rozwijanej ze światami.


Zmiana śladu: style
-------------------

Domyślnie Reeborg zostawia ślad "niewyśrodkowany" by łatwiej pokazać kierunek
poruszania się i obrotów. Jeśli nie ma potrzeby by zaznaczać kierunek, to można zmienić na linię
wycentrowaną używając kodu::

    set_trace_style("thick")

W wyniku otrzymamy taki ślad:

|simple_demo2|

.. |simple_demo2| image:: ../../images/simple_demo2.png

Gdy robot wykonuje skomplikowane manewry i nie ma potrzeby zaznaczania śladu, to zamiast
"thick" użyj "none". W zwykłym stylu jest użyte "default" i jest ustawione automatycznie.


.. important::

    ``set_trace_style`` z wartościami ``"thick"`` lub ``"default"`` jest funkcją globalną,
    która zmienia ślady wszystkich robotów. Jeśli jest wywoływana wiele razy wewnątrz programu,
    to ostatnie wywołanie zostaje zastosowane.

    Wybierając ``"none"`` ślad jest rysowany kolorem przezroczystym, który może być nadpisany.
    Jak pokazano niżej, roboty mogą mieć różnokolorowe ślady.

Zmiana śladu: color
-------------------

Roboty mogą zostawiać ślad różnego koloru lub nawet zmieniać kolor śladu wzdłuż ścieżki
w dowolnym miejscu programu.
Uruchom::

    World("Demo 2")

aby zobaczyć przykład. Prawidłowe nazwy kolorów użyte jako argument funkcji ``set_trace_color()``
mogą zawierać nazwy dostępne w HTML lub wartości RGB i RGBA. Ten ostatni sposób pozwala ustawiać
pozwala ustawić poziom przezroczystości.


|simple_demo2b|

.. |simple_demo2b| image:: ../../images/simple_demo2b.png


Ustawianie modelu robota
------------------------

Wybór modelu robota przez użytkownika jest możliwy po kliknięciu przycisku z obrazem modelu
na górze planszy.

|models|

.. |models| image:: ../../images/models.png

Wszystkie roboty normalnie ustawiane są na ten sam model.
Gdy tworzymy robota jest możliwe przypisanie mu numeru modelu (liczba całkowita
od 0 do 3) tak jak w przykładzie::

    reeborg = UsedRobot()
    reeborg.set_model(0)

Pokazane jest w przykładzie::

    World("Demo 2")


Losowe światy
-------------

Początkowa pozycja robota na niektórych swiatach może być wybierana losowo na wyznaczonych
do tego celu polach. W tym przypadku obraz możliwych pól będzie lekko transparentny.

Ilość przedmiotów także może być wybierana losowo z podanego przedziału. W takim przypadku
można wymagać, by wszysktie przedmioty okreslonego typu pojawiły się w zadanej lokalizacji.
Początkowo, gdy świat jest rysowany pojawia się znak zapytania zamiast liczby przedmiotów. Po
uruchomieniu programu pojawiają się wartości.

Końcowa pozycja robota także może być ustalana losowo z zadanego zbioru kratek.

Przykład użycia elementów losowych::

    World("Demo 3")

|simple_demo3|

.. |simple_demo3| image:: ../../images/simple_demo3.png


Uruchamianie dodatkowego kodu uruchamianego przed/po
----------------------------------------------------

Można dodać kod, który będzie uruchomiony przed lub po
właściwym programie w edytorze.



.. warning::

   Jeśli jest kod *post* a użytkownik użyje funkcji ``done()``
   w swoim programie, wtedy *post* się nie wykona.
   Należy przedefiniować ``done()`` w części **pre**, np. coś s stylu::

        def done():
            raise ReeborgError("Nie powinieneś używać funkcji 'done()'.")

|pre_post_code|

.. |pre_post_code| image:: ../../images/pre_post_code.png

Prosty przykład użycia tej funkcjonalności można zobaczyć w 
**Pre & Post code demo**
po uruchomieniu programu przed częścią dostępną w edytorze oraz po
jest wyświetlany komunikat.
Bardziej rozbudowany przykład z użyciem funkcji ``narration()`` jest dostępne
w świecie **Story**. This program adds a "twist" to the story, simply
included for effect: make sure to let the program
run to the end.


Zamiana domyślnego robota
-------------------------

Modyfikując lub tworząc świat można także dodać robotowi większe możliwości.
Na przykład, chąc pokazać jak powinien poruszać się robot by rozwiązać zadanie.
Jeden ze sposobów:

1. Wykonaj kopię świata.
2. Usuń robota
3. Zapisz świat pod inną nazwą (jeśli używasz tej samej przeglądarki do pokazania
   przykładu) lub na dysku (jeśli świat ma być dostępny w innej przeglądarce, np.
   jako praca domowa lub w klasie)
4. Napisz program który najpierw tworzy robota z wymaganą funkcjonalnością.

Sposób powinien zadziałać ... z niespodzianką - nie będzie widać robota na początku.

Jest lepsza metoda!

.. note::

   Używając kodu w sekcji *pre* lub bibliotece upewnij się, że wykonywana linia nie jest
   "podświtlona" oraz nie widać robota na planszy.

Użycie w "pre" lub w bibliotece instrukcji::

   RUR.world.remove_robots()

jako pierwszej a później stworzenie instancji robota z wymaganą funkcjonalnością.
Jeśli na planszy jest tylko jeden robot, to podstawowe instrukcje ``move()`` lub ``turn_left()``
będą działać. Nie ma potrzeby używania nazwy instancji.

W świecie **Robot replacement** można zobaczyć przykład robota z zaimplementowaną
funkcją obrotu w prawo, jest ona dostępna w bibliotece i zamienia domyślnego robota.

Wspólna praca z TogetherJS
--------------------------

W **Additional menu** u góry ekranu można znaleźć pozycję 
"Collaboration": która aktywuje skrypt z Mozilla TogetherJS który pozwala dwóm lub
więcej użytkownikom na efektywną współpracę na tej samej stronie.

Wykonywanie programu "wprzód"  i "wstecz"
-----------------------------------------

Programy są wykonywane w dwóch kierunkach: jest zmieniana część "ramek" opisująca
kompletny stan świata w danej chwili lub zmiany te są cofane.

W **Additional menu** jest przycisk "step back"
cofania o jedną ramkę.

Przykład użycia: wstawiamy funkcję ``pause()`` w interesującym fragmencie programu.
Można teraz zademonstrować jakiś problem cofając lub wykonując normalnie po jednej ramce.

Wsparcie językowe
-----------------

Na chwilę obecną w pełni wspieranymi językami są francuski i koreański.
Wykonując kod dostajemy francuskie nazwy funkcji::

    from reeborg_fr import *

    avance()           # equivalent to move()
    tourne_a_gauche()  # equivalent to turn_left()

Francuzkojęzyczni użytkownicy powinni używać http://reeborg.ca/monde.html
gdzie jest zmienione także UI.

Użycie standardowej biblioteki Python
-------------------------------------

Brython zawiera pokaźną ilość standardowej biblioteki Python.
Dostępne są tylko moduły samego Python-a.


Pisanie programów w innych językach programowania
-------------------------------------------------

Dostępne są języki Python, Javascript i CoffeScript. Pozostałe języki
mogą być dostępne jeśli mają transpiler do javascript.

Osadzanie w iframe
------------------

.. todo::

    Można osadzić Świat Reeborg-a na dowolnej stronie używając html-owego
    ``iframe``. Powinienem pokazać jak to zrobić.

Integracja z platformami edukacyjnymi
-------------------------------------

Nauczyciel z Litwy osadził Świat Reeborg-a na Moodle. Najlepiej
sprawdza się to wtedy, gdy mamy uruchomioną lokalnie kopię Świata Reeborg-a.

.. _changing-the-user-interface:

Zmiana interfejsu użytkownika
-----------------------------

Jeśli znasz Javascript, html, css i wiesz jak używać jQuery można dostosować
wygląd Świata Reeborg-a przez uruchomienie specjalnie przygotowanego odnośnika bezpośredniego.
Zmiany pozostaną na stronie, do momentu przeładowania strony.

Jeśli potrzebujesz zrobić pewne zmiany, to otwórz Świat Reeborga w oddzielnej zakładce
i włącz konsolę javascript. Później użyj funkcji Javascript/jQuery aby zmienić UI według potrzeb.
Skopiuj **cały** swój kod (nie zapominając o średnikach...) w pole tekstowe niżej.

Przykładowo chcesz ukryć możliwość przełączania języka: wpisz następujące polecenie jQuery:

.. code-block:: javascript

    $("#header-child form").hide();

Możesz użyć powyższego przykładu i skopiować go to pola tekstowego i klikając przycisk
"Create permalink code" otrzymasz rezultat poniżej. Należy wszystkie zmiany w UI stworzyć
w jednym kroku. Mając rezultat skopiuj go i *załącz go* do "normalnego" odnośnika bezpośredniego
stworzonego Świata Reeborg-a. Nowy odnośnik bezpośredni, gdy zostanie użyty zmienia interfejs
użytkownika Świata Reeborg-a.


.. raw:: html
   :file: css_mod.html

Jeśli potrzebujesz pomocy w zmianie interfejsu użytkownika możesz skontaktować się ze mną.
