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


### Notatniki Colab

Poniższa tabela zawiera linki do notatników Google Colab używanych w tym tygodniu.

| Notatnik                            | Opis                                                                                                                                                    | Link                                                                                         |
| :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------- |
| Wprowadzenie do Google Colab        | Notatnik służący do nauki podstaw korzystania z narzędzia Google Colab, przygotowujący do pracy z pozostałymi materiałami kursu.                        | [Otwórz w Colab](https://colab.research.google.com/drive/1bi7TZAq_1Kr0fH5kDKluJSkRu8jRyMpJ?usp=sharing) |
| Import danych z Excela do Supabase | Notatnik demonstrujący proces importowania danych z arkuszy Excel do bazy danych Supabase. | [Otwórz w Colab](https://colab.research.google.com/drive/1NE7AbjT3H81fcsu-uMpv-qXeduWKtPxA?authuser=0#scrollTo=ovOxY2nY5Zdt) |
| *(Więcej notatników pojawi się tutaj)* | *(Opis kolejnego notatnika)*                                                                                                                            | *(Link do kolejnego notatnika)*                                                               |

---

*W przyszłości w tym katalogu pojawią się sekcje dla innych lekcji z Tygodnia 2.*

# Źródła wiedzy

W tej sekcji znajdziesz dodatkowe materiały i źródła, które mogą być pomocne w zgłębianiu tematów poruszanych w tym tygodniu.

*   [Poradnik Google na temat prompt engineeringu](https://www.kaggle.com/whitepaper-prompt-engineering)

