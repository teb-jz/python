# Python

Python to język programowania wysokiego poziomu, ogólnego przeznaczenia. Jego składnia cechuje się przejrzystością i zwięzłością. Posiada w pełni dynamiczny system typów i automatyczne zarządzanie pamięcią.

---

## Podstawowy program

```python
print("Hello world!")
```

Powyższy program ma za zadanie wypisać, przy pomocy *funkcji* `print`, podany pomiędzy nawiasami okrągłymi napis. Jak widać, struktura programu jest znacznie prostsza niż w przypadku większości języków programowania.

> Kolejną istotną różnią jest brak średników kończących daną instrukcję.

## Wyświetlanie tekstu

Najprostszym sposobem na komunikację z użytkownikiem jest konsola, która pomocna może okazać się również w celu prześledzenia pracy programu na różnych jego etapach.

```python
print("Przykładowy" + "tekst")
print("Inny", "przykładowy", "tekst")
print('To również napis')
```

Język Python pozwala na dwa główne sposoby deklarowania napisów. Do tworzenia ciągów znaków można wykorzystać *apostrofy* lub *cudzysłowy*. W większości języków apostrof zarezerwowany jest dla pojedynczych znaków.

*Łańcuchy znaków* można poddać **konkatenacji**, czyli ich łączeniu, sklejaniu ze sobą. W tym celu wykorzystuje się dwuargumentowy operator `+`. Wynikiem jest nowy ciąg znaków.

Funkcja `print` pozwala na przekazanie kilku argumentów, oddzielonych przecinkami.

## Zmienna

**Zmienna** to pewne wydzielone miejsce w pamięci komputera, gdzie mogą być przechowywane dane, między innymi wyniki wykonywanych operacji. Wartością zmiennej może być na przykład liczba lub ciąg znaków. Zmienna musi posiadać nazwę symboliczną, przez którą można odwoływać się do niej w programie.

### Nazwy zmiennych

Nazwa może być dowolna, ale musi spełniać następujące warunki:

- nazwa zmiennej nie może być słowem kluczowym języka Python,
- nazwa nie może zaczynać się od cyfry,
- nazwa nie może zawierać znaków białych i większości znaków specjalnych.

> **Słowa kluczowe** to zastrzeżone słowa, które mają specjalne znaczenie w danym językach programowania.

Ponadto należy pamiętać, że wielkie i małe litery są rozróżnialne. Poza powyższymi wymogami zaleca się nadawanie nazw jawnie określających przeznaczenie danej zmiennej i odradza stosowanie polskich znaków (staramy się korzystać tylko z alfabetu łacińskigo).

W przypadku nazw wieloczłonowych możemy posłużyć się jedną z popularnych notacji:

- **camelCase** - wszystkie wyrazy piszemy łącznie, każdy kolejny zaczynając od wielkiej litery,
- **PascalCase** - wszystkie wyrazy piszemy łącznie, każdy (łącznie z pierwszym) zaczynając od wielkiej litery,
- **snake_case** - wyrazy oddzielamy znakiem myślnika,
- **kebab-case** - wyrazy oddzielamy znakiem myślnika.

### Typy danych

Python cechuje **typowanie dynamiczne**, oznacza to, że nie musimy jawnie wskazywać typu danej zmiennej. Jest on nadawany automatycznie w zależności od przechowywanej przez nią wartości. Podstawowe typy wbudowane oferowane przez język to:
- **str** (string) - ciąg/łańcuch znaków, napis,
- numeryczne:
  - **int** (integer) - liczba całkowita,
  - **float** (floating point number) - liczba zmiennoprzecinkowa, liczba "rzeczywista",
- **bool** (boolean) - wartość logiczna.

```python
text = "Przykładowy tekst" # str
randomNumber = 21 # int
fraction = 9.34 # float
anotherFraction = .37 # float
statement = True # bool
```

### Definicja zmiennej

W języku Python nie możemy zdefiniować zmiennej bez jej inicjalizacji, czyli przypisania wartości początkowej. Na początek odwołujemy się do nazwy symbolicznej, operatorem przypisania jest `=`, po którym następuje podanie wartości.

> W większości języków programowania, również w Python, części dziesiętne ułamków zapisujemy po znaku kropki.

> W przypadku wartości liczbowych z zakresu (1; 1), możemy pominąć zero wiodące. `0.37` jest równoważne z zapisem `.37`. Adekwatnie dla liczb ujemnych, `-0.37` oznacza to samo, co `-.37`.

> Typ logiczny może przyjmować jedynie dwie wartości `True` - prawdę lub `False` - fałsz.

## Operatory arytmetyczne

Podobnie jak inne języki, Python oferuje kilka podstawowych operatorów arytmetycznych, znanych z matematyki:
- `+` - dodawanie,
- `-` - odejmowanie,
- `*` - mnożenie,
- `**` - potęgowanie
- `/` - dzielenie,
- `//` - dzielenia całkowite,
- `%` - dzielenie modulo, reszta z dzielenia.

> Większość oznaczeń operatorów jest intuicyjna. W przypadku `modulo` nie należy sugerować się oznaczeniem i mylić operator z pojęciem procenta.

Dzielenie modulo najczęściej wykorzystywane jest do sprawdzania podzielności liczb. Jeżeli reszta z dzielenia równa jest zero, to znaczy, że pierwsza liczba dzieli się całkowicie przez drugą liczbę.

```python
a = 3
b = -4

result = a + b

print("Suma:", result)
print("Ta sama suma:", a + b)
```

> W celu wyświetlenia wartości zmiennej odwołujemy się do jej nazwy symbolicznej i podajemy ją jako arguement funkcji `print`.

Powyższy przykład przedstawia dodawanie dwóch liczb. Na początku definiujemy dwie zmienne i inicjalizujemy je ustalonymi wartościami całkowitymi. W celu wyświetlenia sumy (wyniku dodawania) możemy zadeklarować kolejną zmienną, ale możemy również wykonać operację bezpośrednio w nawiasach funkcji `print`.

### Dodatkowe operatory przypisania

Często będziemy musieli zmieniać wartość danej zmiennej, nadpisując ją inną wartością.

```python
number = 5
number = number + 2
```

Przykładowo, liczbę możemy nadpisać wartością o 2 większą, przypisując jej nową wartość w postaci sumy jej starej wartości i liczby 2. Taki zapis można skrócić przy pomocy danych operatorów:
- +=,
- -=,
- *=,
- **=
- /=,
- //=
- %=.

```python
number = 5
number += 2
```

Powyższy zapis jest równoważny. Wynik działania będzie identyczny poprzednim. W obu wypadkach zwiększamy liczbę o 2.

> Szczególnym przypadkiem zmiany wartości jest zwiększenie lub zmniejszenie jej o 1. Mowa wtedy odpowednio o **inkrementacji** oraz **dekrementacji**. W większości języków, poza Python, istnieją dla nich oddzielnie operatory.

## Pobieranie wartości od użytkownika

```python
value = input("Wprowadź wartość: ")

print("Podana wartość to:", value)
```

Za pobieranie wartości wprowadzanych przez użytkownika za pośrednictwem klawiatury odpowiada funkcja `input`. Jako argument możemy podać napis, który wyświetli się w konsoli. Może mieć za zadanie na przykład poinformowanie użytkownika o spodziewanej akcji. Funkcja zwraca wartość wprowadzoną przed kliknięciem przycisku *enter*. Jeżeli chcemy z niej skorzystać na dalszym etapie programu, musimy przypisać ją do zmiennej.

```python
x = input("Wprowadź pierwszą liczbę: ")
y = input("Wprowadź drugą liczbę: ")

print("Suma liczb wynosi:", x + y)
```

W powyższym przykładzie pomimo próby wprowadzenia liczb, wyświetlony napis nie będzie oczekiwanym wynikiem. W tym przypadku znak `+` nie oznacza dodawania, a **konkatenację**, w związku z tym zmienne zawierają ciągi znaków, a nie liczby.

Znak `"7"`, a liczba `7` to dla danego języka programowania dwie różne wartości. Znaki pomimo, że są cyframi nie zachowują się jak liczby i nie jesteśmy w stanie swobodnie przeprowadzać na nich operacji arytmetycznych.

### Konwersje typów

Aby dane wprowadzone przez użytkownika zostały poprawnie zinterpretowane należy je najpierw przekonwertować. W tym celu posłużą nam funkcje wbudowane:

- `str` - konwersja na łańcuch znaków,
- `int` - konwersja na liczbę całkowitą,
- `float` - konwersja na liczbę "rzeczywistą",
- `bool` - konwersja na typ logiczny.

```python
text = "4"
number = int(text)

print(number ** 2)
```

Gdzie pomiędzy nawiasami okrągłymi wskazujemy to, co chcemy poddać konwersji.

> W przypadku konwersji na typ logiczny przyjęło się założenie, że każda niezerowa lub niepusta wartość posiada wartość `True`, a zero lub na przykład pusty ciąg znaków - wartość `False`.

```python
text = input("Podaj wartość ułamkową: ")
fraction = float(text)

# fraction = float(input("Podaj wartość ułamkową: "))

print("Odwrotność danego ułamka to:", fraction ** -1)
```

Powyższy zapis można skrócić podając pomiędzy nawiasy funkcji `float` wartość podaną przez użytkownika, czyli wywołanie funkcji `input`.

### Polecenia
1. Napisz program, który pobierze od użytkownika wartość całkowitą i wyświetli jej pierwiastek trzeciego stopnia. Dla ułatwienia zakładamy, że wprowadzona liczba nie będzie ujemna.
2. Napisz program, który pobierze od użytkownika dwie wartości liczbowe i wyświetli ich średnią arytmetyczną (suma liczb podzielona przez ich ilość.
3. Napisać program, który pobiera od użytkownika długość promienia pewnego okręgu i wyświetla jego pole powierzchni. Dla ułatwienia zakładamy, że wprowadzony promień nie będzie wartością ujemną
