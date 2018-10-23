# Funkcje i moduły

Zastanów się, ile rzeczy wyrzucasz każdego dnia: butelki po
wodzie, torebki po chipsach, pudełka po lodach, gazety itd. A teraz wyobraź
sobie, co by się stało, gdyby wszystkie te śmieci lądowały
po prostu na stosie
na podjeździe do Twojego domu, bez segregowania papieru, plastiku i aluminiowych
puszek.

Pewnie w miare możliwości segregujesz odpady i to się chwali, ponieważ
nikt nie lubi w drodze do szkoły przedzieradź się przez górę śmieci. Znacznie
lepiej jest, jeśli te wszystkie
niepotrzebne, szklane pojemniki zostaną
przetopione na nowe słoiki czy butelki, jeśli makulatora zostanie przemielona na
papier makulatorowy, a plastik przerobiony na inne wyroby plastikowe.

W ten
sposób ponownie wykorzystujemy różne rzeczy, które w przeciwnym razie lądowałyby
na coraz wyższym poziomie śmieci. W świecie programowania zasada powtórnego
wykorzystywania jest równie ważna.
Oczywiście programy nie znikają pod górą
śmieci, ale jeśli nie będziemy w jakimś stopniu wielokrotnie wykorzystywać tego,
co już mamy, to od ciągłego
przepisywania kodu zatrzemy sobie palce. Powtórne
wykorzystanie kodu to również krótsze i łatwiejsze do czytania programy. Jak się
wkrótce przekonasz w Pythonie jest kilka sposobów tworzenia kodu
wielokrotnego
użytku.

## Używanie funkcji

Jeden ze sposobów na wielokrone używanie kody
Pythona już znamy. W poprzednim rozdziale użyliśmy funkcji `print`, `range` i
`list`, aby nakazać Pythonowi liczenie:

```python
print(list(range(0,5)))
```

Każdy, kto potrafi liczyć, poradzi sobie z napisaniem listy zawierającej kolejne
liczby, po prostu je wypisując, ale im dłuższa lista, tym więcej pisaniny.
Dzięki funkcjom utworzenie
lisy zawierającej tysiące pozycji nie jest niczym
trudnym.
Poniżej generujemy listę liczb za pomocą funkcji `list` i `range`:

```python
print(list(range(0,100)))
```

Funkcje to fragmenty kodu, które nakazują Pythonowi wykonać jakieś zadanie. Jest
to jeden ze sposobów na wielokrotne wykorzystywanie kodu - funkcji można
wielkrotnie używać w różnych programach.
Przydatność funkcji widać już przy
pisaniu prostych programów. Gdy zaczniesz pisać długie, bardziej skomplikowane
aplikacje, takie jak gry, przekonasz się, że funkcje są niezastąopione.

##
Budowa funkcji

Funkcja składa się trzech części: nazwy, parametrów i treści.
Oto przykład prostej funkcji:

```python
def funkcjaTestowa(mojeImie):
    print("Witaj %s" % mojeImie)
```

Nazwa funkcji to `funkcjaTestowa`. Ma ona jeden parametr, `mojeImie`, a jej
treścią jest blok kodu znajdujący się bezpośrednio pod wierszem zaczynającym się
od `def`.
Aby wykonać funkcję, należy ją wywołać, podając kolejno jej nazwę i
wartość parametru w nawiasach:

```python
def funkcjaTestowa(mojeImie):
    print("Witaj %s" % mojeImie)

funkcjaTestowa("Marta")
```

Możemy też najpierw utworzyć kilka zmiennych, a następnie wywołać funkcje,
podając ich nazwy jako parametry:

```python
def funkcjaTestowa(mojeImie, mojeNazwisko):
    print("Witaj", mojeImie, mojeNazwisko)
    
imie = "Robin"
nazwisko= "Hood"

funkcjaTestowa(imie, nazwisko)
```

Funkcja może również zwrócić jakąś wartość. Na przykład wynik dodawania:

```python
def dodaj(a, b):
    return a + b

print(dodaj(1,2))
```

## Używanie modułów

Moduły służą do organizowania funkcji, zmiennych i innych
elementów kodu w większe programy, które dają więcej możliwości. Niektóre z nich
są wbudowane w Pythona, inne z kolei są
niezależne i można je pobrać. Istnieją
moduły pomagające w pisaniu gier (np. zewnątrzny PyGame), moduły ułatwiające
obróbkę obrazków( np. PIL czyli Python Imaging Library) i do rysowania
trójwymiarowej grafiki (np. Panda3D).

Moduły można używać do różnych zadań.
Przykładowo gdybyśmy chcieli zrobić jakąś symulacje gry, moglibyśmy obliczać
bieżącą date i czas, używając wbudowanego modułu:

```python
>>> import microbit
```

W tym przypadku polecenie `import` informuje Pythona, że chcemy używać modułu
`microbit`. Od tego momentu za pomocą symbolu `.` (kropki) możemy wywoływać
dostępne w danym module funkcje.
Oto przykładowe wywołanie funkcji
`running_time` w module `microbit`, która pokazuje ile milisekund płyta jest już
uruchomiona

```python
import microbit

print(microbit.running_time())
```

Funkcja `asctime` jest częścią modułu `time` i zwraca bieżącą date i czas pod
postacią łańcuchu znaków.

# CZĘŚĆ ZAAWANSOWANA - nieobowiązkowa

# Obiekty i
klasy

Właściwie ten rozdział mógłby być tematem całej serii zajęć, my jednak
skupimy się na absolutnych podstawach.

## Wartości to obiekty
Wszystko co do
tej pory nazywaliśmy wartością możemy nazwać też obiektem.
Widzieliśmy to na
przykładzie liczb całkowitych, gdy `help` wypisało
nam dziesiątki linii
dodatkowych informacji na temat `int`.

## Każdy obiekt ma klasę
Aby się
dowiedzieć jaką wystarczy użyć funkcji`type`:

    >>> type(2)
    <type 'int'>
>>> type(2.0)
    <type 'float'>
    >>> type("Gżegżółka")
    <type 'str'>
>>> x = 1, 2
    >>> type(x)
    <type 'tuple'>
    >>> type([])
    <type
'list'>

Gdy używamy w naszym programie liczby, spodziewamy się, że będzie się
ona zachowywać tak jak liczba - bazujemy na naszej intuicji.

Jednak Python musi
dokładnie wiedzieć co znaczy być liczbą całkowitą,
np. co ma się stać gdy
dodajemy dwie liczby, a co gdy je dzielimy.
Klasa dostarcza tych wszystkich
informacji i więcej.

Sprawdź co oferuje nam klasa ``str`` za pomocą`help`.
Zacytujemy tutaj jedynie kilka ciekawszych funkcji:

    >>> help(str.lower)
Help on method_descriptor:
    <BLANKLINE>
    lower(...)
        S.lower() ->
str
    <BLANKLINE>
        Return a copy of the string S converted to
lowercase.
    <BLANKLINE>
    >>> help(str.upper)
    Help on
method_descriptor:
    <BLANKLINE>
    upper(...)
        S.upper() -> str
<BLANKLINE>
        Return a copy of S converted to uppercase.
    <BLANKLINE>
>>> help(str.ljust)
    Help on method_descriptor:
    <BLANKLINE>
ljust(...)
        S.ljust(width[, fillchar]) -> int
    <BLANKLINE>
Return S left-justified in a Unicode string of length width. Padding is
done using the specified fill character (default is a space).
    <BLANKLINE>
>>> help(str.center)
    Help on method_descriptor:
    <BLANKLINE>
center(...)
        S.center(width[, fillchar]) -> str
    <BLANKLINE>
Return S centered in a Unicode string of length width. Padding is
        done
using the specified fill character (default is a space)
    <BLANKLINE>
Wszystko to są operacje, które każdy napis potrafi wykonać. Możemy
się do nich
dostać używając kropki i wywołując jak funkcję:

    >>> x = "Ala"
    >>>
x.upper()
    u'ALA'
    >>> x.lower()
    u'ala'
    >>> x.center(9)
    u'
Ala   '

I jeszcze jedna istotna funkcjonalność każdej klasy - potrafi ona
stworzyć obiekt mający jej cechy (tzw. swoją instancję):

    >>> int()
    0
>>> str()
    ''
    >>> list()
    []
    >>> tuple()
    ()

Podsumowując,
poznaliśmy już klasy`int`,`str`,`tuple`,
`list`. Aby sprawdzić jakiej klasy jest
wartość (obiekt) używamy funkcji
`type`. Aby stworzyć instancję klasy (czyli
nowy obiekt) wywołujemy
klasę podobnie jak wywoływaliśmy funkcję, dopisując
nawiasy ``()``, na przykład
``int()``.

## Definiowanie klass

Podobnie jak
możemy tworzyć własne funkcje, tak i możemy tworzyć
własne klasy. W gruncie
rzeczy, klasa to nic innego jak zgrupowane
funkcje:

    class Dog(object):
def bark(self):
            print(u"Woof! Woof!")

Klasy rozpoczynają się od
słowa`class`, po którym podajemy
nazwę nowej klasy. Czym jest ``(object)``
wyjaśni się później, gdy
będziemy chcieli stworzyć bardziej skomplikowane klasy.
Warto natomiast zwrócić uwagę na fakt, że każda funkcja w klasie musi mieć
conajmniej jeden argument. Jego wartością będzie obiekt z którego wywołaliśmy
tą
funkcję (czyli to co przed kropką):

    burek = Dog()
    burek.bark()

Wynik:
Woof! Woof!

Argument ten może nazywać się dowolnie, ale intuicyjne jest aby
nazwać go ``self``.

## Atrybuty obiektów
Obiekty poza metodami (funckjami),
mogą posiadać też atrybuty:

    burek = Dog()
    burek.name = "Burek"
print(burek.name)

Wynik:

    Burek

Czasami chcemy aby każdy obiekt danej
klasy miał jakiś atrybut, np. każdy
pies powinien mieć imię. Możemy dodać takie
wymaganie definiując funkcję
o specjalnej nazwie ``__init__``:



    class
Dog(object):

        def __init__(self, name):
            self.name = name
def bark(self):
            return "Woof! %s! Woof!" % (self.name,)

    burek =
Dog(u"Burek")
    pluto = Dog(u"Pluto")
    print(burek.bark())
print(pluto.bark())

Wynik:

    Woof! Burek! Woof!
    Woof! Pluto! Woof!


##
Zadania 

1. Napisz prostą grę, w której przeciwnikiem jest komputer,  która
pozwala wybrać numer z zakresu:
* od 1 do 100 w pięciu próbach,
* od 1 do 7000 w
siedmiu próbach,
* użytkownik może wybrać podpunkt a) lub b) , kiedy zacznie
grę. 
Po zakończeniu gry powinna być informacja ile rozgrywek było rozegranych,
ile wygranych, a ile przegranych.

2. Napisz prosty program który pozwoli uczyć
się prostych japońskich słów. Dostarczamy plik jap_dict.txt (plik dostaniecie od
mentora). 
Twoim zadaniem jest:

* użyć kopiuj+wklej na tekście z tego pliku,
lub użyć funkcję open(file_name) aby pobrać dane, 
* przekształcić tekst na
strukturę danych,
* zadać pytanie o tłumaczenie z angielskiego na japoński słowa
lub frazy, 
* sprawdzić czy tłumaczenie zostało wykonane poprawnie, jeśli tak -
nie pokazywać więcej już tego słowa, 
* poinformować ile słów jest odgadniętych
i ile pozostało,
* opcjonalnie na końcu pogratulować, 
* wskazać różnice w
pisowni.

```python

```
