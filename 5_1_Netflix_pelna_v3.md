# 5.1. System rekomendacyjny platformy streamingowej – studium przypadku Netflix

## Spis treści

1. [5.1.1. Charakterystyka platformy i jej systemu rekomendacyjnego](#511-charakterystyka-platformy-i-jej-systemu-rekomendacyjnego)
2. [5.1.2. Zakres i charakter zbieranych danych osobowych](#512-zakres-i-charakter-zbieranych-danych-osobowych)
3. [5.1.3. Identyfikacja zagrożeń prywatności w systemie rekomendacyjnym Netflixa](#513-identyfikacja-zagrozen-prywatnosci-w-systemie-rekomendacyjnym-netflixa)
4. [5.1.4. Uwagi dotyczące bezpieczeństwa technicznego](#514-uwagi-dotyczace-bezpieczenstwa-technicznego)
5. [5.1.5. Ocena zgodności z zasadą privacy-by-design i wymogami RODO](#515-ocena-zgodnosci-z-zasada-privacy-by-design-i-wymogami-rodo)
6. [5.1.6. Kontekst regulacyjny i ryzyka szczególne](#516-kontekst-regulacyjny-i-ryzyka-szczegolne)
7. [5.1.7. Rekomendacje projektowe](#517-rekomendacje-projektowe)
8. [5.1.8. Wnioski z analizy przypadku](#518-wnioski-z-analizy-przypadku)
9. [Źródła wykorzystane w analizie](#zrodla-wykorzystane-w-analizie)

---


<a id="511-charakterystyka-platformy-i-jej-systemu-rekomendacyjnego"></a>

## 5.1.1. Charakterystyka platformy i jej systemu rekomendacyjnego

Netflix jest globalną platformą streamingową działającą w modelu subskrypcyjnym.<sup><a href="#zrodlo-1">[1]</a></sup> Usługa umożliwia dostęp do filmów, seriali, programów dokumentalnych, animacji oraz gier na urządzeniach połączonych z Internetem. Z perspektywy niniejszego projektu Netflix stanowi bardzo dobry przykład systemu rekomendacyjnego, ponieważ personalizacja treści jest jednym z podstawowych elementów działania platformy. Użytkownik nie korzysta z jednego, neutralnego katalogu treści, lecz z interfejsu dynamicznie dopasowywanego do jego profilu, historii oglądania i przewidywanych preferencji.

Netflix sam opisuje swój model jako usługę subskrypcyjną oferującą spersonalizowane rekomendacje, które mają pomagać użytkownikowi odnajdywać filmy, seriale i gry potencjalnie zgodne z jego gustem.<sup><a href="#zrodlo-2">[2]</a></sup> System rekomendacyjny szacuje prawdopodobieństwo, że dany tytuł będzie dla użytkownika interesujący. W tym celu bierze pod uwagę m.in. historię oglądania, oceny tytułów, podobieństwo do innych użytkowników, cechy treści, porę korzystania z usługi, preferowany język, typ urządzenia oraz czas oglądania konkretnych materiałów.

Rekomendacje nie ograniczają się do prostego wskazania kilku tytułów.<sup><a href="#zrodlo-2">[2]</a></sup><sup><a href="#zrodlo-11">[11]</a></sup> Personalizacja obejmuje wiele warstw interfejsu: wybór wierszy na stronie głównej, dobór tytułów w danym wierszu, kolejność prezentowanych pozycji oraz rozmieszczenie rekomendacji. Oznacza to, że system rekomendacyjny wpływa nie tylko na to, *co* zostanie użytkownikowi zaproponowane, ale również *w jakiej kolejności* i *w jakim kontekście* zostanie to pokazane. Przykładowo sekcje typu „Kontynuuj oglądanie”, „Najlepsze propozycje dla Ciebie” lub listy gatunkowe mogą być inne dla każdego profilu na tym samym koncie.

Z punktu widzenia ochrony prywatności szczególnie istotne jest to, że skuteczność systemu rekomendacyjnego Netflixa opiera się na stałym zbieraniu i analizie sygnałów behawioralnych. Platforma deklaruje, że wykorzystuje informacje z każdej wizyty w usłudze, np. to, które tytuły użytkownik rozpoczyna, czy kończy ich oglądanie oraz jak je ocenia.<sup><a href="#zrodlo-2">[2]</a></sup> Dane, algorytmy i systemy obliczeniowe są następnie używane do ciągłego aktualizowania predykcji dotyczących tego, co użytkownik najprawdopodobniej będzie chciał obejrzeć.

Netflix jest więc przykładem systemu rekomendacyjnego typu AIRS, czyli systemu rekomendacyjnego opartego na sztucznej inteligencji i analizie danych. Jego podstawową funkcją biznesową jest zwiększanie zaangażowania użytkownika, ograniczanie problemu nadmiaru treści oraz zmniejszanie ryzyka rezygnacji z subskrypcji. Z perspektywy użytkownika system zapewnia wygodę i szybki dostęp do treści. Z perspektywy ochrony danych osobowych generuje jednak istotne pytania dotyczące zakresu profilowania, przejrzystości, minimalizacji danych i wtórnego wykorzystywania informacji.

---

<a id="512-zakres-i-charakter-zbieranych-danych-osobowych"></a>

## 5.1.2. Zakres i charakter zbieranych danych osobowych

Polityka prywatności Netflixa wskazuje szeroki katalog danych osobowych i technicznych przetwarzanych w związku z korzystaniem z usługi.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-3">[3]</a></sup> Z perspektywy systemu rekomendacyjnego najważniejsze są dane dotyczące konta, profilu, aktywności oglądania, urządzenia, sieci oraz interakcji z usługą.

### a) Dane przekazywane przez użytkownika

Pierwszą kategorię stanowią dane podawane bezpośrednio przez użytkownika.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-3">[3]</a></sup> Należą do nich przede wszystkim dane kontaktowe, takie jak adres e-mail i numer telefonu, dane logowania, informacje o płatności, dane rozliczeniowe oraz ustawienia konta. W zależności od sposobu korzystania z usługi Netflix może przetwarzać również imię i nazwisko, adres, datę urodzenia, płeć lub inne identyfikatory podane przez użytkownika.

W kontekście rekomendacji istotne są także dane konfiguracyjne profilu: nazwa profilu, ikona, preferencje językowe, lista „Moja lista”, ustawienia napisów i dubbingu, ograniczenia wiekowe, ustawienia autoodtwarzania oraz oceny i reakcje na treści. Dane te mogą być traktowane jako informacje deklaratywne i konfiguracyjne, które pomagają systemowi ustalić początkowe preferencje użytkownika.

### b) Dane zbierane automatycznie podczas korzystania z usługi

Drugą, najważniejszą kategorię stanowią dane zbierane automatycznie.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-2">[2]</a></sup> Netflix przetwarza informacje o interakcjach z usługą, w tym zdarzenia odtwarzania, takie jak rozpoczęcie, zatrzymanie, pauza, kontynuacja lub zakończenie oglądania. Do tej grupy należą również historia oglądania, historia gier, wyszukiwane frazy, kliknięcia w aplikacji, wyświetlenia stron, czas i długość dostępu, reakcje na tytuły oraz informacje o tym, jak długo użytkownik oglądał konkretny materiał.

Takie dane mają szczególne znaczenie dla systemu rekomendacyjnego. Na ich podstawie platforma może wnioskować, jakie gatunki, aktorzy, tematy, formaty i style narracji są dla użytkownika atrakcyjne. Co ważne, wnioski te nie muszą wynikać wyłącznie z jawnych ocen. Nawet brak dokończenia filmu, szybkie przewijanie, częste powroty do jednego gatunku lub pora oglądania mogą być sygnałami używanymi przez algorytm.

### c) Dane o urządzeniu, sieci i kontekście korzystania

Netflix przetwarza również dane o urządzeniach i sieci, w tym identyfikatory urządzeń, adresy IP, typ urządzenia, cechy systemu operacyjnego, konfigurację oprogramowania, dane przeglądarki, typ połączenia, dane o wydajności, raporty awarii, znaczniki czasu, pliki cookie, identyfikatory reklamowe i inne identyfikatory techniczne.<sup><a href="#zrodlo-1">[1]</a></sup>

W praktyce dane te mogą pełnić kilka funkcji. Po pierwsze, umożliwiają prawidłowe świadczenie usługi i dopasowanie jakości transmisji do warunków technicznych. Po drugie, mogą wspierać wykrywanie nadużyć i zabezpieczanie konta. Po trzecie, część z nich może być wykorzystywana do personalizacji doświadczenia, np. przez uwzględnienie urządzenia, na którym użytkownik najczęściej ogląda dane typy treści.

### d) Dane z partnerów i źródeł zewnętrznych

Netflix wskazuje również, że może pozyskiwać dane od partnerów, np. producentów telewizorów, dostawców Internetu, operatorów telefonii komórkowej, dostawców urządzeń streamingowych, partnerów rozliczeniowych lub podmiotów umożliwiających dostęp do Netflixa przez własny interfejs.<sup><a href="#zrodlo-1">[1]</a></sup> Mogą to być m.in. dane kontaktowe, informacje płatnicze, identyfikatory urządzeń, adresy IP, komendy głosowe lub zapytania wyszukiwania wykonywane przez urządzenia partnerów.

Z perspektywy prywatności oznacza to, że środowisko przetwarzania danych nie ogranicza się do samej aplikacji Netflix. Użytkownik może korzystać z usługi przez telewizor Smart TV, konsolę, dekoder operatora, aplikację mobilną lub przeglądarkę. Każdy z tych punktów styku może generować inne dane techniczne i kontekstowe.

### e) Dane reklamowe

Istotną zmianą w modelu prywatności platform streamingowych jest rozwój planów z reklamami. Netflix wskazuje, że przetwarza informacje reklamowe, w tym dane o reklamach wyświetlanych użytkownikowi, interakcjach z reklamami, identyfikatorach urządzeń, adresach IP, wnioskach dotyczących użytkownika lub gospodarstwa domowego oraz informacjach dostarczanych przez firmy reklamowe.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-4">[4]</a></sup> Polityka prywatności wskazuje również, że Netflix może zbierać informacje z witryn i aplikacji reklamodawców w celu wspierania reklam, w tym reklam behawioralnych zgodnie z preferencjami użytkownika.

Ten element jest szczególnie ważny z perspektywy RODO, ponieważ poszerza zakres przetwarzania poza klasyczne rekomendacje treści. Dane o oglądaniu i korzystaniu z platformy mogą być rozdzielone od danych używanych do marketingu i reklam, ale dla użytkownika oba procesy mogą być trudne do odróżnienia. Z tego powodu przejrzyste opisanie celów i ustawień reklamowych ma znaczenie dla realnej kontroli nad danymi.

---

<a id="513-identyfikacja-zagrozen-prywatnosci-w-systemie-rekomendacyjnym-netflixa"></a>

## 5.1.3. Identyfikacja zagrożeń prywatności w systemie rekomendacyjnym Netflixa

### a) Poczucie stałej obserwacji

Pierwszym zagrożeniem jest poczucie stałej obserwacji. Netflix analizuje historię oglądania, wyszukiwania, reakcje na tytuły, czas korzystania z usługi, urządzenia oraz inne sygnały kontekstowe.<sup><a href="#zrodlo-2">[2]</a></sup> Z technicznego punktu widzenia są to dane potrzebne do generowania trafnych rekomendacji. Z perspektywy użytkownika może to jednak tworzyć wrażenie, że platforma bardzo dokładnie „zna” jego gust, rytm dnia, zainteresowania, nastroje oraz zwyczaje domowe.

W przypadku platformy streamingowej problem jest szczególnie istotny, ponieważ treści oglądane przez użytkownika mogą ujawniać informacje bardzo prywatne. Historia oglądania może pośrednio wskazywać zainteresowania zdrowotne, religijne, polityczne, seksualne, rodzinne lub emocjonalne. Nawet jeżeli Netflix nie przypisuje użytkownikowi takich kategorii wprost, to długotrwała historia oglądania może tworzyć profil behawioralny o dużej wartości predykcyjnej.

### b) Profilowanie preferencji i ryzyko nadmiernej personalizacji

Drugim zagrożeniem jest rozbudowane profilowanie preferencji. Netflix deklaruje, że rekomendacje bazują na wielu sygnałach, w tym historii oglądania, ocenach, podobieństwie do innych użytkowników, cechach tytułów, porze dnia, języku, urządzeniu i czasie oglądania.<sup><a href="#zrodlo-2">[2]</a></sup> Taki model pozwala skutecznie dopasowywać treści, ale jednocześnie może ograniczać autonomię informacyjną użytkownika.

System rekomendacyjny wpływa na to, jakie treści są najbardziej widoczne. Użytkownik może formalnie mieć dostęp do całego katalogu, ale praktycznie porusza się po katalogu ułożonym przez algorytm. Jeżeli system stale wzmacnia określone kategorie treści, może prowadzić do efektu zawężania wyboru. W kontekście prywatności problem polega na tym, że użytkownik często nie wie, które dane dokładnie przesądziły o konkretnej rekomendacji i jak może skutecznie zmienić swój profil rekomendacyjny.

### c) Nieuprawnione lub nieoczekiwane wtórne wykorzystanie danych

Trzecim zagrożeniem jest wtórne wykorzystanie danych. Dane zebrane pierwotnie w celu świadczenia usługi streamingowej i rekomendowania treści mogą być używane również do analizy, poprawy usługi, marketingu, komunikacji, bezpieczeństwa, rozliczeń, integracji partnerskich oraz reklam. Część tych celów jest uzasadniona technicznie i biznesowo, ale z perspektywy użytkownika granice między nimi mogą być niejasne.

Największe wątpliwości budzi obszar reklam i marketingu na usługach zewnętrznych. Netflix wskazuje, że używa m.in. identyfikatorów haszowanych i resetowalnych identyfikatorów urządzeń do marketingu na usługach stron trzecich, obsługi reklam oraz analityki.<sup><a href="#zrodlo-4">[4]</a></sup> Wskazuje również, że technologie takie jak cookies, pixel tags i identyfikatory mogą służyć do zbierania informacji o aktywności w czasie i w różnych witrynach. Z punktu widzenia zasady ograniczenia celu konieczne jest jasne oddzielenie personalizacji treści od targetowania reklamowego.

### d) Ryzyko ujawnienia historii oglądania wewnątrz gospodarstwa domowego

Czwartym zagrożeniem, charakterystycznym dla Netflixa, jest prywatność wewnątrz jednego konta. Netflix umożliwia tworzenie profili, ale wskazuje, że osoby mające dostęp do konta mogą widzieć informacje związane z oglądaniem, historią, rekomendacjami i listą „Kontynuuj oglądanie”.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-6">[6]</a></sup> Profile tworzą oddzielne doświadczenia użytkownika, ale nie zawsze oznaczają pełną separację prywatności. Osoba posiadająca dostęp do konta może potencjalnie wejść w profil innej osoby, zmienić jego ustawienia lub zobaczyć historię korzystania, chyba że zastosowano blokadę PIN.

W praktyce oznacza to, że dane rekomendacyjne mogą ujawniać informacje nie tylko Netflixowi, ale również innym osobom korzystającym z tego samego konta. Problem ten ma znaczenie w rodzinach, związkach, mieszkaniach współdzielonych oraz sytuacjach, w których konto jest używane przez kilka osób.

### e) Ryzyko przenoszenia profilu i przenoszenia historii oglądania

Netflix oferuje funkcję transferu profilu, która pozwala przenieść profil na nowe konto, istniejące konto albo konto dodatkowego użytkownika.<sup><a href="#zrodlo-5">[5]</a></sup> Przenoszone mogą być rekomendacje, historia oglądania, oceny, czas oglądania, informacje o urządzeniu, kraj, dane „Kontynuuj oglądanie”, lista „Moja lista”, ustawienia, dane gier i inne elementy profilu.

Funkcja ta ma praktyczne zalety, ponieważ pozwala zachować indywidualne rekomendacje po zmianie konta. Z perspektywy prywatności oznacza jednak, że profil użytkownika jest traktowany jako przenoszalny pakiet danych behawioralnych. Konieczne jest więc, aby użytkownik rozumiał, jakie dane są przenoszone, kto inicjuje transfer i jakie skutki ma skopiowanie profilu do innego konta.

### f) Ryzyko reidentyfikacji i znaczenie historycznego przypadku Netflix Prize

W analizie Netflixa warto wspomnieć o historycznym znaczeniu konkursu Netflix Prize. W 2006 r. Netflix udostępnił dużą, zanonimizowaną bazę ocen filmów do celów badawczych.<sup><a href="#zrodlo-10">[10]</a></sup> Badacze Arvind Narayanan i Vitaly Shmatikov pokazali później, że nawet zanonimizowane dane o preferencjach filmowych mogą zostać powiązane z konkretnymi osobami przy wykorzystaniu zewnętrznych źródeł wiedzy, np. publicznych ocen filmów w serwisie IMDb. Przypadek ten jest często przywoływany jako klasyczny przykład ryzyka reidentyfikacji w zbiorach danych rekomendacyjnych.

Nie oznacza to, że obecny system Netflixa działa w ten sam sposób albo że takie dane są dziś publicznie udostępniane. Przypadek pokazuje jednak, że historia ocen i oglądania jest szczególnie wrażliwym typem danych, ponieważ jest rzadka, osobista i trudna do pełnej anonimizacji. Z tego względu prywatność w systemach rekomendacyjnych powinna być oceniana nie tylko przez pryzmat nazwiska, adresu czy numeru karty, ale także przez pryzmat wzorców zachowania.

---

<a id="514-uwagi-dotyczace-bezpieczenstwa-technicznego"></a>

## 5.1.4. Uwagi dotyczące bezpieczeństwa technicznego

Poza aspektami prawnymi system rekomendacyjny Netflixa należy ocenić również od strony bezpieczeństwa technicznego. Platforma deklaruje stosowanie środków administracyjnych, logicznych, fizycznych i organizacyjnych w celu ochrony danych osobowych przed utratą, kradzieżą, nieuprawnionym dostępem, użyciem i modyfikacją.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-7">[7]</a></sup> Użytkownik ma również dostęp do mechanizmów zabezpieczenia konta, takich jak zmiana hasła, wylogowanie z nieużywanych lub nieznanych urządzeń, zarządzanie dostępem i urządzeniami oraz blokada profilu kodem PIN.

W przypadku Netflixa szczególnie istotne są trzy obszary bezpieczeństwa:

1. **Bezpieczeństwo konta i urządzeń** – konto Netflix może być zalogowane na wielu urządzeniach. Jeżeli użytkownik nie wyloguje się z urządzenia publicznego, sprzedanego lub używanego przez inną osobę, inne osoby mogą uzyskać dostęp do profilu, historii oglądania i danych konta.

2. **Bezpieczeństwo danych płatniczych i identyfikacyjnych** – Netflix przetwarza dane płatnicze oraz informacje kontaktowe. Wyciek takich danych mógłby prowadzić do oszustw, phishingu lub przejęcia konta.

3. **Integralność systemu rekomendacyjnego** – systemy rekomendacyjne są podatne na ataki manipulacyjne, takie jak wstrzykiwanie fałszywych interakcji, zatrucie danych treningowych lub próby sztucznego promowania określonych treści. W przypadku platformy streamingowej takie ryzyko może dotyczyć nie tylko prywatności, lecz także jakości rekomendacji i uczciwości prezentowania treści.

Bezpieczeństwo techniczne jest ważnym elementem zgodności z RODO, zwłaszcza z art. 32. Nie jest jednak równoznaczne z pełnym wdrożeniem privacy-by-design. System może być dobrze zabezpieczony przed nieautoryzowanym dostępem, a jednocześnie nadal przetwarzać więcej danych, niż jest to konieczne, albo robić to w sposób mało przejrzysty dla użytkownika.

---

<a id="515-ocena-zgodnosci-z-zasada-privacy-by-design-i-wymogami-rodo"></a>

## 5.1.5. Ocena zgodności z zasadą privacy-by-design i wymogami RODO

### Minimalizacja danych – art. 5 ust. 1 lit. c RODO

Netflix wykorzystuje szeroki zestaw danych: historię oglądania, wyszukiwania, oceny, czas oglądania, urządzenia, język, porę dnia, informacje o sieci, identyfikatory techniczne i dane reklamowe.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-2">[2]</a></sup><sup><a href="#zrodlo-4">[4]</a></sup> Część tych danych jest uzasadniona funkcjonalnie, ponieważ personalizacja treści wymaga znajomości zachowań użytkownika. Jednocześnie zakres przetwarzania należy ocenić krytycznie w miejscach, w których wykracza on poza podstawową funkcję rekomendacji treści.

Z perspektywy minimalizacji pozytywnie należy ocenić deklarację Netflixa, że system rekomendacyjny nie wykorzystuje informacji demograficznych, takich jak wiek czy płeć, jako części procesu decyzyjnego dotyczącego rekomendacji.<sup><a href="#zrodlo-2">[2]</a></sup><sup><a href="#zrodlo-9">[9]</a></sup> Ogranicza to ryzyko oparcia rekomendacji na kategoriach osobowych, które nie zawsze są konieczne do przewidywania gustu filmowego. Z drugiej strony, system nadal wykorzystuje bardzo bogate dane behawioralne i kontekstowe, które mogą być równie silnym źródłem profilowania.

### Ograniczenie celu – art. 5 ust. 1 lit. b RODO

Podstawowym celem przetwarzania danych przez Netflix jest świadczenie usługi streamingowej, w tym personalizacja rekomendacji.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-2">[2]</a></sup><sup><a href="#zrodlo-9">[9]</a></sup> Problem pojawia się wtedy, gdy te same lub podobne kategorie danych są wykorzystywane również do marketingu, analityki, reklam, integracji partnerskich i poprawy usługi. Z formalnego punktu widzenia Netflix opisuje te cele w polityce prywatności. Z perspektywy użytkownika konieczne jest jednak czytelne rozróżnienie: które dane są używane do rekomendowania filmów i seriali, które do obsługi konta, a które do reklam behawioralnych.

Największe ryzyko dotyczy reklam i technologii śledzących. Jeżeli dane z korzystania z usługi, identyfikatory urządzeń lub informacje od firm reklamowych są wykorzystywane do dobierania reklam, użytkownik powinien mieć łatwą i zrozumiałą kontrolę nad takim przetwarzaniem.

### Przejrzystość – art. 5 ust. 1 lit. a RODO

Netflix wypada relatywnie dobrze pod względem dostępności informacji.<sup><a href="#zrodlo-2">[2]</a></sup> Platforma posiada osobny artykuł wyjaśniający działanie systemu rekomendacyjnego prostym językiem. Wyjaśnia w nim główne sygnały wykorzystywane przez algorytm oraz informuje, że rekomendacje są stale aktualizowane na podstawie zachowań użytkownika.

Mimo to pełna przejrzystość pozostaje ograniczona. Użytkownik otrzymuje opis ogólnych kategorii danych, ale nie widzi konkretnego wyjaśnienia przy każdej rekomendacji, np. „ten film pojawia się, bo oglądałeś X, Y i Z”. Nie ma też pełnego panelu pokazującego, jakie cechy profilu rekomendacyjnego zostały mu przypisane. Z tego względu przejrzystość można ocenić jako lepszą niż w wielu usługach cyfrowych, ale nadal niewystarczającą z punktu widzenia pełnej kontroli nad profilowaniem.

### Privacy-by-default – art. 25 ust. 2 RODO

Privacy-by-default wymaga, aby domyślne ustawienia ograniczały przetwarzanie danych do niezbędnego minimum.<sup><a href="#zrodlo-8">[8]</a></sup><sup><a href="#zrodlo-9">[9]</a></sup> W przypadku Netflixa sytuacja jest niejednoznaczna. Personalizacja jest rdzeniem usługi, więc użytkownik od początku korzysta z rekomendacji i profilowania behawioralnego. Nie jest to funkcja dodatkowa, lecz podstawowy element działania platformy.

Pozytywnie należy ocenić istnienie kontroli rodzicielskich, profili dziecięcych, blokady profilu PIN-em, możliwości ukrywania tytułów z historii oglądania, ustawień komunikacji marketingowej, ustawień prywatności i danych oraz kontroli reklam behawioralnych. Netflix wskazuje również, że na profilach dziecięcych nie stosuje reklam behawioralnych.<sup><a href="#zrodlo-4">[4]</a></sup><sup><a href="#zrodlo-6">[6]</a></sup> Negatywnie należy jednak ocenić to, że przeciętny użytkownik musi aktywnie szukać ustawień ograniczających część przetwarzania. Domyślnie korzystanie z usługi oznacza szeroką personalizację.

### Prawa podmiotów danych – art. 15–22 RODO

Netflix zapewnia mechanizmy korzystania z praw użytkownika, w tym dostęp do danych, aktualizację danych, usunięcie danych, sprzeciw, ograniczenie przetwarzania, wycofanie zgody oraz pobranie kopii danych.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-3">[3]</a></sup> Użytkownik może poprosić o kopię informacji, które Netflix posiada na jego temat, a część danych może zobaczyć bezpośrednio w ustawieniach konta.

Ważne jest również to, że Netflix informuje o prawie do niepodlegania decyzji opartej wyłącznie na zautomatyzowanym przetwarzaniu, jeśli taka decyzja wywołuje skutki prawne lub podobnie istotnie wpływa na osobę. Typowe rekomendacje filmów zwykle nie będą miały takiego ciężaru jak decyzja kredytowa czy rekrutacyjna, ale nadal pozostają formą profilowania i powinny być oceniane przez pryzmat przejrzystości oraz praw użytkownika.

### Bezpieczeństwo – art. 32 RODO

Netflix deklaruje stosowanie środków bezpieczeństwa odpowiednich do ryzyka.<sup><a href="#zrodlo-1">[1]</a></sup><sup><a href="#zrodlo-7">[7]</a></sup> Użytkownik ma dostęp do narzędzi zarządzania urządzeniami, może zmienić hasło, wylogować urządzenia i stosować PIN do profilu. Z punktu widzenia RODO są to istotne mechanizmy ograniczające ryzyko nieuprawnionego dostępu do historii oglądania i danych konta.

Należy jednak pamiętać, że bezpieczeństwo konta zależy również od praktyk użytkownika: siły hasła, kontroli urządzeń, ochrony skrzynki e-mail oraz ostrożności wobec phishingu. Netflix wskazuje, że nie prosi użytkowników o podawanie numerów kart, haseł ani danych bankowych w wiadomościach e-mail lub SMS.

---

<a id="516-kontekst-regulacyjny-i-ryzyka-szczegolne"></a>

## 5.1.6. Kontekst regulacyjny i ryzyka szczególne

Netflix działa w Unii Europejskiej w ramach wymogów RODO, co oznacza konieczność spełnienia zasad legalności, rzetelności, przejrzystości, minimalizacji danych, ograniczenia celu, ograniczenia przechowywania, integralności i poufności oraz rozliczalności.<sup><a href="#zrodlo-9">[9]</a></sup> Szczególne znaczenie ma art. 25 RODO dotyczący ochrony danych w fazie projektowania i domyślnej ochrony danych. Zgodnie z wytycznymi EDPB privacy-by-design powinno być uwzględniane już podczas planowania operacji przetwarzania i stale w trakcie działania systemu.<sup><a href="#zrodlo-8">[8]</a></sup>

W przypadku Netflixa ryzyka regulacyjne koncentrują się wokół czterech obszarów:

1. **Profilowanie behawioralne** – rekomendacje opierają się na ciągłej analizie historii oglądania i interakcji użytkownika.

2. **Reklamy behawioralne** – rozwój planów z reklamami powoduje, że dane mogą być wykorzystywane nie tylko do personalizacji treści, ale również do dobierania reklam.

3. **Udostępnianie danych partnerom i dostawcom** – korzystanie z Netflixa przez telewizory, dekodery, operatorów i urządzenia partnerów zwiększa liczbę punktów styku oraz potencjalnych przepływów danych.

4. **Prywatność profili w gospodarstwie domowym** – profile zapewniają personalizację, ale nie zawsze pełną separację prywatności między osobami korzystającymi z jednego konta.

Historyczny przypadek Netflix Prize pokazuje dodatkowo, że dane rekomendacyjne są trudne do pełnej anonimizacji.<sup><a href="#zrodlo-10">[10]</a></sup> Nawet pozornie techniczna historia ocen i oglądania może być unikalna i możliwa do powiązania z konkretną osobą przy użyciu wiedzy zewnętrznej. Współczesna ocena privacy-by-design powinna więc uwzględniać nie tylko zabezpieczenie baz danych, ale także ograniczanie zakresu danych, skracanie retencji, pseudonimizację, agregację oraz ostrożność przy udostępnianiu danych do celów badawczych lub analitycznych.

---

<a id="517-rekomendacje-projektowe"></a>

## 5.1.7. Rekomendacje projektowe

Na podstawie analizy przypadku Netflixa można wskazać kilka praktycznych rekomendacji dla projektowania systemów rekomendacyjnych zgodnie z privacy-by-design:

1. **Wyraźne rozdzielenie personalizacji treści od personalizacji reklam.** Użytkownik powinien jasno widzieć, które dane służą do rekomendacji filmów i seriali, a które do reklam lub marketingu.

2. **Panel kontroli profilu rekomendacyjnego.** Platforma mogłaby udostępniać użytkownikowi bardziej czytelny widok najważniejszych kategorii wpływających na rekomendacje, np. dominujące gatunki, ostatnie sygnały i możliwość ich usunięcia.

3. **Łatwiejsze czyszczenie i resetowanie historii rekomendacyjnej.** Użytkownik powinien mieć prostą możliwość usunięcia wpływu pojedynczych tytułów albo zresetowania profilu rekomendacji bez konieczności zakładania nowego profilu.

4. **Silniejsza separacja profili.** Domyślna ochrona prywatności mogłaby obejmować wyraźniejszą zachętę do ustawienia PIN-u na profilach dorosłych, szczególnie na kontach współdzielonych.

5. **Ograniczenie retencji surowych danych behawioralnych.** Dane szczegółowe, takie jak dokładne zdarzenia odtwarzania, powinny być przechowywane tylko tak długo, jak jest to rzeczywiście niezbędne dla działania usługi, bezpieczeństwa i rozliczalności.

6. **Stosowanie pseudonimizacji i agregacji tam, gdzie pełna identyfikacja nie jest konieczna.** Modele analityczne i testowe powinny korzystać z danych możliwie odseparowanych od bezpośrednich identyfikatorów użytkownika.

7. **Lepsze wyjaśnienia kontekstowe.** Zamiast wyłącznie ogólnej polityki prywatności, platforma powinna stosować krótkie komunikaty przy funkcjach personalizacji, reklam i transferu profilu.

---

<a id="518-wnioski-z-analizy-przypadku"></a>

## 5.1.8. Wnioski z analizy przypadku

Analiza Netflixa pokazuje, że system rekomendacyjny platformy streamingowej jest jednocześnie narzędziem poprawiającym wygodę użytkownika i mechanizmem intensywnego profilowania. Netflix wykorzystuje dane o historii oglądania, ocenach, wyszukiwaniach, czasie oglądania, urządzeniach i kontekście korzystania z usługi, aby przewidywać, jakie treści będą dla użytkownika atrakcyjne. Taki model jest funkcjonalnie uzasadniony, ale wymaga szczególnej staranności w zakresie ochrony prywatności.

Po pierwsze, Netflix pozytywnie wyróżnia się tym, że publicznie opisuje podstawowe zasady działania systemu rekomendacyjnego i wskazuje główne kategorie sygnałów używanych do personalizacji. Jest to ważny element przejrzystości, którego często brakuje w systemach AI.

Po drugie, zakres danych przetwarzanych przez platformę jest bardzo szeroki. Obejmuje nie tylko dane konta i płatności, ale także szczegółowe dane behawioralne, techniczne, reklamowe i partnerskie. Z tego względu zgodność z zasadą minimalizacji danych powinna być oceniana ostrożnie. Nie wszystkie dane przydatne biznesowo są automatycznie danymi niezbędnymi.

Po trzecie, rozwój reklam behawioralnych zwiększa ryzyko rozmycia pierwotnego celu przetwarzania. Dane używane do rekomendowania treści powinny być wyraźnie odseparowane od danych wykorzystywanych do targetowania reklamowego i marketingu na usługach zewnętrznych.

Po czwarte, Netflix pokazuje, że privacy-by-design nie może ograniczać się do zabezpieczenia systemu przed włamaniem. Równie ważne są: domyślne ustawienia prywatności, kontrola użytkownika, możliwość usuwania wpływu danych na rekomendacje, ograniczenie retencji, transparentność algorytmiczna oraz ochrona prywatności profili w ramach jednego konta.

Ostatecznie Netflix można ocenić jako platformę o stosunkowo dojrzałym podejściu do opisywania personalizacji, ale jednocześnie jako przykład systemu, w którym ekonomiczna logika maksymalizacji zaangażowania pozostaje w napięciu z zasadą minimalizacji danych i pełnej kontroli użytkownika nad profilem behawioralnym.

---

<a id="zrodla-wykorzystane-w-analizie"></a>

## Źródła wykorzystane w analizie

<a id="zrodlo-1"></a>
1. Netflix, *Privacy Statement*, https://help.netflix.com/legal/privacy. **Zakres wykorzystania:** podstawowe informacje o przetwarzanych danych, celach przetwarzania, danych z partnerów, danych reklamowych, bezpieczeństwie oraz prawach użytkownika.

<a id="zrodlo-2"></a>
2. Netflix Help Center, *How Netflix’s Recommendations System Works*, https://help.netflix.com/en/node/100639. **Zakres wykorzystania:** opis działania systemu rekomendacyjnego Netflixa, sygnały wykorzystywane do personalizacji, rola historii oglądania, ocen, podobieństwa użytkowników, cech treści, urządzenia i pory korzystania.

<a id="zrodlo-3"></a>
3. Netflix Help Center, *What personal information Netflix holds about you and how to request a copy*, https://help.netflix.com/en/node/100624. **Zakres wykorzystania:** opis danych dostępnych dla użytkownika, sposobu uzyskania kopii danych oraz kategorii informacji powiązanych z kontem i profilem.

<a id="zrodlo-4"></a>
4. Netflix Help Center, *How to stop certain uses of your personal information*, https://help.netflix.com/en/node/100637. **Zakres wykorzystania:** informacje o wykorzystywaniu danych do reklam, marketingu, analityki, identyfikatorach haszowanych, identyfikatorach urządzeń i mechanizmach kontroli użytkownika.

<a id="zrodlo-5"></a>
5. Netflix Help Center, *Profile transfers*, https://help.netflix.com/en/node/122698. **Zakres wykorzystania:** opis funkcji transferu profilu oraz kategorii danych przenoszonych wraz z profilem, takich jak historia oglądania, rekomendacje, oceny i ustawienia.

<a id="zrodlo-6"></a>
6. Netflix Help Center, *Parental controls on Netflix*, https://help.netflix.com/en/node/264. **Zakres wykorzystania:** informacje o profilach dziecięcych, kontrolach rodzicielskich, blokadzie profilu i ograniczeniach dostępu do treści.

<a id="zrodlo-7"></a>
7. Netflix Help Center, *How to keep your account secure*, https://help.netflix.com/en/node/13243. **Zakres wykorzystania:** opis praktyk bezpieczeństwa konta, zarządzania urządzeniami, wylogowywania z nieznanych urządzeń oraz ochrony przed phishingiem.

<a id="zrodlo-8"></a>
8. European Data Protection Board, *Guidelines 4/2019 on Article 25 Data Protection by Design and by Default*, https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-42019-article-25-data-protection-design-and_en. **Zakres wykorzystania:** interpretacja zasady privacy-by-design i privacy-by-default w świetle art. 25 RODO.

<a id="zrodlo-9"></a>
9. Regulation (EU) 2016/679 – GDPR/RODO, https://eur-lex.europa.eu/eli/reg/2016/679/oj. **Zakres wykorzystania:** podstawy prawne analizy: art. 5 RODO, art. 15–22 RODO, art. 25 RODO oraz art. 32 RODO.

<a id="zrodlo-10"></a>
10. Arvind Narayanan, Vitaly Shmatikov, *Robust De-anonymization of Large Sparse Datasets*, IEEE Symposium on Security and Privacy 2008, https://www.cs.cornell.edu/~shmat/shmat_oak08netflix.pdf. **Zakres wykorzystania:** historyczny przykład Netflix Prize i ryzyka reidentyfikacji w zbiorach danych rekomendacyjnych.

<a id="zrodlo-11"></a>
11. Netflix Research, *Personalization, Recommendations and Search*, https://research.netflix.com/research-area/recommendations. **Zakres wykorzystania:** kontekst techniczny dotyczący personalizacji, rekomendacji i wyszukiwania w ekosystemie Netflixa.
