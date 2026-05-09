# 5.4. Wnioski porównawcze – Netflix i Amazon

## 5.4.1. Cel porównania

Celem porównania jest zestawienie dwóch różnych typów systemów rekomendacyjnych: platformy streamingowej Netflix oraz platformy e-commerce Amazon. Obie usługi wykorzystują dane użytkowników do personalizacji, ale robią to w innym kontekście biznesowym. Netflix rekomenduje głównie filmy, seriale i gry, natomiast Amazon rekomenduje produkty i usługi, które mogą prowadzić bezpośrednio do zakupu.

Z punktu widzenia projektu najważniejsze jest sprawdzenie, jak oba systemy wypadają w kontekście ochrony prywatności, zasady privacy-by-design, privacy-by-default oraz podstawowych zasad RODO: minimalizacji danych, ograniczenia celu, przejrzystości i kontroli użytkownika.

---

## 5.4.2. Podstawowe podobieństwa

Netflix i Amazon działają w różnych sektorach, ale ich systemy rekomendacyjne mają kilka wspólnych cech.

Po pierwsze, oba systemy opierają się na profilowaniu użytkownika. Platformy analizują wcześniejsze zachowania, aby przewidywać, co użytkownik może chcieć obejrzeć albo kupić. W przypadku Netflixa są to głównie dane o oglądaniu, wyszukiwaniu i reakcjach na treści. W przypadku Amazona są to dane o przeglądaniu produktów, zakupach, wyszukiwaniach, aktywności w usługach powiązanych i interakcjach z reklamami.

Po drugie, w obu przypadkach personalizacja jest ważnym elementem modelu biznesowego. Netflix używa rekomendacji, aby użytkownik dłużej korzystał z platformy i łatwiej znajdował interesujące treści. Amazon używa rekomendacji, aby zwiększać prawdopodobieństwo zakupu, proponować produkty podobne lub uzupełniające oraz rozwijać sprzedaż i reklamę.

Po trzecie, oba przypadki pokazują napięcie między skutecznością systemu AI a prywatnością. Im więcej danych platforma posiada o użytkowniku, tym dokładniejsze mogą być rekomendacje. Jednocześnie większy zakres danych oznacza większe ryzyko profilowania, nieprzejrzystości oraz wykorzystania danych w celach, których użytkownik może nie rozumieć.

---

## 5.4.3. Najważniejsze różnice

| Obszar porównania | Netflix | Amazon |
|---|---|---|
| **Rodzaj platformy** | Platforma streamingowa | Platforma e-commerce i ekosystem usług cyfrowych |
| **Główny cel rekomendacji** | Polecanie filmów, seriali i gier | Polecanie produktów, usług i ofert zakupowych |
| **Główne dane używane do rekomendacji** | Historia oglądania, wyszukiwania, oceny, czas oglądania, urządzenie, profil | Historia zakupów, przeglądanie produktów, wyszukiwania, kliknięcia, dane płatnicze, adresowe, dane z innych usług Amazona |
| **Wpływ rekomendacji na użytkownika** | Wpływa głównie na wybór treści i czas korzystania z platformy | Wpływa bezpośrednio na decyzje zakupowe i wydatki użytkownika |
| **Największe ryzyko prywatności** | Szczegółowy profil preferencji oglądania oraz wykorzystanie danych do reklam | Bardzo szeroki profil użytkownika, łączenie danych z wielu źródeł i wtórne użycie danych w reklamie behawioralnej |
| **Zakres ekosystemu danych** | Głównie usługa streamingowa, urządzenia, partnerzy techniczni i reklamowi | Sklep, Prime Video, Kindle, Alexa, reklamy, partnerzy, dostawy, płatności, Whole Foods |
| **Ryzyko kradzieży tożsamości** | Istnieje, ale jest mniejsze niż w e-commerce | Wyższe, bo Amazon przetwarza więcej danych finansowych, adresowych i transakcyjnych |
| **Problem reklam** | Szczególnie istotny przy planach z reklamami i identyfikatorach reklamowych | Bardzo istotny ze względu na Amazon DSP i reklamy poza platformą |
| **Ocena privacy-by-default** | Częściowo spełnione, ale domyślnie działa szeroka personalizacja | Bardziej problematyczne, bo domyślna konfiguracja sprzyja szerokiemu profilowaniu |
| **Ogólna ocena ryzyka** | Średnie do wysokiego | Wysokie |

---

## 5.4.4. Porównanie pod kątem minimalizacji danych

Zasada minimalizacji danych oznacza, że platforma powinna zbierać tylko te dane, które są rzeczywiście potrzebne do konkretnego celu.

W przypadku Netflixa część danych jest dość łatwa do uzasadnienia. Jeśli platforma ma polecać filmy i seriale, musi znać historię oglądania, reakcje użytkownika i podstawowe informacje o profilu. Problem pojawia się wtedy, gdy zakres danych rozszerza się na reklamę, marketing, identyfikatory urządzeń, dane od partnerów i analizę zachowań poza samą funkcją rekomendacji.

W przypadku Amazona problem minimalizacji jest większy. Amazon działa nie tylko jako sklep, ale jako rozbudowany ekosystem usług. Dane z zakupów, wyszukiwań, płatności, dostaw, urządzeń, reklam, Alexy, Kindle, Prime Video i innych usług mogą razem tworzyć bardzo szczegółowy profil użytkownika. Z tego powodu trudniej uznać, że wszystkie dane są niezbędne wyłącznie do podstawowej obsługi zakupów.

**Wniosek:** Netflix zbiera dużo danych, ale ich część jest bezpośrednio związana ze streamingiem. Amazon zbiera dane z większej liczby źródeł, dlatego ryzyko naruszenia zasady minimalizacji jest wyraźnie większe.

---

## 5.4.5. Porównanie pod kątem ograniczenia celu

Zasada ograniczenia celu oznacza, że dane powinny być zbierane w konkretnym, jasno określonym celu i nie powinny być później używane w zupełnie innym celu bez odpowiedniego uzasadnienia i poinformowania użytkownika.

W przypadku Netflixa podstawowym celem jest świadczenie usługi streamingowej. Do tego celu można zaliczyć obsługę konta, odtwarzanie treści, zapamiętywanie historii oglądania i personalizację rekomendacji. Wątpliwości pojawiają się przy reklamach, marketingu, analityce i technologiach śledzących. Użytkownik powinien wyraźnie rozumieć, które dane są używane do rekomendacji filmów, a które do reklam.

W przypadku Amazona ograniczenie celu jest jeszcze trudniejsze do oceny. Dane zebrane przy zakupach mogą być używane nie tylko do realizacji transakcji, ale również do rekomendacji, reklamy behawioralnej, analityki, promocji i działań w usługach partnerskich. Szczególnie problematyczny jest obszar Amazon DSP, czyli wykorzystanie danych do reklam poza samą platformą Amazon.

**Wniosek:** W obu przypadkach istnieje ryzyko rozmycia celu przetwarzania, ale w Amazonie jest ono większe, bo dane zakupowe i behawioralne są mocniej powiązane z reklamą oraz całym ekosystemem usług.

---

## 5.4.6. Porównanie pod kątem przejrzystości

Przejrzystość oznacza, że użytkownik powinien wiedzieć, jakie dane są zbierane, po co są używane i jak wpływają na rekomendacje.

Netflix wypada w tym obszarze stosunkowo dobrze, ponieważ publicznie wyjaśnia podstawowe zasady działania systemu rekomendacyjnego. Użytkownik może dowiedzieć się, że znaczenie mają m.in. historia oglądania, oceny, podobieństwo do innych użytkowników, cechy tytułów, pora oglądania i typ urządzenia. Nadal jednak użytkownik nie widzi dokładnie, dlaczego konkretny film został mu polecony i jakie cechy profilu zostały mu przypisane.

Amazon również informuje o przetwarzaniu danych, ale jego ekosystem jest znacznie bardziej złożony. Przeciętnemu użytkownikowi trudniej zrozumieć, jak dane z zakupów, przeglądania, reklam, Alexy, Prime Video czy partnerów są ze sobą łączone. Sama dostępność polityki prywatności nie oznacza jeszcze, że użytkownik realnie rozumie działanie systemu.

**Wniosek:** Netflix jest bardziej przejrzysty w opisie samej logiki rekomendacji. Amazon jest mniej czytelny dla przeciętnego użytkownika, ponieważ działa w większym i bardziej złożonym ekosystemie danych.

---

## 5.4.7. Porównanie pod kątem privacy-by-default

Privacy-by-default oznacza, że domyślne ustawienia usługi powinny chronić prywatność użytkownika, a nie wymagać od niego samodzielnego wyłączania nadmiarowego przetwarzania.

W przypadku Netflixa domyślna personalizacja jest częścią działania usługi. Nie jest to całkowicie negatywne, bo rekomendacje są jedną z podstawowych funkcji platformy. Problem polega jednak na tym, że użytkownik musi samodzielnie szukać ustawień związanych z prywatnością, reklamami, historią oglądania lub kontrolą profilu.

W przypadku Amazona privacy-by-default budzi większe wątpliwości. Domyślne działanie platformy jest mocno nastawione na personalizację, rekomendacje i reklamę. Użytkownik, który nie zmieni ustawień, podlega szerokiemu profilowaniu w wielu usługach i kanałach.

**Wniosek:** Obie platformy powinny mocniej rozwijać domyślne ustawienia przyjazne prywatności. Większy problem występuje jednak w Amazonie, ponieważ domyślne profilowanie obejmuje więcej celów i źródeł danych.

---

## 5.4.8. Porównanie pod kątem bezpieczeństwa technicznego

Bezpieczeństwo techniczne oznacza ochronę danych przed nieuprawnionym dostępem, wyciekiem lub przejęciem konta. W obu przypadkach platformy deklarują stosowanie środków bezpieczeństwa, takich jak ochrona konta, szyfrowanie, zarządzanie urządzeniami i mechanizmy wykrywania nadużyć.

Netflix daje użytkownikowi narzędzia takie jak zarządzanie urządzeniami, zmiana hasła, wylogowanie urządzeń, kontrola profili i ustawienia rodzicielskie. Są to ważne mechanizmy, ponieważ historia oglądania może ujawniać prywatne zainteresowania użytkownika.

Amazon stosuje rozbudowane mechanizmy bezpieczeństwa, ponieważ przetwarza dane transakcyjne, płatnicze, adresowe i dane sprzedawców. Ryzyko skutków naruszenia jest jednak większe, bo wyciek danych Amazona mógłby obejmować nie tylko zainteresowania użytkownika, ale również dane finansowe, adresowe i zakupowe.

**Wniosek:** Obie platformy mają rozwinięte zabezpieczenia techniczne, ale samo bezpieczeństwo nie oznacza jeszcze pełnej zgodności z privacy-by-design. Platforma może dobrze chronić dane przed włamaniem, a jednocześnie zbierać ich zbyt dużo lub wykorzystywać je do zbyt wielu celów.

---

## 5.4.9. Główne ryzyka prywatności

### Netflix

Najważniejsze ryzyka w przypadku Netflixa to:

- tworzenie szczegółowego profilu gustu i zwyczajów oglądania,
- możliwość wyciągania pośrednich wniosków o zainteresowaniach, nastrojach lub sytuacji życiowej użytkownika,
- wykorzystywanie danych do reklam i marketingu,
- ograniczona wiedza użytkownika o tym, dlaczego konkretne treści są mu rekomendowane,
- prywatność profili na kontach współdzielonych przez kilka osób.

### Amazon

Najważniejsze ryzyka w przypadku Amazona to:

- łączenie danych z wielu źródeł i usług,
- profilowanie użytkownika nie tylko jako odbiorcy treści, ale też jako konsumenta,
- wykorzystywanie danych zakupowych do reklamy behawioralnej,
- ryzyko wtórnego użycia danych w celach innych niż pierwotny zakup,
- większe ryzyko kradzieży tożsamości ze względu na dane adresowe, finansowe i transakcyjne,
- trudność z realnym zrozumieniem całego ekosystemu przetwarzania danych.

---

## 5.4.10. Ocena końcowa

Porównanie Netflixa i Amazona pokazuje, że systemy rekomendacyjne mogą generować różne poziomy ryzyka w zależności od rodzaju platformy i zakresu danych.

Netflix jest przykładem platformy, w której rekomendacje są mocno powiązane z główną usługą. Użytkownik płaci za dostęp do treści, a personalizacja pomaga mu znaleźć filmy i seriale. Ryzyko prywatności polega głównie na tym, że historia oglądania i zachowania w aplikacji mogą tworzyć szczegółowy profil użytkownika. Dodatkowe wątpliwości pojawiają się przy reklamach i współpracy z partnerami.

Amazon jest przykładem platformy o wyższym poziomie ryzyka prywatności. Wynika to z tego, że rekomendacje są powiązane z zakupami, płatnościami, reklamą, dostawami i wieloma usługami dodatkowymi. Amazon może łączyć dane z różnych obszarów życia użytkownika, a rekomendacje mogą wpływać bezpośrednio na decyzje finansowe.

Najważniejszy wspólny wniosek jest taki, że privacy-by-design nie może oznaczać tylko zabezpieczenia danych przed wyciekiem. Musi obejmować także ograniczenie ilości zbieranych danych, jasne określenie celu przetwarzania, proste ustawienia prywatności, kontrolę użytkownika i przejrzyste wyjaśnienie działania rekomendacji.

---
---

## 5.4.11. Syntetyczna ocena

| Kryterium | Netflix | Amazon | Który przypadek jest bardziej ryzykowny? |
|---|---|---|---|
| Minimalizacja danych | Umiarkowane ryzyko | Wysokie ryzyko | Amazon |
| Ograniczenie celu | Ryzyko głównie przy reklamach | Wysokie ryzyko przez reklamy i ekosystem usług | Amazon |
| Przejrzystość | Lepsza w zakresie opisu rekomendacji | Trudniejsza przez złożoność ekosystemu | Amazon |
| Privacy-by-default | Częściowo problematyczne | Bardziej problematyczne | Amazon |
| Bezpieczeństwo techniczne | Istotne, ale mniejsze skutki naruszenia | Bardzo istotne przez dane finansowe i adresowe | Amazon |
| Profilowanie behawioralne | Wysokie w zakresie oglądania | Bardzo wysokie w zakresie zakupów i usług | Amazon |
| Wpływ na użytkownika | Wybór treści i czas korzystania | Decyzje zakupowe, reklamy i wydatki | Amazon |

**Ogólna konkluzja:** Netflix i Amazon pokazują, że systemy rekomendacyjne są użyteczne, ale wymagają ostrożnego projektowania. Netflix jest mniej ryzykowny, ponieważ działa głównie w kontekście treści streamingowych. Amazon jest bardziej ryzykowny, ponieważ łączy rekomendacje z zakupami, płatnościami, reklamą i wieloma usługami dodatkowymi. W obu przypadkach najważniejsze jest to, aby personalizacja była przejrzysta, ograniczona do potrzebnego celu i możliwa do kontrolowania przez użytkownika.

---

## Źródła wykorzystane w porównaniu

- Netflix, *Privacy Statement*, https://help.netflix.com/legal/privacy
- Netflix Help Center, *How Netflix’s Recommendations System Works*, https://help.netflix.com/en/node/100639
- Netflix Help Center, *How to stop certain uses of your personal information*, https://help.netflix.com/en/node/100637
- Amazon, *Amazon.com Privacy Notice*, https://www.amazon.com/gp/help/customer/display.html?nodeId=GX7NJQ4ZB8MHFRNJ
- Amazon Ads, *Amazon DSP*, https://advertising.amazon.com/solutions/products/amazon-dsp
- Rozporządzenie Parlamentu Europejskiego i Rady (UE) 2016/679, RODO/GDPR, https://eur-lex.europa.eu/eli/reg/2016/679/oj
- European Data Protection Board, *Guidelines 4/2019 on Article 25 Data Protection by Design and by Default*.
