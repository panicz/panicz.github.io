---
layout: post
title: Gry tekstowe
---
W epoce kart graficznych dokonujących ray-tracingu
w czasie rzeczywistym łatwo zapomnieć, że był taki moment
w historii gier komputerowych, w którym oprawa
graficzna miała wymiar raczej symboliczny, a większość
akcji była prowadzona za pomocą tekstu: z jednej strony
komputer wyświetlał graczowi opisy miejsc i zdarzeń,
z drugiej zaś - gracz wydawał komputerowi różne polecenia
w rodzaju "idź na północ" albo "weź lampę".

Choć mogłoby się wydawać, że taka forma rozrywki odeszła
już raczej do lamusa, w dalszym ciągu można znaleźć
entuzjastów tego osobliwego medium, zwanego wśród
wtajemniczonych"interaktywną fikcją". I nie chodzi tylko
o osoby grające w stare produkcje, ale przede wszystkim
o to, że tego rodzaju gry w dalszym ciągu powstają.
(Z tego co widziałem, liczba autorów znacząco przewyższa
liczbę graczy.)
Co więcej, równolegle rozwijane są narzędzia, których
celem jest wspomaganie tworzenia takich interaktywnych
opowieści. 

Jednym z takich narzędzi jest środowisko [Inform 7](http://inform7.com/),
którego ważnym składnikiem jest język programowania,
którego główną cechą charakterystyczną jest to, że swoją
składnią bardzo przypomina anglojęzyczną prozę. Przykładowo
definicja *silni* w tym języku wygląda następująco:

```
To decide what number is the factorial of (n - a number):
    if n is zero, decide on one;
    otherwise decide on the factorial of (n minus one) times n.
```

Chociaż takie podejście do pisania programów "podskórnie"
wydaje mi się raczej podejrzane -- bo łatwo zgubić rachubę
w tym, które rzeczy są pisane "na poważnie", a które
stanowią tylko objaśnienia -- jest w tym dla mnie coś
urzekającego, ponieważ tego rodzaju próby pomagają lepiej
zrozumieć, w jaki sposób "działa język", jeżeli w ogóle
można tak powiedzieć.

Problematyka "znaczenia języka", czy też owo samoodnośne
pytanie: "co to znaczy -- znaczyć?", fascynuje mnie już
od dłuższego czasu -- i to być może pod tym względem
programowanie daje mi nieco ukojenia, bo akurat w przypadku
języków programowania kwestia ich znaczenia jest raczej jasna
-- mamy z jednej strony takie pomysły, jak semantyka denotacyjna
i teoria modeli, a z drugiej -- semantykę operacyjną
i abstrakcyjne maszyny obliczeniowe. W każdym razie
wszelkie niejasności w kwestii znaczenia formalnych notacji
są raczej wynikiem niechlujstwa autorów tych notacji,
niż naturalnym stanem rzeczy.

Kwestia języków naturalnych jest jednak nieco bardziej
drażliwa, bo choć w ich przypadku być może można sensownie
mówić o "obiektywnych znaczeniach wypowiedzi", ale
tak naprawdę kluczowe jest to, w jaki sposób nasi rozmówcy
nas zrozumieją -- w różnych sytuacjach możemy tę samą
wypowiedź zrozumieć skrajnie różnie, oraz skrajnie różnie
na nią zareagować.

Albo, mówiąc inaczej, jedną z immanentnych cech języka
naturalnego jest to, że jest on niejako "uwikłany w kontekst"
czy też "zanurzony w świecie". Dla kontrastu, tekst programu
komputerowego, nawet jeśli nie zawsze, to jednak często sam
jest swoim własnym kontekstem -- szczególnie w przypadku
dzieł interaktywnej fikcji i systemów w rodzaju Inform 7.

Jednak mimo tego, jest w interaktywnej fikcji coś, co wzbudza
we mnie pewien opór. Wyobraźmy sobie np. taki fragment:

*"Znajdujesz się w przytulnej bibliotece. Rozglądając się,
dostrzegasz niezliczone rzędy misternie zdobionych drewnianych
regałów, dźwigających przez wieczność całą wiedzę ludzkości,
pokawałkowaną w stronice krótkich chwil namysłu posklejane
ozdobnymi grzbietami."*

Tekst trochę celowo jest "nieco nazbyt poetycki".
Równie dobrze mógłbym napisać:

*"Jesteś w bibliotece. Stoi tutaj dużo regałów. 
Na regałach znajdują się książki".*

Choć oba teksty prezentują te same fakty, wywołują też
w czytelniku inne odczucia. Co więcej, drugi spośród
tych tekstów, jako pozbawiony metafor i przydawek,
jest zdecydowanie prostszy do mechanicznego przetworzenia.

Moja obawa co do systemu Inform 7 jest taka, że coś,
co pozornie wydaje się jednym językiem, tak naprawdę rozszczepi
się na dwa języki: język opisu, zrozumiały dla czytelnika,
oraz język implementacji, zrozumiały dla komputera.

Owo rozszczepienie nie podoba mi się. Moim ideałem
jest rozbudowany język, który w "identyczny" sposób
byłby zrozumiały dla człowieka i dla komputera
(przynajmniej na jakimś poziomie).

Przypadek Inform 7 jest jednak o tyle ciekawy,
że jest to język nadbudowany na języku
[Inform 6](https://www.inform-fiction.org/manual/html/index.html),
będącym już w istocie formalną notacją (w moim odczuciu,
raczej kiepsko zaprojektowanym językiem programowania).
Można zatem powiedzieć, że Inform 6 jest (w jakimś metaforycznym
sensie) modelem dla Inform 7.

Mówiąc konkretniej, Inform 6 jest językiem
wspierającym "programowanie zorientowane obiektowo",
natomiast Inform 7 -- jak twierdzi twórca Graham Nelson
-- koncentruje się raczej na "programowaniu opartym o reguły",
choć docelowo owe reguły istotnie są tłumaczone właśnie
na system obiektowy (pod tym wzgledem dzieło Nelsona
przypomina rozwijany niezależnie na MIT system o nazwie
[Metafor](https://alumni.media.mit.edu/~hugo/publications/drafts/IUI2005-metafor.4.pdf),
który na podstawie opisów w języku naturalnym buduje szablony
klas w Pythonie).

W ogólności lektura
[raportu dotyczącego rozwoju języka Inform 7](https://web.archive.org/web/20180314185630/http://inform7.com/learn/documents/WhitePaper.pdf)
była dla mnie bardzo ciekawym doświadczeniem, bo pokazywała
pewien intelektualny rodowód rozwoju tego systemu. Z jednej
strony Nelson wyjaśnia w nim, że pewna część podsystemu
stanowi właśnie całkiem dosłowną implementację teorii modeli
dla rachunku predykatów (przy czym owe predykaty są maksymalnie
dwuargumentowe. Z drugiej strony, wśród składników "intelektualnego
rodowodu" tego systemu przedstawia metodologię analizy semantycznej
Anny Wierzbickiej i Cliffa Goddarda. (Pewnym zaskoczeniem
jest dla mnie brak, wśród wymienionych źródeł inspiracji, systemu
Prolog -- wygląda to tak, jakby autor w ogóle o tym systemie
nie wiedział, albo go nie rozumiał.)

Wśród wymienioncyh przez Nelsona źródeł nie brakuje także
językoznawców kognitywnych (Ray Jackendoff). Jest nawet miejsce
dla Donalda Knutha i jego koncepcję "programowania piśmiennego"
(bądź "literackiego").

I tak, z jednej strony trochę mnie kusi, żeby spróbować stworzyć
jakąś grę w systemie Inform 7, ale z drugiej mam pewne opory.

O ile lubię zarówno gry komputerowe jak i literaturę, wciąż
nie mogę oprzeć się wrażeniu, że ich połączenie jest raczej
reliktem epoki, w której komputery nie były dostatecznie wydajne,
żeby wyświetlać ładną grafikę w czasie rzeczywistym, aniżeli
"awangardową formą sztuki". Można co prawda znaleźć w tej kwestii
głosy odmienne (polecam obejrzenie niemal dwugodzinnego filmu
dokumentalnego [Get Lamp](https://www.youtube.com/watch?v=LRhbcDzbGSU)),
ale nie ulega wątpliwości, że są to głosy niszowe.

Bo tak jak umiem docenić analizę toku myślenia Raskolnikowa,
przedstawioną przez Dostojewskiego w "Zbrodni i karze", i jestem
w stanie utożsamić się z Gombrowiczowskim Józiem z "Ferdydurke",
tak nie potrafię zrozumieć, co takiego moje doświadczenie
mogłoby zyskać, gdybym nakazał Józiowi "iść na północ"
czy też "zbadać szafkę".

Chociaż kto wie, może niektóre tematy mogłyby wybrzmieć lepiej
jako interaktywna fikcja, niż jako klasyczna forma literacka
(z pomysłów, które przyszły mi do głowy, może warto odnotować
adaptację filmu Christophera Nolana "Memento").

[Hillel Wayne](https://twitter.com/hillelogram) ostatnio sugerował,
żeby użyć tego systemu do opisywania "user stories" na potrzeby
testowania oprogramowania. Propozycja była raczej żartem,
ale znamienne jest, że zamiast po prostu spróbować napisać grę,
część osób potrzebuje racjonalizacji do tego, żeby pobawić
się systemem, który z założenia ma służyć do zabawy.

Wreszcie, zastanawia mnie to, jakie znaczenie miały gry tekstowe
dla rozwoju gier komputerowych w ogóle -- czy to nie im
zawdzięczamy nieco bardziej rozwiniętą wyobraźnię twórców
"złotej ery RPG" (mam na myśli takie produkcje, jak Fallout 1 i 2,
Baldur's Gate czy Planescape: Torment). Nawet John Romero,
współtwórca takich klasycznych gier akcji, jak Doom czy Quake,
swój warsztat gamedesignerski szlifował przemierzając ściany
interaktywnego tekstu. Być może ma to swoje głębokie uzasadnienie:
emulowanie karty graficznej w mózgu jest wszak bardziej rozwijające
dla wyobraźni, niż konsumowanie gotowych wizualizacji. Same gry
tekstowe są drażniące pod tym względem, że -- o ile samemu się
ich nie tworzyło, ani nie studiowało źródeł -- nie wiadomo do
końca, co siedzi pod spodem, a może tam siedzieć naprawdę wszystko.
(Jest to zarazem dobre i złe: dobre, bo buduje nastrój
tajemnicy, którą trzeba odkryć; złe, bo wymaga dużo zapału,
żeby zrobić pierwszy krok.)

Chociaż "zaawansowane przetwarzanie języka naturalnego"
bardzo mi imponuje, i mam wrażenie, że od Inform 7 mógłbym
się niewątpliwie wiele nauczyć, mam wrażenie, że nawet
ten system jest pod pewnym względem dość daleki od ideału.
Chodzi mi konkretnie o zagadnienie modelowania rozmów
i rozmówców. Czasem marzy mi się taki Fallout, w którym
gracz, zamiast mieć do wyboru rozliczne opcje dialogowe,
sam musiałby wpisywać swoje kwestie (na pewno byłoby to dużym
utrudnieniem dla osób, które -- tak jak ja, kiedy grałem
w Fallouta -- nie do końca rozumieją język angielski,
oraz dla takich, które mają problem z szybkim pisaniem
na klawiaturze).

Jedyna gra, o jakiej słyszałem, która realizowałaby podobny
model, to Facade; jednak jej świat obejmował zaledwie dwie
postacie, z którymi dało się rozmawiać, i z jakichś względów
jej twórcy uznali, że rozgrywka powinna odbywać się w czasie
rzeczywistym (co może miałoby sens, gdyby w czasie jej
rozmawiania systemy konwertujące mowę na tekst były lepiej
rozwinięte). Gra była jednak bardziej ciekawostką akademicką,
niż wielkim hitem komercyjnym, ale może dzięki temu uwypuklała
pewną cechę, którą mają języki naturalne (a którą Inform 7
stara się przed nami ukryć) -- mianowicie to, że
poza światem programowania "znaczenia" wypowiedzi mają mocno
przypadkowy i naturalnie wieloznaczny charakter; nasze wypowiedzi
są podzbiorem naszych działań w świecie, a ich rozumienie
jest raczej funkcją kontekstu, niż słownikowych definicji.

Albo, jak to powiedział Humpty Dumpty w "Alicji w Krainie
Czarów", "kiedy używam słowa, oznacza ono dokładnie to,
co chcę, żeby oznaczało - ni mniej, ni więcej!".

Myślę jednak, że owa konstatacja o naturze języka nie
przeszkodzi mi dalej gonić owego króliczka o imieniu
"Zrozumienie" w nadziei, że w końcu uda mi się go złapać.
