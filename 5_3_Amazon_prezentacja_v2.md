# 5.3. System rekomendacyjny Amazon – studium przypadku (ujęcie prawno-prywatyzacyjne)

---

## Wprowadzenie

Amazon jest jedną z największych platform e-commerce na świecie i wzorcowym przykładem wdrożenia systemu rekomendacyjnego opartego na AI (AIRS – _AI-based Recommender System_). Według często cytowanych szacunków rekomendacje odpowiadają za około **35% zakupów** dokonywanych na platformie, co wskazuje na centralne znaczenie tej technologii dla modelu biznesowego firmy.

Do budowy silnika personalizacji Amazon wykorzystuje m.in. usługę **Amazon Personalize** (AWS), trenowaną na danych o zachowaniach użytkowników z całego ekosystemu: platformy zakupowej, urządzeń Kindle, Prime Video, asystenta głosowego Alexa i sieci sklepów Whole Foods.

---

## Zakres przetwarzanych danych osobowych

Polityka prywatności Amazona wyróżnia trzy kategorie przetwarzanych danych:

- **Dane podawane świadomie** – imię, nazwisko, adres, dane płatnicze, nagrania głosowe (Alexa), numer identyfikacji podatkowej i dane bankowe w przypadku sprzedawców.
- **Dane zbierane automatycznie** – historia wyszukiwań, historia przeglądania produktów, historia zakupów, czas na stronach, lokalizacja, dane urządzenia, sposób przewijania strony, kliknięcia.
- **Dane z zewnętrznych źródeł** – informacje od kurierów, partnerów handlowych, biur informacji kredytowej.

> **Kluczowa obserwacja:** Nawet dane pozornie neutralne, zestawione ze sobą i analizowane przez AI, umożliwiają precyzyjne profilowanie wykraczające poza pierwotny cel zakupowy – co rodzi pytania o zgodność z zasadą minimalizacji danych (art. 5 ust. 1 lit. c RODO).

---

## Zidentyfikowane zagrożenia prywatności

Na podstawie badań Chen i in. (2025) wyróżnia się trzy kategorie zagrożeń prywatności w systemach AIRS w e-commerce, które bezpośrednio odnoszą się do praktyk Amazona:

### 1. Poczucie bycia obserwowanym (_perceived surveillance_)
System rekomendacyjny Amazona łączy dane z wielu punktów styku – historii zakupów, wyszukiwań na stronach partnerskich (Amazon Advertising), aktywności głosowej Alexy, wizyt w sklepach Whole Foods. Efektem jest rekomendacja, która dla użytkownika sprawia wrażenie „śledzenia" jego aktywności poza samą platformą.

> *„Rozmawiałem o pewnym produkcie ze znajomym, a potem otworzyłem platformę i zobaczyłem, że system natychmiast mi go rekomenduje. To mnie przeraziło"* – respondent badania Chen i in. (2025).

### 2. Zagrożenie kradzieżą tożsamości (_perceived identity theft_)
Amazon przetwarza szczególnie wrażliwy zestaw danych: numery kart kredytowych, adresy, dane bankowe i podatkowe sprzedawców. Szczegółowe profilowanie przez AIRS powoduje, że zestawienie danych identyfikacyjnych z danymi behawioralnymi tworzy profil, który – w przypadku nieautoryzowanego dostępu – mógłby posłużyć do popełnienia przestępstw na szkodę użytkownika.

### 3. Nieuprawnione wtórne wykorzystanie danych (_perceived unauthorized secondary use_)
Amazon DSP (_Demand-Side Platform_) umożliwia wyświetlanie reklam opartych na historii zachowań na Amazonie na **tysiącach innych witryn i aplikacji partnerskich**. Dane zebrane pierwotnie w celach zakupowych są w ten sposób wtórnie wykorzystywane do targetowania reklamowego – co budzi wątpliwości co do zachowania zasady **ograniczenia celu (art. 5 ust. 1 lit. b RODO)**.

---

## Ocena zgodności z RODO i privacy-by-design

| Zasada RODO | Ocena |
|-------------|-------|
| **Minimalizacja danych** (art. 5 ust. 1 lit. c) | Można krytycznie ocenić w świetle wymogów – zakres zbieranych danych wydaje się wykraczać poza minimum niezbędne do realizacji transakcji |
| **Prywatność jako ustawienie domyślne** (art. 25 ust. 2) | Wydaje się ograniczenie realizowana – domyślna konfiguracja konta maksymalizuje zakres profilowania |
| **Ograniczenie celu** (art. 5 ust. 1 lit. b) | Praktyka Amazon DSP budzi istotne wątpliwości co do zachowania tej zasady wobec danych zakupowych |
| **Przejrzystość** (art. 5 ust. 1 lit. a) | Polityka prywatności istnieje i jest szczegółowa, jednak jej objętość i złożoność mogą ograniczać faktyczną przejrzystość wobec przeciętnego użytkownika |
| **Bezpieczeństwo techniczne** (art. 32) | Wysoki poziom – szyfrowanie end-to-end, certyfikacja PCI DSS, szyfrowanie danych w chmurze AWS |
| **Prawa podmiotów danych** (art. 15–22) | Zapewnione – dostęp do danych, możliwość usunięcia, zarządzanie preferencjami; uczestnictwo w EU–US DPF |

---

## Kontekst regulacyjny

W 2021 r. luksemburska Komisja Ochrony Danych (CNPD) wydała decyzję dotyczącą przetwarzania danych osobowych przez Amazon do celów reklamy behawioralnej, uznając je za niezgodne z RODO. Sprawa stała się następnie przedmiotem postępowania sądowego – w marcu 2026 r. luksemburski sąd uchylił nałożoną karę i skierował sprawę do ponownej oceny przez CNPD.

Niezależnie od ostatecznego rozstrzygnięcia, postępowanie to ilustruje, że **praktyki profilowania i reklamy behawioralnej Amazona budziły poważne wątpliwości organów nadzorczych** co do zgodności z zasadami ograniczenia celu i przejrzystości przetwarzania – nie zaś co do bezpieczeństwa technicznego, które jest odrębnym zagadnieniem.

---

## Wnioski

1. **Amazon jest przykładem strukturalnego napięcia** między ekonomiczną logiką maksymalizacji personalizacji a wymogami RODO dotyczącymi minimalizacji danych i ograniczenia celu.

2. **Zaawansowanie techniczne w zakresie bezpieczeństwa ≠ wdrożenie privacy-by-design.** Amazon chroni dane przed nieautoryzowanym dostępem, jednak zasada prywatności jako ustawienia domyślnego wydaje się ograniczenie realizowana.

3. **Trzy kategorie zagrożeń prywatności** – poczucie nadzoru, zagrożenie kradzieżą tożsamości i wtórne wykorzystanie danych – materializują się w przypadku Amazona w szczególnie wyraźny sposób ze względu na rozbudowany ekosystem zbierania i udostępniania danych.

4. Przypadek Amazona potwierdza, że **privacy-by-design wymaga wbudowania ochrony prywatności w logikę systemu od etapu projektowania** – nie jako wymogu formalnego spełnianego post factum, lecz jako rzeczywistej zasady projektowej ograniczającej zakres przetwarzania od pierwszej linii kodu.

---

*Źródła: Chen i in. (2025), Himeur i in. (2022), Amazon Privacy Notice (2025), CNPD Luxembourg (2021), postępowanie sądowe 2026*
