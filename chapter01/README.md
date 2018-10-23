# Wprowadzenie do Pythona

Kiedy python jest już zainstalowany i jupyter
uruchomiony, możemy coś policzyć np. wpisując 2 + 2. Żeby wyświetlić wynik
użyjemy funkcji `print`. O samych funkcjach będzie więcej w dalszej części
kursu.

```python
print(2+2)
```

Python świetnie sprawdza się jako kalkulator:

```python
print(6*7)
```

```python
print(1252 - 38 * 6)
```

```python
print((3-5)*7)
```

```python
print(21/7)
```

```python
print(3**2)
```

```python
print(5/2)
```

Należy zwrócić szczególną uwagę, że ułamki dziesiętne zapisujemy zgodnie z
zasadami języka angielskiego, czyli z kropką, a nie z przecinkiem. Przecinki
będą nam służyły do definiowania `list`, ale o tym później.

## Przedstaw się
### Napisy

Same liczby to jednak trochę za mało do skutecznego porozumiewania
się. Musimy więc nauczyć się posługiwać napisami (ang. string). Oto kilka
przykładów:

```python
print("Cześć")
print("Micro:bit")
```

Napisy można również dodawać:

```python
print('My name is ' + '"James"')
```

oraz mnożyć przez liczby całkowite:

```python
print('jajko' * 3)
```

Liczba również może być napisem, zapisujemy ją wtedy tak: `'3'`

```python
print("3")
```

Napis zawsze musi zaczynać się i kończyć tym samym znakiem. Może to być apostrof
(') albo cudzysłów ("). Nie ma to wpływu na wartość napisu, tzn. wpisując
"Batman" tworzymy napis Batman - cudzysłowowy nie są jego częścią, służą jedynie
wskazaniu, że jest to napis (niestety, Python nie jest aż tak sprytny, aby się
tego domyślić).

## Wywoływanie funkcji

Funkcję `print` już poznaliśmy. Wyświetla ona tekst na
ekranie. Przetestujmy teraz funkcje `int` i `float`, którę zamieniają tekst na
liczbę. Funkcja `int` zamienia tekst na liczbę całkowitą.

```python
print(int("0"))
```

```python
print(int(" 63 "))
```

```python
print(int("60.5"))
```

`int("60.5")` zwróciło błąd, ponieważ 60.5, nie jest liczbą całkowitą. Do
zamiany tekstu na liczbę zmiennoprzecinkową trzeba użyć funkcji `float`

```python
print(float("0"))
```

```python
print(float(" 63 "))
```

```python
print(float("60.5"))
```

Podsumowując: aby wywołać funkcję, musimy znać jej nazwę (poznaliśmy dotąd część
`print`, `int`, `float`), oraz wiedzieć, jakich danych ona od nas oczekuje (tzw.
lista argumentów).

## Porównania: prawda czy fałsz?

Kolejnym elementem, o
którym jeszcze nie wspomnieliśmy, są porównania. Dla liczb działają one
identycznie jak na lekcjach matematyki:
2 > 1

```python
print(1 == 2)
```

```python
print(1 == 1.0)
```

```python
print(10 >= 10)
```

```python
print(13 <= 1 + 3)
```

```python
print(-1 != 0)
```

Wynikiem porównania jest zawsze True albo False. Porównania można łączyć w
bardziej skomplikowane warunki za pomocą słów `and` oraz `or`:

```python
x = 5
print(x < 10)
print(2*x > x)
print((x < 10) and (2*x > x))
print((x != 5) and (x != 4))
print((x != 5) and (x != 4) or (x == 5))
```

## Listy

Na samym początku wspomnieliśmy już, że nie możemy używać przecinka w
liczbach, bo będzie nam potrzebny później do list. A oto i one:

```python
print([1, 2, 3])
```

```python
print(["Ala", 15])
```

Lista to nic innego jak kilka wartości zgrupowanych w jedną. Wartości, które
chcemy zgrupować, rozdzielamy przecinkami i umieszczamy międzu kwadratowymi
nawiasami.

Listy można ze sobą łączyć:

```python
names = ["Paulina", "Kowalska"]
details = [27, 1.70]
print(names + details)
```

Mogą też zawierać inne listy, np. informację o punkcie na mapie możemy zgrupować
w następujący sposób:

```python
x,y = 1,2
punkt = ["punkt", [x, y]]
print(punkt)
```

gdzie x i y to jakieś liczby.

Do zgrupowanych wartości możemy odwołać się
używając ich pozycji w liście (licząc od zera), np.:

```python
p = [10, 15]
print("Pierwsza wartość: ", p[0])
print("Druga wartość: ", p[1])
```

```python

```
