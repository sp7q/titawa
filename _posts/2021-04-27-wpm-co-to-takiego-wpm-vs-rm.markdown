---
title: "WPM – co to takiego? WPM vs RM"
date: 2021-04-27
categories: 
  - "ciekawostki"
---

Kiedyś przy okazji dyskusji na temat telegrafii na forum SP7PKI ktoś zachwycał się rekordowym rezultatem w odbiorze z zapisem uzyskanym w 1935 r. przez Theodore Roosevelt McElroy wynoszącym 77WPM (21 dot of standard). Czy to dobry wynik? Jeżeli ktoś powie, że odbiera 70WPM to dużo czy mało?

 

Tak właśnie powstają legendy. Ktoś coś usłyszał, dodał co nieco od siebie i wynik urósł do niebotycznych wartości. Przy podawaniu prędkości telegrafii zawsze powinna być informacja według jakiego standardu wykonany był pomiar. Krótkofalowcy  powszechnie stosują tzw. WPM  czyli standard według słowa PARIS. W zawodach HST już dawno zrezygnowano z tej metody na rzecz prędkości rzeczywistych (Real Marks – RM).

Metody „xx dot of standard”, m.in. WPM(PARIS) – „50 dot of standard” bazują na stałej długości „kropki” (czyli jak powinno się poprawnie mówić - krótkiego sygnału) wynikającej z ilości „kropek” , którą zawiera grupa wzorcowa, w tym przypadku słowo PARIS – „50 długości kropki”. Obrazowo mówiąc, 30WPM(PARIS) oznacza, że należy tak ustawić szybkość urządzenia nadającego, aby w ciągu minuty zostało nadane dokładnie 30 słów PARIS z zachowaniem standardowych odstępów. Ilość grup lub znaków nadanych w ciągu minuty tekstu rzeczywistego przy tym ustawieniu będzie różna, w zależności od struktury tekstu. Dla cyfr (długie znaki) będzie to dużo mniej, dla tekstu literowego zawierającego dużo krótkich liter (e, t, a, n itp.) może zdarzyć się, że będzie więcej.

Przy metodzie według „prędkości rzeczywistej” dla każdego konkretnego tekstu określa się długość trwania „kropki” tak, żeby w ciągu minuty została nadana określona liczba grup lub znaków tekstu. Oznacza to, że w zależności od struktury tekstu, długość trwania „kropki” jest różna. Oczywiście, nikt nie bawi się w obliczanie dla każdego tekstu, zakłada się równomierny rozkład znaków (liter, cyfr, znaków pisarskich) i stąd wynikają przeliczniki podane poniżej:

 

dla tekstu literowego: WPM(PARIS) = 1,20 \* WPM(RM)

dla tekstu cyfrowego: WPM(PARIS) = 1,78 \* WPM(RM)

dla tekstu mieszanego: WPM(PARIS) = 1.43 \* WPM(RM)

 

Jak wcześniej wspomniano, wszystkie metody "xx dot of standard", w tym również stosowana w krótkofalarstwie metoda według słowa PARIS (50 dot of standard), bazują na stałym, odpowiednim do danej szybkości, czasie trwania "kropki" (krótkiego sygnału). Co to w praktyce oznacza? Jest bardzo łatwe w zastosowaniu, ale oznacza tylko tyle, że w urządzeniu nadającym ustawiamy na skali lub wyświetlaczu określony czas trwania krótkiego sygnału, niezależnie co i jak będzie nadawane. Np. dla prędkości 40 WPM(PARIS) będzie to 30 milisekund dla „kropki”. Natomiast rzeczywista prędkość zależna będzie od naszego sposobu nadawania i rodzaju tekstu. Jeżeli ktoś będzie robił bardzo długie przerwy między nadawanymi znakami pisarskimi, np. 1 znak co 5 sekund, to w rzeczywistości nada tylko 2,4 WPM(RM) zamiast ustawionych 40WPM! Dlatego ustawienie i próba nadawania z szybkością 100WPM nie oznacza pobicia światowego rekordu. W przypadku pomiaru według „tempa rzeczywistego”, ilość faktycznie nadanych znaków pisarskich (np. 243) dzieli się przez czas trwania nadawania w minutach (np. 1 minuta) i otrzymujemy faktyczną szybkość nadawania (w tym przypadku 243 CPM(RM) czyli 48,6WPM(RM)). (RM oznacza Real Marks). Czas trwania „kropki” (krótkiego sygnału) będzie w tym przypadku zależny od rodzaju tekstu i sposobu nadawania. Dlatego tak ważne jest przy podawaniu lub porównywaniu wszelkich wyników czy rekordów określenie warunków w jakich były mierzone. Ten sam wynik, np. 60 WPM(RM) tekstu literowego da różne wartości w zależności od metody pomiaru: 72(WPM(PARIS), 60WPM(CODEX), 170WPM(21 dot  standard). Jeszcze inne gdy będzie to tekst cyfrowy: 104WPM(PARIS), 86.5WPM(CODEX), 259.4 WPM(21 dot standard). Jeżeli w publikacji pominiemy część w nawiasie po słowie WPM, to tak naprawdę sama liczba określająca szybkość niewiele mówi. Dlatego najbardziej wiarygodne wydają się być rekordy osiągnięte na oficjalnych zawodach o określonym i powtarzalnym regulaminie, z podanym standardem wyznaczania prędkości nadawania i odbioru.

 

Dla formalności, wspomniana na wstępie rekordowa prędkość 77WPM(21 dot of standard) odpowiada  32.34WPM, a więc na dzisiejsze czasy to żadna rewelacja.

 

Poniżej tłumaczenie artykułu  Iuliana YO3FCA / M0IPU zmieszczonego na stronie: [https://www.qsl.net/yo3fca/hstc.htm](https://www.qsl.net/yo3fca/hstc.htm) , rozszerzającego wiedzę na temat standardów określania prędkości nadawania i odbioru telegrafii,

 

### Bogusław sp7ivo

 

  **_Wprowadzenie – dlaczego PARIS?_**

 

_Nie mogłem znaleźć oficjalnego lub nieoficjalnego wyjaśnienia systemu „Real Marks” używanego w konkurencjach odbioru i transmisji High Speed Telegraphy Championship. Tylko kilka pytań bez odpowiedzi rozsianych po postach na forach internetowych._

 

_W naszej codziennej pracy HF / VHF CW wszyscy posługujemy się wszechobecnym WPM - Words Per Minute (standard PARIS), czy jesteśmy tego świadomi, czy nie. Programy komputerowe CW dla krótkofalowców, kluczy elektronicznych, czytników CW, wbudowane urządzenia do kluczowania itp. są zgodne z WPM PARIS lub po prostu w skrócie WPM. I wydaje się całkiem normalne. Ponieważ znaki, których używamy w kodzie Morse'a nie są równe pod względem długości (czasu trwania), nigdy nie możemy określić prędkości  zliczając ich liczbę w danej jednostce czasu (nie możemy ustanowić systemu określania prędkości w oparciu o te kryteria, chyba, że radiogramy są starannie spreparowane, podobnie jak radiogramy „rzeczywistych znaków”(„Real Marks”), które są przedmiotem tego artykułu). Prędkość według słowa PARIS jest bezpośrednio skorelowana z czasem trwania jednej „kropki” (dit – krótkiego sygnału)  wyjaśnionej poniżej, która we współczesnym kodzie Morse'a jest podstawową jednostką czasu/prędkości. Oczywiście mało komunikatywnie jest powiedzieć, że odbieramy/nadajemy kod Morse'a z czasem trwania „kropki” „t” wynoszącym 40 milisekund lub 30 milisekund, dlatego słowo PARIS, które składa się z 50 podstawowych jednostek, może nam służyć jako jednostka miary, jako podstawa standardu. Można to nazwać swojego rodzaju zegarem. Mamy sekundy jako jednostkę bazową, ale mamy również minuty i godziny. Nie możemy powiedzieć, że czas to 155362 sekund. To jest konwencja._

 

_Powyższe wyjaśnienie jest nieco uproszczone, ale jest to stan obecny. Pochodzenie standardu PARIS to nieco inna historia, która jednak nie zmienia dzisiejszego obrazu. Nie jestem pewien, czy standard PARIS został opracowany samodzielnie, czy też był częścią większego, elektronicznego systemu zawierającego standard CODEX i inne standardy. Standard PARIS dominował w świecie krótkofalowców i być może w innych dziedzinach  (obecnie cały sprzęt używający kodu Morse'a jest skalibrowany do systemu PARIS) cywilnych, w marynarce wojennej, w wojsku itp., najprawdopodobniej jako uproszczony, zunifikowany system. Tak przynajmniej odbieram fakty. Obecnie obejmuje całe spektrum znaków używanych w kodzie Morse'a, biorąc pod uwagę różnorodność aplikacji, języków itp., w których używany jest kod Morse'a, łatwiej jest przyjąć standard oparty na „t” (lub szybkości znaków), mimo że został on pierwotnie zbudowany w określonym celu (patrz poniżej). Nie jest to metoda naukowa, ale jest bardzo praktyczna._

 

_\- Standard PARIS, 50 jednostek (patrz następny rozdział). Samo słowo odzwierciedla liczbę „kropek”/jednostek czasu w „przeciętnym słowie” w potocznym języku angielskim, oczywiście zakodowanym alfabetem Morse'a. Został opracowany do pomiaru szybkości transmisji zwykłego tekstu w języku angielskim. Jak wspomniano w poprzednim akapicie, jest on teraz „wymuszony”, używany jako standard „t” w całym zakresie wykorzystania kodu Morse'a. (Nie jestem do końca pewien, w jaki sposób określane jest tutaj średnie słowo. Czy bierze się pod uwagę częstotliwość słów i inne aspekty, takie jak długość słów itp. A może stosuje się bardziej uproszczone podejście, zliczając całkowitą liczbę „kropek” (patrz rozdział PARIS) w całym tekście, im dłuższy, tym lepiej, a następnie dzieląc go przez liczbę znaków w tekście, dodając na końcu standardowe przerwy?)_

 

_\- Standard CODEX, 60 jednostek, który wydaje się przypominać liczbę kropek występujących w przeciętnym słowie utworzonym z pięciu losowych znaków, wykorzystujących 26 liter alfabetu łacińskiego, łącznie z odstępami. Suma „kropek” („t”) każdej z 26 liter kodu Morse'a, wynosząca łącznie 214, podzielona przez 26 razy 5, a następnie dodana 3 \* 4 + 7 = 19 jednostek dla przerw, daje prawie dokładnie 60 jednostek. Zostało to użyte w pięcioznakowych radiogramach słownych (szyfrowanie zwykłego tekstu) używanych głównie w wojsku._

 

_\- Wygląda na to, że były również inne standardy, np. 12345 lub 67890, które były używane tylko podczas odbierania lub przesyłania cyfr. Nie mam informacji na ten temat, ale dałyby one wzorce 84 i 94 „kropek”, gdybyśmy obliczyli według ich nazw. Ten standard był także najczęściej używany w wojsku._

 

_Powyższe „średnie słowa” zostały opracowane jako punkt odniesienia, aby odzwierciedlić rzeczywistą liczbę słów dla określonego zestawu znaków, tekstu itp., nadawanego lub odbieranego w danej jednostce czasu, zwykle jednej minuty. Oczywiście standardy mogą być opracowane w jakimkolwiek konkretnym celu, na przykład w innym języku niż angielski, innym zestawie znaków itp. Przynajmniej w teorii. Kto na świecie by tego chciał?_

 

_Zanim przejdziemy do Real Marks (tempo rzeczywiste), głównego tematu artykułu, rzućmy okiem na inne standardy i ich korelacje._

 

_Na pierwszy rzut oka relacyjne równanie między PARIS, CODEX lub jakimkolwiek innym „standardem” opartym na „t”, jednostkach czasu można zapisać w następujący sposób:_

 

1 min = 50 \* WPM (PARIS) \* t = 60 \* WPM (CODEX) \* t = (liczba kropek „standard”) \* WPM (STANDARD) gdzie t = jednostka czasu „kropki”.

 

_W związku z tym:_

 

WPM (PARIS) = 1,2 \* WPM (CODEX) (pamiętajcie szczególnie o tym, dopóki nie dotrzemy do Real Marks - obliczenia „liter”) lub WPM (CODEX) = 0,833 \* WPM (PARIS)

 

WPM (PARIS) = (liczba „kropek” standardu) \* WPM (STANDARD) / 50

 

_Albo między dowolnymi dwoma standardami:_

 

WPM (STANDARD 1) = (liczba „kropek” standardu 2) \* WPM (SANDARD 2) / (liczba „kropek” standard 1)

 

_Graficzne przedstawienie PARIS i CODEX można znaleźć tutaj [https://www.qsl.net/dk5ke/geschwindigkeitsmessung.html](https://www.qsl.net/dk5ke/geschwindigkeitsmessung.html) lub w innych nielicznych miejsca w Internecie. Moją własną wersję można zobaczyć poniżej._

 

_A teraz wróćmy do naszego tematu Real Marks a PARIS._

 

 

**_Czas trwania „kropki” (PARIS - prędkość znaku)._**

 

_Prawdopodobnie można znaleźć opis systemu PARIS w każdej książce z kodem Morse'a lub w Internecie (Wikipedia)._

_Krótko mówiąc, słowo PARIS składa się z 50 „kropek” (di, dit, dih). „Kropka” to jednostka podstawowa, „kreska” (myślnik, dah) to 3 „kropki”, odstęp między „kropkami” i „kreskami” w znaku to 1 „kropka”, odstęp między dwoma znakami w słowie to 3 „kropki”, a odstęp między dwoma słowami to 7 „kropek”._

 

_Graficznie:_

![](/images/kropki.jpg)

 

 

Jedna minuta radiogramu „PARIS” składa się z 50 (jednostek w słowie) razy ilość słów (prędkość) razy „t” (czas trwania „kropki” w milisekundach).

 

1 min = 50 \* WPM \* t

 

# Jedna minuta to 60s \* 1000 = 60000ms

 

60000 ms = 50 \* WPM \* t

 

t = 1200 / WPM lub WPM = 1200 / t

 

_Na przykład, radiogram 40 WPM (lub 200 CPM - znaków na minutę - gdzie CPM = 5 \* WPM) zawierający tylko słowa PARIS ma 2000 jednostek przy t = 30 ms. To jest rzeczywisty czas trwania „kropki” przy tej prędkości 40WPM._

_Zauważmy, że szybkość nadawania wyrażona w systemie PARIS nie zależy od rodzaju tekstu. Ustawiając na urządzeniu nadającym czas trwania kropki t=30ms  odpowiadający szybkości 40 WPM dowolny tekst będzie nadawany z tymi samymi parametrami czasowymi „kropki”._

 

Uwaga: Dla tych, którzy nie są jeszcze pewni, jak działa system PARIS; utrzymując tę samą prędkość na twoim kluczu, powiedzmy, że przesłałeś jeden z następujących radiogramów w dokładnie 1 minutę z prawidłowymi odstępami między słowami i znakami:

 

DHJYT ARUIO QPIUY XNLKA LKSJU

HJSYE AKJSY POIWT BSHUY LAKUI

AKJSY POIWT BSHUY LAKUI XNLKA

 

_albo_

 

54632 78965 32156 47865 36524

23651 78564 96532 12365 98562

 

_albo_

 

S4L.L ?6PO0 DF,6E ASFG/ 56YO4

RDW?9 IPU73 RTY9= 96DFG /,.YO

4SVZ, =.EIE

 

 

_Zauważysz, że otrzymałeś 15 słów w tekście literowym, 10 tekście cyfrowym lub 12 w tekście mieszanym. Żadna z tych liczb nie jest Twoją szybkością nadawania WPM. Sprawy komplikowałyby się jeszcze bardziej, gdy tekst nie jest „grupowy”, a w postaci  zdań mowy potocznej. Występują słowa dłuższe i krótsze, z innym zestawem liter używanym częściej lub rzadziej. Uwaga: testy zawierające „tekst otwarty” nie są używane w zawodach HST, ponieważ słowa są łatwe do odgadnięcia. Przynajmniej jest to jeden z oczywistych powodów. Co więcej, jakiego języka należałoby używać?_

 

_Teraz nadawaj wielokrotnie słowo PARIS z tą samą co poprzednio ustawioną prędkością nadawania i zobacz, ile ich zmieści się w ciągu 1 minuty. To jest twoja prędkość WPM, 18 WPM. Niektóre zaawansowane programy do kluczowania, takie jak MFJ-464 lub MFJ-495, wyświetlają prędkość na ekranie LCD. Zobaczysz, że jest taka sama, jak liczba słów PARIS przesłanych w ciągu 1 minuty._

 

PARIS PARIS PARIS PARIS PARIS

PARIS PARIS PARIS PARIS PARIS

PARIS PARIS PARIS PARIS PARIS

PARIS PARIS PARIS

 

 

_System określania prędkości konkurencji nadawania i odbioru  na mistrzostwach IARU High Speed Telegraphy._

 

_Prawie dwadzieścia lat minęło od czasu, gdy  zaangażowałem się w HST, a właściwie w cokolwiek związanego z krótkofalarstwem. W 2012 roku zacząłem zwracać trochę uwagi za pośrednictwem odpowiednich stron internetowych na działalność HST. Szybko zdałem sobie sprawę, że znalazłem się w raczej obcym środowisku, jeśli chodzi o system określania szybkości nadawania i odbioru z kodem Morse'a, coś, do czego nie mogłem się odnieść. Byłem bardzo zaintrygowany i nie mogłem nigdzie znaleźć żadnych informacji, nawet w czasie kilku rozmów, które odbyłem z kilkoma starymi kumplami z HST. Nie znalazłem niczego oficjalnego ani nieoficjalnego. Sam musiałem znaleźć odpowiedź._

 

_Wyjaśnienie, w jaki sposób mierzona jest prędkość, znajduje się w przepisach High Spee Telegraphy Championship: „Szybkość odbioru i transmisji będzie mierzona w RZECZYWISTYCH znakach”. Nic więcej. Mogę powiedzieć, że nie jest to zbyt oczywiste. Tak więc w IARU HSTC po prostu zliczają ustaloną liczbę znaków (liter, cyfr, mieszanych) na 1-minutowym radiogramie. WYSIWYG (What You See Is What You GET)._

 

_Gdybyśmy mieli tylko słowa PARIS w 1-minutowym radiogramie, wówczas prędkość „Real Marks” (w skrócie RM) byłaby oczywiście taka sama jak prędkość PARIS. Co się stanie, jeśli zastąpimy słowo PARIS grupami losowych liter? Cóż, słowo PARIS jest dość krótkie, z punktu widzenia liczby „kropek”. Jeśli zastąpimy go, powiedzmy grupą ZQJXP otrzymamy 72 „kropki” w tym słowie, zamiast 50. Będziemy mieli więc znacznie większą liczbę kropek do nadania w tym samym czasie. Jeszcze „gorzej” jest, gdy zastępujemy litery tekstem mieszanym lub cyfrowym, które zawierają jeszcze dłuższe znaki. Otrzymamy jeszcze większą liczbą kropek. Dlatego, żeby utrzymać taki sam czas trwania nadawania tego słowa, czas trwania kropki” musi zostać znacznie skrócony, a zatem równoważna prędkość wyrażona według standardu PARIS wzrośnie._

 

_W standardzie RM, o ile nie przestrzegamy pewnych zasad, mielibyśmy różne prędkości odpowiadające standardowi PARIS (długość kropki) dla tej samej szybkości RM i zestawu znaków. Jednak tak nie jest w przypadku HSTC. System używany w mistrzostwach szybkiej telegrafii opiera się na liniowym wzorze z punktu widzenia długości „kropki”._

 

_Jeśli przeanalizujesz kilka radiogramów dla tej samej szybkości i typu znaków wygenerowanych przez HST2006, jeden z programów, których używany jest w HSTC, zobaczysz, że wszystkie mają taką samą liczbę jednostek, np. 2406 dla 200 RM dla tekstu literowego. Dlatego zawsze będziemy mieć określoną prędkość WPM (lub CPM) skorelowaną z prędkością HSTC RM. Jak już wspomniałem, wzrost prędkości musi być liniowy, czyli różnica w ilości „kropek” pomiędzy sąsiednimi prędkościami RM powinna być zawsze taka sama dla danego zestawu znaków (litery, cyfry lub tekst mieszany)._

 

 

**_Korelacja WPM i RM._**

 

_Początkowo ustalamy równoważną prędkość WPM standardu PARIS dla radiogramu wygenerowanego przez HST2006, znajdując liczbę „kropek” w tym radiogramie._

 

_Jako programista wyobrażam sobie, że można łatwo napisać program, który policzyłby liczbę „kropek” w radiogramie. Przy braku takiego można zastosować bardziej proste metody. Najpierw należy określić ile „kropek” znajduje się w każdej literze, cyfrze lub znaku (patrz załącznik), a następnie użyć internetowego licznika częstotliwości występowania znaków, a na koniec użyć podstawowego programu Excel. Nie zapomnij dodać przerw między znakami i słowami {liczba „kropek” w przerwach = 19 razy liczba słów na radiogramie (3 „kropki” razy 4 przerwy między znakami w słowie razy liczba słów plus 7 „kropek” między słowami razy liczba słów), zakładając, że na końcu radiogramu jest odstęp 7 kropek}._

 

_Aby obliczyć prędkość według standardu PARIS, musimy podzielić liczbę jednostek w 1-minutowym radiogramie przez 50 (jednostek w słowie PARIS)._

 

WPM = (liczba „kropek”) / 50 lub (liczba „kropek”) = 50 \* WPM

 

Wyjaśnienie dotyczące czasu trwania kropki:

 

t = 1200 / WPM = 60000 / (liczba „kropek”)

 

_Biorąc pod uwagę fakt, że wzrost prędkości RM (w stosunku do liczby jednostek) musi być liniowy (patrz poprzedni rozdział), możemy następnie policzyć liczbę „kropek” w radiogramach sąsiednich prędkości, a następnie odjąć je, aby znaleźć przyrost prędkości. Zobaczymy, że na każde 10 RM jest różnica 120 jednostek dla liter i 178 jednostek dla cyfr (z jednym lub dwoma wyjątkami różniącymi się o 2 jednostki). W przypadku tekstu mieszanego, biorąc pod uwagę jego złożoność, istnieje niewielkie odchylenie, ale średnia wynosi 143 jednostki. Wszystko to można powtórnie sprawdzić, obliczając różnicę w liczbie „kropek” między radiogramami przy prędkościach oddalonych od siebie (np. 100 RM i 400 RM), a następnie dzieląc ją przez liczbę przyrostów prędkości._

 

_Możemy teraz napisać proste równanie ze zmienną (liczba „kropek”), a następnie porównać je z powyższym._

 

_Jeśli dla danego RM mamy (ilość „kropek”), to dla (RM + 10) będziemy mieli (ilość „kropek”) + 120 {dla liter}._

 

_Dlatego (liczba „kropek”) = 12 \* RM {dla liter}_

 

_Jak już ustaliliśmy kilka akapitów powyżej, że (liczba „kropek”) = 50 \* WPM, równania korelacji prędkości będą wyglądać następująco:_

 

_Dla tekstów literowych: WPM = 120 \* RM / 500 lub CPM = 1,20 \* RM (to dokładnie odpowiada standardowi CODEX, który został celowo zbudowany dla transmisji tego zestawu znaków)._

 

_Dla tekstów cyfrowych: WPM = 178 \* RM / 500 lub CPM = 1,78 \* RM (jest to dokładnie połowa między standardami 12345 (1,68) i 67890 (1,88). Ma to sens, ponieważ odpowiada średniemu pięciocyfrowemu słowu)._

 

_Dla tekstów mieszanych: WPM = 143 \* RM / 500 lub CPM = 1,43 \* RM (myślę, że tutaj powinien obowiązywać standard zdefiniowany przez „średnie słowo”. Sprawdźmy to. Podsumowując liczbę kropek we wszystkich literach alfabetu, cyfrach i symbolach \[łącznie 431\] dzieląc to przez całkowitą ich liczbę 41 razy 5, a następnie dodając odstępy 4 \* 3 + 7, otrzymamy standard 71,5 jednostek. Dzieląc to przez 50 \[PARIS\] otrzymujemy 1.43. (Możesz nawet znaleźć dla niego odpowiadającą nazwę, składającą się z 5 znaków, które składają się na 51 lub 52 kropki. Może 88MIX lub 143SN?))_

_![](/images/tableka.jpg)_

 

Graficzne przedstawienie danych zawartych w powyższe tabeli:

![](/images/tabela-2.jpg)

 

_Nasuwa się pytanie „Jaka jest relacja pomiędzy WPM lub CPM RM w wynikach HST lub rekordach świata?”_

_Możesz również empirycznie uzyskać prędkości standardu WPM PARIS dla odpowiadającej mu RM. Jeśli uruchomisz  HST2006 i podłączysz czytnik CW, taki jak klucz / czytnik MFJ-464 do line out na swoim komputerze, zobaczysz prędkość PARIS wyświetlaną na MFJ (nie zapomnij dopasować częstotliwości tonu na obu) . Prawdopodobnie powinieneś być w stanie odebrać dane z HST2006 za pomocą innego programu na tym samym komputerze, jak CW Get, za pośrednictwem karty dźwiękowej wewnętrznej._

 

_Uwaga: w ten sposób po raz pierwszy odkryłem odpowiednik RM do WPM, podłączając jeden z moich kluczy MFJ do komputera. Drugie objawienie nastąpiło  niedługo po tym, jak czytałem artykuł w Wikipedii o_ _kodzie Morse'a i zdałem sobie sprawę, że jeśli znamy liczbę „kropek” w radiogramie lub tekście w danej jednostce czasu, to dokładną prędkość PARIS można określić za pomocą prostego równania matematycznego WPM = (liczba kropek) / 50. Reszta to tylko praca biurowa. Oczywiście, gdybym miał bardzo dobrą znajomość standardów „przeciętnych słów” od samego początku (nie przed 2015 rokiem), byłbym w stanie pojąć „Prędkość Rzeczywistą”, patrząc tylko na to, jak skonstruowano radiogramy RM, z których każdy zawiera w przybliżeniu taką samą ilość jednostek podstawowych. Jednak ze względu na dokładność w każdym przypadku obowiązkowe byłoby podejście matematyczne. Kilka lat temu przeczytałem o CODEX-ie itp., Ale nie zwróciłem na to zbytniej uwagi._

 

**_Podsumowanie i wnioski._**

 

_Zakładam, że system Real Marks to zmodyfikowany „oldschoolowy” system prędkości kodu Morse'a WYSIWYG (ulepszony, jak wyjaśniono wcześniej), lub, inaczej mówiąc, (matematyczne) podobieństwo do innych, starszych, opartych na „przeciętnym słowie” systemów pomiaru prędkości, jeśli nie identyczne. Można go postrzegać jako zbiór starszych standardów pod jedną nazwą. W końcu inne, starsze systemy zostały naukowo opracowane, aby odzwierciedlić rzeczywistą liczbę znaków w zależności od typu radiogramu, a przynajmniej tak mi się wydaje. Czytałem, że RM jest pochodzenia rosyjskiego, a przynajmniej jest to jeden z krajów, w których jest nadal używany. Czy był inspirowany literaturą amerykańską itp.? Czy opracowali go niezależnie i osiągnięto takie same wyniki, jak CODEX itp.? Nie wiem. Ostatecznie jednak, gdyby ktoś chciał na przykład opracować standard komercyjny transmisji liter Morse'a, który powinien odzwierciedlać rzeczywistą liczbę znaków, najprawdopodobniej osiągnąłby ten sam wynik co standard „przeciętne słowo”. Jak inaczej byś to zrobił? Jeśli wrzucisz do radiogramu równą ilość, każdej litery, cyfry lub znaku pisarskiego, tekstu w danej jednostce czasu z różnymi prędkościami, z natury rzeczy będziesz postępować zgodnie ze standardem CODEX, standardami cyfrowymi lub standardem dla tekstu mieszanego. Możesz uzyskać potwierdzenie, jak zbudowany jest RM, kopiując / wklejając radiogramy HST2006 itp. W statystyce częstotliwości znaków Real Marks wcale nie jest systemem opartym na prostym zliczaniu liczby znaków w tekście, radiogramie itp., jakby sugerowała nam  jego nazwa, ale raczej fasadą dobrze skonstruowanego, estetycznego, liniowego zestawu radiogramów ._

 

_To niesamowite, jak historia jest ignorowana i zapomniana. Natknąłem się na posty na forach internetowych amerykańskich radioamatorów pytających, czym jest Real Marks? Moja odpowiedź brzmiałaby: „To twój, najprawdopodobniej zapomniany, zbiór standardów kodu Morse'a!”. Nie wiedziałem o tym do samego początku 2015 roku, kiedy na podstawie kilku faktów, intuicji i kilka podstawowych obliczeń matematycznych doszedłem do wniosków zawartych w tym artykule. Czy masz prędkość 88 czy 99 „rzeczywistych znaków”? Skoro już wiemy, co to jest, możemy nauczyć się tego._

 

_Problem z RM polega na tym, że nie można go wyjąć z kontekstu HSTC. Nie wiem na pewno, dlaczego został przyjęty, ponieważ nie byłem zaangażowany w szybką telegrafię (w rzeczywistości w żadną działalność związaną z krótkofalarstwem) przez ostatnie 20 lat. Paradoksalnie reszta świata krótkofalarskiego jest nieco zdziwiona, ponieważ nie stosuje RM. Prawie żaden krótkofalowiec nie wie, co to, powiedzmy, 200 zn / min (RM) (OK, w zależności od twoich umiejętności, możesz, w pewnym sensie, ocenić, jaka jest prędkość, po prostu słuchając nadawania). Dlatego bardzo pomocne byłoby dodanie prędkości PARIS do wyników HSTC, rekordów prędkości itp. Mam nadzieję, że ten artykuł rzuci trochę światła na ten problem._

 

_Dlaczego RM jest używany w HST? Mogę tylko spekulować na ten temat, więc nie bierz tego za pewnik! Jedyne prawdopodobne wyjaśnienia mogą być takie:_

 

 _- Mój stary przyjaciel wspomniał, że w latach 80 mieli kibiców na zawodach HST w byłym ZSRR, kraju używającym RM. Zakładam, że system prędkości WYSIWYG był „wymagany” w tego rodzaju sytuacjach. Mogliście mieć niewtajemniczonych kibiców, którzy od początku nie rozumieliby systemu „dot standard”. Tę „teorię” można oczywiście zastosować do dzisiejszych zawodów HST i sposobu, w jaki szybkość kodu Morse'a jest postrzegana przez niewtajemniczony świat zewnętrzny. To prowadzi nas do drugiej spekulacji._

_Trudno porównywać rekordy Guinnessa na podstawie systemu PARIS. Prawdopodobnie potrzebny by był WYSIWYG, „prosty” do użycia system. Znowu „łącznik” z zewnętrznymi kręgami._

 

_\- O ile dobrze pamiętam, istniał problem w konkurencji odbioru w zawodach HST  w porównaniu prędkości WPM (CPM) standardu PARIS w czasach przed lub u zarania ery komputerów. Zdarzały się sytuacje, w których ostatnie słowo w radiogramie było obcięte, aby dopasować radiogram do nadania dokładnie w ciągu jednej minuty lub, aby uniknąć obcięcia, radiogram skończyłby się kilka sekund wcześniej lub zostałby przedłużony o kilka sekund, aby mieć ostatnią 5-znakową grupę. Jednak  czy aplikacje, takie jak te wymienione w załączniku, które dawałyby „estetyczny”, jednorodny zestaw radiogramów PARIS pod koniec lat 90. lub na początku XXI wieku, stanowiłoby problem? Nie wiem._

 

\*(Moje uzupełnienie (sp7ivo) – wydaje mi się, że głównym powodem zastosowania metody RM w zawodach HST był fakt, że w przypadku odbioru z zapisem, ograniczeniem jest sam zapis, a nie umiejętność odbioru słuchowego, która znacznie przewyższa możliwości zapisu. Zauważmy, że rekordy szybkości odbioru poszczególnych rodzajów tekstu wyrażone w „prędkości rzeczywistej” są bardzo zbliżone, wynoszą w granicach 60-64 gr/min., natomiast wyrażone w WPM różnią się znacznie - 70 do 115 WPM odpowiednio dla tekstu literowego i cyfrowego. Poza tym, w przypadku konkurencji nadawania, pomiar „prędkości rzeczywistej” wydaje się być jedynym realnym do zastosowania sposobem oceny tej konkurencji. )

 

_Główną wadą idei systemu WYSIWYG z kodem Morse'a, „znaków rzeczywistych” lub jakiegokolwiek zbioru standardów jest to, że żadne urządzenie (nie mówiąc o programie generującym zaprogramowane radiogramy) nie może być skalibrowane zgodnie z nimi wszystkimi. Jeżeli skalibrujesz je dla kilku standardów, będziesz poza zasięgiem jakiegokolwiek innego rodzaju standardu szybkości transmisji. Nie poznasz swojej „szybkości”, dopóki faktycznie nie zakończysz tego, co przesyłałeś lub odbierałeś i nie policzysz znaków. Może jednak lepiej odzwierciedlać stopień trudności nadawania dla tej samej prędkości. Teraz znowu zależy, jak na to spojrzysz. Albo bierzesz pod uwagę  „szybkość znaku” wokół tej samej liczby „rzeczywistych znaków”, albo z liczbą „rzeczywistych znaków” wokół ustalonej „szybkości znaku”. Chyba mam teraz ból głowy._

 

_W przypadku PARIS, im dalej odbiegasz od zestawu znaków, dla którego został zbudowany (tekst angielski, w którym przeważają litery takie jak t, e, i itp.), tym niższa jest równoważna prędkość rzeczywista, oczywiście szczególnie mała w przypadku cyfr, które są bardzo długie z punktu widzenia liczby „kropek”._

_Korzyści systemu WPM (PARIS) ? W istocie istnieje tylko jeden punkt odniesienia. W prosty sposób możemy skalibrować urządzenie. Wiemy, jakiej prędkości będziemy używać._

 

_W obu przypadkach musimy zaznaczyć, jakie system stosujemy, np. 500 CPM cyfr, 300 zn /m liter RM itp._

_Uwaga: alfabet Morse'a został zbudowany w taki sposób, aby jak najszybciej przesłać tekst w języku angielskim, w którym dominujące są litery t, e, i, itp. Są najkrótsze (pod względem ilości „kropek”). Następstwem tego jest fakt, że standard PARIS jest również „krótki”._

 

_73, Iulian_
