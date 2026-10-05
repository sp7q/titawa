---
title: "Prosty odbiornik lampowy plus tranzystor."
date: 2021-12-17
categories: 
  - "technika"
---

Kiedy znalazłem w swoich skarbach płytkę PCB z wlutowanymi dwoma podstawkami do lamp, od razu wiedziałem, że ona nie może się zmarnować. Kiedyś był to moduł VOX do lampowego nadajnika firmy Kenwood, co udało mi się zidentyfikować po symbolu. Oryginalnie były tam lampy 6BA6 (mała siedmionóżkowa pentoda), oraz 6AQ8 - ścisły odpowiednik podwójnej triody ECC85. Po krótkim namyśle zdecydowałem, że wykorzystam ją do zbudowania odbiornika homodynowego, co było pewnym wyzwaniem (na pewno na dwóch lampach udało by się łatwiej skonstruować radio o bezpośrednim wzmocnieniu, czy też super reakcyjne).

Postanowiłem maksymalnie wykorzystać istniejące na płytce ścieżki, tak aby uniknąć ich niepotrzebnego cięcia, a potrzebne elementy wlutowywać w miejsce starych, na ile to możliwe. Zrobiłem wstępny szkic - schemat, poszukałem odpowiednich lamp i przystąpiłem do pracy. Generalnie miało to wyglądać tak: pierwsza połówka triody jako oscylator, druga jako mieszacz, a jeśli się da to przy okazji przedwzmacniacz, oraz pentoda jako stopień końcowy. Użyłem lamp ECC85 i 6CB6A (tylko taka mi została z siedmionóżkowych pentod). Mając pewne doświadczenie w budowie odbiorników tranzystorowych, również homodynowych, liczyłem że radio będzie grało pomimo braku wzmacniacza w.cz. Schemat blokowy wyglądał mniej więcej tak:

![](/images/Schemat-blokowy-300x77.jpg)

Radio rzeczywiście zagrało, ale bardzo cicho, za cicho. Pomyślałem, że użycie triody na mieszacz przy tak skromnym budżecie lampowym to marnotrawstwo, tym bardziej, że spisywała się ona w tej roli niezbyt dobrze. Postanowiłem zrobić detektor diodowy, a zwolnioną triodę użyć jako dodatkowy wzmacniacz. Teraz zrobię mały przeskok i pominę opis wielu, wielu eksperymentów takich jak: zmiana punktu pracy lamp, wzmacniacz przed mieszaczem/po mieszaczu, różne rodzaje mieszaczy, różne obwody wejściowe, filtry w.cz./m.cz., transformatory głośnikowe itd. Miła i pożyteczna zabawa na kilka wieczorów. W efekcie odbiornik zaczął grać głośniej i wyraźniej, ale wciąż zbyt cicho jak na moje wymagania.

Podając sygnał z MP3 na wejście pentody stwierdziłem, że jako wzmacniacz audio spisuje się ona naprawdę  dobrze (mówimy cały czas o odbiorze na słuchawkach), również podanie odpowiednio mocnego sygnału na wejście odbiornika (generator sygnałowy) dawało dobre rezultaty, czyli wniosek - trzeba dodać na wejściu brakujący wzmacniacz w.cz. Pomyślałem, że dodanie kolejnej lampy przy braku (na razie) obudowy, a nawet chassis w projekcie który ma być zabawą i polem do edukacji mija się z celem, więc zrobiłem wzmacniacz na tranzystorze - po kilku próbach najlepszym z posiadanych do tego celu okazał się 2N2369. Taki odbiornik jest świetną okazją do przekonania się o wyższości telegrafii nad fonią, jeśli chodzi o łatwość czytania sygnału ;) - o ile każdy sygnał cw odbieramy wyraźnie i bez problemów, o tyle SSB wymaga już dość mocnego sygnału, żeby czytać go komfortowo, tym bardziej, że często występuje spletter lub inne zakłócenia. Na wejściu odbiornika pozostawiłem tylko jeden obwód filtra pasmowego, po to żeby zminimalizować tłumienie obwodów LC.

Na pewno, gdyby poeksperymentować, dodać jeszcze jeden stopień wzmacniacza, odbiór byłby mocniejszy i możliwy na głośniku, ale uznałem to w tym projekcie za niekonieczne - na słuchawkach słucha się całkiem dobrze i nie ma potrzeby odkręcania radia na pełny regulator. ;) Odbiornik sprawia mi wiele radości, choć jest bardzo prosty - to mój pierwszy projekt jeśli chodzi o homodynę lampową - mimo że porównując go do tego zbudowanego na półprzewodnikach, gra słabiej. Ale... ile stopni ma ten na półprzewodnikach, a ile ten, policzmy:

\- odbiornik homodynowy półprzewodnikowy - ilość tranzystorów 3 plus 10 w scalaku audio ;) razem daje trzynaście

\- tutaj mamy tylko cztery stopnie. Efekt zupełnie zadowalający.

Jestem pozytywnie zaskoczony też pracą oscylatora - jest stabilny, można słuchać przez długi czas sygnału SSB, bez konieczności dostrajania się, co jest istotne.

Kondensatory w obwodach wejściowych (po wstępnych obliczeniach) dobierałem podłączając równolegle do cewek kondensator zmienny, kręcąc rotorem aż uzyskałem najgłośniejszy sygnał, następnie dobierałem kondensatory stałe o prawie identycznych pojemnościach.

Przekładni transformatora słuchawkowego nie obliczałem (należałoby podłączyć napięcie zmienne do uzwojenia pierwotnego, zmierzyć napięcie na uzwojeniu wtórnym i podstawić wzór, ale podszedłem bardziej praktycznie. Wziąłem te transformatory głośnikowe, które miałem pod ręką i sprawdziłem które słuchawki/głośniczki o różnej impedancji grają najgłośniej - zwyciężył mały transformatorek i słuchawki lotnicze 100 Ω (grały lepiej niż słuchawki o oporności 50Ω i 200Ω).

Poniżej zamieszczam rysunek schematu w wersji obecnej (brakuje na nim paru szczegółów, głównie chodzi o elementy filtrujące, ale można powiedzieć, że to kosmetyka):

![](/images/Schemat-300x213.jpg)

 

A to zdjęcia z pracy nad odbiornikiem:

![](/images/PCB_2-300x225.jpg)![](/images/PCB_1-300x225.jpg)

![](/images/RX_1-300x225.jpg)  ![](/images/RX_3-300x225.jpg)  ![](/images/RX_2-300x225.jpg)

Zresztą on na razie właśnie tak wygląda, bo jeszcze nie udało mi się znaleźć czy wymyślić fajnej obudowy.

Żeby nie być gołosłownym, zamieszczam również krótkie nagrania, ale uprzedzam, że są one zrealizowane za pomocą telefonu przyłożonego do jednej ze słuchawek, w dodatku spletteruje bardzo mocna, nadająca blisko stacja:

\[audio mp3="http://titawa.pl/wp-content/uploads/2021/12/Nagranie-standardowe-34.mp3"\]\[/audio\]

I trochę telegrafii, również z rodzimego podwórka:

\[audio mp3="http://titawa.pl/wp-content/uploads/2021/12/lampa-homodyn-cw.mp3"\]\[/audio\]

 

Reasumując, trochę żartem, myślę że to byłby fajny odbiornik  dla początkującego konstruktora radioamatora, ale... ze czterdzieści lat temu ;) Teraz wszyscy mają za pieniądze, co tylko sobie zamarzą.

 

Krzysztof, SQ8LUV

[http://sq8luv.pzk.pl](http://sq8luv.pzk.pl)
