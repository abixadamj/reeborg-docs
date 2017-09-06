Tworzenie własnych światów
==========================

Możesz stworzyć własną kolekcję światów i uczynić ją dostępną
wszystkim zainteresowanym. Najczęściej spotykanym sposobem
udostępniania światów jest udostępnienie ich w Internecie
(np. Github lub własna strona) z odpowiednio przygotowanym menu.
Nim wyjaśnię jak to zrobić zobaczmy w jaki sposób można uruchomić
świat.

Domyślne światy
---------------

.. figure:: ../../images/select.png
   :figwidth: 20%
   :align: left

   Domyślne swiaty są pokazane na białym tle. Stworzone lokalnie i zapisane
   w przeglądarce mają kolorowe tło.

Świat Reeborg-a posiada kilka domyślnych światów. Poprzednio załączane światy
służyły do nauki Python-a z tej strony. Obecnie załączane światy są wybierane
by pokazać specyficzne właściwości, które są opisane gdzieś w tej dokumentacji
lub na blogu.

Domyślne światy można wybrać z listy rozwijanej umieszczonej w górnej części strony.


Tworzenie światów
-----------------

.. note::

    Tworzenie i edycja światów jest opisana szczegółowo w innej części

Gdy tworzysz nowy świat (lub edytujesz istniejący) możesz wybrać opcję
do automatycznego zapisu w magazynie danych twojej przeglądarki (ang. *local storage*)
Po zapisaniu jest on dostępny na liście rozwijanej do wybierania świata.
Domyślne światy są pokazane na liście na białym tle, zaś światy zapisane w przeglądarce
mają kolorowe tło.

Możliwe jest także zapisanie światów do pliku w formacie *json*. Zapisany plik
zawiera dodatkowe spacje aby poprawić czytelność i móc go edytować.


Odnośnik bezpośredni
--------------------

Oprócz zapisywania konfiguracji świata jest możliwość zapisania zawartości edytora,
bibliotek i użytego języka programowania. [Jest także możliwy zapis zmian interfejsu
użytkownika :ref:`changing-the-user-interface`.]
Wszystko to jest zakodowane w *odnośniku bezpośrednim* (ang. *permalink*), którego
można później użyć jako URL w hiperłączu (ang. hyperlink)

Na przykład `ten odnośnik bezpośredni`_ załaduje świat i rozwiązanie.

.. _ten odnośnik bezpośredni: http://reeborg.ca/world_dev.html?proglang=python-en&world=%7B%0A%20%20%22robots%22%3A%20%5B%0A%20%20%20%20%7B%0A%20%20%20%20%20%20%22x%22%3A%201%2C%0A%20%20%20%20%20%20%22y%22%3A%201%2C%0A%20%20%20%20%20%20%22tokens%22%3A%20%22infinite%22%2C%0A%20%20%20%20%20%20%22orientation%22%3A%200%2C%0A%20%20%20%20%20%20%22_prev_x%22%3A%201%2C%0A%20%20%20%20%20%20%22_prev_y%22%3A%201%2C%0A%20%20%20%20%20%20%22_prev_orientation%22%3A%200%0A%20%20%20%20%7D%0A%20%20%5D%2C%0A%20%20%22walls%22%3A%20%7B%0A%20%20%20%20%222%2C1%22%3A%20%5B%0A%20%20%20%20%20%20%22east%22%0A%20%20%20%20%5D%2C%0A%20%20%20%20%224%2C1%22%3A%20%5B%0A%20%20%20%20%20%20%22east%22%0A%20%20%20%20%5D%2C%0A%20%20%20%20%226%2C1%22%3A%20%5B%0A%20%20%20%20%20%20%22east%22%0A%20%20%20%20%5D%2C%0A%20%20%20%20%228%2C1%22%3A%20%5B%0A%20%20%20%20%20%20%22east%22%0A%20%20%20%20%5D%2C%0A%20%20%20%20%2210%2C1%22%3A%20%5B%0A%20%20%20%20%20%20%22east%22%0A%20%20%20%20%5D%0A%20%20%7D%2C%0A%20%20%22goal%22%3A%20%7B%0A%20%20%20%20%22possible_positions%22%3A%20%5B%0A%20%20%20%20%20%20%5B%0A%20%20%20%20%20%20%20%208%2C%0A%20%20%20%20%20%20%20%201%0A%20%20%20%20%20%20%5D%0A%20%20%20%20%5D%2C%0A%20%20%20%20%22position%22%3A%20%7B%0A%20%20%20%20%20%20%22image%22%3A%20%22racing_flag%22%2C%0A%20%20%20%20%20%20%22x%22%3A%208%2C%0A%20%20%20%20%20%20%22y%22%3A%201%0A%20%20%20%20%7D%0A%20%20%7D%2C%0A%20%20%22small_tiles%22%3A%20false%2C%0A%20%20%22rows%22%3A%203%2C%0A%20%20%22cols%22%3A%2010%2C%0A%20%20%22pre_code%22%3A%20%22RUR.world.remove_robots()%5Cn%5Cnclass%20RepairedRobot(UsedRobot)%3A%5Cn%20%20%20%20def%20turn_right(self)%3A%5Cn%20%20%20%20%20%20%20%20self.body._orientation%20%2B%3D%203%5Cn%20%20%20%20%20%20%20%20self.body._orientation%20%25%3D%204%5Cn%20%20%20%20%20%20%20%20RUR.rec.record_frame()%5Cn%5Cnr%20%3D%20RepairedRobot()%5Cnturn_right%20%3D%20r.turn_right%5CnRUR.vis_robot.set_trace_style(%5C%22thick%5C%22)%5Cn%22%2C%0A%20%20%22description%22%3A%20%22Hurdle%20race%20by%20better%20robot%22%2C%0A%20%20%22post_code%22%3A%20%22%22%0A%7D&editor=%0Adef%20jump()%3A%0A%20%20%20%20move()%0A%20%20%20%20turn_left()%0A%20%20%20%20move()%0A%20%20%20%20turn_right()%0A%20%20%20%20move()%0A%20%20%20%20turn_right()%0A%20%20%20%20move()%0A%20%20%20%20turn_left()%0A%0Arepeat(jump%2C%203)%0Amove()%0A&library=

.. _tutaj: http://reeborg.ca/world_dev.html?proglang=python-en&world=%7B%0A%20%20%22robots%22%3A%20%5B%0A%20%20%20%20%7B%0A%20%20%20%20%20%20%22x%22%3A%201%2C%0A%20%20%20%20%20%20%22y%22%3A%201%2C%0A%20%20%20%20%20%20%22orientation%22%3A%200%2C%0A%20%20%20%20%20%20%22_prev_x%22%3A%201%2C%0A%20%20%20%20%20%20%22_prev_y%22%3A%201%2C%0A%20%20%20%20%20%20%22_prev_orientation%22%3A%200%2C%0A%20%20%20%20%20%20%22objects%22%3A%20%7B%0A%20%20%20%20%20%20%20%20%22token%22%3A%202%2C%0A%20%20%20%20%20%20%20%20%22star%22%3A%201%2C%0A%20%20%20%20%20%20%20%20%22triangle%22%3A%20%22infinite%22%0A%20%20%20%20%20%20%7D%2C%0A%20%20%20%20%20%20%22start_positions%22%3A%20%5B%0A%20%20%20%20%20%20%20%20%5B%0A%20%20%20%20%20%20%20%20%20%201%2C%0A%20%20%20%20%20%20%20%20%20%201%0A%20%20%20%20%20%20%20%20%5D%0A%20%20%20%20%20%20%5D%0A%20%20%20%20%7D%0A%20%20%5D%2C%0A%20%20%22walls%22%3A%20%7B%7D%2C%0A%20%20%22description%22%3A%20%22Using%20%3Ccode%3Emove()%3C%2Fcode%3E%2C%20%3Ccode%3Eturn_left()%3C%2Fcode%3E%2C%20%3Ccode%3Efront_is_clear()%3C%2Fcode%3E%2C%20%3Ccode%3Eright_is_clear()%3C%2Fcode%3E%2C%20%3Ccode%3Eat_goal()%3C%2Fcode%3E%20and%20the%20Python%20keywords%20%3Ccode%3Eif%2C%20else%2C%20elif%2C%20while%2C%20not%2C%20def%3C%2Fcode%3E%2C%20have%20Reeborg%20decide%20on%20its%20own%20how%20to%20follow%20the%20path%20so%20it%20can%20go%20home.%5Cn%3Cbr%3E--%3Cbr%3E%3Cem%3EEn%20utilisant%20%3Ccode%3Eavance()%3C%2Fcode%3E%2C%20%3Ccode%3Etourne_a_gauche()%3C%2Fcode%3E%2C%20%3Ccode%3Erien_devant()%3C%2Fcode%3E%2C%20%3Ccode%3Erien_a_droite()%3C%2Fcode%3E%2C%20%3Ccode%3Eau_but()%3C%2Fcode%3E%20et%20les%20mots%20Python%20%3Ccode%3Eif%2C%20else%2C%20elif%2C%20while%2C%20not%2C%20def%3C%2Fcode%3E%2C%20aidez%20Reeborg%20%C3%A0%20trouver%20son%20chemin%20par%20lui-m%C3%AAme%20pour%20qu'il%20puisse%20retourner%20%C3%A0%20sa%20maison%20en%20suivant%20le%20sentier.%3C%2Fem%3E%22%2C%0A%20%20%22small_tiles%22%3A%20false%2C%0A%20%20%22rows%22%3A%2012%2C%0A%20%20%22cols%22%3A%2014%2C%0A%20%20%22tiles%22%3A%20%7B%0A%20%20%20%20%221%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C8%22%3A%20%22water%22%2C%0A%20%20%20%20%223%2C8%22%3A%20%22water%22%2C%0A%20%20%20%20%223%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C9%22%3A%20%22water%22%2C%0A%20%20%20%20%222%2C8%22%3A%20%22water%22%2C%0A%20%20%20%20%221%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C9%22%3A%20%22water%22%2C%0A%20%20%20%20%222%2C10%22%3A%20%22water%22%2C%0A%20%20%20%20%221%2C10%22%3A%20%22water%22%2C%0A%20%20%20%20%221%2C11%22%3A%20%22water%22%2C%0A%20%20%20%20%221%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%224%2C6%22%3A%20%22water%22%2C%0A%20%20%20%20%225%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%224%2C7%22%3A%20%22water%22%2C%0A%20%20%20%20%221%2C1%22%3A%20%22gravel%22%2C%0A%20%20%20%20%222%2C1%22%3A%20%22gravel%22%2C%0A%20%20%20%20%223%2C1%22%3A%20%22gravel%22%2C%0A%20%20%20%20%224%2C1%22%3A%20%22gravel%22%2C%0A%20%20%20%20%224%2C2%22%3A%20%22gravel%22%2C%0A%20%20%20%20%224%2C3%22%3A%20%22gravel%22%2C%0A%20%20%20%20%225%2C3%22%3A%20%22gravel%22%2C%0A%20%20%20%20%226%2C3%22%3A%20%22gravel%22%2C%0A%20%20%20%20%227%2C3%22%3A%20%22gravel%22%2C%0A%20%20%20%20%227%2C4%22%3A%20%22gravel%22%2C%0A%20%20%20%20%227%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%227%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C7%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2210%2C8%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2210%2C9%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2211%2C9%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2212%2C9%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2212%2C10%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2212%2C11%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2213%2C11%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2214%2C11%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2214%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C11%22%3A%20%22water%22%2C%0A%20%20%20%20%225%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%226%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%228%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%229%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%2210%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%2211%2C5%22%3A%20%22water%22%2C%0A%20%20%20%20%2211%2C4%22%3A%20%22water%22%2C%0A%20%20%20%20%2212%2C4%22%3A%20%22water%22%2C%0A%20%20%20%20%2213%2C4%22%3A%20%22water%22%2C%0A%20%20%20%20%2213%2C3%22%3A%20%22water%22%2C%0A%20%20%20%20%2214%2C3%22%3A%20%22water%22%2C%0A%20%20%20%20%2212%2C3%22%3A%20%22water%22%2C%0A%20%20%20%20%2211%2C3%22%3A%20%22water%22%2C%0A%20%20%20%20%2211%2C2%22%3A%20%22water%22%2C%0A%20%20%20%20%2212%2C2%22%3A%20%22water%22%2C%0A%20%20%20%20%2213%2C2%22%3A%20%22water%22%2C%0A%20%20%20%20%2214%2C2%22%3A%20%22water%22%2C%0A%20%20%20%20%2214%2C1%22%3A%20%22water%22%2C%0A%20%20%20%20%2213%2C1%22%3A%20%22water%22%2C%0A%20%20%20%20%2212%2C1%22%3A%20%22water%22%2C%0A%20%20%20%20%2211%2C1%22%3A%20%22water%22%2C%0A%20%20%20%20%225%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%225%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C4%22%3A%20%22gravel%22%2C%0A%20%20%20%20%229%2C4%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2210%2C4%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2210%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C1%22%3A%20%22grass%22%2C%0A%20%20%20%20%223%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%222%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C3%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%221%2C2%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%226%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%2211%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%2211%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%2211%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%2212%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C11%22%3A%20%22grass%22%2C%0A%20%20%20%20%227%2C12%22%3A%20%22grass%22%2C%0A%20%20%20%20%228%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%229%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%2210%2C6%22%3A%20%22gravel%22%2C%0A%20%20%20%20%2211%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%2212%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%2212%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C5%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C4%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C6%22%3A%20%22grass%22%2C%0A%20%20%20%20%2211%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%2211%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%2212%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%2212%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C7%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C8%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C9%22%3A%20%22grass%22%2C%0A%20%20%20%20%2213%2C10%22%3A%20%22grass%22%2C%0A%20%20%20%20%2214%2C10%22%3A%20%22grass%22%0A%20%20%7D%2C%0A%20%20%22objects%22%3A%20%7B%0A%20%20%20%20%222%2C6%22%3A%20%7B%0A%20%20%20%20%20%20%22dandelion%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%226%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22dandelion%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%225%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22dandelion%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%225%2C11%22%3A%20%7B%0A%20%20%20%20%20%20%22dandelion%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%226%2C1%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%227%2C12%22%3A%20%7B%0A%20%20%20%20%20%20%22daisy%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2214%2C7%22%3A%20%7B%0A%20%20%20%20%20%20%22daisy%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%221%2C4%22%3A%20%7B%0A%20%20%20%20%20%20%22daisy%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2214%2C5%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%227%2C1%22%3A%20%7B%0A%20%20%20%20%20%20%22daisy%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%223%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%224%2C9%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%229%2C6%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%226%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22daisy%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2213%2C12%22%3A%20%7B%0A%20%20%20%20%20%20%22tulip%22%3A%201%0A%20%20%20%20%7D%0A%20%20%7D%2C%0A%20%20%22top_tiles%22%3A%20%7B%0A%20%20%20%20%225%2C1%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%223%2C3%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%223%2C4%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%2C%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%224%2C4%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%228%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%227%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%223%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%222%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_double%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%221%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2213%2C8%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2213%2C9%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2213%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%2C%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2214%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2211%2C12%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%2C%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2212%2C12%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2211%2C11%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2210%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2211%2C10%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2210%2C5%22%3A%20%7B%0A%20%20%20%20%20%20%22bridge%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2212%2C8%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%2210%2C3%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_left%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%229%2C3%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_double%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%228%2C3%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_right%22%3A%201%2C%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%225%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_vertical%22%3A%201%2C%0A%20%20%20%20%20%20%22fence_right%22%3A%201%0A%20%20%20%20%7D%2C%0A%20%20%20%20%226%2C2%22%3A%20%7B%0A%20%20%20%20%20%20%22fence_double%22%3A%201%0A%20%20%20%20%7D%0A%20%20%7D%2C%0A%20%20%22goal%22%3A%20%7B%0A%20%20%20%20%22possible_positions%22%3A%20%5B%0A%20%20%20%20%20%20%5B%0A%20%20%20%20%20%20%20%2014%2C%0A%20%20%20%20%20%20%20%2012%0A%20%20%20%20%20%20%5D%0A%20%20%20%20%5D%2C%0A%20%20%20%20%22position%22%3A%20%7B%0A%20%20%20%20%20%20%22image%22%3A%20%22house%22%2C%0A%20%20%20%20%20%20%22x%22%3A%2014%2C%0A%20%20%20%20%20%20%22y%22%3A%2012%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D&editor=think(100)%0Awhile%20not%20at_goal()%3A%0A%20%20%20%20if%20front_is_clear()%3A%0A%20%20%20%20%20%20%20%20move()%0A%20%20%20%20elif%20right_is_clear()%3A%0A%20%20%20%20%20%20%20%20turn_left()%0A%20%20%20%20%20%20%20%20turn_left()%0A%20%20%20%20%20%20%20%20turn_left()%0A%20%20%20%20else%3A%0A%20%20%20%20%20%20%20%20turn_left()%0A%0A&library=%0A

Używanie odnośników bezpośrednich jako hiperłączy może być bardzo pomocne
w pisaniu tutoriali. Należy jednak pamiętać, że:

1. Świat Reeborg-a musi być wczytany za każdym razem, gdy takie hiperłącze
   jest użyte; pobierana jest większa ilość danych.

2. Długie odnośniki bezpośrednie mogą spowodować, że serwer używany przez
   Świat Reeborg-a może poinformować o błędzie, np. `tutaj`_


.. note::

    Odnośniki bezpośrednie mogą być także używane w html-owym formularzu ``select``.
    Zobacz przykład ``Gravel path (solution)``.


Możliwe jest ominięcie tych trudności kopiując odnośnik bezpośredni (w Windows
zrobisz to klikając prawym przyciskiem na link i wybierając odpowiednie polecenie)
a następnie używając menu zaawansowanego w Świecie Reeborg-a zamieniamy aktualny
odnośnik bezpośredni przez skopiowany. Zobacz na przykładzie niżej jak to zrobiono.


|update permalink|

.. |update permalink| image:: ../../images/update_permalink.gif



Użycie funkcji ``World()``
--------------------------

Zamiast klikać na listę rozwijaną ``select`` i wybierać świat, można
ładować świat używając funkcji ``World()`` w programie. Jest to wygodne
w wielu sytuacjach, np. chcesz mieć jeden program z rozwiązanymi zadaniami
w światach "Rain 1" i "Rain 2". Wtedy dobrym zwyczajem jest umieszczenie
na początku programu następujących dwóch linii::

    #World("Rain 1")
    #World("Rain 2")
    
Po usunięciu komentarza w jednej z linii przy wykonaniu programu nastąpi wybór
tego świata (jeśli nie wybrano jeszcze świata). Ponowne wybieranie tego samego
świata zostanie zignorowane.


Takie wybieranie świata działa również gdy używamy go z odnośnika bezpośredniego.
Zmienia się wtedy zawartość edytora i biblioteki (jeśli zakodowano ją w odnośniku).
Spróbuj prześledzić wykonanie programu::

    World("Gravel path (solution)")

Zaobserwuj jak zmieniła się lista rozwijana z wyborem światów po uruchomieniu
tego programu i jak edytor zawiera teraz rozwiązanie zadania. Metoda ta także
działa gdy świat jest zapisany w przeglądarce - zakładając, ze nazwy stworzonych
światów są inne od istniejących. Jeżeli użyto nazwy która jest taka sama jak
istniejącego predefiniowanego, to mozna się do niego dostać pisząc ``user_world:``
przed nazwą nowego świata::

    World("user_world:My World")

Po wykonaniu tego polecenia tylko świat zostanie wczytany (edytor i biblioteka
nie wczytają się).

Jeszcze jeden sposób użycia funkcji ``World()``; prawdopodobnie najbardziej
użyteczny.

Załóżmy, że masz zapisany świat w pliku lub odnośniku bezpośrednim (w pliku)
na publicznie dostępnej witrynie. Możesz go załadować używając::

    World(pelna_sciezka)

Przykład, który można wypróbować::

    World("http://personnel.usainteanne.ca/aroberge/reeborg/test_sokoban1")


.. important::

   Ładowanie plików z zewnętrznych serwerów jest wykonywane przez pośredni serwer
   (cors-anywhere.herokuapp.com)
   który pozwala na `Cross-origin resource sharing`_ . Czasem mogą wystąpić sytuacje,
   gdy usługa nie jest dostępna przez kilka minut.

.. _Cross-origin resource sharing: https://pl.wikipedia.org/wiki/Cross-Origin_Resource_Sharing

Tworzenie niestandardowego menu
-------------------------------

Po przeczytaniu całego tekstu powyżej, wiadomo już co jest potrzebne do stworzenia
niestandardowego menu w którym użytkownik może wybierać własne światy.
Mianowicie w edytorze piszemy program, który używa funkcji ``MakeCustomMenu``::

    contents = [ [full_url_1, name_1],
                 [full_url_2, name_2],
                 [full_url_3, name_3],
                 ... ]
    MakeCustomMenu(contents)


Następnie tworzymy odnośnik bezpośredni i zapisujemy go w pliku.
Załadowanie tego pliku wykorzystując ``World()`` umieści odpowiednią treść.
Wykonując ten nowy program otrzymamy niestandardowe menu, które zamieni istniejącą
listę rozwijaną na górze strony.


Spróbuj wykonać ten przykład::

    World('http://personnel.usainteanne.ca/aroberge/reeborg/custom_menu')

W przykładzie tym są pobierane światy z dwóch witryn, w tym wykorzystując
odnośniki bezpośrednie. Uruchomienie przykładu spowoduje zamianę listy rozwijanej
tak, że tylko światy podane w przykładzie będą dostępne.


