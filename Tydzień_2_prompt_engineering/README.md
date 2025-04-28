# Materiały do lekcji "Automatyczny prompt engineering"

Ten katalog zawiera zestawy danych (datasety) wykorzystywane w lekcji dotyczącej automatycznego generowania promptów (Automatyczny prompt engineering).

## Dostępne Zestawy Danych

*   **`processed_keywords.zip`**: Archiwum zip zawierające pliki JSON. Każdy plik reprezentuje jedno główne słowo kluczowe i listę powiązanych z nim fraz. Dane te są przeznaczone do ćwiczeń związanych z analizą i grupowaniem słów kluczowych.

    **Format danych (`.json` wewnątrz archiwum):**
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
        "Audyt SEO online",
        "audyt strony",
        "audyt seo profesjonalistom",
        "audyt SEO swojej strony",
        "analiza strony internetowej",
        "zaawansowany audyt SEO",
        "Wyniki audytu SEO",
        "potrzebujesz audytu seo",
        "zrobić audyt seo",
        "Darmowy audyt SEO z SEMPIRE",
        "wyniki audytu",
        "przeprowadzenie darmowego audytu",
        "kompleksowy audyt seo",
        "optymalizacja SEO",
        "audyt seo przeprowadzony",
        "optymalizacja strony",
        "Zalety audytu SEO",
        "dzięki audytowi seo",
        "audyt seo zawiera",
        "audyt seo pozwala",
        "analiza seo",
        "ocena strony internetowej",
        "Ocena zdrowia SEO",
        "Raport audytu SEO",
        "analiza techniczna strony",
        "optymalizacja strony internetowej",
        "techniczna analiza SEO",
        "seo witryny internetowej",
        "audyt seo wymaga",
        "pozycjonowanie strony internetowej",
        "Analiza linków wewnętrznych",
        "działania SEO",
        "automatyczny audyt seo",
        "analiza seo widoczności",
        "strategia SEO",
        "warto przeprowadzić audyt",
        "Zalety audytu SEO WeNet",
        "analizy słów kluczowych",
        "struktura strony",
        "Słowa kluczowe",
        "Analiza ruchu organicznego",
        "szybkość ładowania strony",
        "widoczność strony internetowej",
        "organiczne wyniki wyszukiwania",
        "treść strony",
        "wyszukiwarce google",
        "wyszukiwarek internetowych",
        "właściciel strony",
        "właściciel strony internetowej"
      ]
    }
    ```

W przyszłości w tym katalogu mogą pojawić się inne zestawy danych związane z tą lekcją. 