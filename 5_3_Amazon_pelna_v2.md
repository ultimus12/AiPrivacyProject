## 5.3. System rekomendacyjny platformy e-commerce – studium przypadku Amazon

### 5.3.1. Charakterystyka platformy i jej systemu rekomendacyjnego

Amazon jest jedną z największych platform e-commerce na świecie i jednocześnie pionierem stosowania systemów rekomendacyjnych w handlu elektronicznym. Firma wprowadziła algorytmy rekomendacyjne do swojej platformy już w latach dziewięćdziesiątych XX wieku, a stosowane przez nią rozwiązanie oparte na filtrowaniu kolaboratywnym zorientowanym na przedmioty (_item-to-item collaborative filtering_) stało się z czasem wzorcem dla całej branży. Według często cytowanych szacunków rekomendacje odpowiadają za około 35% zakupów dokonywanych na platformie, co jasno wskazuje na ekonomiczne znaczenie tej technologii.

Systemy rekomendacyjne stosowane przez Amazon należą do kategorii AIRS (ang. _AI-based Recommender Systems_). Platforma wdraża te mechanizmy w wielu punktach styku z użytkownikiem: na stronie głównej, na kartach produktów, w procesie zakupu, w wiadomościach e-mail oraz w sekcji „Klienci, którzy kupili ten produkt, kupili również". Do budowy i obsługi silników personalizacji Amazon wykorzystuje m.in. usługę **Amazon Personalize** – własną platformę dostępną w ramach Amazon Web Services (AWS), która umożliwia trenowanie modeli uczenia maszynowego na danych o zachowaniach użytkowników i katalogu produktów w celu generowania spersonalizowanych rekomendacji. System ten zasilany jest danymi ze wszystkich punktów interakcji użytkownika z ekosystemem Amazona: platformy zakupowej, urządzeń Kindle, serwisu Prime Video, asystenta głosowego Alexa oraz – w przypadku posiadaczy kart lojalnościowych – z sieci sklepów stacjonarnych Whole Foods.

---

### 5.3.2. Zakres i charakter zbieranych danych osobowych

Polityka prywatności Amazona wyraźnie wskazuje, że platforma zbiera dane osobowe użytkowników w celu świadczenia i ciągłego doskonalenia swoich usług. Zakres pozyskiwanych informacji jest bardzo szeroki i obejmuje trzy zasadnicze kategorie.

**Dane przekazywane przez użytkownika** obejmują: imię i nazwisko, adres, numery telefonów, informacje płatnicze, wiek, dane logowania, fotografie w profilu, a nawet nagrania głosowe w przypadku korzystania z asystenta Alexa i urządzeń Echo.

**Dane zbierane automatycznie** to wyniki pasywnej obserwacji aktywności użytkownika na platformie. Należą do nich między innymi: adres IP, historia wyszukiwań, historia przeglądania kart produktów, historia zakupów, czas spędzony na poszczególnych stronach, liczba i czas trwania sesji streamingowych, dane o interakcjach z treściami (kliknięcia, przewijanie, najechania kursorem), dane o urządzeniu (typ, system operacyjny, ustawienia), lokalizacja geograficzna oraz informacje o błędach technicznych.

**Dane z zewnętrznych źródeł** obejmują zaktualizowane informacje adresowe od firm kurierskich, dane o interakcjach z partnerami handlowymi i kooperatorami Amazona, a także informacje z biur informacji kredytowej używane do oceny ryzyka finansowego.

Z perspektywy niniejszej analizy szczególnie istotne jest to, że Amazon wprost deklaruje, iż dane osobowe są wykorzystywane m.in. do personalizowania rekomendacji i identyfikowania preferencji użytkownika. Polityka prywatności stanowi, że platforma używa danych osobowych do „rekomendowania funkcji, produktów i usług, które mogą być interesujące, identyfikowania preferencji i personalizowania doświadczenia z usługami Amazon". Zakres gromadzonych informacji sytuuje Amazon jako jeden z podmiotów o najintensywniejszym profilowaniu użytkowników na rynku cyfrowym.

---

### 5.3.3. Identyfikacja zagrożeń prywatności w systemie rekomendacyjnym Amazona

Opierając się na taksonomii zagrożeń prywatności w systemach AIRS wypracowanej przez Chen i in. (2025) na podstawie badań jakościowych i ilościowych z udziałem ponad 580 użytkowników platform e-commerce, można zidentyfikować trzy kluczowe kategorie zagrożeń prywatności bezpośrednio odnoszące się do praktyk Amazona.

#### a) Poczucie bycia obserwowanym (_perceived surveillance_)

Pierwsze i najczęściej wymieniane zagrożenie polega na postrzeganiu systemu rekomendacyjnego jako narzędzia stałego nadzoru. Badani przez Chen i in. (2025) użytkownicy opisywali sytuacje, w których platforma e-commerce proponowała im dokładnie ten produkt, o którym rozmawiali ze znajomymi lub który wyszukiwali w innych usługach. Jeden z respondentów stwierdził wprost: „Rozmawiałem o czymś ze współpracownikiem, a potem otworzyłem platformę i zobaczyłem, że system od razu rekomenduje mi ten produkt. To mnie przeraziło. Nie wiem, kiedy moje dane zostały zebrane" (C7, za: Chen i in., 2025).

W przypadku Amazona zjawisko to przejawia się w szczególnie wyraźny sposób, ponieważ system zbiera dane o aktywności użytkownika z wielu źródeł jednocześnie: historii wyszukiwań na platformie, aktywności reklamowej na stronach partnerskich korzystających z Amazon Advertising, historii zakupów, aktywności głosowej rejestrowanej przez Alexę oraz – w przypadku posiadaczy kart Whole Foods – zachowań w sklepach stacjonarnych. Wynikiem jest rekomendacja, która nierzadko sprawia wrażenie, jakby platforma „wiedziała" o potrzebach użytkownika zanim on sam je w pełni uświadomił.

Z technicznego punktu widzenia zdolność ta wynika z architektury, w której dane użytkownika są zbierane na wielu niezależnych punktach styku, a następnie łączone i analizowane w sposób scentralizowany. Himeur i in. (2022) wskazują, że właśnie ten centralizowany model przechowywania i przetwarzania danych jest jednym z głównych źródeł zagrożeń prywatności w nowoczesnych systemach rekomendacyjnych.

#### b) Zagrożenie kradzieżą tożsamości (_perceived identity theft_)

Drugie zagrożenie dotyczy ryzyka nieautoryzowanego wykorzystania danych tożsamościowych zebranych przez platformę. W przypadku Amazona jest to ryzyko o szczególnym znaczeniu, ponieważ platforma przetwarza dane wrażliwe: numer karty kredytowej, adres zamieszkania, dane rozliczeń finansowych, a w przypadku zarejestrowanych sprzedawców – numery identyfikacji podatkowej i informacje bankowe.

Chen i in. (2025) stwierdzili, że ponad połowa badanych użytkowników platform e-commerce wskazała obawę przed kradzieżą tożsamości jako istotny czynnik kształtujący ich stosunek do systemów AIRS. Respondenci wyrażali obawy, że szczegółowe „etykietowanie" przez systemy AI – czyli przypisywanie im profili zawierających jednocześnie dane identyfikacyjne i dane behawioralne – może w przypadku wycieku danych stworzyć pełny obraz osoby, który będzie mógł zostać przez niepowołane podmioty wykorzystany do nieautoryzowanego zaciągania zobowiązań finansowych lub popełniania przestępstw na szkodę ofiary.

#### c) Nieuprawnione wtórne wykorzystanie danych (_perceived unauthorized secondary use_)

Trzecia kategoria zagrożeń dotyczy obaw użytkowników o to, że dane zebrane w jednym celu – rekomendacji zakupowych – są wtórnie wykorzystywane w celach, na które użytkownik nie wyraził odrębnej, świadomej zgody. W badaniu Chen i in. (2025) ponad połowa respondentów wskazywała na tę formę zagrożenia jako szczególnie niepokojącą.

Polityka prywatności Amazona stanowi, że dane użytkownika są udostępniane podmiotom zewnętrznym realizującym usługi na zlecenie platformy: dostawcom przesyłek, firmom analitycznym, agencjom reklamowym i partnerom płatności. Co istotne, Amazon dzieli się danymi z siecią partnerów reklamowych za pośrednictwem platformy Amazon DSP (_Demand-Side Platform_), która umożliwia wyświetlanie reklam opartych na historii zachowań na Amazonie na tysiącach innych witryn i aplikacji partnerskich. Mechanizm ten, określany w literaturze jako _cross-site behavioral advertising_, powoduje, że dane zebrane pierwotnie w celach transakcyjnych są wykorzystywane w odmienny sposób i w odniesieniu do podmiotów trzecich, o których użytkownik nie był w pełni poinformowany. Budzi to zasadne wątpliwości co do zgodności z zasadą ograniczenia celu, określoną w art. 5 ust. 1 lit. b RODO.

---

### 5.3.4. Uwagi dotyczące bezpieczeństwa technicznego

Poza zagrożeniami prywatności o charakterze prawnym i strukturalnym, warto odnotować, że systemy rekomendacyjne są narażone na zagrożenia bezpieczeństwa technicznego. Himeur i in. (2022) wskazują m.in. na tzw. ataki przez wstrzykiwanie fałszywych profili (_shilling attacks_), w których złośliwi aktorzy tworzą fikcyjne konta z odpowiednio spreparowaną historią ocen w celu manipulowania wynikami rekomendacji, oraz ataki zatrucia danych (_data poisoning attacks_), polegające na wprowadzaniu sfałszowanych danych do procesu trenowania modelu. W odpowiedzi Amazon stosuje zaawansowane mechanizmy wykrywania anomalii, weryfikację tożsamości sprzedawców i szyfrowanie danych w chmurze AWS, a w zakresie transakcji kartowych – certyfikację PCI DSS. Aspekty bezpieczeństwa technicznego, choć istotne, stanowią jednak zagadnienie odrębne od problematyki ochrony danych osobowych i prawa do prywatności, które jest głównym przedmiotem niniejszej analizy.

---

### 5.3.5. Ocena zgodności z zasadą privacy-by-design i wymogami RODO

Ocena Amazona przez pryzmat zasad privacy-by-design i wymogów RODO prowadzi do wniosków niejednoznacznych.

**Minimalizacja danych (art. 5 ust. 1 lit. c RODO)** – Zasada ta nakłada obowiązek ograniczenia zbieranych danych do tych, które są adekwatne i niezbędne do realizacji określonego celu. W przypadku Amazona zakres gromadzonych informacji – obejmujący dane głosowe, aktywność w sklepach stacjonarnych, historię przeglądania stron partnerskich – można krytycznie ocenić w świetle tego wymogu, ponieważ znaczna część tych danych wykracza poza to, co byłoby niezbędne do realizacji transakcji zakupowej.

**Prywatność jako ustawienie domyślne (art. 25 ust. 2 RODO)** – Zasada ta wymaga, aby domyślne ustawienia systemu były skonfigurowane tak, by przetwarzać wyłącznie dane niezbędne. W przypadku Amazona wydaje się ona ograniczenie realizowana: użytkownik, który nie podejmie aktywnych działań (takich jak zarządzanie preferencjami reklam w sekcji „Your Ads Privacy Choices" lub konfiguracja ustawień konta), automatycznie podlega pełnemu zakresowi personalizacji i profilowania, w tym behawioralnym reklamom cross-site. Domyślna konfiguracja konta odpowiada więc maksymalizacji przetwarzania, nie jego minimalizacji.

**Ograniczenie celu (art. 5 ust. 1 lit. b RODO)** – Zasada ta zakazuje przetwarzania danych w celach sprzecznych z pierwotnym celem ich zebrania. Praktyka udostępniania danych behawioralnych partnerom reklamowym przez Amazon DSP budzi istotne wątpliwości co do zachowania tej zasady, szczególnie z perspektywy użytkownika dokonującego zakupu.

**Przejrzystość (art. 5 ust. 1 lit. a RODO)** – Polityka prywatności Amazona jest szczegółowa i dostępna publicznie, jednak jej objętość i poziom skomplikowania sprawiają, że przeciętny użytkownik nie jest w stanie zrozumieć pełnego zakresu operacji przetwarzania. Chen i in. (2025) wskazują, że jednym z głównych czynników generujących poczucie nadzoru jest właśnie brak zrozumienia przez użytkowników sposobu działania systemów AIRS. Przejrzystość realizowana na poziomie dokumentu prawnego nie przekłada się automatycznie na przejrzystość funkcjonalną z perspektywy użytkownika.

**Bezpieczeństwo techniczne (art. 32 RODO)** – W tym obszarze Amazon prezentuje wysoki poziom dojrzałości. Certyfikacja PCI DSS, szyfrowanie end-to-end przy transmisji danych płatniczych, szyfrowanie danych w chmurze AWS z użyciem indywidualnych kluczy oraz wielostopniowe mechanizmy uwierzytelniania świadczą o tym, że ochrona przed nieautoryzowanym dostępem jest traktowana priorytetowo.

**Prawa podmiotów danych (art. 15–22 RODO)** – Amazon zapewnia użytkownikom możliwość dostępu do danych za pośrednictwem sekcji „Your Account", złożenia wniosku o dostęp lub usunięcie danych przez portal „Data Privacy Queries" oraz zarządzania preferencjami reklamowymi. Platforma uczestniczy w programie EU–US Data Privacy Framework, co zapewnia określony poziom ochrony dla transferów danych transatlantyckich.

---

### 5.3.6. Kontekst regulacyjny

Napięcie między modelem biznesowym Amazona a wymogami europejskich regulacji ochrony prywatności znalazło swoje odzwierciedlenie w postępowaniach przed organami nadzorczymi. W 2021 r. luksemburska Komisja Ochrony Danych (CNPD) wydała decyzję nakładającą na Amazon karę administracyjną dotyczącą przetwarzania danych osobowych do celów reklamy behawioralnej w sposób uznany za niezgodny z RODO. Decyzja ta stała się następnie przedmiotem postępowania sądowego – w marcu 2026 r. luksemburski sąd uchylił nałożoną karę i skierował sprawę do ponownej oceny przez CNPD. Niezależnie od ostatecznego rozstrzygnięcia, samo postępowanie ilustruje, że praktyki profilowania użytkowników i reklamy behawioralnej stosowane przez Amazon budziły poważne wątpliwości organów nadzorczych co do ich zgodności z zasadami ograniczenia celu i przejrzystości przetwarzania.

---

### 5.3.7. Wnioski z analizy przypadku

Analiza systemu rekomendacyjnego Amazona prowadzi do następujących wniosków:

Po pierwsze, Amazon jest przykładem platformy, w której system rekomendacyjny integruje ogromną ilość danych z wielu źródeł, tworząc jeden z najbardziej rozbudowanych profili użytkownika w sektorze e-commerce. Zakres zbieranych informacji – od historii zakupów, przez dane głosowe, po zachowania w sklepach stacjonarnych – generuje ryzyka prywatności, które w literaturze przedmiotu są opisywane jako poczucie nadzoru, zagrożenie kradzieżą tożsamości i obawy przed wtórnym wykorzystaniem danych.

Po drugie, model biznesowy oparty na reklamie behawioralnej (Amazon DSP) powoduje, że dane zebrane w celach zakupowych są intensywnie wykorzystywane do celów reklamowych wobec podmiotów trzecich. Budzi to uzasadnione wątpliwości co do zgodności z zasadami minimalizacji danych i ograniczenia celu wynikającymi z RODO.

Po trzecie, zaawansowanie techniczne w zakresie bezpieczeństwa danych nie jest równoznaczne z wdrożeniem privacy-by-design. Amazon stosuje silne mechanizmy ochrony przed naruszeniami bezpieczeństwa, jednak zasada prywatności jako ustawienia domyślnego wydaje się ograniczenie realizowana – domyślna konfiguracja konta maksymalizuje zakres profilowania, nie jego ograniczenie.

Po czwarte, przypadek Amazona potwierdza ogólną obserwację formułowaną zarówno w literaturze naukowej (Himeur i in., 2022; Chen i in., 2025), jak i w orzecznictwie organów nadzorczych: że zagrożenia prywatności w nowoczesnych systemach rekomendacyjnych wynikają nie tylko z niewystarczających zabezpieczeń technicznych, ale przede wszystkim z fundamentalnego napięcia między ekonomiczną logiką maksymalizacji personalizacji a wymogami minimalizacji danych i transparentności przetwarzania.

---

*Źródła:*
- *Chen, T., Liu, F., Shen, X.-L., Wu, J., Liu, Y. (2025). Conceptualization of privacy concerns and their influence on consumers' resistance to AI-based recommender systems in e-commerce. Industrial Management & Data Systems, 125(5), 1844–1868.*
- *Himeur, Y., Sohail, S.S., Bensaali, F., Amira, A., Alazab, M. (2022). Latest trends of security and privacy in recommender systems: A comprehensive review and future perspectives. Computers & Security, 118, 102746.*
- *Amazon.com Privacy Notice (aktualnie obowiązująca wersja, dostęp: kwiecień 2025).*
