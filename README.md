# European Real Estate Intelligence Gdzie naprawd warto inwestować
Analiza atrakcyjności inwestycyjnej rynków nieruchomości w krajach UE — gdzie ceny rosną szybciej niż zarobki, gdzie jest przestrzeń wzrostu i gdzie ryzyko jest najwyższe.

## 📌 O projekcie

Interaktywny dashboard Power BI analizujący atrakcyjność inwestycyjną 
rynków nieruchomości mieszkaniowych w 34 krajach europejskich w latach 
2015–2024. Projekt odpowiada na pytanie: **gdzie w Europie warto lokować 
kapitał w nieruchomości, aby maksymalizować długoterminowy zwrot przy 
akceptowalnym poziomie ryzyka?**

Dane źródłowe pochodzą z **Eurostatu** i obejmują wskaźniki 
makroekonomiczne oraz dane rynku nieruchomości.

---

## 🎯 Kluczowe pytania badawcze

- Które kraje oferują najlepszy stosunek potencjału wzrostu do poziomu ryzyka?
- Jak wygląda ranking krajów na podstawie wskaźnika PIS?
- Które czynniki mają największy wpływ na atrakcyjność inwestycyjną?
- Czy wysoka dynamika cen przekłada się na atrakcyjność, czy wiąże się z większym ryzykiem?

---

## 🛠️ Narzędzia i technologie

| Narzędzie | Zastosowanie |
|---|---|
| **Power BI** | Modelowanie danych, wizualizacje, interaktywny dashboard |
| **DAX** | Miary obliczeniowe, normalizacja, ranking, dekompozycja wskaźnika |
| **Eurostat** | Źródło danych makroekonomicznych i rynku nieruchomości |

---

## 📊 Wskaźnik PIS (Property Investment Score)

Na potrzeby analizy skonstruowałem autorski wskaźnik **PIS Score** 
agregujący cztery wymiary atrakcyjności inwestycyjnej w jedną miarę 
syntetyczną (zakres 0–1).

### Składowe wskaźnika

| Składowa | Waga | Uzasadnienie |
|---|---|---|
| **HPI Growth 5Y %** | 35% | Historyczna dynamika wzrostu wartości kapitału — kluczowy czynnik dla inwestora długoterminowego |
| **Price to Income Ratio** | 30% | Dostępność cenowa jako wskaźnik płynności rynku i ryzyka przesycenia |
| **Avg GDP Index** | 20% | Wzrost gospodarczy jako fundament popytu na nieruchomości |
| **Avg Unemployment** | 15% | Stabilność rynku pracy jako wskaźnik bezpieczeństwa spłat i stabilności najmu |

> Wagi zostały skalibrowane empirycznie na podstawie analizy literatury inwestycyjnej oraz własnej oceny istotności czynników dla  długoterminowego zwrotu na rynkach europejskich.

### Skala ocen

| Kategoria | Zakres | Interpretacja |
|---|---|---|
| 🟢 **Wysoki potencjał** | > 0,60 | Silne fundamenty i wysoka dynamika wzrostu |
| 🟡 **Stabilny** | 0,40 – 0,60 | Umiarkowany potencjał, stabilne rynki |
| 🔴 **Ryzykowny** | < 0,40 | Podwyższone ryzyko strukturalne lub brak danych |

---

## 📈 Kluczowe wyniki analizy

### Rozkład krajów według kategorii
- 🟢 **17 krajów** — High Potential
- 🟡 **11 krajów** — Stable  
- 🔴 **6 krajów** — Caution

### TOP 5 najbardziej atrakcyjnych rynków

| Pozycja | Kraj | PIS Score | Profil |
|---|---|---|---|
| 🥇 1 | **Islandia** | 0,84 | Jedyny prawdziwy Sweet Spot — wysoki wzrost, niskie PTI |
| 🥈 2 | **Węgry** | 0,82 | Najwyższe PTI w całej analizie kompensowane ekstremalną dynamiką wzrostu |
| 🥉 3 | **Litwa** | 0,78 | Silny wzrost przy wysokim PTI — atrakcyjne dla inwestora zagranicznego |
| 4 | **Polska** | 0,76 | Dynamiczny rynek z rosnącym PTI — okno inwestycyjne się zwęża |
| 5 | **Bułgaria / Estonia / Irlandia** | 0,73 | Zróżnicowane profile, wspólny mianownik wzrostu cen |


### Bottom 3 — rynki podwyższonego ryzyka

| Kraj | PIS Score | Główna przyczyna |
|---|---|---|
| **Szwajcaria** | 0,30 | Ujemna dynamika cen (-0,23), ekstremalnie wysokie PTI |
| **Macedonia Północna** | 0,33 | Brak danych HPI i GDP w Eurostacie |
| **Czarnogóra** | 0,35 | Brak danych HPI, minimalne GDP i Risk score |

---

## 💡 Wnioski i rekomendacje

### Wniosek 1 — Europa Środkowo-Wschodnia dominuje ranking
Pięć najbardziej atrakcyjnych rynków to kraje regionu CEE lub rynki 
wschodzące. Łączą dynamiczny wzrost cen z PTI poniżej średniej 
europejskiej (0,60) — oznacza to że rynki te rosną, ale nie są jeszcze 
przesycone cenowo. To optymalny moment dla inwestora długoterminowego 
szukającego wzrostu wartości kapitału.

### Wniosek 2 — Jedynym prawdziwym Sweet Spot jest Islandia
Scatter plot HPI Growth vs PTI ujawnia że spośród wszystkich 34 krajów 
**tylko Islandia** spełnia oba kryteria Sweet Spot jednocześnie — wysoki 
wzrost cen przy niskim PTI. 

Pozostałe kraje z TOP 5 mają wysokie PTI względem zarobków lokalnych. 
Węgry jako paradoks rankingu zajmują 2. miejsce mimo **najwyższego PTI 
spośród wszystkich 34 krajów** — wysoki PIS Score zawdzięczają 
ekstremalnej dynamice wzrostu cen (0,42) która kompensuje niską 
dostępność cenową. Litwa, Polska i Bułgaria/Estonia podążają podobną 
ścieżką — rosnące ceny przy PTI coraz mniej dostępnym dla lokalnych 
nabywców. To oznacza że liderzy rankingu są **atrakcyjni dla inwestora 
zagranicznego** nastawionego na wzrost kapitału, ale stanowią rosnące 
wyzwanie dla rodzimych nabywców. To ryzyko długoterminowe dla płynności 
rynku które inwestor powinien monitorować.

### Wniosek 3 — Wysoki wzrost cen bez dostępności to pułapka
Francja, Finlandia i Szwecja mimo że klasyfikują się jako Stable (żółte) 
grawitują w kierunku strefy Unikaj — łączą słabą dynamikę wzrostu z 
wysokim PTI. To rynki drogie bez perspektyw wzrostu wartości kapitału. 
Szwajcaria jako skrajny przypadek tej tendencji osiąga najniższy PIS 
Score (0,30) mimo najsilniejszego GDP w analizie — ujemna dynamika cen 
(-0,23) dyskwalifikuje ją jako cel inwestycyjny.

### Wniosek 4 — GDP samo w sobie nie decyduje o rankingu
Dekompozycja wskaźnika PIS ujawnia że składowa GDP jest najbardziej 
wyrównana między krajami — bogactwo gospodarcze nie różnicuje rankingu 
inwestycyjnego. Kluczowym czynnikiem różnicującym jest **relacja między 
dynamiką wzrostu cen a dostępnością cenową** — czyli HPI Growth vs PTI. 
Szwajcaria i Luksemburg są tego najlepszym dowodem — silne GDP, słaby 
wynik inwestycyjny.

### Wniosek 5 — Brakujące dane jako sygnał ostrzegawczy
Macedonia Północna i Czarnogóra osiągają niskie wyniki (0,33–0,35) 
głównie z powodu braku danych w Eurostacie, nie słabych fundamentów. 
Rynki te wymagają osobnej analizy przed podjęciem decyzji inwestycyjnej 
— niska pozycja w rankingu nie jest równoznaczna z niską atrakcyjnością.

---

## 🎯 Rekomendacja inwestycyjna

> Przy średniej europejskiej PIS Score na poziomie 0,60 inwestor długoterminowy powinien koncentrować się na rynkach Europy Środkowo-Wschodniej — szczególnie **Polsce, Litwie i Węgrzech** — gdzie 
> wzrost wartości nieruchomości wyprzedza poziom nasycenia cenowego. 
> Islandia pozostaje jedynym rynkiem spełniającym kryteria Sweet Spot dla 
> obu grup inwestorów — zagranicznych i lokalnych.
> Rynki Europy Zachodniej oferują stabilność makroekonomiczną ale 
> ograniczony potencjał wzrostu kapitału. Inwestor akceptujący niższy 
> zwrot w zamian za bezpieczeństwo może rozważyć Luksemburg (0,68) lub 
> Norwegię (0,66) jako alternatywę defensywną.

---

## ⚠️ Ograniczenia analizy

- Dane wyłącznie z Eurostatu — brak danych transakcyjnych i lokalnych
- Analiza statyczna (2015–2024) — nie jest prognozą przyszłych wyników
- PTI obliczony jako relacja indeksu HPI do zarobków — nie jest 
  klasycznym wskaźnikiem lat pracy
- Brak uwzględnienia podatków, kosztów transakcyjnych i regulacji prawnych
- Kraje z niepełnymi danymi (Macedonia, Czarnogóra, Bośnia) mogą być 
  niedoszacowane w rankingu



## 📬 Kontakt

Projekt stworzony jako część portfolio analitycznego.  
LinkedIn:
