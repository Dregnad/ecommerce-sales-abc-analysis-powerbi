# 📊 E-Commerce Sales Analytics Dashboard | ABC & Pareto Analysis (Power BI)

## 📌 Project Overview

Projekt przedstawia kompleksową analizę sprzedaży sklepu internetowego z wykorzystaniem metody **ABC & Pareto Analysis** opartej na zasadzie Pareto (80/20).

Celem projektu było zidentyfikowanie produktów mających największy wpływ na przychody firmy oraz stworzenie interaktywnego dashboardu wspierającego decyzje biznesowe dotyczące:

- zarządzania asortymentem,
- priorytetyzacji produktów,
- optymalizacji zapasów,
- analizy trendów sprzedaży.

Projekt obejmuje pełny proces analityczny:
- przygotowanie danych transakcyjnych,
- kalkulację metryk sprzedażowych,
- segmentację produktów metodą ABC,
- analizę geograficzną i czasową,
- stworzenie raportu menedżerskiego w Power BI.

---

# 🎯 Business Questions

W projekcie odpowiedziano na następujące pytania biznesowe:

- Które produkty generują największą część przychodów?
- Jaki udział asortymentu odpowiada za większość sprzedaży?
- Jak wygląda struktura sprzedaży według klas ABC?
- Które kraje generują największy obrót?
- Jak zmieniała się sprzedaż w czasie?
- Które segmenty produktów wymagają dalszej optymalizacji?

---

# 📂 Dataset

W projekcie wykorzystano publiczny zbiór danych:
🔗 **Kaggle:** [An Online Shop Business](https://www.kaggle.com/datasets/gabrielramos87/an-online-shop-business)

Zbiór zawiera informacje dotyczące:
- transakcji sprzedażowych,
- produktów,
- ilości zakupionych sztuk,
- cen jednostkowych,
- dat sprzedaży,
- lokalizacji klientów.

> 💡 **Nota techniczna:** Oryginalny plik został zmniejszony do **50 000 wierszy** ze względu na limity rozmiaru. Kolumny `Przychód`, `% skumulowany` oraz `Klasa ABC` zostały wcześniej wyliczone na pełnej bazie danych i wklejone jako stałe wartości, co zapewnia pełną spójność z wynikami na wykresach.

---

# 🛠️ Tools & Technologies

## Excel
Wykorzystano do przygotowania danych:
- Obliczenie wartości sprzedaży:
  `Total Revenue = Quantity × Unit Price`
- Agregacja sprzedaży według produktów oraz sortowanie malejąco.
- Obliczenie udziału procentowego i wartości skumulowanej w celu klasyfikacji ABC.

### Reguły klasyfikacji:

| Klasa | Charakterystyka |
|---|---|
| **A** | Produkty kluczowe, generujące do 80% skumulowanego przychodu |
| **B** | Produkty o średnim znaczeniu, generujące kolejne 15% przychodu |
| **C** | Produkty o niskim wpływie (ostatnie 5%), generujące tzw. długi ogon asortymentowy |

---

# 📊 Power BI Dashboard

Raport został podzielony na trzy główne sekcje wspierające analizę sprzedaży i podejmowanie decyzji biznesowych.

### 1. Executive Summary – ABC Analysis
Dashboard przedstawia kluczowe wskaźniki efektywności (KPI), udział klas ABC oraz rozkład przychodów według segmentów.

![Executive Summary](Podsumowanie%20ABC.png)

**Najważniejsze obserwacje:**
- Klasa A odpowiada za około **80% całkowitego przychodu**, obejmując około **25% unikalnych produktów**.
- Klasa C obejmuje największą liczbę produktów pod względem liczby unikalnych pozycji asortymentowych, jednak odpowiada za relatywnie niewielką część całkowitego przychodu.

> **Wniosek:** Firma powinna koncentrować działania sprzedażowe, marketingowe i logistyczne przede wszystkim na produktach klasy A, jednocześnie analizując zasadność utrzymywania produktów klasy C.

---

### 2. Market & Sales Trends
Analiza koncentruje się na strukturze geograficznej rynków oraz dynamice sprzedaży w czasie (ujęcie roczne).

![Market & Sales Trends](Rynki%20i%20Trendy.png)

**Najważniejsze obserwacje:**
- Najwyższą średnią wartość transakcji generują rynki skandynawskie oraz azjatyckie (m.in. **Sweden, Netherlands, Japan**).
- Skokowy wzrost sprzedaży pomiędzy 2018 a 2019 rokiem jest w największym stopniu napędzany przez rozwój produktów z klasy A.
- Analiza trendów pozwala identyfikować okresy wzrostu i spadku sprzedaży.

---

### 3. Product & Market Drilldown
Tabela szczegółowa przygotowana jako operacyjne narzędzie wspierające decyzje zakupowe i optymalizację stanów magazynowych.

![Product & Market Drilldown](Tabela%20Szczegółowa.png)

---

# 📈 Key Business Insights

1. **Efekt Pareto w praktyce:** Około 80% przychodów firmy generowane jest przez produkty klasy A, które stanowią kluczowy segment sprzedażowy.
2. **Optymalizacja asortymentu:** Produkty klasy C wymagają dodatkowej analizy pod kątem rotacji, kosztów magazynowania oraz zasadności utrzymywania ich w ofercie.
3. **Priorytetyzacja działań:** Produkty klasy A powinny otrzymywać najwyższy priorytet w zarządzaniu zapasami, działaniach marketingowych i planowaniu sprzedaży.

---

# 📁 Project Structure

```text
📂 Ecommerce-Sales-Analytics-Dashboard
│── 📂 Data
│   └── Sales Transaction.xlsx
│── 📂 Dashboard
│   └── ecommerce-sales-abc-analysis-powerbi.pbix
│── 📂 Screenshots
│   ├── Podsumowanie ABC.png
│   ├── Rynki i Trendy.png
│   └── Tabela Szczegółowa.png
└── README.md
