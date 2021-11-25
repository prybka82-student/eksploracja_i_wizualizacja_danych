Eksploracja i wizualizacja danych - wykł. 2 - 2.10.2021

!!! Quiz po wykładzie, 5 pytań.

Biblioteka tensorflow

# Podstawy matematyczne nauki o danych

## Algebra liniowa

- Skalary, wektory, macierze i tensory
- Mnożenie macierzy i wektorów
- Macierze tożsamości i odwrotne
- Zależność liniowe i rozpiętość (Span)
- Normy
- SPecjalne rodzaje macierzy i wektorów

## Prawdop. i teoria informacji

- Teoria prawdop. 
- Prawdop. 

## Obliczenia numeryczne

- Overflow i Underflow
- Słabe kondycjonowanie 
- Optymalizacja oparta na gradientach 

## Tensor 

- macierz wielowymiarowa 
- liczba wymiarów to ranga tensora 
- macierz 3-wymiarowa to najprostszy rodzaj tensoru 

## SVD - rozkład stosowany w rozpoznawaniu obrazów, sygnałów.

## Skalary, wektory, macierze i tensory

SKalar - to tylko 1 liczba, np. temperetura (1 liczba) 

Wektory - tablica liczb ułożonych w kolejności, zidentifykować każdy nr po indeksie...

Macierze - 2-wymairowa tablica liczb, więc każdy element identyfikuje się przezd 2 indeksy 

Tensor - 3- i więcej wymiarowa macierz liczb, reprezentacja za pom. 3 i więcej indeksó 

Zapis: $A_{i,j,k}$

Wektor można rzutować na 3 osie

Macierz 3-wymairową można przedstawić 3 wektorami  

Macierze można dodawać do siebie, o ile mają ten sam kształt: 

$C = A + B$, gdzie $C_{i,j} = A_{i,j} + B_{i,j}$

W bibliotece tensorflow: 

- tensor rangi 0 to skalar
- tensor rangi 1 to wektor 
- tensor rangi 2 to matryca 
- tensor rangi 3 to 3-tensor 
- tensor rangi n to n-tensor 

Dodawanie i mnożenie macierzy przez skalar

Transpozycja  - odbicie lustrzane wpoprzek linii zw. głóną przekątną 

$A^T$ definijujemy: $(A^T)_{i,j}=A_j$

## Broadcasting 

...

## Mnożenie macierzy i wektora 

Macierz A musi mieć taką samą liczbę kolumn co B_i - mnożenie zwykłe 

Jeśli macierze mają ten sam rozmiar, to możemy zastosować iloczyn poszczegółnych elementów, zw. też element wise product lub Hadaman product 

## Iloczyn skalarny macierzy 

## Właściwość rozdzielna tensorów 

A(B+C) = AB + AC

## Właściwość asocjacyjna tensorów 

...

## Mnożenie macierzy jest nieprzemiene!! 

## Transpozycja mnożenia 

...

## Odwrócenie macierzy 

... 

## Macierz tożsamości (jednostkowa) 

- nie zmienia wartości macierzy podczas mnożenia 

## Macierz odwrotna 

$A^-1$

Taka, że $AA^{-1} = I_n$

W rzeczywistości nie dla każdej macierzy istneije macierz odwrotna. 

Mając macierz odwrotną można...

## Rozkład macierzy 

Dla $A^-1$, $Ax = b$ musi mieć 1 rozwiążanie dla każdej wartości bibliotece

...

Jeśli x i y są rozwiązanaimi, to z = \alpha x + (1- \alpha)y jest też rowiązaniem dla każdego \alpha (liczba rzeczyiwista) 

- tak tworzy się rozpiętość wektorów 

Rozpiętość zbioru wektorów to zbió wszystkich liniowych kominacji wektorów. Formalnie otrzymujemy mnożąc każdy wektor v(i) przed odpowiedni współczynnik skalarny i dodając wyniki: 

$\sum_c_i v^(i)$

Wektory liniowo niezależne - jeśli jedyne rozwiążaie równianai wektorowego \lambda 1 v1 + ... \lambda... 

... 

Aby macierz byłą odwrotna, musi być kwadartowa, czyli wymagamy, aby m=n i aby wszystkie kolumny były liniowo niezależne. Macierz kwadratowa z liniowo zależnymi kolumnami jest znana jako singular. 

Jeśli A nie jest kwadratowe lub jest kwadratowe, ale... 

## Normy 

Norma jest tym, co jest używane do oceny blędu modelu. Formalnie norma L^P to: 

||x||_p = (\sum_i |x_i}^p) ^{1/p)| 

...

Na poziomie intuicyjnym norma wektora x miedzy odległość od początku współrzednych do pktu x. 
 
Dokładniej: norma - odolna funkcja, które spełni właściwości: 
 
$f(x) = 0 -> x = 0$

$f(x+y) <= f(x) + ...$

W przypadku $L^2$ z $p=2$ to norma euklidesowa 

Norma $L^1$

...

Norma Frobeniusa - stosowana w przypadku macierzy 

## Specjalne rodzaje macierzy i wektorów 

Macierze diagonalne (przekątne) mają głównie zera i niezerowe elementy tylko wzdół góównej przekątnej 
  
Aby obliczyć diag(v)x wystarczy przeskalować każdy elemtn x_i o v_i: 


$$diag(v)x = v (*) x$$

...

## Macierz symetryczna 

- jest równa własnej transpozycji 


...

## Wektory ortogonalne 

- dla nich iloczyn skalarny równy jest 0

...

## Wektor jednostkowy 

- to wektor z normą jednostkową ... 

## Wektory ortonormalne 

Macierz ortogonalna to macierz kwadratowa, w której wiersze są wzajemnie ortonormalne, a kolumy wzajemni e ortonormalne: 

$A^TA = AA^T = I_n$

a więc $A^-1 = A^T$

## Tensorflow 

zob. ćw. 18

## Zależność liniowa 

- macierz odwrotna nie istnieje, jeśli wektory liniowo zależne???

## Wektor własny 

- współczynnik... 

...

## Dodatnia/ujemna określoność/półokreśloność macierzy...

...

## SVD 

- dekompozycja wg wartości osobliwych (singularnych) 

Ten rozkład zawsze istnieje (inne - nie zawsze).

Wartości osobliwe (singularne) to wartości zerowe. 

Może być stosowany dla dowolnego kształtu macierzy A

...

# Prawdopodobieństwo i obliczenia numeryczne 

## Słabe warunkowanie/kondycjonowanie 

## Funkcje słabo warunkowane 

- małe zmiany na we powodują duże zmiany na wyjściu 

## Liczba warunkowania 

- stosunek największej do najmniejszej wartości własnej

...

## Optymalizacja oparta na gradientach 

...

## Pochodna kierunkowa

...

## Algorytm poruszanai się małymi krokami...

...


