---
title: "Konwerter lampowy KF"
date: 2021-10-28
categories: 
  - "technika"
---

Dziś podzielę się wrażeniami z uruchomienia lampowego konwertera na pasma KF. Konwerter ten dostałem od Krzysztofa SP8GSC, który ma dar obdarowywania mnie różnymi ciekawymi urządzeniami (oraz elementami z których takie urządzenia można zbudować ;) ). Z tego co wiem, nabył go on od Krzysztofa SP7GIQ (wówczas SP5GIQ) wraz z całym zestawem - odbiornik, nadajnik i PA. Umożliwiał on pracę na pięciu podstawowych pasmach amatorskich. W tamtych latach urządzenia takie budowano z powodów ściśle praktycznych, a że Krzysztof SP8GSC miał już odbiornik KF ale bez tzw. warców, postanowił go przebudować właśnie na te pasma, czyli 10, 18 i 24 MHz, co też uczynił z powodzeniem. Teraz urządzenie potrzebuje do współpracy odbiornika na pasmo 20m. W związku z wykonywaniem elewacji domu i związanego z tym rozgardiaszem, stłukły się dwie lampy, tak więc kiedy postanowiłem uruchomić konwerter, nie bardzo było wiadomo co tam włożyć. Po przestudiowaniu chassis i schematu (który nie podawał rodzajów lamp) w końcu udało mi się je zidentyfikować i na szczęście miałem je w zapasie (oczywiście od SP8GSC). Wszystkie użyte w urządzeniu są z rodzaju miniaturowych. Kilka elementów było odlutowanych na skutek wstrząsów jakich konwerter doznał podczas prac remontowo-budowlanych, ale udało się wszystko przywrócić do stanu użytkowalności, pomógł mi w tym generator sygnałowy (NWT-7) i oscyloskop. I tak, zaczynając od wejścia konwertera, jako wzmacniacz w.cz. pracuje pentoda EF95 na której siatkę pierwszą podawany jest sygnał z anteny poprzez strojony obwód wejściowy w składzie: kondensator zmienny 155pF i dwie dołączane do niego zamiennie cewki: jedna (ok. 13,5 uH) na pasma dolne, czyli 3.5, 7 oraz 10 MHz i druga, o małej indukcyjności na pasma wyższe. Cewki są  zamieniane za pomocą przełącznika podającego napięcie na dwa przekaźniki. Następnie, sygnał z anody EF95 przechodzi przez bliźniaczy obwód strojony LC na siatkę pierwszą mieszacza, w którego roli pracuje 6Ż1P. Na jego katodę podawany jest sygnał z generatora, również z pentodą 6Ż1P w obwodzie którego pracują przełączane kwarce 4 i 10,7 MHz oraz dodany przeze mnie kwarc 7,158 MHz, dzięki któremu, oprócz "warców" mogę odbierać również inne pasma KF. Kiedy w generatorze pracuje kwarc o częstotliwości 4 MHz, możliwy jest odbiór pasm 10 i 18 MHz, z kwarcem 10,7 MHz odbieramy pasma 3.5 i 24 MHz, a dzięki kwarcowi 7158 kHz możliwy jest odbiór pasm 7 i 21 MHz (to ostatnie tylko częściowo, chyba że mamy odbiornik na 14 MHz pracujący też trochę poniżej zakresu pasma. Ostatni stopień urządzenia to wtórnik katodowy (separator) na triodzie EC92 - tutaj trafia zmieszany sygnał zanim zostanie podany na wejście odbiornika.

Uświadomiłem sobie, że taki konwerter był najwyraźniej skonstruowany z myślą o telegrafii, gdyż jeśli nasz odbiornik odbierał tylko górną wstęgę, jak to często bywało w przypadku prostych RX-ów na 20 metrów, odbiór fonii na niższych pasmach był praktycznie niemożliwy, chyba że zbudowaliśmy odbiornik DSB z obiema wstęgami - wtedy przydałby się  też jakiś dobry filtr audio. Współczesne odbiorniki zwykle mają już możliwość przełączania wstęg, tak jak chociażby mój Icom 745 na którym robiłem testy.

A czy można do tego urządzenia podłączyć odbiornik na pasmo inne niż 20m? Oczywiście, teoretycznie na dowolne, ale wtedy trzeba dobrać odpowiednie  kwarce. Zrobiłem mały eksperyment - na częstotliwości 14,267 MHz pracowała stacja z Finlandii OH6RX, którą postanowiłem odebrać za pomocą odbiorników na różne pasma. Gdy generator w konwerterze ustawiłem na częstotliwość 7,158 MHz i podłączyłem RX na pasmo 40m, stację tę mogłem odbierać w odbiorniku nastrojonym na 7,109 MHz (7,109 + 7,158  = 14,267). Z kolei kiedy konwerter ustawiłem  na F = 10,7 MHz, tę samą stację mogłem usłyszeć w odbiorniku 80 - metrowym nastrojonym na 3,567 MHz.

Schemat konwertera narysowany ręką Krzysztofa zamieszczam poniżej:

![](/images/konwerter-lampowy.jpg)

 

Zdjęcie konwertera:

![](/images/IMG20211026221208-1024x768.jpg)

 

Krótki film z opisem urządzenia:

https://www.youtube.com/watch?v=H\_1FbUToTFc

 

I dwa krótkie, poglądowe filmiki jak konwerter działa na różnych pasmach (końcówka jednego urwana - brak pamięci w telefonie, przepraszam :) )

https://www.youtube.com/watch?v=v2hHjZtPcpA

 

https://www.youtube.com/watch?v=dJD5TNgOcg0

 

Krzysztof, SQ8LUV
