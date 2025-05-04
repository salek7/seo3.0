**Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/258)

---

**Przydatne linki:**

* **ChatGPT:** [https://chat.openai.com/](https://chat.openai.com/) (Platforma do tworzenia i używania GPTs)
* **Senuto:** [https://www.senuto.com/](https://www.senuto.com/) (Wspomniane jako przykład integracji API)

---

## Wprowadzenie do GPTs: Twój spersonalizowany ChatGPT

Ta notatka wyjaśnia, czym są GPTs (niestandardowe wersje ChatGPT) i jak możesz stworzyć własne, aby zautomatyzować powtarzalne zadania lub dostosować działanie czatu do konkretnych potrzeb. Dowiesz się, jak przeglądać istniejące GPTs i jak krok po kroku skonfigurować własny model.

GPTs pozwalają skonfigurować ChatGPT do wykonywania specyficznych zadań, takich jak:

* Generowanie opisów `meta title` i `meta description`.
* Tworzenie wpisów na LinkedIn lub inne media społecznościowe.
* Humanizowanie (nadawanie bardziej naturalnego brzmienia) tekstów.
* Analiza danych z zewnętrznych źródeł poprzez integrację API (np. pobieranie danych o widoczności strony z Senuto).

## Krok 1: Odkrywanie istniejących GPTs

Zanim stworzysz własny model, możesz przejrzeć gotowe rozwiązania dostępne w "sklepie" GPTs.

1.  W głównym widoku ChatGPT kliknij **Explore GPTs** (Odkryj modele GPT) w lewym panelu.
2.  Przeglądaj dostępne kategorie (np. Pisanie, Badania, Edukacja) lub użyj wyszukiwarki, aby znaleźć GPTs dopasowane do Twoich potrzeb (np. `LinkedIn Post`, `SEO Analyzer`, `WordPress Helper`).
3.  Wybierz interesujący Cię GPTs (np. `Viral LinkedIn Post Formatter`, `WordPress Wizard`).
4.  Kliknij **Start chat** (Rozpocznij czat), aby zacząć używać wybranego modelu. Będziesz teraz w specjalnym interfejsie tego konkretnego GPTs, który jest już skonfigurowany do określonego zadania.

**Przykład użycia gotowego GPTs:** W czacie z `Viral LinkedIn Post Formatter` możesz wpisać polecenie: "Napisz mi wpis na LinkedIn na temat szkolenia AI Akademii", a model wygeneruje treść zgodnie ze swoją konfiguracją (np. używając emoji i hashtagów, w odpowiednim formacie).

## Krok 2: Tworzenie własnego GPTs

Jeśli nie znalazłeś gotowego rozwiązania lub potrzebujesz czegoś specyficznego, możesz łatwo stworzyć własny GPTs.

1.  Wróć do głównego widoku ChatGPT.
2.  Kliknij **Explore GPTs**.
3.  W prawym górnym rogu kliknij **Create** (Utwórz).
4.  Otworzy się interfejs tworzenia GPTs z dwoma zakładkami: **Create** (gdzie możesz konfigurować model poprzez rozmowę z asystentem) i **Configure** (gdzie ręcznie wprowadzasz ustawienia). Skupimy się na zakładce **Configure**.

## Krok 3: Konfiguracja własnego GPTs (zakładka "Configure")

W tej sekcji określasz, jak ma działać Twój GPTs.

* **Name (Nazwa):** Wpisz nazwę dla swojego GPTs, np. `Generator postów na LinkedIn`.
* **Description (Opis):** Dodaj krótki opis wyjaśniający, co robi Twój GPTs, np. `Generuje krótkie, angażujące wpisy na LinkedIn z emoji i hashtagami`.
* **Instructions (Instrukcje):** To najważniejsza część. Tutaj definiujesz zadanie dla modelu. Podaj jasne wytyczne.
    * **Przykład:** "Twoim zadaniem jest napisać viralowy wpis na LinkedIn. Wpis powinien mieć maksymalnie 300 znaków. Użyj odpowiednich emoji. Dodaj 3-5 trafnych hashtagów na końcu."
    * *(W przyszłych lekcjach dowiesz się więcej o zaawansowanych technikach tworzenia instrukcji - prompt engineeringu).*
* **Conversation starters (Przykładowe rozpoczęcia rozmowy):** Możesz dodać przykładowe polecenia, które użytkownik zobaczy na początku czatu, np. "Napisz post o nowym produkcie".
* **Knowledge (Wiedza):** Możesz tutaj wgrać pliki (np. PDF, DOCX), które będą stanowiły bazę wiedzy dla Twojego GPTs. Model będzie korzystał z informacji zawartych w tych plikach podczas generowania odpowiedzi. Jest to przydatne, jeśli chcesz, aby GPTs opierał się na firmowej dokumentacji, specyfikacjach produktów, treści książki itp. Technika ta nazywa się RAG (Retrieval Augmented Generation).
* **Capabilities (Zdolności):** Zaznacz, czy Twój GPTs ma mieć dostęp do:
    * `Web Browse` (Przeglądanie sieci)
    * `DALL·E Image Generation` (Generowanie obrazów)
    * `Code Interpreter` (Analiza danych, uruchamianie kodu Python)
* **Actions (Działania):** W tej zaawansowanej sekcji możesz skonfigurować połączenia z zewnętrznymi API, aby Twój GPTs mógł pobierać lub wysyłać dane do innych serwisów (np. sprawdzić widoczność w Senuto, pobrać dane z systemu CRM). Kliknij **Create new action** (Utwórz nowe działanie), aby dodać integrację.

## Krok 4: Zapisywanie i udostępnianie GPTs

Po skonfigurowaniu modelu kliknij **Save** (Zapisz) lub **Update** (Aktualizuj) w prawym górnym rogu. Pojawi się okno z opcjami udostępniania:

* **Only me (Tylko ja):** GPTs będzie widoczny i dostępny tylko dla Ciebie.
* **Anyone with a link (Każdy z linkiem):** Możesz udostępnić GPTs innym osobom (np. współpracownikom, znajomym), wysyłając im bezpośredni link.
* **Everyone (Wszyscy):** Twój GPTs zostanie opublikowany w GPT Store i będzie publicznie dostępny (wymaga dodatkowej weryfikacji profilu).

Wybierz odpowiednią opcję i potwierdź.

## Krok 5: Używanie stworzonego GPTs

Po zapisaniu zostaniesz przeniesiony do interfejsu czatu Twojego nowego GPTs. Możesz teraz z niego korzystać, wpisując polecenia zgodne z instrukcjami, które zdefiniowałeś.

**Przykład:** Jeśli stworzyłeś `Generator postów na LinkedIn`, wpisz: "Napisz wpis na LinkedIn o szkoleniu AI". Model powinien wygenerować odpowiedź zgodną z Twoimi wytycznymi (długość, emoji, hashtagi).

## Podsumowanie

GPTs to potężne narzędzie do personalizacji ChatGPT pod kątem konkretnych, powtarzalnych zadań. Pozwalają zaoszczędzić czas i zapewnić spójność wyników. Możesz korzystać z gotowych modeli z marketplace'u lub łatwo stworzyć własne, dopasowane do Twoich unikalnych potrzeb, a nawet zintegrować je z zewnętrznymi narzędziami poprzez API. Eksperymentuj z tworzeniem własnych GPTs, aby usprawnić swoją pracę. 