# Temat lekcji: Narzędzia do Przygotowania Danych dla Modeli Językowych

**Cel Lekcji:** Poznanie trzech narzędzi ułatwiających przetwarzanie danych ze stron internetowych przez modele językowe (LLM) poprzez konwersję do przyjaznych formatów (głównie Markdown).

---

## 1. Jina Reader

* **Producent:** Jina AI (firma tworząca różne rozwiązania AI).
* **Główna funkcja:** Pobiera zawartość strony internetowej z podanego adresu URL i zwraca ją w formacie **Markdown**.
    * Przykład użycia: `r.jina.ai/adres-strony.pl`
* **Zalety formatu Markdown:** Bardziej przyjazny dla LLM niż czysty HTML, mniej zbędnych tagów, niższe koszty przetwarzania przez LLM.
* **Dodatkowe funkcje:**
    * **API:** Umożliwia integrację z innymi narzędziami i automatyzacjami (np. Make).
    * **Wyszukiwarka:** Dostępna pod `s.jina.ai`.
    * **Czytanie obrazków (OCR):** Zwraca tekstowy opis obrazka.
    * **Czytanie PDF:** Przetwarza treść z plików PDF dostępnych pod URL.
    * **Konfiguracja API:** Format wyjściowy (Markdown, HTML, tekst), screenshot, timeout, crawl wg. selektora CSS, proxy.
* **Cennik:** Płatne, ale relatywnie tanie (np. 200 USD za 11 mld tokenów).
* **Opinia:** Sprawne, szybkie, niezawodne narzędzie.

---

## 2. FireCrawl

* **Charakterystyka:** Popularne narzędzie.
* **Różnica vs Jina Reader:** Można podać **domenę**, a FireCrawl spróbuje scrawlować całą witrynę (nie tylko pojedynczy URL).
* **Kluczowa funkcja: `LLM Extract`**
    * Umożliwia **ekstrakcję ustrukturyzowanych danych** za pomocą wbudowanego LLM.
    * Zamiast selektorów CSS/XPath, definiuje się **schemat danych** i zadaje pytanie (prompt) modelowi.
    * Model analizuje treść strony (w Markdown) i zwraca dane w żądanej strukturze (np. JSON).
    * Przykład: Sprawdzenie, czy firma (np. Senuto) jest z Polski.
* **Zastosowania:**
    * Masowe sprawdzanie cech firm.
    * Ekstrakcja informacji ze stron o różnej strukturze (np. autorzy blogów, cenniki).
    * Uporządkowanie nieustrukturyzowanych danych.
* **Dostępność:**
    * **Open source:** Kod na GitHubie.
    * **Wersja płatna/przeglądarkowa:** Dostępna komercyjnie.

---

## 3. Crawl for AI

* **Charakterystyka:** Nowsze narzędzie, konkurent dla FireCrawl.
* **Podobieństwa do FireCrawl:** Pobieranie do Markdown, ekstrakcja strukturalna `LLM Extract`.
* **Wyróżnik:** Twierdzi, że jest **znacznie szybszy** od FireCrawl.
* **Dostępność (w momencie nagrania):**
    * **Tylko Open source:** Brak wersji komercyjnej.
    * Uruchamianie: Docker lub biblioteka Pythona (np. w Google Colab).
* **Przykłady użycia (Google Colab):**
    * **Pobranie do Markdown:** Podanie URL -> treść w Markdown (darmowa alternatywa dla Jina Reader w Colab).
    * **Ekstrakcja danych (JSON):** Konfiguracja LLM (np. GPT-4o przez API key), zdefiniowanie promptu i schematu JSON -> narzędzie pobiera treść, wysyła do LLM, zwraca ustrukturyzowane dane (np. cennik).
* **Koncepcja:** "Nowa era crawlowania" z pomocą LLM do strukturyzacji danych.

---

## 4. Przykład Automatyzacji w Make.com (No-Code)

* **Cel:** Pokazanie alternatywy bez kodowania dla podobnych zadań.
* **Przepływ pracy:**
    1.  **Źródło:** Lista URL z Google Sheets.
    2.  **Pobranie treści:** Pętla, wywołanie **API Jina Reader** dla każdego URL.
    3.  **Analiza LLM:** Wysłanie treści do LLM (np. GPT-4o mini) przez moduł OpenAI w Make.
    4.  **Prompt:** Zdefiniowanie zadania (np. "Podaj miasto i opis firmy") i formatu JSON.
    5.  **Parsowanie:** Make parsuje odpowiedź JSON.
    6.  **Zapis:** Aktualizacja Google Sheets o sparsowane dane.
* **Koncepcja: Data Enrichment (Wzbogacanie danych):** Dodawanie wartościowych informacji do istniejących danych.
* **Dostępność:** Gotowy plik automatyzacji Make dostępny w materiałach.

---

**Podsumowanie:**

* Kluczowe narzędzia: **Jina Reader**, **FireCrawl**, **Crawl for AI**.
* Omówiono różnice (URL/domena, szybkość, dostępność).
* Pokazano przykład no-code w **Make.com** dla **Data Enrichment**.
* Narzędzia te są ważne do efektywnego przygotowania danych webowych dla LLM. 