# Narzędzie pomocnicze REUSE – samouczek

Poniższy samouczek opisuje podstawowe kroki, które mają na celu doprowadzić projekt oprogramowania do bycia zgodnym z [REUSE](https://reuse.software). Po zakończeniu samouczka wszystkie pliki projektu będą miały wyraźnie oznaczone prawa autorskie i licencje, a ponadto będzie można to zweryfikować używając narzędzia pomocniczego REUSE.

Samouczek pochodzi ze strony <https://reuse.software/tutorial/> i jest udostępniony na licencji [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.pl).

## Instalacja

Narzędzie REUSE instalujemy jako moduł Pythona 3 przy pomocy menadżera pakietów PIP:

```shell
$ pip3 install reuse
```

W przypadku Linuxa należy upewnić się, że katalog `~/.local/bin` znajduje się w zmiennej środowiskowej `$PATH`. W systemie Windows wymagana ścieżka, w zależności od zainstalowanej wersji Pythona, może mieć wartość `%USERPROFILE%\AppData\Roaming\Python\Python39\Scripts` (standardowa instalacja) lub `%USERPROFILE%\AppData\Local\Packages\PythonSoftwareFoundation.Python.3.9_<tutaj-wprowadź-id>\LocalCache\local-packages\Python39\Scripts` (instalacja przez Microsoft Store).

Dodatkowy opis instalacji znajduje się w [repozytorium projektu](https://github.com/fsfe/reuse-tool#install).

### Narzędzie tree

Podczas pracy będziemy wyświetlali strukturę katalogu projektu. Pomocne przy tym będzie polecenie [`tree`](https://linux.die.net/man/1/tree), które w dystrybucjach Linuxa najczęściej trzeba osobno doinstalować, np.:

```shell
$ sudo apt install tree
```

## Przygotowanie repozytorium

Będziemy pracowali na przykładowym, minimalistycznym projekcie odzwierciedlajacym jakiś projekt oprogramowania. Sklonujmy poniższe repozytorium:

```shell
$ git clone --branch noncompliant https://github.com/fsfe/reuse-example.git
```

Wyświetlmy początkową strukturę naszego projektu  (wyświetlimy również ukryte pliki i katalogi z wyłączeniem katalogu `.git`):

```shell
$ tree -a -I ".git" reuse-example
```

Struktura naszego przykładowego projektu wygląda następująco:

```plaintext
reuse-example
├── .gitignore
├── Makefile
├── README.md
├── img
│   ├── cat.jpg
│   └── dog.jpg
└── src
    └── main.c

2 directories, 6 files
```

W kolejnych krokach przy pomocy narzędzia REUSE nadamy plikom oznaczenia dotyczące praw autorskich oraz licencji.

## Inicjalizacja REUSE

Przejdźmy do katalogu projektu:

```shell
$ cd reuse-example
```

Zainicjalizujemy REUSE w naszym projekcie:

```shell
$ reuse init
```

W interaktywnym dialogu możemy zdefiniować właściwości naszego projektu, a także dodać od początku jedną lub wiele licencji. Pod koniec procesu konfiguracji wskazane przez nas licencje zostaną automatycznie pobrane do właściwej lokalizacji. My nie będziemy wskazywali początkowych licencji; w trakcie samoczuczka będziemy je sukcesywanie dodawali i pobierzemy je w ostatnim kroku. 

W kolejnych monitach wprowadzamy kolejno:

* `<ENTER>`
* `My project`
* `https://example.com`
* `Jane Doe`
* `jane@example.com`

Wynik na ekranie może wyglądać następująco:

```plaintext
Initializing project for REUSE.

What license is your project under? Provide the SPDX License Identifier.
To stop adding licenses, hit RETURN.


What is the name of the project?
My project

What is the internet address of the project?
https://example.com

What is the name of the maintainer?
Jane Doe

What is the e-mail address of the maintainer?
jane@example.com

All done! Initializing now.


Creating .reuse/dep5

Initialization complete.
```

Możemy zauważyć, że został utworzony plik `.reuse/dep5`, który zawiera wprowadzone przez nas informacje. Wrócimy jeszcze do tego pliku pod koniec samouczka.

## Dodanie informacji o prawach autorskich i licencjach do każdego pliku

Na początku musimy zdecydować której licencji będziemy używali – możemy do tego wykorzystać np. stronę <https://choosealicense.com/>. Załóżmy, że w naszym projekcie nasze pliki chcemy głównie obejmować licencją GNU General Public License (GPL) v3.0 lub dowolną późniejszą wersją. Na stronie <https://spdx.org/licenses/> znajdujemy identyfikator SPDX tej licencji – jest to `GPL-3.0-or-later`. Przy pomocy polecenia `reuse addheader` dodamy nagłówki o prawach autorskich i tej licencji do plików `src/main.c`, `Makefile` i `README.md`:

```shell
$ reuse addheader --copyright="Jane Doe <jane@example.com>" --license="GPL-3.0-or-later" src/main.c Makefile README.md
```

Wynik:

```plaintext
Successfully changed header of src/main.c
Successfully changed header of Makefile
Successfully changed header of README.md
```

Możemy zauważyć, że np. w pliku `src/main.c` został dodany odpowiedni nagłówek:

```shell
$ head -5 src/main.c
```

Wynik:

```c
// SPDX-FileCopyrightText: 2021 Jane Doe <jane@example.com>
//
// SPDX-License-Identifier: GPL-3.0-or-later

#include <stdio.h>
```

Pliki `Makefile` i `README.md` również mają dodane nagłówki, ale oczywiście w innym stylu komentowania.

Domyślnie używany jest aktualny rok, ale można go zmienić przy pomocy parametru `--year=` polecenia `reuse addheader`. Można wybrać np. rok pierwszej publikacji, rok ostatniej publikacji, wszystkie lata publikacji, jako zakres (np. 2017-2019) lub jako oddzielne pozycje (np. 2017, 2018, 2019) lub można w ogóle nie podawać roku.

## Pliki binarne i pliki bez możliwości dodawania komentarzy

W naszym projekcie chcemy również oznaczyć licencją `GPL-3.0-or-later` pliki graficzne. Niestety, obrazy i inne pliki binarne nie mają łatwo edytowalnych nagłówków jako komentarze. Innym przykładem są pliki generowane automatycznie, niektóre pliki danych i pliki konfiguracyjne, dla których dodawanie komentarzy nie jest łatwe.

Obejdziemy ten problem tworząc pliki `cat.jpg.license` i `dog.jpg.license`, w których tak w poprzednim kroku każdy będzie zawierał te same informacje o licencji i właścicielu praw autorskich.

Narzędzie REUSE powinno automatycznie wykrywać pliki binarne i automatycznie tworzyć odpowiedni pliki `.license`. Jeśli tak się nie stanie lub jeśli chcielibyśmy wymusić ich tworzenie, to dodajemy parametr `--force-dot-license` do polecenia `reuse addheader`. Tak więc polecenie dla powyższego zadania może wyglądać następująco:

```shell
$ reuse addheader --copyright="Jane Doe <jane@example.com>" --license="GPL-3.0-or-later" --force-dot-license img/cat.jpg img/dog.jpg
```

Wynik:

```plaintext
Successfully changed header of img/cat.jpg.license
Successfully changed header of img/dog.jpg.license
```

Możemy podejrzeć jeden z utworzonych plików:

```shell
$ cat img/cat.jpg.license
```

Wynik:

```plaintext
SPDX-FileCopyrightText: 2021 Jane Doe <jane@example.com>

SPDX-License-Identifier: GPL-3.0-or-later
```

## Zmiana informacji o licencjonowaniu

Pracując nad projektem nagle odkrywamy, że nasze zdjęcia kota i psa (`cat.jpg` i `dog.jpg`) nie były na licencji GPL, ale na Creative Commons Uznanie autorstwa 4.0 i ich właścicielem jest Max Mehl. 

Identyfikator SPDX dla tej licencji to `CC-BY-4.0`. Narzędzie REUSE jak na razie nie zapewnia sposobu na zastąpienie istniejących informacji o prawach autorskich i licencjach. Uruchomienie polecenia `reuse addheader` nie zastąpi, ale rozszerzy pliki `.license` o dwie dodatkowe linie określające prawa autorskie Maxa Mehla i licencję CC-BY-4.0. W takiej sytuacji możemy te pliki albo edytować ręcznie albo usunąć i wygenerować od nowa:

```shell
$ rm img/cat.jpg.license img/dog.jpg.license
$ reuse addheader --copyright="Max Mehl <max.mehl@fsfe.org>" --license="CC-BY-4.0" --force-dot-license img/cat.jpg img/dog.jpg
```

Wynik:

```plaintext
Successfully changed header of img/cat.jpg.license
Successfully changed header of img/dog.jpg.license
```

## Artefakty procesu budowania aplikacji

Kiedy kompilujemy nasz program, generujemy pewne artefakty kompilacji, np. `src/main.o`. Nie musimy dostarczać żadnych informacji o licencjach dla tego rodzaju plików. Wystarczy dodać odpowiednie informacje w pliku `.gitignore`, tak aby zignorować te artefakty. Narzędzie REUSE będzie respektowało zawartość `.gitignore`. Możemy zauważyć, że informacje te już tam się znajdują:

```shell
$ cat .gitignore
```

Wynik:

```plaintext
helloworld
*.o
```

## Pliki nieistotne

W naszym projekcie mogą być pliki, których nie będziemy uważali za takie, które jakoś szczególnie muszą by chronione prawem autorskim, na przykład pliki konfiguracyjne takie jak `.gitignore`. Możemy nie chcieć licencjonować tych plików, ale podstawową ideą REUSE jest to, że wszystkie pliki mają wyraźnie oznaczone prawa autorskie i licencje.

Wszystkie pliki, które są oryginalnymi pracami autorskimi, są objęte prawem autorskim. W szczególności, jeśli ktoś usiadł i spisał na komputerze swoje własne oryginalne myśli, to posiada prawa autorskie do ich rezultatów. Typowe przykłady to kod źródłowy, dokumentacja, pliki audio i wideo. Istnieją jednak pewne skrajne przypadki. Na przykład, program `print("Hello, REUSE!")` prawdopodobnie nie spełnia wymogu oryginalności. Podobnie, pliki danych i pliki konfiguracyjne również mogą nie spełniać tego wymogu.

W takiej sytuacji dla naszego pliku `.gitignore` możemy użyć licencji [CC0](https://creativecommons.org/publicdomain/zero/1.0/). Jest to praktycznie identyczne z umieszczeniem pliku w domenie publicznej.

```shell
$ reuse addheader --copyright="Jane Doe <jane@example.com>" --license="CC0-1.0" .gitignore
```

Wynik:

```plaintext
Successfully changed header of .gitignore
```

Możemy teraz sprawdzić zawartość pliku:

```shell
$ cat .gitignore
```

Wynik:

```plaintext
# SPDX-FileCopyrightText: 2021 Jane Doe <jane@example.com>
#
# SPDX-License-Identifier: CC0-1.0

helloworld
*.o
```

## Pobranie plików licencji

Utworzymy teraz katalog `LICENSES`, do którego pobierzemy wszystkie wykorzysytwane przez nas licencje:

```shell
$ reuse download --all
```

Wynik:

```plaintext
Successfully downloaded ./LICENSES/CC0-1.0.txt.
Successfully downloaded ./LICENSES/GPL-3.0-or-later.txt.
Successfully downloaded ./LICENSES/CC-BY-4.0.txt.
```

Możemy zobaczyć jak wygląda teraz struktura naszego projektu:

```shell
$ tree -a -I ".git"
```

Wynik:

```plaintext
.
├── .gitignore
├── .reuse
│   └── dep5
├── LICENSES
│   ├── CC-BY-4.0.txt
│   ├── CC0-1.0.txt
│   └── GPL-3.0-or-later.txt
├── Makefile
├── README.md
├── img
│   ├── cat.jpg
│   ├── cat.jpg.license
│   ├── dog.jpg
│   └── dog.jpg.license
└── src
    └── main.c

4 directories, 12 files
```

## Potwierdzenie zgodności z REUSE

Możemy teraz sprawdzić czy nasz projekt jest zgodny z REUSE:

```shell
$ reuse lint
```

Wynik:

```plaintext
# SUMMARY

* Bad licenses:
* Deprecated licenses:
* Licenses without file extension:
* Missing licenses:
* Unused licenses:
* Used licenses: CC-BY-4.0, CC0-1.0, GPL-3.0-or-later
* Read errors: 0
* Files with copyright information: 6 / 6
* Files with license information: 6 / 6

Congratulations! Your project is compliant with version 3.0 of the REUSE Specification :-)
```

## FAQ

### Wyświetlenie zestawienia licencji i praw autorskich

Jeśli chcemy wyświetlić w formacie SPDX zestawienie licencji i praw autorskich dla plików w projekcie, to możemy to zrobić poleceniem:

```shell
$ reuse spdx
```

### Masowe licencjonowanie całych katalogów

Jeśli chcemy ustawić za jednym zamachem licencje dla wielu katalogów i plików, to możemy odpowiednio edytować plik `.reuse/dep5`, np.:

```plaintext
Format: https://www.debian.org/doc/packaging-manuals/copyright-format/1.0/
Upstream-Name: my-project
Upstream-Contact: Jane Doe <jane@example.com>
Source: https://git.example.com/jane/my-project

Files: resources/img/* resources/aud/*
Copyright: 2017 Jane Doe <jane@example.com>
License: CC-BY-4.0

Files: resources/vid/*
Copyright: 2017 Jane Doe <jane@example.com>
           2017 John Doe <john@example.com>
License: CC0-1.0
```

Więcej na temat tego formatu można znaleźć [tutaj](https://www.debian.org/doc/packaging-manuals/copyright-format/1.0/).

### Ustawienie licencji projektu na GitHubie

Najlepiej jest utworzyć w głównym katalogu projektu plik `LICENSE.md` z krótką informacją jak wygląda struktura licencjonowania w naszym projekcie.

### Pozostałe pytania

Odpowiedzi na pozostałe często pojawiające się pytania można znaleźć na stronie <https://reuse.software/faq/>.
