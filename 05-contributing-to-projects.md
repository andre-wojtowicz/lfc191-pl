# Udział w projektach

## Introduction

### Przegląd rozdziału

Zanim przekażesz swój kod do projektu otwartego oprogramowania, upewnij się, że wolno ci to zrobić.

Jeśli nie pracujesz dla firmy ani organizacji, a swój kod lub inne treści przekazujesz jako osoba indywidualna posiadająca pełnię praw autorskich, to sprawa wydaje się oczywista. Projekty mają zasady dla indywidualnych współpracowników i należy się z nimi dokładnie zapoznać, wypełnić potrzebne dokumenty, wyrazić wymagane zgody, a następnie przekazać swoje poprawki do projektu.

Jeśli jednak pracujesz dla jakiejś firmy lub organizacji, to musisz sprawdzić, czy twoi przełożeni zgadzają się na przesłanie twojej pracy do projektu. Od firmy może być wymagane podpisanie jakiejś umowy o współpracy lub wskazanie praw autorskich albo przedstawienie DCO (Developer Certificate of Origin), aby można było przyjąć jej wkład.

### Założenia rozdziału

W tym rozdziale nauczysz się, jak:

* rozumieć typowe warunki, na podstawie których projekty akceptują pracę współpracowników, i na co zwracać szczególną uwagę.

## Udział w projektach

### Uzyskanie zgody na przesłanie kodu należącego do pracodawcy

Jeśli chcesz przesłać kod w imieniu swojego pracodawcy - czyli taki, do którego to pracodawca, a nie ty, ma prawa - to musisz upewnić się, czy pracodawca zgadza się na twój udział w danym projekcie.

Może to wymagać od twojego pracodawcy między innymi wyrażenia zgody na stosowane w projekcie mechanizmy współpracy: podpisania CLA (Contributor License Agreement) lub przedstawienia DCO (Developer Certificate of Origin). Oba te mechanizmy opisujemy bardziej szczegółowo na kolejnych stronach.

Dodatkowym wymogiem może być określenie przez twojego pracodawcę, czy treści, jakie zamierzasz przekazać, są odpowiednie dla projektu. Twój pracodawca może chcieć przekazać twój kod lub inne treści do wykorzystania w jakimś zakresie, ale nie zgodzić się na przekazanie kodu innego rodzaju. Każda organizacja ma w takich sprawach własne zasady i procedury. Przed przekazaniem kodu należącego do twojej firmy należy zasięgnąć opinii komórki zajmującej się otwartym oprogramowaniem, działu prawnego lub innych odpowiednich osób.

### Mechanizmy współpracy

Aby zachować założone cele i zapewnić użytkownikom możliwość korzystania z pełni praw przyznanych licencją projektu, może on wymagać spełnienia pewnych formalności, zanim będzie mógł przyjąć wprowadzone przez ciebie zmiany.

Zazwyczaj w pliku `CONTRIBUTING` w repozytorium lub na stronie www projektu umieszcza się dokumentację na temat wymaganych formalności.

Nie wszystkie projekty mają takie wymagania. Sporo projektów na GitHub przyjmuje prośby o połączenie (pull requests) bez dodatkowych wymagań. Jednak wiele dużych i ważnych projektów otwartego oprogramowania wykorzystuje sformalizowane mechanizmy współpracy, aby lepiej chronić społeczność, użytkowników i współpracowników oraz ich oczekiwania.

Do przykładów formalnych mechanizmów współpracy można zaliczyć:

* Contributor License Agreements (CLA)
  * np. Apache Software Foundation, Google, Kubernetes
* Copyright Assignment
  * np. GNU toolchain
* Developer’s Certificate of Origin (DCO)
  * np. jądro Linuxa, Zephyr

### Contributor License Agreements (CLA)

Contributor License Agreement (CLA) to umowa pomiędzy projektem a właścicielem współtworzonych treści. Jak wynika z nazwy, współpracownik przyznaje projektowi **licencję**. Tekst CLA określa zakres przyznanej licencji.

Oznacza to, że dodane treści pozostają własnością ich twórcy. Podpisanie CLA nie oznacza zrzeczenia się własności na rzecz projektu. Zamiast tego CLA przyznaję licencję, ale właściciel dodanych treści nadal zachowuje swoje prawa autorskie do nich i może licencjonować je w inny sposób w innych przypadkach.

CLA mogą się różnić w zależności od projektu i mogą przyznawać inne zakresy uprawnień, nakładać inne wymagania itp. Zakres licencji przyznanych projektowi często nie jest taki sam jak licencja „zewnętrzna” przyznawana przez projekt reszcie świata. Z tego powodu ty i/lub twój dział prawny powinniście dokładnie przeanalizować przed podpisaniem każdą CLA.

Wiele projektów używa CLA w dwóch różnych formach:

* **indywidualna** - Indywidualna CLA (ICLA) jest przeznaczona dla osób fizycznych, które dodają kod niebędący ich własnością.
* **korporacyjna** - Koroporacyjna CLA (CCLA) jest przeznaczona dla firm i organizacji, których pracownicy dodają kod w imieniu pracodawcy.

Jeśli dodajesz kod, którego właścicielem jest twój pracodawca, to jego dział prawny powinien przeanalizować korporacyjną CLA i, jeśli zostanie zatwierdzona, powinien podpisać ją ktoś uprawniony do zawierania umów w imieniu firmy. Nie próbuj obchodzić etapów analizy, zatwierdzenia i podpisania CCLA, podpisując samodzielnie indywidualną CLA, jeśli kod jest własnością twojego pracodawcy i dodajesz go w jego imieniu.

### Copyright Assignment

Stronami umowy Copyright Assignment (o przeniesieniu praw autorskich), podobnie jak CLA, są projekt i właściciel dodanych treści. W odróżnieniu od CLA umowa Copyright Assignment rzeczywiście „przenosi” własność praw autorskich ze współtwórcy na sam projekt. Współtwórca traci prawa autorskie do dodanych przez siebie treści.

Przeniesienie praw autorskich zazwyczaj występuje w projektach, które chcą egzekwować ich ochronę i zachować na przyszłość prawno do zmian licencji. (Umowy CLA, w zależności od ich konkretnej treści, mogą również umożliwiać zmiany typu licencji.)

Typowym przykładem takiej sytuacji jest współpraca z Free Software Foundation (FSF) przy kompilatorze GNU. W tym przypadku mechanizm współpracy wymaga przeniesienia praw autorskich przed akceptacją zmian, dzięki czemu projekt otrzymuje wszystkie prawa autorskie do zmienionych treści.

Przeniesienie praw autorskich w tym projekcie nie tylko jest pomocne w egzekwowaniu warunków GPL, ale również pozwoliło FSF jako właścicielowi praw współpracować z innymi organizacjami i osobami przy egzekwowaniu postanowień licencji oraz wydawaniu materiałów, takich jak GCC Runtime Library Exceptions, które wyjaśniają zapisy licencji lub dają dodatkowe pozwolenia, które można uznać za zmieniające zapisy licencji.

### Developer Certificate of Origin 1.1

Inna metoda, z której korzysta część projektów, to Developer Certificate of Origin. Zamiast skorzystać z Contributor License Agreement, społeczność tworząca jądro Linuxa w maju 2004 roku zdecydowała o ujednoliceniu wymagań stosowanych przy współtworzeniu jądra do Developer Certificate of Origin (znanego również jako DCO). 

Dodając własne treści, współpracownik załącza w metadanych DCO, w którym stwierdza, że na podstawie określonej licencji ma prawo do przesłania zmian i do upublicznienia ich, a jeżeli jego praca jest oparta na wcześniejszej pracy innych osób, to zgodnie z jego najlepszą wiedzą wszystkie te treści również mogą być przesłane.

Poniżej znajduje się oryginalny tekst ["Developer's Certificate of Origin Version 1.1"](https://www.developercertificate.org/):

```plaintext
By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

Można również znaleźć go w drzewie źródeł jądra Linuxa, w pliku [Documentation/process/submitting-patches.rst](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/process/submitting-patches.rst).

Inne projekty otwartego oprogramowania także przyjęły tę metodę zamiast CLA lub umów przeniesienia praw autorskich. Aby mechanizm ten mógł działać, w każdym pliku kodu źródłowego należy umieścić licencję. Trzeba też rozumieć, czy dodawane treści są kompatybilne z licencją otwartego oprogramowania obejmującą modyfikowany plik i użyć formatu podpisu pokazanego na kolejnym ekranie.

### Jak podpisać DCO

DCO nie wymaga uzyskania podpisanej umowy (ani od ciebie, ani od twojego pracodawcy). Zamiast tego, jeśli dodajesz treści do projektu korzystającego z DCO, w swojej poprawce musisz umieścić odpowiednie oświadczenie sformatowane według następującego wzoru:



Znacznik „Signed-off-by”, po którym następują nazwisko osoby i adres email. Możesz je w prosty sposób dołączyć przy zatwierdzaniu własnych zmian narzędziami git, dodając w wierszu poleceń do polecenia commit '-s'.

```plaintext
Signed-off-by: Linus Torvalds <torvalds@linuxfoundation.org>
```

W powyższym przykładzie pokazujemy, jak wyglądałoby oświadczenie Linusa Torvaldsa dla zmiany, którą chciałby zatwierdzić w jądrze.

Niektóre narzędzia ułatwiają egzekwowanie DCO, pomagając sprawdzać, czy poprawki zawierają oświadczenie „Signed-off-by”, i dodawać je do kodu projektu tylko w przypadku, jeśli tak jest. Na przykład na GitHubie [DCO app](https://github.com/apps/dco) umożliwia taką weryfikację przy zgłoszeniu poprawek do połączenia.

## Podsumowanie

### Konkluzje

Mamy nadzieję, że rozumiesz już podstawy typowych mechanizmów współpracy w projektach i wiesz, na co zwracać szczególną uwagę.
