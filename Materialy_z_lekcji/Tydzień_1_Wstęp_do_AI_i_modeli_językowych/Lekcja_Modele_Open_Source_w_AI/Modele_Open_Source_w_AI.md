**Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/255)

---

Ta lekcja poświęcona jest modelom sztucznej inteligencji typu Open Source (OS). Dowiemy się, czym są, dlaczego warto się nimi zainteresować, gdzie szukać informacji i samych modeli oraz jak wygląda kwestia infrastruktury potrzebnej do ich uruchomienia – zarówno w chmurze, jak i lokalnie na własnym komputerze. Zrozumiemy też, w jakich sytuacjach modele OS mogą być lepszym wyborem niż ich komercyjni odpowiednicy.

### Dlaczego warto rozważyć modele Open Source?

* **Dostępność:** Wielu liderów rynku (Meta, Google, Mistral, NVIDIA) udostępnia swoje zaawansowane modele **za darmo**. Skoro firmy inwestujące setki milionów dolarów dzielą się technologią, warto z tego korzystać.
* **Alternatywa:** Stanowią ważną alternatywę dla modeli komercyjnych, zwłaszcza w kontekście zmiany charakteru OpenAI z non-profit na for-profit.
* **Szybki rozwój:** Świat OS AI rozwija się niezwykle dynamicznie, często wyprzedzając lub dorównując modelom komercyjnym pod względem jakości i możliwości. Nowe modele pojawiają się niemal co tydzień.
* **Kontrola i bezpieczeństwo:** Dają możliwość uruchomienia na własnej infrastrukturze, co zapewnia pełną kontrolę nad danymi, kluczową przy danych wrażliwych i wymogach GDPR.
* **Optymalizacja kosztów:** Mogą znacząco obniżyć koszty przetwarzania AI, zwłaszcza przy dużych skalach.
* **Dostosowanie:** Możliwość `fine-tuningu` (dostrajania) modeli do specyficznych zadań lub języków.

### Gdzie szukać modeli Open Source i informacji?

Istnieje kilka kluczowych miejsc, gdzie można znaleźć modele OS, śledzić nowości i porównywać ich możliwości:

* **AI Leaderboards:** Strony (np. pierwszy wynik w Google dla "AI leaderboards") prezentujące rankingi modeli AI na podstawie różnych benchmarków (testów logicznych, zadań itp.). Pozwalają zobaczyć, jak modele OS wypadają na tle komercyjnych.
* **Hugging Face (`huggingface.co`):** Centralny hub społeczności OS AI.

    **Modele:** Ogromna baza modeli, sortowana wg trendów, pobrań itp. Znajdziemy tu modele od Mety, Mistrala, Google (np. `Gemma`), ale też specjalistyczne jak `Whisper Large` (audio-na-tekst od OpenAI OS), `Flux` (obrazy od NVIDIA), modele Apple (głębia obrazu) czy polskiego `Bielika`.

    **Datasety:** Zbiory danych, w tym polskie, przydatne do `fine-tuningu`.

    **Infrastruktura:** Możliwość uruchomienia modeli bezpośrednio na Hugging Face lub poprzez zintegrowane chmury (Azure, AWS, Google Cloud).
* **OpenRouter (`openrouter.ai`):**

    **Katalog modeli:** Przeglądarka modeli z opcjami filtrowania, informacjami o gotowych `fine-tuningach` i statystykami popularności (ile tokenów przetwarza dany model w ich infrastrukturze).

    **Infrastruktura:** Działa również jako "router" mocy obliczeniowej (więcej o tym później).
* **Ollama (`ollama.com`):**

    **Oprogramowanie:** Narzędzie do łatwego uruchamiania modeli OS **lokalnie** na własnym komputerze (Windows, macOS, Linux). Zostanie pokazane w kolejnej lekcji.

    **Katalog modeli:** Lista modeli gotowych do instalacji przez Ollama, w tym `Bielik`.

### Kluczowi gracze i ich modele Open Source

* **Meta (Facebook):** Lider w udostępnianiu darmowych, wysokiej jakości modeli.

    **`Llama 3.1`:** Rodzina modeli do tekstu i logiki. Rozmiary od `8B` (miliardów parametrów - do prostych zadań, chatbotów, klasyfikacji) przez `70B` (standardowe zadania) do `405B` (najwyższa jakość generowania treści, porównywalna z GPT-4, radzi sobie po polsku).

    **`Llama 3.2`:** Rodzina modeli **wizyjnych** (widzących), lepszych od niektórych komercyjnych modeli wizyjnych. Zastosowania: skanowanie faktur, odczyt PDF, analiza obrazów.
* **Google:** Udostępnia za darmo modele z rodziny `` `Gemma` ``. Modele `Gemini` są płatne i dostępne w Google Cloud.
* **Mistral AI:** Francuska firma oferująca darmowe, wydajne modele tekstowe (np. `Mistral 7B`, `Mixtral 8x7B`) i wizyjne, które dobrze radzą sobie również po polsku.
* **Polskie inicjatywy:**

    **`Bielik`:** Stworzony przez grupę Spichlerz we współpracy z AGH. **Trenowany głównie na polskich danych**, co może dawać przewagę w zadaniach związanych z językiem polskim mimo mniejszego rozmiaru (11B parametrów) w porównaniu do globalnych gigantów. Dostępny na Hugging Face i Ollama. Aktywna społeczność na Discordzie/LinkedIn.

    **`PluM`:** Projekt polskich uczelni (Politechnika Wrocławska i Poznańska) finansowany z dużego grantu. Ma na celu stworzenie dużego polskiego modelu językowego. Projekt w toku.

### Infrastruktura dla modeli Open Source

W przeciwieństwie do modeli komercyjnych (jak GPT-4), które działają na infrastrukturze dostawcy, modele OS wymagają zapewnienia im mocy obliczeniowej. Masz kilka opcji:

* **Specjalistyczni dostawcy AI:** Firmy oferujące dostęp do mocy obliczeniowej zoptymalizowanej pod AI, często z preinstalowanymi popularnymi modelami OS.

    **`AnyScale`:** Popularna platforma, używana przez duże firmy. Oferuje głównie modele Mety, `fine-tuning`, deployment, playground.

    **`Together AI`:** Szeroka oferta modeli OS (Llama, Mistral, Snowflake, Stable Diffusion), playground, konkurencyjne ceny.

    **`Perplexity API`:** Dostęp do modeli używanych przez wyszukiwarkę Perplexity (głównie `fine-tuningi` Lamy). Playground dostępny.

    **`Grok Platform`:** Reklamowana jako **najszybsza** infrastruktura na świecie. Idealna do aplikacji wymagających niskich opóźnień (np. chatboty głosowe). Oferuje modele Mety, Mistrala, Whisper. Playground dostępny.
* **Routery Infrastruktury:**

    **`OpenRouter`:** Działa jak inteligentny pośrednik. Kieruje Twoje zapytania do różnych dostawców infrastruktury (np. `Deep Infra`, `Together AI`, `Hyperbolic`) w zależności od tego, gdzie dany model jest aktualnie dostępny **najtaniej** i ma wolne moce obliczeniowe. Upraszcza wybór i optymalizuje koszty.
* **Prywatna / Dedykowana Infrastruktura:**

    **`RunPod`:** Oferuje wynajem dedykowanych maszyn (GPU) lub serverless endpoints do uruchamiania modeli w **całkowicie prywatnym** środowisku. Maksymalne bezpieczeństwo danych.
* **Lokalne Uruchomienie:**

    **`Ollama`:** Oprogramowanie pozwalające zainstalować i uruchomić modele OS bezpośrednio na **Twoim komputerze** (MacBook, PC). Zapewnia 100% prywatności danych.

### Kiedy stosować modele Open Source? Główne zastosowania

Modele OS są szczególnie wartościowe w następujących scenariuszach:

**Operacje Backendowe:** Zadania niewidoczne dla użytkownika końcowego, np. kategoryzacja słów kluczowych, przypisywanie produktów do kategorii, klasyfikacja obrazów (np. kolor sukienki).

**Przygotowanie Danych dla Modeli Komercyjnych:** Wykonywanie wielu pośrednich kroków przetwarzania danych w złożonym workflow generowania treści, zanim finalny tekst zostanie wygenerowany przez najlepszy model komercyjny (np. GPT-4.5).

**Optymalizacja Kosztów:** Gdy koszty korzystania z API komercyjnych stają się zbyt wysokie, zwłaszcza przy dużej skali.

**Przetwarzanie na Ogromną Skalę:** Obsługa milionów rekordów (np. 100 mln słów kluczowych Senuto) lub tysięcy produktów.

**Bezpieczeństwo Danych:** Gdy absolutnie nie możesz pozwolić sobie na wysyłanie danych (np. wrażliwych, biznesowych) do zewnętrznych dostawców.

**`Fine-Tuning`:** Dostosowanie modelu do specyficznego zadania (np. analiza prawna) lub poprawa jego działania w konkretnym języku (np. polskim).

**Przyszłość: Destylacja Modeli:** Tworzenie małych, wyspecjalizowanych i bardzo wydajnych modeli na bazie dużych modeli OS, możliwych do uruchomienia nawet na urządzeniach mobilnych (trend, który ma nadejść).

### Podsumowanie i następne kroki

Modele Open Source stanowią potężną i dynamicznie rozwijającą się część ekosystemu AI. Oferują elastyczność, kontrolę, możliwość optymalizacji kosztów i dostosowania, co czyni je atrakcyjną alternatywą lub uzupełnieniem dla modeli komercyjnych. Kluczowe jest zrozumienie dostępnych modeli, platform do ich wyszukiwania oraz opcji infrastrukturalnych.

W kolejnej lekcji przejdziemy do praktyki: pokażę, jak zainstalować i uruchomić model językowy OS lokalnie na Twoim komputerze za pomocą Ollama oraz jak zrobić to samo na zdalnej maszynie w chmurze (np. używając RunPod). 