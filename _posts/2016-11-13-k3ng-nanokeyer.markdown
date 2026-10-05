---
title: "K3NG NanoKeyer"
date: 2016-11-13
categories: 
  - "technika"
---

![nanokeyery-01](/images/Nanokeyery-01-225x300.jpeg)Podstawowy program do klucza arduino, o którym mowa, został napisany przez Anthony'ego K3NG i z założenia miał stanowić otwartą platformę, co udało się autorowi w 100%. Na początku zyskał miano Nanokeyer, od rodzaju płytki arduino nano 3, na której pierwotnie był uruchomiony. Dość szybko zaczął jednak rosnąć do takich rozmiarów, że płytka nano nie była w stanie pomieścić wszystkich jego funkcji. Dlatego ostatnią jego wersję wykonałem na arduino MEGA, gdzie po wgraniu wszystkich funkcji pozostaje jeszcze około 75% wolnego miejsca w pamięci procesora. Nazwa klucz CW, czy keyer jest symboliczna, gdyż w zasadzie jest to mały komputer, którego podstawowy schemat i wszystkie funkcje opisane są szczegółowo na stronie:

[https://blog.radioartisan.com/arduino-cw-keyer/](https://blog.radioartisan.com/arduino-cw-keyer/)

a najaktualniejszy wsad do procesora zawsze można znaleźć pod adresem:

[https://github.com/k3ng/k3ng\_cw\_keyer](https://github.com/k3ng/k3ng_cw_keyer)

![nanokeyer\_2-01](/images/Nanokeyer_2-01-300x225.jpeg)Ponieważ urządzenie jest wykonane w oparciu o platformę arduino, nie potrzebny jest żaden zewnętrzny programator, wystarczy ściągnąć program - środowisko arduino, ustawić za jego pomocą wszystkie interesujące nas funkcje, oraz przypisać odpowiednie wejścia pinów i można wgrywać oprogramowanie na płytkę arduino za pomocą kabla mini USB (arduino nano), lub micro USB w przypadku płytki MEGA. Jeśli zdecydujemy się na zakup płytki nano3, lub klona – ceny są delikatnie mówiąc bardzo przystępne ;) ,   to kabel USB jest zwykle w komplecie. Do płytki MEGA trzeba raczej użyć własnego kabla micro USB od smartfona, bo możemy nie znaleźć go w nabytym zestawie.

![](/images/Nanokeyer-01-225x300.jpeg)

Podstawowe możliwości i funkcje klucza:

1) Keyer CW (do 999 wpm) z możliwością ustawienia dowolnego, dolnego i górnego limitu prędkości, przy czym tempo można regulować na kilka sposobów: a) enkoderem - gdzie jeden skok enkodera w dół lub w górę powoduje zmianę prędkości o 1 wpm, ale dokonując małej ingerencji w oprogramowanie, można ustawić dowolny skok, np. co 5 grup/min. b) za pomocą przycisku MENU i nadania odpowiedniej komendy: np: nadanie komendy W030 spowoduje ustawienie się klucza na tempo 30 wpm) c) za pomocą potencjometru (opcjonalnie zamiast enkodera) d) za pomocą interface’u CLI (Command Line Interface) i programu Putty, lub innego podobnego, np. monitoru portu szeregowego, który jest zawarty w środowisku arduino e) za pomocą klawiatury PS2

2) Protokół WINKEY, umożliwiający pracę z programami logującymi typu N1MM, HRD Log itd.

3) Możliwość użycia przycisku MENU i przycisków pamięci, oraz makr - do wywoływania różnych funcji i komunikatów z buforu pamięci procesora, np. po naciśnięciu przycisku nr 1, klucz nadaje CQ CQ CQ DE .... itd., czy co tam sobie zażyczymy, albo zmienia tempo na takie, jakie pod danym przyciskiem ustawimy w formie makra

4) Command Line Interface (CLI) - do komunikacji z komputerem przy pomocy monitora portu szeregowego, lub innych podobnych programów, polecam PUTTY, jest mały (nie wymaga instalacji, otwiera się jedynie w formie aplikacji) i bardzo czytelny. Za pomocą tego programu i CLI można łatwo sprawdzić jakie są aktualne ustawienia klucza, oraz zmienić wiele funkcji, np. włączyć lub wyłączyć CMOS SUPER KEYER TIMING, czy auto space, ustawić dowolny pośredni tryb pracy pomiędzy IAMBIC A i IAMBIC B od 0 do 100%, gdzie 0% to pełna pamięć znaków przeciwnych, a 100% to pełny IAMBIC A). Ta funkcja jest bardzo przydatna w szybkich tempach, kiedy nie nadążamy z ucieczką palców z dźwigni podczas pracy w pełnym trybie IAMBIC B i zamiast np. litery A, nadajemy niechcący literę R, zamiast litery U - literę F itd... Za pomocą CLI możemy też wygodnie zaprogramować pamięci i makra, aby później odtwarzać je także za pomocą przycisków pamięci i makr

5) Klawiatura PS2 lub USB (do tej ostatniej potrzebny jest dodatkowy układ). Klawiatura PS2 jest tania (ok. 5 zł), a bardzo wygodnie zmienia się za jej pomocą różne funkcje, np. wysokość tonu monitora, stosunek RATIO, tempo i wiele, wiele innych., a przyciski funkcyjne od F1 do F12 są odpowiednikami przycisków pamięci i makr. Oczywiście można klawiatury użyć po prostu jako klucza CW - piszemy tekst, a w eter płyną sygnały Morse'a :) Nie potrzeba podłączać komputera, jedynie klawiaturę (sam klucz jest komputerem).

6) Dobry dekoder oparty na algorytmie Geortzela, do którego opcjonalnie możemy podłączyć diodę (jej działanie jest zawarte w programie i jest ona bardzo przydatna podczas ustawiania odpowiedniego poziomu sygnału dekodowanego)

7) Łatwa możliwość podłączenia wyświetlacza LCD, na którym widzimy w formie tekstu to co nadajemy, wszelkie zmiany funkcji, prędkości i inne, oraz oczywiście tekst zdekodowanej transmisji (jeśli jest uruchomiony dekoder)

To tylko krótki szkic możliwości tego klucza. Pełny jego opis, szczegółowa instrukcja, schemat i dokładny spis komend znajdziemy na stronie do której podałem wyżej linka. Jeśli ktoś budując go napotka problemy, proszę o kontakt. Jest on dość prosty do wykonania, ale możemy natrafić na pewnego rodzaju kłopoty, z którymi uporanie się może zająć niepotrzebnie dużo czasu. Poniżej link do krótkiego filmiku z prezentacją keyera:

 

 

<iframe src="https://www.youtube.com/embed/SCNL_2b9odA" width="560" height="315" frameborder="0" allowfullscreen="allowfullscreen"></iframe>

 

**Krzysztof SQ8LUV**
