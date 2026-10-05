---
title: "Manipulator dotykowy w kluczu arduino"
date: 2019-12-03
categories: 
  - "technika"
---

Większość właścicieli klucza arduino K3NG chyba wie, że ma on na pokładzie funkcję manipulatora dotykowego. Ale prawdopodobnie nie wszyscy sprawdzali jak on działa? ;)

Dziś postanowiłem go przetestować.

Żeby uruchomić tą funkcję wystarczy w pliku _keyer\_features\_and\_options.h_  odkomentować zdanie: #define FEATURE\_CAPACITIVE\_PADDLE\_PINS

i w miejsce mechanicznego manipulatora podpiąć dwie elektrody metalowe służące za „łopatki dotykowe”. Bardzo ważne jest żeby usunąć dwa kondensatory 10nF blokujące wyjście dźwigni manipulatora do masy. Dlatego ja, żeby było szybciej, podłączyłem dźwignie na „krótko”, co widać na filmiku, do dwóch wolnych pinów w arduino i wgrałem na nowo oprogramowanie z uwzględnieniem tej zmiany pinów w pliku _keyer\_pin\_settings.h_

Wrażenia – sam manipulator jako dotykowy działa zaskakująco dobrze, mimo że nie ma on żadnej regulacji czułości. Soft jest tak napisany, że długością kabelków i wielkością powierzchni elektrod dotykowych można łatwo dostosować czułość do swoich potrzeb. Oczywiście przy zmianie temperatury, wilgotności powietrza itp. może się ona trochę zmieniać.

Wadą niestety tego keyera (pomimo jego wielu zalet) jest to, że jeżeli procesor jest obciążony wieloma funkcjami, manipulator zarówno dotykowy jak i mechaniczny potrafi się zacinać, szczególnie przy szybkich tempach. Im większa płytka i ilość uruchomionych funkcji tym niestety bardziej. Gdyby ktoś chciał używać tego rozwiązania, to proponuję zastosować małą płytkę nano 3 i wgrać tylko niezbędne funkcje – bez dekodera, winkeya, klawiatury PS2 itp. odciążając w ten sposób procesor - zrobiłem taki test i okazało się że  klucz nie zacina się. W razie potrzeby, np. udziału w zawodach i używania protokołu Winkey zawsze można na ten czas wgrać zmodyfikowany do potrzeb soft, zajmie nam to kilka czy kilkanaście sekund.

Poniżej krótki filmik z testem manipulatora dotykowego w kluczu K3NG:

https://www.youtube.com/watch?v=WH1yANC5dUg

 

Krzysztof, SQ8LUV
