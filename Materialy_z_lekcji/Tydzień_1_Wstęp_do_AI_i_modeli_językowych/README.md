# Materiały do Tygodnia 1: Wstęp do AI i modeli językowych

Ten katalog zawiera materiały dodatkowe do lekcji z pierwszego tygodnia kursu SEO 3.0, wprowadzającego w świat sztucznej inteligencji i modeli językowych.

**Uwaga:** Wszystkie datasety używane w kursie są dostępne w centralnym katalogu [`../Datasety`](../Datasety).

---

## Lekcja: Historia modeli językowych

W tej lekcji przyglądamy się ewolucji technologii rozumienia języka naturalnego, od wczesnych koncepcji jak Word2Vec, przez Sequence-to-Sequence, aż po rewolucyjną architekturę Transformerów. Analizujemy, jak działają Transformery (tokenizacja, embedding, self-attention) na przykładzie materiałów Financial Times i omawiamy kluczowe momenty w rozwoju AI, w tym pojawienie się BERT i GPT. Lekcja zawiera również aktualizację dotyczącą gwałtownego przyspieszenia w rozwoju AI, multimodalności i przyszłości związanej z agentami AI i robotyką.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/252)
*   **Notatka z lekcji:** [./L01_Historia_Modeli_Jezykowych/Historia_Modeli_Jezykowych.md](./L01_Historia_Modeli_Jezykowych/Historia_Modeli_Jezykowych.md) - Szczegółowy przewodnik po historii modeli językowych, działaniu Transformerów i najnowszych trendach w AI.
*   **Transkrypcja:** [./L01_Historia_Modeli_Jezykowych/Historia_Modeli_Jezykowych.txt](./L01_Historia_Modeli_Jezykowych/Historia_Modeli_Jezykowych.txt) - Pełna transkrypcja lekcji.

---

## Lekcja: Zrozumieć Modele Językowe

*   **Cel:** Wyjaśnienie kluczowych pojęć związanych z LLM, ich działania, ograniczeń (halucynacje, bias) i potencjału. Omówienie benchmarków i sposobu oceny modeli.
*   **Opis:** Modele językowe to nie magia, a technologia oparta na danych i uczeniu głębokim. Ta lekcja demistyfikuje LLM, pokazując jak powstają (dane, trening), jak działają (przewidywanie tokenów, planowanie), jakie mają wyzwania (halucynacje, stronniczość, bezpieczeństwo danych, kontekst) i jak je klasyfikujemy (małe/duże, komercyjne/open-source, czat/instruct, wizyjne, reasoningowe). Dowiesz się, jak interpretować benchmarki (np. MMLU, HumanEval, HellaSwag, Arena Score, Humanity Last Exam) i jak ocenić, który model wybrać do konkretnego zadania. Zrozumiesz też, dlaczego karmienie modeli danymi jest kluczowe dla redukcji halucynacji.
*   **Materiały:**
    *   Notatki: [./L02_Zrozumiec_Modele_Jezykowe/Zrozumiec_Modele_Jezykowe.md](./L02_Zrozumiec_Modele_Jezykowe/Zrozumiec_Modele_Jezykowe.md)
    *   Transkrypcja: [./L02_Zrozumiec_Modele_Jezykowe/Czym_sa_modele_jezykowe.txt](./L02_Zrozumiec_Modele_Jezykowe/Czym_sa_modele_jezykowe.txt)

---

## Lekcja: Podstawowe narzędzia AI

W tej lekcji dokonujemy przeglądu kluczowych narzędzi AI dostępnych na rynku (stan na kwiecień 2025). Omawiamy funkcjonalności, modele językowe, unikalne cechy i typowe zastosowania popularnych platform, aby ułatwić wybór odpowiedniego narzędzia do konkretnych zadań, szczególnie w marketingu i SEO.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/254)
*   **Notatka z lekcji:** [./L03_Podstawowe_Narzedzia_AI/Podstawowe_Narzedzia_AI.md](./L03_Podstawowe_Narzedzia_AI/Podstawowe_Narzedzia_AI.md) - Szczegółowy opis i porównanie narzędzi Chat GPT, Perplexity, Grok, Claude, Gemini i Google AI Studio.
*   **Transkrypcja:** [./L03_Podstawowe_Narzedzia_AI/Podstawowe_Narzedzia_AI.txt](./L03_Podstawowe_Narzedzia_AI/Podstawowe_Narzedzia_AI.txt) - Pełna transkrypcja lekcji.

### Omawiane narzędzia:

*   [Chat GPT (OpenAI)](https://chat.openai.com/)
*   [Perplexity](https://www.perplexity.ai/)
*   [Grok (xAI)](https://grok.com/)
*   [Claude (Anthropic)](https://claude.ai/)
*   [Gemini (Google)](https://gemini.google.com/)
*   [Google AI Studio](https://aistudio.google.com/)

### Tabela porównawcza (stan na kwiecień 2025 wg lekcji):

| Narzędzie         | Dostawca        | Główny Cel / Zastosowanie               | Kluczowe / Unikalne Funkcje                                                                                                | Dostępne Modele (przykłady)                 | Link                                       |
| :---------------- | :-------------- | :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------- | :----------------------------------------- |
| **Chat GPT** | OpenAI          | Ogólne zastosowania, kod, treść        | `Canvas` (edytor), GPTs, Biblioteka, `/`-komendy, Projekty (proste)                                                         | `GPT-4o`, `GPT-4.5`, `O3`, `O4 mini`         | [chat.openai.com](https://chat.openai.com/) |
| **Perplexity** | Perplexity AI   | Wyszukiwanie i synteza aktualnej wiedzy | Cytowanie źródeł, API, Automatyczny tryb Pro, Elastyczny wybór modeli (różni dostawcy)                                       | Różni dostawcy (OpenAI, Google, Anthropic) | [perplexity.ai](https://www.perplexity.ai/) |
| **Grok** | X / xAI         | Programowanie, research, kontekst X    | `Workspaces` (separacja kontekstu), `Thinking`, Integracja z X, Dostęp przez `grok.com`                                    | `Grok`                                     | [grok.com](https://grok.com/)               |
| **Claude** | Anthropic       | Programowanie, praca projektowa        | `Artifacts` (kod live), `Projekty` (separacja + instrukcje), Integracja GitHub/Drive, Własny styl (Tone of Voice)             | `Claude 3.7 Sonnet`                        | [claude.ai](https://claude.ai/)             |
| **Gemini** | Google          | Zastosowania ogólne, integracja Google | Dostęp do `Gemini 2.5 Pro`, `Canvas`, Integracja z GSuite (wymaga zgód admina)                                              | `Gemini 2.5 Pro Experimental`              | [gemini.google.com](https://gemini.google.com/) |
| **Google AI Studio** | Google          | Zaawansowana konfiguracja, deweloperka | `Grounding` (Google Search), Kontrola parametrów (temperatura), Generowanie wideo (`Veo 2`), Wybór modeli (`Gemma`, `Gemini`) | `Gemma`, `Gemini 1.5/2.5 Pro`, `Veo 2`     | [aistudio.google.com](https://aistudio.google.com/) |

---

## Lekcja: Pozyskiwanie wiedzy i Deep Research

Ta lekcja skupia się na technikach zdobywania aktualnej wiedzy za pomocą narzędzi AI, ze szczególnym uwzględnieniem funkcji `Deep Research` / `Deep Search`. Omawiamy problem nieaktualnej wiedzy modeli LLM i pokazujemy, jak proste wyszukiwanie (np. w Perplexity) oraz zaawansowane funkcje głębokiego badania (w Chat GPT, Perplexity, Grok, Gemini) pozwalają budować kompleksową, opartą na wielu źródłach bazę wiedzy. Porównujemy działanie tych funkcji w różnych narzędziach i przedstawiamy praktyczny workflow wykorzystania wyników deep research do tworzenia i optymalizacji treści.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/256)
*   **Notatka z lekcji:** [./L04_Pozyskiwanie_Wiedzy_Deep_Research/Pozyskiwanie_Wiedzy_Deep_Research.md](./L04_Pozyskiwanie_Wiedzy_Deep_Research/Pozyskiwanie_Wiedzy_Deep_Research.md) - Szczegółowe omówienie i porównanie funkcji Deep Research/Search w popularnych narzędziach AI.
*   **Transkrypcja:** [./L04_Pozyskiwanie_Wiedzy_Deep_Research/Pozyskiwanie_wiedzy_i_deep_research.txt](./L04_Pozyskiwanie_Wiedzy_Deep_Research/Pozyskiwanie_wiedzy_i_deep_research.txt) - Pełna transkrypcja lekcji.

### Porównanie funkcji Deep Search / Research (wg lekcji):

| Narzędzie         | Nazwa Funkcji                 | Kluczowe Cechy / Proces                                     | Unikalne Dane / Możliwości          | Liczba Źródeł (Przykład "kortyzol") | Rekomendacja Prelegenta (dla Deep Research) |
| :---------------- | :---------------------------- | :---------------------------------------------------------- | :---------------------------------- | :---------------------------------- | :------------------------------------------ |
| **Chat GPT** | `Zbadaj głęboko`              | Query expansion, głęboki research (prawdopodobnie Bing)     | -                                   | ? (demo nie zadziałało)             | -                                           |
| **Perplexity** | `Badania` / `Zaaw. analiza` | Widoczny proces query expansion, iteracyjne wyszukiwanie    | Dobra wizualizacja procesu          | 39                                  | Dobry punkt startowy                     |
| **Grok** | `Deep Search`/`Deeper Search` | Query expansion, iteracyjne wyszukiwanie                    | Dostęp do danych z platformy X       | 32                                  | Dobry, zwłaszcza dla tematów z X        |
| **Gemini** | `Deep Research`               | Najbardziej rozbudowany proces, głębokie wnioskowanie (reasoning) | Największa liczba analizowanych źródeł | >73 (proces trwał)                 | **Najlepszy** pod względem kompleksowości  |

---

## Lekcja: Modele Open Source w AI: Przegląd, Zastosowania i Infrastruktura

Ta lekcja wprowadza w świat modeli AI typu Open Source (OS). Omawiamy, dlaczego warto się nimi interesować (dostępność, kontrola danych, koszty, rozwój), gdzie szukać modeli i informacji (AI Leaderboards, Hugging Face, OpenRouter, Ollama) oraz przedstawiamy kluczowych graczy (Meta, Google, Mistral, polskie inicjatywy jak Bielik i PluM). Analizujemy różne opcje infrastrukturalne do uruchamiania modeli OS – od specjalistycznych dostawców AI (AnyScale, Together AI, Perplexity API, Grok Platform), przez routery (OpenRouter) i prywatne chmury (RunPod), aż po lokalne uruchomienie na własnym komputerze (Ollama). Wskazujemy typowe zastosowania modeli OS (backend, optymalizacja kosztów, bezpieczeństwo danych, fine-tuning) i zapowiadamy przyszłe trendy (destylacja modeli).

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/255)
*   **Notatka z lekcji:** [./L05_Modele_Open_Source_w_AI/Modele_Open_Source_w_AI.md](./L05_Modele_Open_Source_w_AI/Modele_Open_Source_w_AI.md) - Szczegółowy przegląd świata modeli AI Open Source, platform, infrastruktury i zastosowań.
*   **Transkrypcja:** [Modele Open Source w AI - Transkrypcja](./L05_Modele_Open_Source_w_AI/Modele_Open_Source_w_AI_Transkrypcja.md)

### Omawiane platformy i narzędzia OS:

*   **Gdzie szukać modeli/informacji:**
    *   AI Leaderboards (wyszukaj w Google)
    *   [Hugging Face](https://huggingface.co/)
    *   [OpenRouter](https://openrouter.ai/)
    *   [Ollama](https://ollama.com/)
*   **Dostawcy infrastruktury AI:**
    *   AnyScale
    *   Together AI
    *   [Perplexity API](https://www.perplexity.ai/) (część platformy Perplexity)
    *   [Grok Platform](https://grok.com/)
    *   RunPod
*   **Kluczowi gracze OS (modele):**
    *   Meta (`Llama 3.1`, `Llama 3.2`)
    *   Google (`Gemma`)
    *   Mistral AI (`Mistral`, `Mixtral`)
    *   Polska (`Bielik`, `PluM` - w trakcie)

### Lekcja: Modele Open Source w AI

- **Notatki:** [Modele Open Source w AI](./L05_Modele_Open_Source_w_AI/Modele_Open_Source_w_AI.md)
- **Transkrypcja:** [Modele Open Source w AI - Transkrypcja](./L05_Modele_Open_Source_w_AI/Modele_Open_Source_w_AI_Transkrypcja.md)
- **Opis:** Omówienie świata modeli open source, liderów rynku (Meta, Mistral), źródeł wiedzy (leaderboardy, HuggingFace, OpenRouter), modeli polskich (Bielik, Plum) oraz infrastruktur alternatywnych (AnyScale, TogetherAI, Perplexity, Grok, RunPod) i korzyści z ich stosowania (optymalizacja kosztów, bezpieczeństwo, fine-tuning).

---

## Lekcja: Lokalne oraz zdalne uruchamianie modeli językowych

Ta lekcja pokazuje praktyczne sposoby uruchamiania modeli językowych Open Source. Uczymy się, jak zainstalować i używać narzędzia **Ollama** do łatwego pobierania i uruchamiania modeli na własnym komputerze (Mac, Windows, Linux) za pomocą terminala. Następnie przechodzimy do uruchamiania modeli na zdalnej infrastrukturze chmurowej za pomocą platformy **RunPod**, omawiając proces wynajmu mocy obliczeniowej (GPU), wybór szablonów (np. z preinstalowaną Ollamą), różnice między trybem "On Demand" i "Spot" oraz zarządzanie kosztami. Dowiadujemy się również, jak połączyć się ze zdalną maszyną i uruchomić na niej model, a także o możliwości dostępu przez API.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/257)
*   **Notatka z lekcji:** [./L06_Lokalne_Zdalne_Uruchamianie_Modeli/Lokalne_Zdalne_Uruchamianie_Modeli.md](./L06_Lokalne_Zdalne_Uruchamianie_Modeli/Lokalne_Zdalne_Uruchamianie_Modeli.md) - Przewodnik krok po kroku po uruchamianiu modeli z Ollama lokalnie i na RunPod zdalnie.
*   **Transkrypcja:** [./L06_Lokalne_Zdalne_Uruchamianie_Modeli/Lokalne_oraz_zdalne_uruchamianie_modeli_językowych_Transkrypcja.md](./L06_Lokalne_Zdalne_Uruchamianie_Modeli/Lokalne_oraz_zdalne_uruchamianie_modeli_językowych_Transkrypcja.md)

### Omawiane narzędzia:

*   [Ollama](https://ollama.com/) - Uruchamianie modeli lokalnie.
*   [RunPod](https://www.runpod.io/) - Wynajem mocy obliczeniowej (GPU) w chmurze.
*   [Hugging Face](https://huggingface.co/) - Repozytorium modeli (wspomniane przy RunPod Serverless).

---

## Lekcja: Poznajemy GPTs

Ta lekcja wprowadza do świata GPTs – niestandardowych wersji ChatGPT. Omawiamy, czym są, do czego służą (automatyzacja zadań, personalizacja) oraz jak przeglądać istniejące modele w GPT Store. Krok po kroku pokazujemy proces tworzenia własnego GPTs w zakładce "Configure", omawiając kluczowe elementy: nazwę, opis, instrukcje, dodawanie bazy wiedzy (Knowledge/RAG), włączanie zdolności (Web Browse, DALL-E, Code Interpreter) oraz konfigurowanie działań (Actions) do integracji z zewnętrznymi API (np. Senuto). Wyjaśniamy również opcje zapisywania i udostępniania stworzonych GPTs.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/258)
*   **Notatka z lekcji:** [./L07_Poznajemy_GPTs/Poznajemy_GPTs.md](./L07_Poznajemy_GPTs/Poznajemy_GPTs.md) - Przewodnik po tworzeniu i używaniu niestandardowych modeli GPTs w ChatGPT.
*   **Transkrypcja:** [./L07_Poznajemy_GPTs/T01L07_Poznajemy_GPTs_Transkrypcja.md](./L07_Poznajemy_GPTs/T01L07_Poznajemy_GPTs_Transkrypcja.md) - Pełna transkrypcja lekcji.

### Omawiane narzędzia:

*   [ChatGPT](https://chat.openai.com/) (Platforma do tworzenia i używania GPTs)
*   [Senuto](https://www.senuto.com/) (Przykład integracji API)

---

## Lekcja: Google NotebookLM

Ta lekcja przedstawia narzędzie NotebookLM od Google, skupiając się na jego funkcjach przydatnych w pracy z treścią i SEO. Omawiamy, jak dodawać źródła wiedzy (odkrywanie stron WWW, pliki z Drive, YouTube), jak wykorzystać funkcje czatu do interakcji z danymi oraz jak generować i interpretować mapy myśli do planowania treści. Pokazujemy również zaawansowany workflow wykorzystania wyeksportowanej mapy myśli w innych narzędziach AI (np. ChatGPT) do dalszej analizy i tworzenia np. planów artykułów. Zwracamy uwagę na obecne ograniczenia językowe narzędzia.

*   **Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/259)
*   **Notatka z lekcji:** [./L08_Google_NotebookLM/NotebookLM.md](./L08_Google_NotebookLM/NotebookLM.md) - Przewodnik po funkcjach NotebookLM, w tym dodawaniu źródeł, generowaniu map myśli i ich wykorzystaniu.
*   **Transkrypcja:** [./L08_Google_NotebookLM/T01L08_Notebook_LM_Transkrypcja.md](./L08_Google_NotebookLM/T01L08_Notebook_LM_Transkrypcja.md) - Pełna transkrypcja lekcji.

### Omawiane narzędzia:

*   [NotebookLM (Google)](https://notebooklm.google.com/)
*   [ChatGPT (OpenAI)](https://chat.openai.com/) (jako przykład narzędzia do dalszej analizy mapy myśli) 