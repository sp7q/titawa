---
title: "Nauka telegrafii z Tuxem"
date: 2016-04-09
categories: 
  - "bez-kategorii"
  - "programy"
---

![](/images/linux_cw.png) Wspomniany Tux to imię pingwinka obecnego w logo systemu GNU/Linux. Czy Tux może pomóc w nauce telegrafii? Oprogramowanie do nauki CW na Windowsa jest powszechnie znane a co z użytkownikami Linuxa? Pod tym systemem także nie możemy narzekać na brak oprogramowania wspierającego naukę telegrafii. <!--more-->

Przedstawię poniżej kilka prostych narzędzi z których sam korzystam. Prawie wszystkie są dostępne w wersji gotowej do pobrania czy to ze stron ich autorów czy bezpośrednio z repozytoriów Debiana i dystrybucji na Debianie bazujących (na przykład popularnym Ubuntu).

Dodatkowo opiszę (podając kilka prostych przykładów) jak za pomocą narzędzi dostępnych w Linuxie samodzielnie generować lekcje na bazie własnego słownika (na przykład do trenowania najczęściej występujących wyrazów, wyrazów z którymi mamy problemy, skrótów, kodu Q i temu podobnych).

# unixcw

[http://unixcw.sourceforge.net/](http://unixcw.sourceforge.net/) To chyba najpopularniejszy pakiet programów do zamiany tekstu na telegrafię. Można go zainstalować w dystrybucjach Debian i Ubuntu poniższym poleceniem (wydanym z poziomu administratora, na przykład konta użytkownika `root`):

`apt-get install cw cwcp xcwcp`

Składa się z kilku małych prostych programów (oraz biblioteki dla chcących wyposażyć swoje programy w funkcję nadawania komunikatów telegraficznych przez głośnik komputera). Przy odrobinie znajomości programowania (na przykład w C, Pythonie czy nawet Bashu) pakiet można wykorzystać do wielu fajnych rzeczy takich jak powiadomienia telegrafią o nowej poczcie czy o kończącej się baterii w laptopie (i taki jest główny cel powstania pakietu `unixcw` - zamiany komunikatów tekstowych na telegraficzne) ale w tym artykule opisze jak można wykorzystać ten pakiet do nauki odbioru telegrafii.

W skład pakietu wchodzą poniższe programy:

- `cw` - program który odtwarza telegrafią tekst jaki otrzymuje na standardowym wejściu
- `cwgen` - program generujący 5-znakowe losowe grupy
- `cwcp` - połączenie programu `cwgen` i `cw` wraz z tekstowym interfejsem użytkownika
- `xcwcp` - jak `cwcp` tyle że dla miłośników myszek i GUI (oraz pozwala na podłączenie klucza sztorcowego i trening nadawania - ale to już dla nieco ambitniejszych użytkowników Linuxa :D).

Jak tego używać? To bardzo proste! Jeśli mamy na przykład e-booka w pliku o nazwie `ebook.txt` to wystarczy z linii komend wydać polecenie

`cw < ebook.txt`

i już... Linux będzie nam ,,czytał'' e-booka telegrafią. Można też oczywiście wykorzystać mechanizm potoków aby przekierować wyjście dowolnego programu do programu `cw` (i z tej własności też będziemy korzystać używając `cwgen` jak i innych programów, ale wszystko w swoim czasie :D), na przykład:

`date | cw`

Przerwać działanie programu możemy w każdej chwili tak jak w przypadku każdego innego programu uruchomionego w linii poleceń, czyli naciskając `Ctrl+C` (lub inną kombinacją jaką masz ustawioną w terminalu, co można sprawdzić poleceniem `stty -a` i sprawdzić jaka kombinacja jest przypisana do `intr` :D).

Jak zmienić parametry nadawanej telegrafii (prędkość, ton itp.)? Można to zrobić na dwa sposoby. Pierwszy to podanie parametrów w linii poleceń dla programu. Podstawowe opcje to:

- `-w` prędkość nadawania (WPM)
- `-t` wysokość tonu (w hercach)
- `-v` głośność (w procentach, podajemy liczbę w zakresie od 0 do 100 na przykład `-v 50`)
- `-g` dodatkowy odstęp (wyrażony w ilościach kropek) pomiędzy poszczególnymi znakami (przy nauce metodą Farnsworth-a).
- `-e` wyłączenie wyświetlania nadawanych znaków (noecho)
- `-c` wyłączenie obsługi komend umieszczonych w tekście (o szczegółach później)
- `-o` wyłączenie obsługi znaków operatorskich (podawanych w nawiasach kwadratowych) takich jak \[as\] \[ar\] itp.
- `-k` proporcje długości między kropką i kreską (nie używaj tego w początkowej fazie nauki!)

Jeśli więc chcemy aby program nadawał w tempie 20 wpm tonem o częstotliwości 600 Hz i dodawał dodatkowy odstęp między literami długości trzech kropek, to można to zrobić tak:

`cw -w 20 -t 600 -g 3 < ebook.txt`

Oczywiście jeśli chcemy to zrobić dla danych pochodzących z jakiegoś innego programu, to postępujemy analogicznie, na przykład:

`uptime -p | cw -w 20 -t 600 -g 3`

Jest też inna metoda ustawiania parametrów pracy programu. Można mianowicie w treści pliku (lub wyjściu programu) umieścić specjalne sekwencje sterujące modyfikujące parametry już w trakcie działania programu. Podstawowe sekwencje to:

- `%Tn;` zmiana wysokości tonu (na przykład `%T600`)
- `%Wn;` zmiana tempa (WPM)
- `%Gn;` ekstra odstęp między znakami (jak dla -g)
- `{...}` komentarze (wyświetlane na ekranie ale nie nadawane telegrafią)

Te osadzone w tekście polecenia pozwalają na stworzenie gotowych lekcji które oprócz dźwięków wypisują też odpowiednie komentarze i instrukcje na ekranie. Na przykład utwórz plik `lekcja.txt` o treści:

```
%W20; %T600; %G3;
{Za chwilę usłyszysz znak [KN] oznaczający koniec własnego nadawania
i zapraszający do nawawania tylko Twojego korespondenta}
[kn] [kn] [kn] [kn]

```

i odtwórz go za pomocą polecenia

`cw < lekcja.txt`

Program ma też wiele innych możliwości (na przykład możliwość przedefiniowania wbudowanego alfabetu lub zdefiniowania nowych znaków jeśli na przykład chcesz się uczyć polskich ,,ogonków''). Po szczegóły odsyłam do podręcznika opisującego dokładnie wszystkie możliwości programu, czyli polecenie `man cw` (wyjście poprzez naciśnięcie `q` :D).

Kolejnym programem z pakietu unixcw jest program `cwgen`. Podstawową funkcją programu jest generowanie tekstów do ćwiczenia odbioru losowych grup. Nie będę się rozpisywał o wszystkich możliwościach programu, opiszę jedynie podstawowe:

- `-g` ile losowych grup wygenerować
- `-n` wielkość grupy (domyślnie pięcioznakowe, można też podać argument w rodzaju 2-5 a wtedy program będzie losował grupy długości od 2 do 5 znaków)
- `-r` ile razy powtarzać grupę (domyślnie bez powtórzeń)
- `-c` spośród jakich znaków losować grupy (domyślnie wszystkie litery i cyfry bez znaków pisarskich)

Czyli jeśli chcemy wygenerować 5 grup wielkości od 2 do 7 znaków składających się tylko z liter "ABCDEFGHIJ" i każda powtórzona jeden raz, to wydajemy polecenie:

`cwgen -g 5 -r 1 -n 2-7 -c "ABCDEFGHIJ"`

Oczywiście wygenerowany tekst możemy ,,wpuścić'' do programu `cw` za pomocą polecenia:

`cwgen -g 5 -r 1 -n 2-7 -c "ABCDEFGHIJ" | cw -w 20 -t 600`

lub zapisać do pliku poleceniem:

`cwgen -g 5 -r 1 -n 2-7 -c "ABCDEFGHIJ" > nazwa_pliku.txt`

Programów `cwcp` jak i `xcwcp` nie ma sensu szczegółowo opisywać, mają one dosyć intuicyjny interfejs użytkownika a w praktyce są tylko nakładką na programy opisane wyżej. Bez problemu sam dojdziesz co i jak.

# morse + QSO

[http://www.catb.org/~esr/morse-classic/](http://www.catb.org/~esr/morse-classic/) Instalacja w Debianie i Ubuntu poleceniem:

`apt-get install morse`

Pakiet funkcjonalnie podobny do wymienionego wyżej `unixcw`, a opisuję go tylko dlatego, że zawiera program o nazwie `QSO` generujący krótkie przykładowe QSO prowadzone otwartym tekstem. Wynik działania programu `QSO` możemy jak wyżej przekierować do programu `cw` lub do programu `morse` (działającego w analogiczny sposób).

Program `morse` ma jeszcze ciekawą możliwość ćwiczenia odbierania nadawanego tekstu poprzez pisanie go na bieżąco na klawiaturze (czy wręcz automatycznego przeprowadzania testów przepisywania odbieranego tekstu na klawiaturze), ale najpewniej nie będziesz z tego na początku korzystał.

Oto podstawowe opcje programu `morse`:

- `-i` nadawanie tego co wpisujemy z klawiatury (bez wyświetlania znaków na ekranie)
- `-I` jak wyże, tyle że z wypisywaniem na ekran
- `-w` tempo nadawania (wpm)
- `-f` częstotliwość tonu (w hercach)
- `-v` głośność (od 0 do 1, na przykład 0.5 to 50% maksymalnej głośności)
- `-F` tempo Farnsworth-a (wpn), używane w połączeniu z -w dla dodatkowych odstępów
- `-T` piszemy na klawiaturze to, co nadaje program, a program weryfikuje czy prawidłowo odbieramy
- `-t` jak wyżej, tylko na ekranie nie jest wypisywane to co piszemy
- `-s` program nadaje literę i czeka aż na klawiaturze ją wpiszemy (i oczywiście weryfikuje czy prawidłowo odebraliśmy)
- `-q` jak -T tylko program próbuje inteligentnie się ,,resynchronizować'' mimo popełnianych przez nas błędów (w przypadku -T po prostu się zatrzymuje i czeka aż poprawimy tekst, nie ignorując błędów)
- `-d` w połączeniu z -T, -t lub -q program automatycznie dobiera tempo w zależności od tego jak nadążamy z pisaniem i ile błędów popełniamy (zwalnia gdy popełniamy więcej błędów i przyspiesza gdy tych błędów nie popełniamy)

Na przykład jeśli chcemy potrenować odbieranie losowych grup z zapisem na klawiaturze z automatycznym dobieraniem tempa, wyświetlaniem tego co piszemy (z podświetlaiem błędów) i inteligentnym ,,dopasowaniem'' do popełnianych przez nas błędów, możemy wydać polecenie:

`cwgen | morse -d -q -T`

Po więcej szczegółów odsyłam do dokumentacji programu (`man morse`).

# ebook2cw

[https://fkurz.net/ham/ebook2cw.html](https://fkurz.net/ham/ebook2cw.html)

Instalacja w Debianie i Ubuntu poleceniem:

`apt-get install ebook2cw`

Nakładkę graficzną do programu (wymaga wcześniejszego zainstalowania `ebook2cw`) można zainstalować poleceniem:

`apt-get install ebook2cwgui`

Działa podobnie do programów opisanych powyżej, jednak wynikiem jego działania nie są dźwięki w głośniku lecz plik MP3 (lub OGG) na dysku. Program umożliwia nam więc przygotowanie sobie lekcji do słuchania bez użycia komputera (na przykład na odtwarzaczu MP3, telefonie itp.).

Przejdę od razu do omówienia podstawowych opcji programu:

- `-w` prędkość nadawania (wpm)
- `-e` prędkość ,,odstępów'' między znakami (wpm, umożliwia naukę metodą Farnsworth-a)
- `-W` dodatkowy odstęp między wyrazami (nie zmienia odstępu pomiędzy literami w wyrazie)
- `-f` częstotliwość tonu (w hercach)
- `-T` rodzaj generatowanego tonu (0 - sinus, 1 - połokształtny, 2 - prostokąt)
- `-Q` co ile minut program ma automatycznie podnosić tempo o 1 wpm (tempo jest resetowane po każdym rozdziale, jeśli chcemy uniknąć resetowania prędkości, to należy dodać też opcję `-n`)
- `-p` wyłącza generowanie znaku <BT> przy napotkaniu nowego paragrafu (pustej linii)
- `-O` generowanie pliku w formacie OGG (bez tej opcji generowany jest plik MP3)
- `-q` jakość generowanego pliku 1 - najlepsza, 9 - najgorsza (nie zmienia bitrate!)
- `-b` bitrate pliku MP3 (domyślne jest 16, nie ma sensu używać wyższego niż 32 jeśli ton jest sinusoidalny)
- `-R` i `-F` tzw. twardość kluczowania czyli jak szybko sygnał narasta od zera do maksimum (-R) i jak szybko maleje od maksimum do zera (-F), domyślne wartości to 50
- `-c` sekwencja znaków oddzielająca rozdziały (na przykład `-c "ROZDZIAL"`), napotkanie tej sekwencji spowoduje rozpoczęcie generowania kolejnego pliku MP3/OGG
- `-o` nazwa pliku wyjściowego (program sam dodaje do podanej nazwy numery rozdziałów i końcówkę .mp3/.ogg)
- `-a` i `-t` umieszcza w tzw. tagach ID3 pliku odpowiednio autora (-a) i tytuł utworu (-t), które są wyświetlane przez odtwarzacze MP3/OGG
- `-N` dodaje szum tła, wartość parametru od -10 do 10 (wartości ujemne należy podawać w cudzysłowie, na przykład `-N "-3"`)
- `-B` szerokość symulowanego filtra w hercach (dopuszczalne wartości to 100,500,1000,2100), częstotliwość środkowa filtru jest na stałe zakodowana w programie i nie można jej zmienić (800 Hz)

Znaki specjalne typu AR, SK (które mają być nadane bez odstępu między literami) umieszczamy w nawiasach trójkątnych, czyli jako <AR>, <SK> itd.

Jeśli chcemy przykładowo wygenerować plik MP3 z jakimś tekstem nadawanym w tempie 20wpm ale z dodatkowym odstępem między wyrazami (przykładowo 5 kropek) tonem o częstotliwości 700 Hz i umieścić to w pliku zaczynającym się od "lekcja", to robimy to nastepująco:

`echo "sp1abc sp1abc sp1abc de sq2xyz sq2xyz sq2xyz <ar>" | ebook2cw -w 20 -W 5 -f 700 -o lekcja`

Jeśli chcemy zamienić ebooka `ebook.txt` na telegraficznego audiobooka w krótym rozdziały są rozdzielone słowem CHAPTER (a nazwy plików niech się zaczynają od ,,lekcja'') i chcemy aby każdy rozdział był w osobnym pliku oraz tempo początkowe wynosiło 15wpm i wzrastało o 1wpm co 5 minut, to użyjemy polecenia:

`ebook2cw -w 15 -Q 5 -c "CHAPTER" -o lekcja < ebook.txt`      (znak `<` można pominąć)

Tak samo jak poprzednie programy, także i ten obsługuje polecenia umieszczane wewnątrz tekstu wejściowego zmieniające podstawowe parametry (tym razem dla odmiany poprzedzamy je znakiem `|` czyli pionową kreską. Oto one:

- `|f` częstotliwość w hercach (na przykład `|f700` dla tonu 700Hz)
- `|w` tempo (wpm)
- `|e` tempo efektywne (Farnsworth-a)
- `|v` głośność od 1 do 100 (w połączeniu z `|N` pozwala na symulowanie QSB)
- `|T` rodzaj generatora (wartości jak przy `-T`)
- `|N` poziom szumów tła (jak przy `-N`)

Jak w przypadku poprzednich programów, pełna dokumentacja jest dostępna w podręczniku systemowym (`man ebook2cw`).

Jesli nie chcesz się bawić w przełączniki i opcje, możesz skorzystać z graficznej nakładki na program (która jest tak intuicyjna, że nie ma sensu jej opisywać), wystarczy wydać polecenie:

`ebook2cwgui`

Pewnym problemem może być konwersja e-booków zawierających polskie litery (ogonki), ale i na to Tux ma swoje sposoby. Jednym z nich jest program `iconv`, aby skonwertować e-booka w kodowaniu utf-8 do wersji bez ogonków wystarczy polecenie:

`iconv -f utf-8 -t us-ascii//TRANSLIT//IGNORE < ebook.txt > ebook_nopl.txt`

Jeśli mamy e-booka z inną tablicą kodową polskich znaków, na przykład Windows-1250 lub ISO-8859-2, to jako argument opcji `-f` podajemy odpowiednio `windows-1250` lub `iso_8859-2`.

# QRQ

[https://fkurz.net/ham/qrq.html](https://fkurz.net/ham/qrq.html)

Autor programu ebook2cw napisał też program do ćwiczenia QRQ. Nazwa programu chyba nie będzie wielkim zaskoczeniem, nazywa się `QRQ`.

Instalacja jak to w Debianie i dystrybucjach pochodnych (takich jak Ubuntu), banalnie prosta (jeszcze :D), wystarczy wpisać (jak zawsze przy instalacji oprogramowania z repozytorium potrzebujemy uprawnień administratora, czyli robimy to z terminala/konta `root`):

`apt-get install qrq`

Program w swojej pierwotnej postaci służy ćwiczeniu odbierania znaków amatorskich nadawanych w szybkim tempie, ale co to dla takich hackerów jak my, nauczymy się przystosowywać program do nauki dowolnych słówek! Skorzystamy z faktu, że program trzyma bazę znaków w pliku tekstowym i go po prostu podmienimy na swój zestaw słówek (czy skrótów, kodów Q itp., zależnie od tego co akurat chcemy ćwiczyć).

W przeciwieństwie do poprzednich programów ten... nie ma zadnych opcji, po prostu wydajemy polecenie:

`qrq`

Przy pierwszym uruchomieniu program informuje o domyślnych opcjach konfiguracyjnych, potwierdzamy je klawiszem `ENTER` i już widzimy ekran startowy. Program prosi nas o podanie znaku i wyświetla informację o możliwości zmiany ustawień konfiguracyjnych poprzez naciśnięcie klawisza `F5`. Wyjść z programu można poprzez naciśnięcie klawisza `F10` (czasem kilkukrotne gdy potrzebujemy wyjść z kilku ,,ekranów'').

Jeśli chcemy ćwiczyć słówka z własnych słowników, to należy je utworzyć w postaci zwykłych plików tekstowych (po jednym słówku w wierszu) i zapisać je pod dowolną nazwą zakończoną na `.qcb` a następnie należy ten plik umieścić w folderze `~/.qrq` (przykładowy słownik podstawowych słów z języka angielskiego znajduje się w pliku `/usr/share/qrq/english.qcb`). Następnie po uruchomieniu programu można wybrać utworzony przez nas słownik wchodząc w ekran konfiguracyjny (`F5`) i wybierając opcję `d` (Callsign database) wskazać utworzony przez nas słownik (po wybraniu słownika i powrocie do ekranu konfiguracyjnego można nacisnąć klawisz `F2` aby ustawienie zmienić na stałe).

Sama nauka przebiega w sposób nie wymagający szczegółowych objaśnień. Program losuje 50 słówek ze wskazanego słownika i kolejno odgrywa je a my wpisujemy je na klawiaturze (możemy wcisnąć `F6` aby program odtworzył ponownie słówko, normalnie program pozwala na jednokrotne powtórzenie, ale można w konfiguracji ustawić nielimitowane powtórzenia). Jeśli odebraliśmy słówko bezbłędnie, to program nalicza nam punkty oraz zwiększa tempo nadawania słówka, zaś jeśli popełniliśmy błąd, to program nalicza mniej punktów za słówko (zależnie od popełnionych błędów) oraz zmniejsza tempo nadawania (nie schodząc jednak poniżej ustawionego przez nas minimum). W ten sposób program już po kilku słówkach dopasuje się do optymalnego dla nas tempa.

# MorsePractice

[https://github.com/jawatson/MorsePractice](https://github.com/jawatson/MorsePractice)

Instalacja już będzie nieco większą ,,przeprawą'', bo konieczna będzie samodzielna kompilacja ze źródeł (to nic strasznego!). Ale po kolei... MorsePractice to klon programu G4Fon. Do działania wymaga zainstalowanego w miarę aktualnego środowiska JRE (JavaSE Runntime). Działa zarówno pod Javą od Oracle jak i tej z OpenJDK. Java od Oracle (JDK) jest prosta do zainstalowania, ale my pójdziemy na łatwiznę i skorzystamy z jeszcze łatwiejszego do zainstalowania OpenJDK (i kilku innych narzędzi) po prostu po to aby nie kopać się z przysłowiowym koniem, tylko maksymalnie jak się da wykorzystać gotowe pakiety z repozytorium. Potrzebować będziemy następujących narzędzi:

- `java/javac` - środowisko wirtualnej maszyny Java wraz z kompilatorem (bo będziemy budować `MorsePractice` ze źródeł)
- `git` - program do zarządzania wersjami kodu źródłowego, my wykorzystamy go jedynie do pobrania najnowszej wersji `MorsePractice` z serwisu GitHub (na którym autor udostępnia wersję źródłową najnowszej wersji programu)
- `ant` - program do automatyzowania kompilacji i budowania gotowej aplikacji (można to zrobić ręcznie, ale to zabawa dla osób zaznajomionych z programowaniem w Javie, my pójdziemy na łatwiznę)

A więc do dzieła. Przystępujemy do instalowania wymaganych pakietów (instalację pakietów, a dokładniej polecenie `apt-get` wykonujemy z konta administratora).

`apt-get install git ant openjdk-8-jdk default-jdk`

`update-alternatives --config java` (wybieramy wersję java-8-openjdk, w moim przypadku jest to cyfra 2, ale u Ciebie może być inna)

Mamy już wszystkie niezbędne narzędzia, resztę czynności wykonujemy już z konta zwykłego użytkownika (z terminala).

`mkdir MP; cd MP` (tworzymy folder do pracy i wchodzimy do niego)

`git clone https://github.com/jawatson/MorsePractice.git` (pobieramy źródła)

`cd MorsePractice` (wchodzimy do utworzonego przez program `git` folderu ze źródłami)

`ant jar` (kompilujemy program i zlecamy utworzenie paczki JAR gotowej do uruchomienia)

W folderze `build/jar` (wchodzimy do niego poleceniem `cd build/jar`) znajdziemy plik `MorsePractice.jar` z gotowym programem. Kopiujemy ten plik gdzie nam się podoba, a program uruchamiany poleceniem:

`java -jar MorsePractice.jar` (lub podajemy ścieżkę do pliku jeśli nie jesteśmy akurat w tym samym folderze co plik z programem).

Obsługa programu jest intuicyjna, więc nie ma sensu się rozwodzić nad wszystkimi opcjami.

# Textutils

To nie jest nazwa jakiegoś konkretnego programu tylko zwyczajowe określenie narzędzi do przetwarzania plików tekstowych, obecnych w każdym UNIX-ie (a więc i Linuxie).

Linux koncepcyjnie pochodzi od wcześniejszych UNIX-ów (o których możesz posłuchać na przykład tu [AT&T Archives: The UNIX operating system](https://www.youtube.com/watch?v=tc4ROCJYbm0) - wyobraź sobie system komputerowy gdzie nie ma folderów, pliki nie mają nazw, nie ma driverów do urządzeń, nie ma wielozadaniowości, nie ma kont użytkowników i haseł, nie ma mechanizmów komunikacji między programami i wielu innych ,,oczywistych'' rzeczy... koszmar? to wszystko zawdzięczamy tym kilku osobom pokazanym na filmiku :D).

Jako że u swoich założeń rodzina UNIX jest dla osób ,,technicznych'' (myślących algorytmicznie), to środowisko użytkownika zostało zbudowane w postaci małych, prostych programów oraz rozbudowanych mechanizmów komunikacji między tymi programami (UNIX a co za tym idzie i Linux jest jak klocki Lego - zamiast dawać gotowy przedmiot-zabawkę dają zestaw klocków, z których można zbudować sobie co się chce). Jednym z takich zestawów ,,klocków'' jest właśnie pakiet textutils (domyślnie zainstalowany w każdym Linuxie, więc nie musisz nic robić, wystarczy z nich korzystać).

Narzędzia z jakich będziemy korzystać to:

- `sort` - wbrew nazwie program nie tylko sortuje, my wykorzystamy go do czegoś wręcz przeciwnego, czyli do losowego ,,pomieszania'' zawartości pliku
- `bash` - shell (domyślny w Linuxie) w którym będziemy pisać proste skrypty
- `cat` - prosty program który... wyświetla zawartość pliku na ekranie (a dokładniej przekierowuje go na standardowe wyjście, którym domyślnie jest ekran, ale my to zmienimy)
- `head` - program podobny do `cat` ale wyświetlający tylko konkretnie wskazaną ilość początkowych linijek z podanego pliku
- `tail` - jak `head` tylko wyświetla końcówkę pliku
- `tr` - podmienia znaki w pliku (na przykład końce linii na spacje itp.)

Potrzebny też będzie jakiś edytor tekstu (ASCII), tu już wybór pozostawiam tobie, czy będzie to Vim, czy Emacs, czy Joe, czy gedit nie ma znaczenia - wybierz to co jest dla Ciebie wygodne.

Zaczniemy od utworzenia sobie pliku tekstowego ze zbiorem słówek jakich będziemy się uczyć. Każde słówko umieść w osobnej linijce, tak jak w przykładowym poniższym pliku (nazwijmy go roboczo `slownik.txt`):

```
  cq
  de
  qsl
  hr
  is
  73
  qth
  name

```

 

A teraz napiszemy sobie prosty skrypt, nie będę tłumaczył szczegółów, możesz ten skrypt portaktować jako ,,gotowca''. Załóżmy, że skrypt zapiszemy w pliku `skrypt.sh`

```
for X in $*
do
 head -q -n 3 "${X}" | tail -q -n 2 | sort -R | tr '\n' ' '
done

```

Jak działa ten skrypt? To nic skomplikowanego! Pętla `for` przebiega po wszystkich argumentach jakie podamy do skryptu ($\*) i dla każdego obiegu tej pętli przypisując zmiennej X bieżącą jego wartość wykonuje polecenia zawarte pomiędzy `do` i `done`. Co robią polecenia wewnątrz pętli? Polecenie `head` bierze trzy linijki tekstu (liczba po `-n`) z każdego pliku jaki dostanie na wejście, czyli w naszym przypadku wyrazy "cq de qsl", następnie wynik przekazuje do programu `tail`, który z tego co dostał bierze dwie ostatnie linijki, czyli w naszym wypadku zostaje "de qsl", następnie wynik jest przekazany do programu `sort`, który ,,sortuje'' wyrazy przy pomocy losowo wygenerowanej kolejności alfabetycznej (opcja `-R` programu), za każdym razem innej, następnie wynik idzie do programu `tr`, który podmienia wszystkie znaki nowej linii (\\n) na spacje i... ponieważ wynik polecenia `tr` nie jest przekierowany do dalszych programów, więc ląduje na standardowym wyjściu, którym domyślnie jest ekran.

Oczywiście liczby po parametrze `-n` w programach `head` i `tail` możesz modyfikować wedle uznania aby skrypt generował losowe sekwencje z wybranego przez Ciebie fragmentu słownika.

Jak to uruchomić? To też prosta sprawa, wystarczy polecenie:

`bash skrypt.sh slownik.txt`

i na ekranie zobaczysz losową sekwencję wyrazów. Jeśli chcesz utworzyć dłuższą lekcję możesz jako argument podać kilkakrotnie ten sam plik słownika, na przykład:

`bash skrypt.sh slownik.txt slownik.txt slownik.txt`

Jeśli chcesz ćwiczyć cały słownik (wolisz modyfikować zasób słówek w słowniku zamiast modyfikować skrypt), to możesz go uprościć do postaci:

```
for X in $*
do
 cat "${X}" "${X}"| sort -R | tr '\n' ' '
done

```

Przy okazji zauważ zwielokrotniony argument `"${X}"` dla polecenia `cat` - zwiększając lub zmniejszając ilość `"${X}"` możesz regulować ile razy dane wyrazy mają być powtórzone w sekwencji wyjściowej (w podanym przykładzie każdy wyraz pojawi się dwukrotnie), to się może przydać w początkowym etapie nauki gdy będziesz potrzebował kilkukrotnego powtórzenia wyrazu zanim go prawidłowo rozpoznasz.

No dobra, masz wyrazy na ekranie ale jak to wykorzystać? Nic prostszego, wystarczy przekierować wyjście skryptu do pliku, na przykład tak:

`bash skrypt.sh slownik.txt slownik.txt slownik.txt > audiobook.txt`

Wynik działania skryptu zamiast na ekranie, będzie zapisany w pliku `audiobook.txt` z którym już sobie poradzisz za pomocą wcześniej poznanych programów (`cw` lub `ebook2cw`).

* * *

,,Pingwin z kluczem'' jest logiem programu [CWirc](http://myspace.voo.be/pcoupard/cwirc/) - klienta IRC na Linuxa przeznaczonego specjalnie dla telegrafistów (umożliwia rozmawianie telegrafią przez internet).
