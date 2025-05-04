# Materiały do Tygodnia 2: Przygotowanie do pracy z modelami językowymi

Ten katalog zawiera materiały dodatkowe do lekcji z drugiego tygodnia kursu SEO 3.0, skupiającego się na przygotowaniu do efektywnej pracy z modelami językowymi.

**Uwaga:** Wszystkie datasety używane w kursie, w tym te z tego tygodnia, są również dostępne w centralnym katalogu [`../Datasety`](../Datasety).


## Lekcja: Google Colab - wprowadzenie do narzędzia

W tej lekcji zapoznajemy się z Google Colab - narzędziem, które pozwala na tworzenie i udostępnianie notatników zawierających kod Python, tekst, wykresy i inne elementy. Pokazujemy, jak efektywnie korzystać z tego narzędzia podczas pracy z modelami językowymi i analizy danych dla potrzeb SEO.

### Materiały dodatkowe

*   [Notatnik wprowadzający do Google Colab](https://colab.research.google.com/drive/1bi7TZAq_1Kr0fH5kDKluJSkRu8jRyMpJ?usp=sharing) - ten notatnik służy do nauki podstaw korzystania z narzędzia Google Colab
*   [Przykładowe notatniki Google Colab](https://colab.google/notebooks/) - różne notatniki od Google, które można wykorzystać we własnych projektach.

## Lekcja: Supabase

W tej lekcji poznajemy Supabase - platformę do szybkiego tworzenia backendów dla aplikacji, oferującą bazę danych PostgreSQL (w tym przechowywanie i wyszukiwarnie wektorowe), autentykację i przechowywanie plików. Uczymy się, jak importować dane z plików Excel do Supabase oraz jak wykorzystać tę platformę w projektach SEO do efektywnego zarządzania danymi.

### Materiały dodatkowe

*   [Notatnik do importu danych z Excela do Supabase](https://colab.research.google.com/drive/1NE7AbjT3H81fcsu-uMpv-qXeduWKtPxA?authuser=0#scrollTo=ovOxY2nY5Zdt) - ten notatnik demonstruje proces importowania danych z arkuszy Excel do bazy danych Supabase
*   [Konwersacja z Claude na temat Supabase](https://claude.ai/public/artifacts/cc8b12f9-6927-4998-a59c-c52614cb35dd) - przykładowa konwersacja z asystentem AI używana podczas lekcji
*   **Plik danych**: [`../Datasety/analiza_widocznosci_senuto.com.xlsx`](../Datasety/analiza_widocznosci_senuto.com.xlsx) - raport widoczności dla domeny senuto.com wygenerowany w aplikacji Senuto, używany podczas lekcji do demonstracji importu danych do Supabase
*   Przykładowe zapytanie SQL do analizy struktury tabeli w Supabase - używane podczas lekcji do wygenerowania opisu tabeli, który następnie służy jako kontekst dla modeli językowych przy budowaniu zapytań:

```sql
SELECT 
    column_name, 
    data_type,
    character_maximum_length,
    numeric_precision,
    numeric_scale,
    is_nullable
FROM 
    information_schema.columns
WHERE 
    table_name = 'master_data';
```

## Lekcja: Komunikacja z API modeli językowych

Ta lekcja pokazała, jak komunikować się programowo z API Modeli Językowych przy użyciu Pythona, obejmując podstawy HTTP, formatu JSON, bezpiecznego zarządzania kluczami API oraz praktyczne przykłady interakcji z usługami takimi jak OpenAI czy Google Gemini za pomocą ich bibliotek SDK. Poznaliśmy również kluczowe aspekty pracy z API, takie jak ograniczenia tokenów, oraz zaawansowane techniki, w tym Wywoływanie Funkcji, Ustrukturyzowane Odpowiedzi, narzędzia hostowane (Web Search) i przetwarzanie wsadowe (Batch API), co pozwala na tworzenie bardziej złożonych i efektywnych integracji AI.

### Materiały dodatkowe

*   [Notatnik Colab: Interaktywny przewodnik po API modeli językowych](https://colab.research.google.com/drive/1O8ueKXMOqn0S2yanBHD4XJrBmixVeRAL?usp=sharing) - Praktyczny notatnik pokazujący, jak korzystać z API modeli językowych w Pythonie.
*   **Narzędzia wspomniane w lekcji:**
    *   [OpenRouter](https://openrouter.ai/) - Agregator API różnych modeli językowych.
    *   [Google AI Studio](https://aistudio.google.com/) - Interfejs webowy do modeli Gemini.
    *   [OpenAI Playground](https://platform.openai.com/playground) - Interfejs webowy do modeli GPT.
    *   [Anthropic Console](https://console.anthropic.com/) - Interfejs webowy do modeli Claude.

## Lekcja: Pozyskiwanie danych dla modeli językowych

W tej lekcji skupiamy się na kluczowym aspekcie pracy z modelami językowymi – pozyskiwaniu odpowiednich danych, które posłużą jako kontekst lub materiał do dalszego przetwarzania. Omawiamy różne metody dostarczania danych do modeli, w tym:

*   **Wykorzystanie API zewnętrznych:** Jak integrować się z różnymi usługami za pomocą ich interfejsów programistycznych (API) w celu pobierania aktualnych i specyficznych informacji (np. danych o produktach, statystyk, informacji z baz danych).
*   **Przetwarzanie danych dla modelu:** Jak przygotować i sformatować pozyskane dane (np. z API, plików, baz danych), aby były zrozumiałe i efektywnie wykorzystane przez modele językowe (np. tworzenie odpowiednich struktur, czyszczenie danych).

### Materiały dodatkowe

*   [Notatnik Colab: Ćwiczenia z pozyskiwania danych dla modeli](https://colab.research.google.com/drive/1eI7_Te5IZBOh-hvxFnHJVRNrfgFAAqa7#scrollTo=WMUMmKCBrYXK) - Praktyczne ćwiczenia pokazujące, jak pobierać i przygotowywać dane z różnych źródeł.
*   **Narzędzia (Marketplace API):**
    *   [RapidAPI Hub](https://rapidapi.com/hub) - Duży marketplace z różnorodnymi API.
    *   [Apify](https://apify.com/) - Platforma z gotowymi scraperami (aktorami) i narzędziami do automatyzacji webowej, często dostępnymi przez API.

## Lekcja: Generowanie prostych skryptów python przy wykorzystaniu modeli językowych

W tej lekcji przyjrzymy się, jak efektywnie wykorzystać modele językowe do generowania prostych skryptów w języku Python. Omówimy, które modele sprawdzają się najlepiej w zadaniach programistycznych oraz jak formułować zapytania (prompty), aby uzyskać działający i poprawny kod.

**Najlepsze modele do programowania (stan na Q3 2024):**

*   **Modele Claude (Anthropic):** Szczególnie Claude 3.5 Sonnet i przyszłe wersje (np. zapowiedziany 3.7 Sonnet) wykazują doskonałe zdolności w rozumieniu i generowaniu kodu.
*   **Modele Gemini (Google):** Najnowsze wersje, takie jak Gemini 2.5 Pro, również oferują zaawansowane możliwości w zakresie kodowania.

**Specjalistyczne GPTs do kodowania w Pythonie (OpenAI):**

*   [Python GPT by Nicholas Barker](https://chatgpt.com/g/g-cKXjWStaE-python) - Specjalnie dostosowany GPT do zadań związanych z Pythonem.

**Inne przydatne zasoby:**

*   [Cursor Rules Directory (Python)](https://cursor.directory/rules/python) - Strona zawierająca różne instrukcje systemowe (rules) dla AI, które mogą być pomocne przy programowaniu w Pythonie.

*(Uwaga: W tej lekcji nie korzystamy z dedykowanego notatnika Colab, skupiamy się na interakcji z modelami poprzez ich interfejsy webowe lub API.)*

## Lekcja: AI Crawling

Ta lekcja prezentuje różne narzędzia i techniki pokazujące, w jaki sposób można realizować proces crawlowania (zbierania danych ze stron internetowych) przy wykorzystaniu modeli językowych. Zobaczymy, jak AI może pomóc w ekstrakcji, strukturyzacji i przetwarzaniu informacji z sieci.

### Materiały dodatkowe

*   [Notatnik Colab: Crawl4AI - Wprowadzenie](https://colab.research.google.com/drive/1dgALAwthnxbpaUu_0p5xf08W45JrLvdt?usp=sharing) - Praktyczne wprowadzenie do narzędzia Crawl4AI.
*   **Narzędzia do AI Crawlingu:**
    *   [crawl4ai (GitHub)](https://github.com/unclecode/crawl4ai) - Narzędzie Open Source do crawlowania zoptymalizowane pod kątem modeli językowych.
    *   [Firecrawl](https://www.firecrawl.dev/) - Komercyjne narzędzie do crawlingu oferujące również wersję open source.

*   **Porównanie narzędzi do AI Crawlingu:**

	| Narzędzie                              | Open source                                       | Python SDK | Crawlowanie całej witryny | Wersja no-code | Zalety                                 | Wady                                               |
	| :------------------------------------- | :------------------------------------------------ | :--------: | :-----------------------: | :------------: | :------------------------------------- | :------------------------------------------------- |
	| [Jina reader](https://jina.ai/reader/) |     *✅* (posiada również wersję komercyjną)    |     ❌     |             ❌            |       ❌       | Proste API                             | Mała liczba funkcji                                |
	| [Firecrawl](https://www.firecrawl.dev/) |     *✅* (posiada również wersję komercyjną)    |     ✅     |             ✅            |       ✅       | Mnogość funkcji                        | Wysoki koszt w wersji komercyjnej                  |
	| [Crawl4AI](https://github.com/unclecode/crawl4ai) |     ✅                                            |     ✅     |             ✅            |       ❌       | Szybkość, bezpłatne (open source)      | Trudność wdrożenia                                 |

### Notatniki Colab

Poniższa tabela zawiera linki do notatników Google Colab używanych w tym tygodniu.

| Notatnik                            | Opis                                                                                                                                                    | Link                                                                                         |
| :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------- |
| Wprowadzenie do Google Colab        | Notatnik służący do nauki podstaw korzystania z narzędzia Google Colab, przygotowujący do pracy z pozostałymi materiałami kursu.                        | [Otwórz w Colab](https://colab.research.google.com/drive/1bi7TZAq_1Kr0fH5kDKluJSkRu8jRyMpJ?usp=sharing) |
| Import danych z Excela do Supabase | Notatnik demonstrujący proces importowania danych z arkuszy Excel do bazy danych Supabase. | [Otwórz w Colab](https://colab.research.google.com/drive/1NE7AbjT3H81fcsu-uMpv-qXeduWKtPxA?authuser=0#scrollTo=ovOxY2nY5Zdt) |
| Komunikacja z API modeli językowych | Praktyczny przewodnik po programowej komunikacji z API modeli językowych (np. OpenAI, Gemini) przy użyciu Pythona.                                    | [Otwórz w Colab](https://colab.research.google.com/drive/1O8ueKXMOqn0S2yanBHD4XJrBmixVeRAL?usp=sharing) |
| Pozyskiwanie danych dla modeli      | Ćwiczenia praktyczne z pozyskiwania i przygotowywania danych z różnych źródeł (np. API) dla modeli językowych.                                       | [Otwórz w Colab](https://colab.research.google.com/drive/1eI7_Te5IZBOh-hvxFnHJVRNrfgFAAqa7#scrollTo=WMUMmKCBrYXK) |
| AI Crawling - Wprowadzenie do Crawl4AI | Wprowadzenie do narzędzia Crawl4AI, pokazujące jego możliwości w zakresie AI-driven web crawlingu.                                                | [Otwórz w Colab](https://colab.research.google.com/drive/1dgALAwthnxbpaUu_0p5xf08W45JrLvdt?usp=sharing) |

---

*W przyszłości w tym katalogu pojawią się sekcje dla innych lekcji z Tygodnia 2.*

# Źródła wiedzy

W tej sekcji znajdziesz dodatkowe materiały i źródła, które mogą być pomocne w zgłębianiu tematów poruszanych w tym tygodniu.

*   [Poradnik Google na temat prompt engineeringu](https://www.kaggle.com/whitepaper-prompt-engineering)

## Lekcja: Narzędzia do Przygotowania Danych dla Modeli Językowych

W tej lekcji przyglądamy się narzędziom, które ułatwiają konwersję treści stron internetowych do formatu Markdown, optymalnego dla modeli językowych. Omawiamy Jina Reader, FireCrawl i Crawl for AI, porównując ich funkcjonalności, takie jak obsługa pojedynczych URL vs całych domen, ekstrakcja danych za pomocą LLM (`LLM Extract`) oraz różnice w szybkości i dostępności (open source vs wersje komercyjne). Pokazujemy również przykład automatyzacji procesu wzbogacania danych (Data Enrichment) za pomocą Make.com i API Jina Reader.

*   **Notatka z lekcji:** [./Lekcja_Narzędzia_do_Przygotowania_Danych_LLM/Narzędzia_do_Przygotowania_Danych_LLM.md](./Lekcja_Narzędzia_do_Przygotowania_Danych_LLM/Narzędzia_do_Przygotowania_Danych_LLM.md) - szczegółowe omówienie narzędzi Jina Reader, FireCrawl, Crawl for AI oraz przykład automatyzacji w Make.com.

