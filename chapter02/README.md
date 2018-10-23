# Instrukcje warunkowe IF i ELSE

W programowaniu często zadajemy pytania
rostrzygające (na tak lub nie) i na podstawie odpowiedzi, podejmujemy decyzję co
robić. Możemy na przykład zapytać: "Czy masz więcej niż 15 lat?" i jeśli
odpowiedź brzmi "tak", i odpowiedzieć "Ale dużo :o".
Tego rodzaju pytania są
nazywane `warunkami`, łączymy wraz z odpowiedziami w instrukcje `if`(jeżeli).
Warunki mogą składać się z wielu pytań, a instrukcje `if` można konstruować na
podstawie różnych odpowiedzi na te pytania. W tym rozdziale dowiesz się jak
używać instrukcji `if` do pisania programów.

## Instrukcje IF

```python
wiek = 23
if wiek > 15:
    print("Ale dużo :o")
```

Instrukcja if składa się ze słowa kluczowego `if`, po którym podajemy warunek
oraz dwukropek (:), tak jak `wiek > 20:`. Wiersze po dwukropku muszą znajdować
się w bloku, a jeśli odpowiedź na pytanie to `tak`, to polecenia w bloku zostaną
wykonane. Dowiedzmy się teraz jak pisać bloki i warunki.

Blok kodu to w
programowaniu celowo oddzielny zbiór instrukcji. Jeśli przykładowo warunek `if
wiek >10`: jest prawdziwy, możemy wyświetlić informacje ale i nawet kilka innych
zdań. W pythonie bloki kodu wydziela się przez wcięciac(spacje albo tabulatory)

```python
wiek = 23
if wiek > 20:
    print("Ale dużo :o")
    print("Pomóż ojcu w pracach domowych")
```

Powyższy blok składa się z dwóch instrukcji `print`, które są wykonywane tylko
wtedy, gdy warunek `wiek > 20` okaże się prawdziwy. Każdy wiersz w bloku ma o
cztery spacje więcej niż znajdująca się powyżej instrukcja `if`.
W Pythonie
odstęp taki jak np. tabulacja (wstawiana przez naciśnięciu tabulatora) albo
spacja (wstawiana po naciśnięciu spacji) jest bardzo ważny. 

Symbole używane w
instrukcjach warunkowych:

| Symbol        | Definicja         |
| -------------
|:-----------------:|
|==             | równa się         |
|!=  	        |
różny od          |
|>              | większy niż       |
|<		| mniejszy niż
|
|>=		| większy lub równy |
|<=		| mniejszy lub równy|

Jeżeli na przykład masz
10 lat, warunek `wiek == 10 ` zwróci `True`. Jeśli jest inaczej zwróci `False`.
Jeśli masz lat 13, warunek wiek > 10 zwróci `True`. 

Wykonajmy kilka prostych
przykładów. Ustawimy tutaj zmienną, następnie zapisujemy instrukcje warunkową,
która wyświetla tekst "Jesteś za stary na breakdance!", jeśli zmienna wiek ma
wartość większą niż 10:

```python
wiek = 10
if wiek > 10:
    print("Jesteś za stary na breakdance!")
```

Python nie uruchamia bloku `print`. Jeżeli zmienimy to ustawiając wartość wieku
na 20, komunikat zostanie zwrócony.

Zmieńmy teraz powyższy przykład, aby użyć
warunku "większy lub równy" (>=):

```python
wiek = 10
if wiek >= 10:
    print("Jesteś za stary na moje żarty")
```

Ponieważ nasza zmienna wiek ma wartość 10, na ekranie powinniśmy zobaczyć tekst
"Jesteś za stary na moje żarty". Spróbujmy użyć teraz warunku "równa się" (==):

```python
wiek = 10
if wiek == 10:
    print("Jestes za stary na pieluchy")
```

Na ekranie powinien zostać wyświetlony tekst "Jesteś za stary na pieluchy".

##
Instrukcje IF-ELSE

Instrukcji `if` możemy używać nie tylko do wykonywania kodu
w przypadku spełnienia kryteriów warunku (`True`) ale również wtedy, gdy warunek
nie jest zgodny z prawdą. Na przykład treść wyświetlanego komunikatu może
zależeć od tego, czy zmienna `wiek` ma wartość 12 czy też jakąś inną (`False`).
W przypadku tym używamy `if-else`, której sens można wyjaśnić tak: "Jeśli coś
jest zgodne z prawdą, to zrób to, w przeciwnym przypadku, zrób tamto". 

No to
napiszmy instrukcje `if-else`:

```python
print ("Powiedzieć Ci coś śmiesznego")
wiek = 12
if wiek == 12:
    print("Coś śmiesznego")
else:
    print("Ciiiii nie bo ktoś usłyszy!")
```

Ponieważ ustawiliśmy zmienną `wiek` na 12, a warunek sprawdza, czy wartość
zmiennej `wiek` to 12, powinien się pojawić na ekranie pierwszy komunikat. Teraz
zmieńmy wartość na jakąś inną:

```python
print("Powiedzieć Ci coś śmiesznego")
wiek = 7
if wiek == 12:
    print("Coś śmiesznego")
else:
    print("Ciiiii nie bo ktoś usłyszy!")
```

Tym razem powinien być widoczny drugi komunikat.

## Instrukcje IF, ELSE i ELIF
Instrukcje `if` można rozbudować jeszcze za pomocą słowa kluczowego `elif` ( co
jest skrótem od `else-if`). Możemy na przykład sprawdzać, czy osoba ma np. 10,
11, czy 12 lat i nakazać programowi zróżnicowane działania w zależności od
odpowiedzi.  Instrukcje te różnią się od `if-then-else` tym, że jedna instrukcja
może zawierać więcej niż jedno słowo kluczowe `elif`.

```python
wiek = 12
if wiek == 10:
    print("Co robi worek, gdy jest zmęczony?")
    print("Śpiwór!")
elif wiek == 11:
    print("Ile nóg ma koń?")
    print("8! 2 z prawej, 2 z lewej, 2 z tyłu i 2 z przodu")
elif wiek == 12:
    print("Co mówi programista na łożu śmierci?")
    print("Bye world")
elif wiek == 13:
    print("Co rośnie w sadzie programisty?")
    print("Drzewo binarne")
else:
    print("Co?")
```

W tym przykładzie istrukcja `if` w drugim wierszu sprawdza czy wartość zmiennej
`wiek` jest równa 10. Jeśli zmienna wiek ma wartość 10, wykonywana jest
znajdująca się w kolejnym wierszu instrukcja `print`. Ponieważ jednak
ustawiliśmy jednak wiek na 12, program przeskakuje do kolejnej instrukcji `if` i
sprawdza, czy zmienna `wiek` ma wartość 11. Nie ma, więc program przeskakuje do
kolejnej instrukcji `if`, gdzie sprawdza, czy `wiek` równa się 12. Równa się,
więc program wykonuje instrukcje `print`.

Na ekranie powinnien zostać
wyświetlony tekst:

```python
Co mówi programista na łożu śmierci?
    Bye world
```

## Warunki łączone

Warunki można łączyć za pomocą słów kluczowych and (i)
i or (lub), a dzięki temu kod staje się krótszy i prostszy. Oto przykładowe
użycie słowa kluczowego or:

```python
wiek - 13
if wiek == 10 or wiek == 11 or wiek == 12 or wiek == 13:
    print ("Mamo piszę do Ciebie wiersz")
else:
    print("Ale dlaczego?")
```

Widzimy w tym kodzie, że jeśli kiedykolwiek z warunków w pierwszym wierszu jest
spełniony ( jeśli wiek to 10,11,12 lub 13) wykonany zostanie blok kodu w
kolejnym wierszu, zaczynający się od print. Jeżeli nie jest spełniony żaden z
warunków podanych w wierszy pierwszym ( `else`), Python przechodzi do bloku w
ostatnim wierszu, wyświetlając na ekranie `Ale dlaczego?`


## Zadania
1. Utwórz
instrukcje, która sprawdza, czy liczba wafelków (zapisana w zmiennej `wafelki`)
jest mniejsza niż 100 lub większa niż 500. Jeśli warunek jest spełniony, program
powinien wyświetlać komunikaty: "za mało" lub "za dużo".

2. Utwórz instrukcje
`if`, która sprawdza, czy kwota pieniędzy zapisana w zmiennej 'kwota' mieści się
w przedziale od 100 do 500 lub w przedziale od 1000 do 5000.

## Podsumowanie
W tym rozdziale dowiedzieliśmy się, jak za pomocą instrukcji tworzyć bloki kodu,
które są wykonywane tylko po spełnieniu zdefiniowanych warunków. Wiemy, jak
rozbudować instrukcje `if` za pomocą `elif`, aby różne fragmenty kodu były
wykorzystywane w zależności od spełnienia różnych warunków, oraz jak
wykorzystywać `else`, aby wykonywać kod, jeśli żaden z warunków nie zostanie
spełniony.

```python

```
