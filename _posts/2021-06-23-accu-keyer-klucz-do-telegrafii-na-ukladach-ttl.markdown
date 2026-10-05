---
title: "Accu-Keyer - klucz do telegrafii na układach TTL"
date: 2021-06-23
categories: 
  - "technika"
tags: 
  - "keyer"
  - "klucz"
---

Słyszałem, że przed nastaniem ery kluczy z serii K-5, rządził Accu-Keyer. Wiele współczesnych tego typu urządzeń posiada w swoim menu imitację timingu tego klucza, co tym bardziej zachęciło mnie do jego budowy. W dobie łatwości dostępu do arduino, wykonania keyera na siedmiu układach scalonych TTL może podjąć się tylko człowiek, który naprawdę jest pasjonatem telegrafii.  :) Najpierw trzeba było wyretuszować płytkę (nie znalazłem w pełni gotowego projektu PCB), wytrawić ją i nanieść ręcznie oraz wywiercić dużą ilość dziurek na tyle równo, żeby udało się w nie włożyć wszystkie układy scalone. Reszta to poezja. Autorem klucza jest James M. Garret WB4VVF.                                                                          Nie będę zamieszczał szczegółowego opisu klucza, jeśli ktoś jest zainteresowany poznaniem dokładnej zasady jego działania, odsyłam do oryginalnego artykułu (link nieco poniżej), podam tylko niektóre możliwości jakie posiada:

\- pamięć znaków przeciwnych - pełny iambic - auto-space (tak, tak, jest w nim ta opcja :)) - bardzo przyjemny timing

Ostatnio zastanawiałem się, czy gdyby padł mi mój główny klucz, używałbym w zastępstwie accu-keyera czy też klucza na arduino (nanokeyera) i stwierdziłem, że gdyby ten pierwszy posiadał tą funkcję, którą mają k-5 i nanokeyer, mianowicie opóźnioną pamięć znaków przeciwnych, to chyba wybór padłby na accu-keyera - jego timing jest bardzo przyjemny i miękki, jednak brak tej funkcji wyklucza go u mnie jako narzędzie do nadawania bardzo szybką telegrafią, której jestem miłośnikiem. Kto próbował nadać mój znak tempem 60 wpm za pomocą klucza pracującego w trybie _pełny iambic B_, ten wie o czym mówię ;) - jest bardzo trudno uciec z dźwigni kropek przed nadaniem kreski, tak żeby klucz nie nadał na końcu niechcianej "kropki". W wolniejszych tempach, powiedzmy do 40 wpm, nadawanie na tym kluczu jest bardzo przyjemne. Oryginalnie w opisie podany jest zasięg prędkości keyera od 5 do 50 wpm, ale można to zmienić dobierając odpowiednio wartości elementów. Mojego accu-keyera zmodyfikowałem w taki sposób, że za pomocą przełącznika hebelkowego mogę ustawić w nim dwa zakresy prędkości - nazwijmy je QRS i QRQ. Pierwszy zakres - QRS od 5 do 30 wpm w skrajnych położeniach potencjometru, kiedy hebelek przełącznika jest w górze i drugi zakres - QRQ, od około 25 do 57 wpm gdy hebelek przełącznika jest skierowany do dołu. Na kolejnym przełączniku dodałem też włącznik "nośnej", tak żeby można było wygodniej dostrajać się do anteny, oraz przełącznik do włączania i wyłączania funkcji auto-space. Potencjometr prędkości posiada przy okazji wyłącznik zasilania i sygnalizującej go diody.

Poniżej link do strony z pdf, w którym znajduje się schemat blokowy i ideowy, oraz diagram obrazujący timing klucza, a także dokładny opis autora w języku angielskim:

[https://inza.files.wordpress.com/2011/01/accu-keyer.pdf](https://inza.files.wordpress.com/2011/01/accu-keyer.pdf)

 

 

A to mój egzemplarz klucza: ![](/images/IMG_20210621_231731-225x300.jpg)

![](/images/IMG_20210621_231816-225x300.jpg)

I oczywiście krótki filmik pokazujący jak accu-keyer pracuje:

[https://youtu.be/WqWtnHCdvx4](https://youtu.be/WqWtnHCdvx4)

 

Krzysztof, SQ8LUV
