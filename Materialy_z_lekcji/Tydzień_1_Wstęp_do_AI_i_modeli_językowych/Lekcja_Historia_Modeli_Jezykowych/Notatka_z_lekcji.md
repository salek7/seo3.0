## Przewodnik po Lekcji: Historia Modeli Językowych 🧠 (Wersja Poprawiona)

**Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/252)

Cześć! Ta notatka pomoże Ci zrozumieć fascynującą historię sztucznej inteligencji (AI), a zwłaszcza modeli językowych, które rewolucjonizują nasz świat. Dowiesz się, skąd wzięła się ta technologia, jak działa (na świetnym przykładzie od `Financial Times`) i dlaczego jest tak ważna. Zaczynajmy!

### Dlaczego AI i Modele Językowe? Cel Google 🎯

-   **Problem:** Google od zawsze potrzebowało rozumieć **kontekst** – zarówno tego, co wpisujesz w wyszukiwarkę (np. "czarna konsola do gier" -> myślisz PlayStation), jak i treści na stronach internetowych.
-   **Cel Google:** Dostarczać jak najlepsze wyniki wyszukiwania. To napędzało rozwój technologii rozumienia języka.
-   **Kluczowa Rola Google:** Według prowadzącego, Google jest głównym motorem rozwoju AI dzięki swoim technologiom i patentom.

### Kamienie Milowe w Rozumieniu Języka

1.  **2013: `Word2Vec` - Słowa jako Wektory**

    **Co to?** Algorytm zamieniający słowa na wektory (liczby) w przestrzeni matematycznej.

    **Co to dało?** Google zrozumiało, że pewne słowa są sobie "bliskie" znaczeniowo (np. "pianino" jest blisko "skrzypiec", "Mercedes" blisko "Volkswagen"). To był początek rozumienia powiązań tematycznych na stronach (np. strona o instrumentach powinna omawiać pianino, skrzypce, gitarę).

    **Ograniczenie:** Jeszcze nie pozwalało to w pełni zrozumieć kontekstu całych zdań.

2.  **2014: `Sequence-to-Sequence` - Tłumaczenie Maszynowe**

    **Co to?** Metoda pozwalająca na przetwarzanie sekwencji danych (np. zdań).

    **Zastosowanie:** Umożliwiło stworzenie `Google Translate`. Okazało się, że słowa o tym samym znaczeniu w różnych językach (np. "pies" i "dog") mają podobne reprezentacje wektorowe.

### Rewolucja: Architektura Transformerów ✨

To technologia, która **rządzi obecnym AI**. Prowadzący omawia ją na podstawie doskonałego opracowania `Financial Times` (znajdziesz je [tutaj](https://ig.ft.com/ai-explained/)).

**Jak Działają Transformery (Krok po Kroku wg Financial Times):**

1.  **Tokenizacja:** Zdanie jest dzielone na mniejsze jednostki – **tokeny**. W przykładzie FT dla uproszczenia tokenami są całe słowa (np. "We | go | to | work | by | train"). *W praktyce tokeny to często fragmenty słów (więcej o tym później).*

2.  **Szukanie Bliskich Słów i Prawdopodobieństwa:** Algorytm analizuje, jakie słowa często występują obok siebie (np. co może wystąpić obok słowa "work"? "processes", "hour", "from home", ale raczej nie "zebra" czy "polka").

3.  **Embedding (Zamiana na Wektory):** Tokeny (lub ich kombinacje) są zamieniane na wektory (liczby). Pozwala to matematycznie mierzyć "dystans" między słowami/konceptami.
    *Przykład:* "Sea" (morze) jest blisko "ocean", ale to nie to samo. "Football" jest blisko "soccer".

4.  **Klastrowanie:** Podobne koncepcyjnie słowa grupują się razem (np. "train", "bus", "car" jako pojazdy; "walk", "swim", "run" jako sporty).

5.  **Self-Attention (Samouważność) - Klucz do Kontekstu!** 🧠

    **Co to?** Mechanizm, dzięki któremu model **rozumie relacje między słowami w zdaniu** i określa, które słowa są najważniejsze dla ogólnego znaczenia.

    *Przykład 1:* W zdaniu "I have **no** interest in politics", `Self-Attention` wie, że słowo "**no**" jest kluczowe i zmienia sens całości.

    *Przykład 2:* W zdaniu "Bank **interest** rate rises", `Self-Attention` rozumie, że "**interest**" oznacza tu "oprocentowanie", a nie "zainteresowanie" (jak w przykładzie 1), dzięki kontekstowi słów "bank" i "rate".

    *Przykład 3:* W "The dog chewed the bone because **it** was hungry", model wie, że "**it**" odnosi się do "**dog**". Ale w "The dog chewed the bone because **it** was delicious", model wie, że "**it**" odnosi się do "**bone**".

6.  **Generowanie Treści (Przewidywanie):** Modele językowe generują tekst, przewidując najbardziej prawdopodobne następne słowo (token) w danym kontekście.
    *Przykład:* Po "The Financial Times is...", model oblicza **wynik prawdopodobieństwa (`probability score`)** dla różnych możliwych następnych słów ("a", "about", "the"...) i wybiera to najbardziej prawdopodobne (np. "a newspaper found in 1888").

    **Cel:** Naszym celem (np. w SEO, marketingu) jest tworzenie treści, gdzie prawdopodobieństwo wystąpienia kolejnych "dobrych" tokenów jest jak najwyższe.

**Podsumowanie Procesu Transformera:**
-   Tokenizacja
-   Embedding
-   Self-Attention
-   Wynik (Encoded Output)

### Tokenizacja w Praktyce: Więcej niż Słowa

-   **Realne Tokeny:** Modele AI (jak te od OpenAI) zazwyczaj dzielą tekst na **fragmenty słów** lub **częste sekwencje znaków**, a nie tylko całe słowa.
    *Przykład:* "Hej, co u Ciebie słychać?" (24 znaki) zostało podzielone na 11 tokenów (różne kolory w przykładzie).

-   **Dlaczego To Ważne?**

    **Koszt:** Płacisz za przetwarzanie **tokenów**, nie słów czy znaków.

    **Wydajność:** Język angielski jest zwykle "tańszy" w tokenizacji niż polski (mniej tokenów na tę samą treść). *Pro Tip: Promptowanie po angielsku może być tańsze.*

    **SEO:** Google używa Transformerów (jak `BERT`) do oceny treści, a one działają właśnie na tokenach.

### Oś Czasu Kluczowych Wydarzeń

-   **2018:** Google wprowadza `BERT` (Bi-directional Encoder Representations from Transformers) – kluczowy algorytm do oceny treści w wyszukiwarce. Powstaje też pierwszy `GPT` od OpenAI.
-   **2021:** Google zapowiada pierwsze kroki w kierunku multimodalności (wyszukiwanie głosem, obrazem), ale technologia nie była jeszcze gotowa.
-   **~2022:** Pojawia się `ChatGPT` – przełom i początek ogromnego przyspieszenia.
-   **2024:** Mamy już `GPT-4o` (zaawansowany model multimodalny).
-   **Wycena OpenAI:** Gwałtownie rośnie, pokazując tempo rozwoju (wspomniane 157 mld USD, a później aktualizacja do 300 mld USD).

### Aktualizacja na Rok 2025: Niesamowite Przyspieszenie 🚀

*(Ta część została nagrana później, aby odzwierciedlić błyskawiczny postęp)*

-   **Postęp Wykładniczo-Wykładniczy:** Rozwój AI przyspiesza w niewyobrażalnym tempie.
-   **Nowe Modele:** Pojawiają się modele z zaawansowanym **reasoningiem** (wnioskowaniem), przewyższające średnie ludzkie IQ (np. `Gemini 2.5`, `O3`, `O4`). *Porównanie: Średnie IQ 100, modele 130+, Einstein 167.*
-   **Grafika i Wideo - Zdjęcia:** Fotorealizm, generowanie napisów (narzędzie `Ideogram`).
-   **Grafika i Wideo - Wideo:** Niesamowity detal, kontrola kamery, generowanie dźwięku, storytelling, kategoria Oscarów dla AI.
-   **Multimodalność Pełną Parą:** AI rozumie i wnioskuje nie tylko z tekstu, ale i z obrazów (np. analiza kreacji reklamowych konkurencji).
-   **Przyszłość:** Generative AI ➡️ Agenci AI (autonomiczne programy) ➡️ Physical AI (robotyka).
-   **Physical AI - Trening:** Wirtualne światy jak `NVIDIA Cosmos` do treningu autonomicznych samochodów i humanoidów.
-   **Physical AI - Zastosowania:** Humanoidy w produkcji (np. iPhony), polska firma tworząca zaawansowanego humanoida, neuroprotezy (przywracanie mowy), dekodowanie języka delfinów, medycyna (diagnostyka, odkrywanie leków).

### Podsumowanie i Co Dalej?

Zrozumieliśmy, jak ewolucja potrzeby rozumienia kontekstu doprowadziła do powstania Transformerów – kluczowej technologii AI. Widzieliśmy, jak działają (tokenizacja, embedding, self-attention, prawdopodobieństwo) i jak błyskawicznie rozwija się cała dziedzina.

W kolejnej lekcji zagłębimy się bardziej w **modele językowe**, ich wyzwania i jak sobie z nimi radzić. Do zobaczenia! 👋 