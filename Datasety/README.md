# Centralny Katalog Datasetów Kursu SEO 3.0

Ten katalog gromadzi wszystkie zestawy danych (datasety) wykorzystywane w różnych lekcjach kursu SEO 3.0.

## Tabela Datasetów

| Nazwa pliku | Opis | Tydzień | Lekcja | Link |
|:------------|:-----|:--------|:-------|:-----|
| `processed_keywords.zip` | Archiwum zip zawierające pliki JSON z głównymi słowami kluczowymi i powiązanymi frazami | 3 | Automatyczny prompt engineering | [Pobierz](processed_keywords.zip) |
| `analiza_widocznosci_senuto.com.xlsx` | Raport widoczności dla domeny senuto.com z aplikacji Senuto | 2 | Supabase | [Pobierz](analiza_widocznosci_senuto.com.xlsx) |

## Dostępne Datasety

*   **`processed_keywords.zip`**
    *   **Opis:** Archiwum zip zawierające pliki JSON. Każdy plik reprezentuje jedno główne słowo kluczowe i listę powiązanych z nim fraz.
    *   **Lekcja:** Tydzień 3 - Automatyczny prompt engineering.
    *   **Przeznaczenie:** Automatyczne generowanie promptów do modeli językowych
    *   **Format danych (`.json` wewnątrz archiwum):**
        ```json
        {
          "main_keyword": "Przykładowe Główne Słowo Kluczowe",
          "keyword_list": [
            "Powiązana fraza 1",
            "Powiązana fraza 2",
            "..."
          ]
        }
        ```
        *Przykład (`Audyt SEO`):*
        ```json
        {
          "main_keyword": "Audyt SEO",
          "keyword_list": [
            "Bezpłatny audyt SEO",
            "bezpłatny audyt",
            "Darmowy audyt SEO",
            "Darmowy audyt online",
            "przeprowadzić audyt seo",
            "audyt seo strony",
            // ... (pełna lista w pliku)
          ]
        }
        ```

*   **`analiza_widocznosci_senuto.com.xlsx`**
    *   **Opis:** Raport widoczności dla domeny senuto.com wygenerowany w aplikacji Senuto.
    *   **Lekcja:** Tydzień 2 - Supabase.
    *   **Przeznaczenie:** Demonstracja importu danych z Excela do bazy danych Supabase i przykład struktury danych używanej w analizie SEO.
    *   **Format danych:** Arkusz Excel zawierający dane o widoczności domeny w wynikach wyszukiwania Google, w tym informacje o słowach kluczowych, ich pozycjach, miesięcznym wolumenie wyszukiwań i innych metrykach SEO.

---

*W przyszłości w tym katalogu będą dodawane kolejne datasety wraz z ich opisami.* 