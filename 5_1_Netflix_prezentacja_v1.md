# 5.1. System rekomendacyjny Netflix – materiał do prezentacji

## Slajd 1. Tytuł

**System rekomendacyjny platformy streamingowej – studium przypadku Netflix**

Kontekst:
- projekt dotyczy relacji między AI a prywatnością,
- analizowany obszar: systemy rekomendacyjne,
- perspektywa: RODO, privacy-by-design, ryzyko profilowania.

---

## Slajd 2. Dlaczego Netflix?

Netflix jest dobrym przykładem systemu rekomendacyjnego, bo personalizacja jest rdzeniem usługi.

Najważniejsze punkty:
- użytkownik nie widzi neutralnego katalogu,
- strona główna jest układana indywidualnie,
- rekomendacje wpływają na wybór filmów, seriali i gier,
- system stale uczy się na podstawie zachowania użytkownika.

**Teza:** Netflix nie tylko pokazuje treści, ale aktywnie kształtuje sposób poruszania się po katalogu.

---

## Slajd 3. Jak działa system rekomendacyjny Netflixa?

Netflix deklaruje, że rekomendacje opierają się m.in. na:
- historii oglądania,
- ocenach i reakcjach użytkownika,
- podobieństwie do innych użytkowników,
- cechach tytułów: gatunek, aktorzy, rok, kategorie,
- porze dnia,
- języku,
- typie urządzenia,
- czasie oglądania danego tytułu.

System personalizuje:
- wybór wierszy na stronie głównej,
- tytuły w wierszach,
- kolejność tytułów,
- sekcje typu „Kontynuuj oglądanie”.

---

## Slajd 4. Jakie dane są przetwarzane?

**Dane konta:**
- e-mail, hasło, telefon,
- informacje płatnicze,
- plan subskrypcji,
- ustawienia konta.

**Dane profilu:**
- nazwa profilu i ikona,
- lista „Moja lista”,
- historia oglądania,
- oceny,
- ustawienia języka, napisów i autoodtwarzania.

**Dane behawioralne:**
- play, pause, stop,
- wyszukiwania,
- kliknięcia,
- czas oglądania,
- moment porzucenia treści.

**Dane techniczne:**
- adres IP,
- identyfikatory urządzeń,
- typ urządzenia,
- system i aplikacja,
- cookies i identyfikatory reklamowe.

---

## Slajd 5. Kluczowy problem prywatności

Dane streamingowe są pozornie niewinne, ale mogą ujawniać bardzo prywatne informacje.

Historia oglądania może pośrednio sugerować:
- zainteresowania polityczne,
- kwestie zdrowotne,
- religię lub światopogląd,
- orientację seksualną,
- problemy rodzinne,
- stan emocjonalny,
- rytm dnia i zwyczaje domowe.

**Wniosek:** dane o oglądaniu są danymi behawioralnymi o dużej wartości profilującej.

---

## Slajd 6. Zagrożenie 1 – poczucie bycia obserwowanym

Netflix analizuje każdą interakcję z usługą:
- co użytkownik ogląda,
- czego nie kończy,
- kiedy ogląda,
- na czym ogląda,
- co wyszukuje,
- jak długo zostaje przy danej treści.

Efekt:
- rekomendacje mogą sprawiać wrażenie bardzo dokładnej znajomości użytkownika,
- użytkownik nie zawsze rozumie, skąd wynika konkretna propozycja,
- rośnie poczucie stałego monitorowania.

---

## Slajd 7. Zagrożenie 2 – nadmierne profilowanie

System rekomendacyjny wpływa na widoczność treści.

Ryzyka:
- użytkownik formalnie ma dostęp do katalogu, ale praktycznie widzi katalog ułożony przez algorytm,
- algorytm może wzmacniać wcześniejsze preferencje,
- może powstać efekt zawężania wyboru,
- użytkownik nie widzi pełnego profilu, który system o nim zbudował.

**Problem:** wygoda personalizacji może ograniczać autonomię informacyjną.

---

## Slajd 8. Zagrożenie 3 – wtórne wykorzystanie danych

Dane mogą służyć nie tylko do rekomendacji, ale też do:
- analityki,
- poprawy usługi,
- marketingu,
- integracji partnerskich,
- reklam,
- bezpieczeństwa i wykrywania nadużyć.

Największe ryzyko:
- rozmycie granicy między rekomendacją treści a reklamą behawioralną,
- wykorzystanie identyfikatorów urządzeń,
- marketing na usługach zewnętrznych,
- dane od firm reklamowych i partnerów.

**Wniosek:** cele przetwarzania muszą być wyraźnie oddzielone.

---

## Slajd 9. Zagrożenie 4 – prywatność w ramach jednego konta

Netflix umożliwia profile, ale profil nie zawsze oznacza pełną prywatność.

Ryzyka:
- inne osoby z dostępem do konta mogą zobaczyć historię, rekomendacje lub „Kontynuuj oglądanie”,
- rekomendacje mogą ujawniać zainteresowania użytkownika,
- profil można zabezpieczyć PIN-em, ale użytkownik musi o tym wiedzieć i aktywnie to zrobić.

**Przykład:** członek rodziny widzi treści oglądane przez inną osobę i wyciąga z nich prywatne wnioski.

---

## Slajd 10. Profil transfer – ważny element prywatności

Netflix pozwala przenosić profil na inne konto.

Przenoszone mogą być:
- rekomendacje,
- historia oglądania,
- oceny,
- czas oglądania,
- informacje o urządzeniu,
- lista „Moja lista”,
- ustawienia profilu,
- dane gier.

Plus:
- wygoda i ciągłość personalizacji.

Ryzyko:
- profil staje się pakietem danych behawioralnych,
- użytkownik musi rozumieć, co dokładnie jest przenoszone.

---

## Slajd 11. Historyczny kontekst – Netflix Prize

Netflix Prize to znany przypadek pokazujący ryzyko reidentyfikacji.

Co się stało:
- Netflix udostępnił zanonimizowany zbiór ocen filmów,
- badacze pokazali, że dane można było powiązać z publicznymi ocenami w IMDb,
- nawet anonimowa historia ocen może ujawniać konkretną osobę.

Wniosek:
- dane rekomendacyjne są trudne do pełnej anonimizacji,
- historia oglądania jest unikalnym wzorcem zachowania.

---

## Slajd 12. Ocena RODO – minimalizacja danych

**Art. 5 ust. 1 lit. c RODO – minimalizacja danych**

Pozytywnie:
- Netflix deklaruje, że rekomendacje nie używają wieku ani płci jako elementu procesu decyzyjnego.

Krytycznie:
- system używa bardzo szerokich danych behawioralnych,
- dane techniczne i kontekstowe mogą silnie profilować użytkownika,
- nie wszystkie dane przydatne biznesowo są automatycznie niezbędne.

Ocena:
- częściowo zgodne,
- wymaga ostrożnej oceny proporcjonalności.

---

## Slajd 13. Ocena RODO – przejrzystość

**Art. 5 ust. 1 lit. a RODO – przejrzystość**

Pozytywnie:
- Netflix publikuje prosty opis działania rekomendacji,
- wskazuje podstawowe kategorie danych używanych przez system,
- użytkownik może pobrać kopię danych.

Ograniczenia:
- brak wyjaśnienia przy konkretnej rekomendacji,
- brak pełnego panelu profilu rekomendacyjnego,
- polityka prywatności jest obszerna i trudna dla przeciętnego użytkownika.

Ocena:
- lepiej niż minimum formalne,
- nadal ograniczona przejrzystość funkcjonalna.

---

## Slajd 14. Ocena RODO – privacy-by-default

**Art. 25 ust. 2 RODO – domyślna ochrona danych**

Pozytywnie:
- profile dziecięce,
- kontrola rodzicielska,
- blokada profilu PIN,
- możliwość ukrywania tytułów z historii,
- ustawienia reklam behawioralnych,
- brak reklam behawioralnych na profilach dziecięcych.

Krytycznie:
- personalizacja jest domyślnym elementem usługi,
- użytkownik musi sam szukać ustawień ograniczających przetwarzanie,
- trudno całkowicie wyłączyć profilowanie rekomendacyjne bez utraty sensu usługi.

---

## Slajd 15. Bezpieczeństwo techniczne

Netflix deklaruje środki administracyjne, logiczne, fizyczne i organizacyjne chroniące dane.

Użytkownik może:
- zmienić hasło,
- wylogować nieznane urządzenia,
- zarządzać dostępem i urządzeniami,
- blokować profil PIN-em,
- chronić się przed phishingiem.

Ważne rozróżnienie:
- bezpieczeństwo techniczne ≠ pełne privacy-by-design,
- dobrze zabezpieczone dane nadal mogą być przetwarzane zbyt szeroko.

---

## Slajd 16. Rekomendacje projektowe

Dla lepszego privacy-by-design Netflix mógłby:

1. Wyraźniej oddzielić rekomendacje treści od reklam.
2. Pokazywać użytkownikowi profil rekomendacyjny.
3. Umożliwić łatwy reset rekomendacji.
4. Ułatwić usuwanie wpływu pojedynczych tytułów.
5. Mocniej promować PIN dla profili.
6. Ograniczać retencję surowych danych oglądania.
7. Stosować pseudonimizację i agregację w analizach.
8. Dodawać krótkie wyjaśnienia przy funkcjach personalizacji.

---

## Slajd 17. Wnioski końcowe

1. Netflix jest przykładem dojrzałego systemu rekomendacyjnego opartego na AI.
2. Personalizacja zwiększa wygodę, ale wymaga intensywnego profilowania.
3. Dane o oglądaniu mogą ujawniać bardzo prywatne informacje.
4. Największe ryzyka dotyczą: profilowania, reklam behawioralnych, wtórnego wykorzystania danych i prywatności profili.
5. Netflix zapewnia pewne mechanizmy kontroli, ale pełne privacy-by-design wymaga większej przejrzystości i silniejszych ustawień domyślnych.
6. Najważniejszy wniosek: skuteczność rekomendacji nie powinna być osiągana kosztem nadmiernego przetwarzania danych użytkownika.

---

## Źródła do slajdu końcowego

- Netflix Privacy Statement: https://help.netflix.com/legal/privacy
- Netflix Help Center – How Netflix’s Recommendations System Works: https://help.netflix.com/en/node/100639
- Netflix Help Center – Profile transfers: https://help.netflix.com/en/node/122698
- Netflix Help Center – How to stop certain uses of your personal information: https://help.netflix.com/en/node/100637
- EDPB Guidelines 4/2019 on Article 25 GDPR: https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-42019-article-25-data-protection-design-and_en
- GDPR/RODO: https://eur-lex.europa.eu/eli/reg/2016/679/oj
- Narayanan, Shmatikov, Robust De-anonymization of Large Sparse Datasets: https://www.cs.cornell.edu/~shmat/shmat_oak08netflix.pdf
