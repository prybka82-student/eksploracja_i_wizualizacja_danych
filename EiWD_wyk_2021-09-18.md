Eksploracja i wizualizacja danych, wykład, prof. Vasyl Martsenyuk, 18.09.2021

EiWD_wyk_2021-09-18

Prezentacje na e-uczelni

!!!
Będzie quiz po wykładzie do zrobienia!!!
!!!

Wykład - ocena - średnia z quizów. 

Ćw. laboratoryjne - na podstawie ocen ze sprawozdań przesłanych na e-uczelnię. 

---

# Wykład 1

## Treść wykładu

W por. z analizą procesów uczenia, na tych zajęciach temat ogólniejszy - nauka o danych (ang. data science). 

Eksploracja danych - początkowe przygotowanie i analiza danych. 

Wstęp
- Historia
- Czym zajmuje się nauka o danych
- Perspektywa nauki o danych
- Przykłady realnych zadań
- Małe i duże dane

Wstęp do Pythona. Platforma Anaconda
- Dlaczego Python
- Ekosystem
- Anaconda
- Interaktywne środowiska programowania REPL

Podstawy Pythona

Biblioteka Pandas

---

## Nauka o danych (Data Science)

Dyscyplina powstała na styku analizy danych i informatyki. 

Nauka o danych (data science) = analiza danych (data analysis) + informatyka (computer science)

Główny twórca: John W. Tukey (The Future of Data Analysis, 1962). 

Już w latach 60. zauważono, że metody matematyczne nie mogą być stosowane do analizy danych z wykorzystaniem komputerów. 

Nowy paradygmat: nie próbuj przedstawiać wszelkich wymagań dot. danych, ale pozwól im opowiedzieć o sobie. 

Termin "nauka o danych" wprowadzony w latach 1996-7.

---

## Czym zajmuje nauka o danych

Wydobywa z danych nietrywialną i praktycznie użyteczną wiedzę. 

Tworzy modele biznesowe danych i oprogramowanie aplikacyjne (do użycia). 

---

## Perspektywy nauki o danych

- procesy i zjawiska społeczne
- przemysł i handel
- medycyna
- sport

---

## Przykłady zadań

- badania analit. w biznesie i gospodarce (analiza zahcować klientów, prognoza sprzedaży towarów, optymalizacja magazynów)
- sieci społecznościowe, komunikacja i przemysł rozrywkocy (rekomendacje odnośnie do przyjaciół i grup zainteresowań, analiza dyskusji, rekomendacje dot. filmów i kompozycji muz.)
- finanse i bankowość (prognozowanie notowań giełdowych, przewidywanie niewypłacalności osób. fizycznych i prawnych)

---

## Małe i duże dane

Małe dane - można przechowywać i analizować na własnym komputerze. 

Duże dane (big data) - nie wystarczy 1 komputer, konieczne klaster, np. Apache Spark, Hadoop, przetwarzanie online

Przykłady
- obrazy: klasyfikacja obrazów (np. określić markę samochodu na podst. zdjęcia, klasyfikacja obrazów efektywnie rozwiązywane przy użyciu splotowych sieci neuronowych, wymagane karty graf.)
- tekst
- dane rzadkie, z brakującymi wartościami, związ. z prywatnością, bezpieczeństwem
- wyznaczanie ceny mieszkania (nie będzie wymagało dużej mocy oblicz.)
- wybór reklamy dla użytkownika po jego wejściu na stronę, w oparciu o dane historyczne i info o użytkowniku.

---

## Dlaczego Python

- łatwy
- otwarty kod źródłowy
- interaktywny (REPL, Jupyter Notebook, Google Colab)
- istnieje cały ekosystem bibliotek do obliczeń naukowych
- język ogólnego przeznaczenia
- łatwa implementacja w zakresie pobierania danych z witryn Simple Web Server, operacji na plikach 
- przewaga nad R i MatLab
- dynamiczny i wysokiego poziomu
- powstał w 1991 roku
- Python3 z roku 2008 (niezgodny z Python2)
- implementacja referencyjne - CPython - opracowywany przez Python Software Foundation

---

## Ekosystem bibliotek

- NumPy - szybkie operacje na tablicach, algebra liniowa, napisany w C i Fortranie, wysoka optymalizacja
- SciPy - dodatek do NumPy, metody optymalizacji, metody numeryczne, statystyki i in.
- MatplotLib - biblioteka graficzna, wizualizacja danych
- Scikit-Learn - nauczanie maszynowe, wiele gotowych algorytmów, m.in. sieci rekurencyjne, konwolucyjne, wstępne przetwarzanie danych
- Pandas - manipulacja dwuwymiarowymi tablicami danych, analiza danych, tzw. ramki danych
- Statsmodels - modele i testy statystyczne 
- Scitit-image, Pillow - przetwarzanie obrazu
- NLTK, spaCy, gensim - praca z tekstem
- Scrapy - crawler wydobywający dane ze stron internetowych
- TensorFlow, Theano - sieci neuronowe
- inne nakładki na biblioteki (np. OpenCV)

---

## Anaconda 

- zawiera dystrybucję Pythona, instalator dla Windows, Linux, macOS
- wiele bibliotek preinstalowanych
- zob. https://docs.anaconda.com/anaconda/install//
- ustawiać Python3
- alternatywnie można korzystać z kontenerów dockerowych z Anakondą

---

## Interaktywne środowiska programowania REPL

REPL (ang. read-eval-print loop)
- proste, interaktywne środowisko programowania 
- najczęściej oznacza język programowania Lisp, ale może też oznaczać programowanie przy użyciu poleceń powłoki
- inne popularne środowiska dla języków: Smalltalk, Perl, Python, Ruby, Haskell, Scheme, Clojure i in.
- praktycznie każdy język interpretowany posiada REPL

Jupyter Notebook
- dalszy rozwój pomysłu REPL
- z aplikacji Anaconda wybrać Jupyter Notebook lub w wierszu poleceń:

`jupyter-notebook`

lub

`jupyter-lab`

- to ostatnie pozwala opracowywać wiele plików pythona 
- komórki: kod zawiera tekst w formacie Markdown lub kod Pythona
- kernel - obsługa innych języków (Julia, R)

Przydatne skróty notatników:
- Ctrl Enter - uruchomienie komórki
- Esc m - wstawia komórki w trybie Markdown
- Esc a - wstawia nową komórkę przed bieżącą
- Esc b - wstawia nową komórkę pod bieżącą 
- Esc d d - usuwa komórkę

## Podstawy formatowania w Markdownie

`#`, `##`, `###` - nagłówki

`-` - lista

`kod` - kod źródłowy

`$$ \sqrt(x) $$` - LaTeX

`<html kod>` - kod HTML

---

## Podstawy Pythona

- Podstawowe typy
- Ciągi znaków
- Warunki if, elif, else
- Pętle while, for
- Listy, słowniki, krotki, zbiory
- Funkcje
- Sortowanie
- Generatory
- Rekursja
- Wyjątki

---

reversed
sorted

---

































ZAINSTALOWAĆ ANACONDĘ!!!

QUIZ!!!
