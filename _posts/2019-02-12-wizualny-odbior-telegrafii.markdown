---
title: "Wizualny odbiór telegrafii"
date: 2019-02-12
categories: 
  - "ciekawostki"
---

Dużo łączności radioamatorskich wykonuje się stosując emisję CW, zwaną telegrafią. Telegrafię na ogół odbiera się słuchowo, jednak wymaga to treningu i wprawy, jeśli chodzi o sam odbiór nadawanego sygnału. Niektórzy próbują korzystać z automatycznych dekoderów i skimmerów, jednak są one bardzo zawodne, szczególnie w przypadku występowania zakłóceń i zmian siły sygnału. Wynika to z faktu, że niektórzy traktują CW jako jedną z emisji cyfrowych.

Samo słowo "telegrafia" sugeruje, że jest to coś związane z wyświetlaniem lub zapisywaniem (grafia) na odległość (tele). Pierwsze telegrafy działały wykorzystywały ruchomy pisak, który unosił się i opadał bazując na odbieranym sygnale, pisak rysował kreski i kropki na wstędze papieru. Telegrafiści zauważyli, że wystarczy zapamiętać odgłosy pracy telegrafu podczas odbioru poszczególnych znaków, żeby móc odbierać przekaz bez oglądania generowanego zapisu. W ten sposób telegrafia stała się emisja do odbierania na słuch.

W obecnych czasach, możliwe jest bezproblemowe generowanie spektrogramu dźwięku lub sygnału radiowego, co umożliwia obrazowanie sygnału telegraficznego w sposób zbliżony do zapisu przekazu w pierwszych telegrafach. Ta forma prezentacji została zastosowana między innymi w programie Pileup runner (gra symulująca pracę stacji przy bardzo duże liczbie korespondentów) i Argo (program używany w emisjach QRSS w pasmach 630m i 2200m).

W wolnym czasie postanowiłem opracować prostą aplikację działającą w przeglądarce internetowej. Przetestowana w przeglądarkach Chrome i Firefox na komputerze z systemem Windows i na smartfonie z systemem Android, nie gwarantuję poprawnego działania w innych przeglądarkach i systemach operacyjnych, wymaganiem jest przeglądarka obsługująca interfejs WebAudio. [https://github.com/andrzejlisek/AudioSpectrum](https://github.com/andrzejlisek/AudioSpectrum)

Sama aplikacja może służyć do obrazowania dowolnego dźwięku rejestrowanego przez urządzenie (komputer lub smartfon), jednym z jej zastosowań jest odbiór telegrafii w sposób wizualny. Spektrogram można wyświetlać w dowolnym kierunku (poprzez zmianę orientacji wyświetlania), można też zmieniać parametry wraz ze wstecznym odmalowaniem widma. Aplikacja nie wymaga instalacji, może działać zarówno jako online (uruchomiona na serwerze HTTP/HTTPS), jak i offline (pliki skopiowane do pamięci trwałej w urządzeniu docelowym).

Odbiór wizualny również wymaga treningu, takiego samego, jak odbiór słuchowy (można stosować te same metody pod względem zbioru znaków, prędkości nadawania i czasu przerw między znakami i grupami), jednak efekt osiąga się w krótszym czasie i mniejszym wysiłkiem (miarą efektu jest umiejętność odbioru treści składającej się z ciągu losowych znaków w założonej/zaplanowanej prędkości). Tak, jak przy telegrafii słuchowej, przy telegrafii wzrokowej sam proces dekodowania jest dokonywany przez człowieka, zadaniem aplikacji jest jedynie prezentować odebrany dźwięk, sposób prezentacji dźwięku można zmieniać w sposób uwydatniający sygnał przeznaczony do odebrania. Przy odbiorze wzrokowym, podobnie jak przy odbiorze słuchowym, nie należy postrzegać poszczególnych sygnałów (kresek i kropek). Każdy znak należy traktować jako jeden, niepodzielny obraz. Można powiedzieć, że na ekranie pojawiają się poszczególne znaki, przy czym jest inna forma zapisu, podobnie, jak alfabet grecki, rosyjski, gdzie większość znaków jest wspólna z alfabetem łacińskim, jednak stosuje się inne symbole graficzne tych znaków.

Odbiór wzrokowy ma swoje zalety nad odbiorem słuchowym:

\- Metoda łatwiejsza do nauczenia niż odbiór słuchowy

\- Nie wymaga pełnej koncentracji na odbiorze dźwięku - odczuwalne jest mniejsze zaangażowanie umysłu podczas odbioru

\- Możliwy jest jednoczesny odbiór kilku sąsiednich sygnałów przez kilka osób (każda koncentruje się na innym sygnale) lub odczyt najważniejszych fragmentów różnych sygnałów (na przykład znaki wywoławcze stacji)

\- Chwilowe rozproszenie uwagi lub chwilowa koncentracja na określonym miejscu sygnału nie powoduje straty bieżącego sygnału (w zależności od ustawień wyświetlania, dostępna jest cała treść od kilku sekund do kilku minut wstecz)

\- Przy pewnej wprawie możliwy jest odbiór z dużą prędkością wykorzystując te same zdolności i mechanizmy człowieka, co w przypadku tekstu pisanego

Ale, jak każda rzecz, ma też wady:

\- Wymagane jest dodatkowe urządzenie oprócz samego radioodbiornika - tę wadę można zniwelować poprzez odpowiednie przygotowanie smartfonu, który niemal zawsze ma się przy sobie

\- W przypadku odbioru z zapisem odebranej treści na kartce, możliwe jest "zgubienie" aktualnej pozycji odbieranej treści spowodowane oderwaniem wzroku od wyświetlacza treści

\- W pewnych przypadkach bardzo słabych sygnałów odbiór może nie być możliwy lub być znacznie utrudniony podczas, gdy odbiór słuchowy jest możliwy

**Andrzej SP3ANL**
