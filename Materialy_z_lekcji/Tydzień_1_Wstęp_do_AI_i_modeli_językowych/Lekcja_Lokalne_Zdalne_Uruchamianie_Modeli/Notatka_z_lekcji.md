**Link do lekcji na platformie:** [Obejrzyj lekcję na SensAI Academy](https://learn.sensai.academy/next/public/lesson/257)

---

## Wprowadzenie

Ten przewodnik wyjaśnia, jak uruchamiać modele językowe na własnym komputerze (lokalnie) oraz na zdalnych serwerach (w chmurze). Dowiesz się, jak korzystać z narzędzia Ollama do łatwej instalacji i uruchamiania modeli lokalnie oraz jak wykorzystać platformę RunPod do wynajmu mocy obliczeniowej i uruchamiania modeli zdalnie, optymalizując koszty przy większych zadaniach.

## Omawiane narzędzia

* **Ollama:** [https://ollama.com/](https://ollama.com/) (Narzędzie do uruchamiania modeli lokalnie)
* **RunPod:** [https://www.runpod.io/](https://www.runpod.io/) (Platforma chmurowa do wynajmu mocy obliczeniowej)
* **Hugging Face:** [https://huggingface.co/](https://huggingface.co/) (Repozytorium modeli, wspomniane w kontekście RunPod Serverless)

## Uruchamianie modeli lokalnie za pomocą Ollama

Ollama to narzędzie ułatwiające pobieranie i uruchamianie modeli językowych na komputerach z systemem macOS, Linux lub Windows.

### Instalacja i konfiguracja

1.  **Pobierz Ollama:** Wejdź na stronę [https://ollama.com/](https://ollama.com/) i pobierz instalator odpowiedni dla Twojego systemu operacyjnego.
2.  **Zainstaluj Ollama:** Proces instalacji jest standardowy (kilka kliknięć "dalej").
3.  **Uruchom Ollama:** Po instalacji Ollama działa w tle (np. na macOS widoczna jest ikona na górnym pasku). Nie posiada ona tradycyjnego interfejsu graficznego.

### Praca z Ollama w terminalu

Do interakcji z Ollama używa się terminala (wiersza poleceń).

1.  **Otwórz terminal:**
    * Na macOS: Naciśnij `Command + Spacja`, wpisz `Terminal` i naciśnij Enter.
    * Na Windows: Wyszukaj `cmd` lub `PowerShell`.
    * Na Linux: Użyj skrótu `Ctrl + Alt + T` lub znajdź aplikację terminala.
2.  **Podstawowe komendy:**
    * `ollama`: Wyświetla listę dostępnych funkcji i komend Ollama.
    * `ollama list`: Pokazuje modele językowe, które już pobrałeś i zainstalowałeś na swoim komputerze. Zwraca uwagę na kolumnę `SIZE`, która wskazuje rozmiar modelu – jest to przybliżona ilość pamięci RAM, jakiej potrzebujesz, aby go uruchomić.

### Znajdowanie i uruchamianie modelu

1.  **Przeglądaj modele:** Odwiedź bibliotekę modeli na stronie Ollama, aby znaleźć interesujący Cię model (np. `llama3`, `bielik`). Możesz tam sprawdzić różne wersje, rozmiary, przeczytać opis (`readme`) i zobaczyć benchmarki.
    * **Wskazówka:** Zwróć uwagę na rozmiar modelu. Mniejsze modele (np. 1B, 3B parametrów) wymagają mniej RAM (np. kilka GB), podczas gdy duże modele (np. 70B, 405B) mogą potrzebować dziesiątek lub nawet setek GB RAM, często na karcie graficznej.
2.  **Skopiuj komendę uruchamiającą:** Na stronie modelu znajdź komendę w formacie `ollama run nazwa-modelu:wersja` (np. `ollama run llama3:8b` lub `ollama run spychalski/bielik-7b-instruct-v0.1`). Wersja często jest domyślna (`latest`), więc wystarczy `ollama run nazwa-modelu`.
3.  **Wklej i uruchom w terminalu:** Wklej skopiowaną komendę do terminala i naciśnij Enter.
    * Jeśli model nie był wcześniej pobrany, Ollama automatycznie go ściągnie (może to chwilę potrwać).
    * Następnie model zostanie załadowany.
4.  **Rozmawiaj z modelem:** Po załadowaniu modelu terminal zamieni się w interfejs czatu. Możesz zadawać pytania lub wydawać polecenia bezpośrednio w terminalu.

**Przykład 1: Uruchomienie Llama 3 (8 miliardów parametrów)**

```bash
ollama run llama3:8b
```

Po załadowaniu zapytaj: `what is hamburger?`

**Przykład 2: Uruchomienie modelu Bielik (polski model)**

Znajdź model `bielik` na stronie Ollama, skopiuj komendę (np. `ollama run spychalski/bielik-7b-instruct-v0.1`, lub jeśli jest oznaczony jako `bielik` po prostu `ollama run bielik`).

```bash
ollama run bielik
```

Po załadowaniu zapytaj po polsku: `Co to jest hamburger?`

## Uruchamianie modeli zdalnie za pomocą RunPod

RunPod to platforma chmurowa, która pozwala wynająć moc obliczeniową (głównie GPU) na godziny. Jest to opłacalne przy dużych zadaniach obliczeniowych lub gdy potrzebujesz bardzo wydajnych kart graficznych, których nie posiadasz. Płacisz za czas użytkowania maszyny, a nie za przetworzone tokeny (jak np. w OpenAI API).

### Dostępne podejścia w RunPod

* **Serverless:** Prostsze podejście, gdzie podajesz link do modelu (np. z Hugging Face), konfigurujesz parametry i otrzymujesz endpoint API do wykorzystania. Nie omawiane szczegółowo w tej lekcji.
* **Pods:** Bardziej elastyczne podejście, polegające na wynajęciu wirtualnej maszyny z określoną kartą graficzną (GPU). Na tej maszynie instalujesz i uruchamiasz potrzebne oprogramowanie (np. Ollama) i modele.

### Wynajmowanie maszyny (Pod) w RunPod

1.  **Zaloguj się do RunPod:** Załóż konto i przejdź weryfikację.
2.  **Przejdź do sekcji Pods:** W panelu RunPod wybierz "Pods".
3.  **Rozpocznij tworzenie maszyny:** Kliknij "Deploy".
4.  **Wybierz GPU:** Przeglądaj dostępne karty graficzne.
    * **Community Cloud:** Często tańsze opcje, udostępniane przez innych użytkowników.
    * **Secure Cloud:** Serwery należące bezpośrednio do RunPod.
    * Wybierz kartę odpowiednią do Twoich potrzeb (np. tańsze RTX dla mniejszych modeli, potężne H100 dla największych).
5.  **Wybierz szablon (Template):** Wyszukaj i wybierz szablon `Ollama`. Spowoduje to zainstalowanie Ollama na wynajętej maszynie.
6.  **Wybierz typ wynajmu:**
    * **On Demand:** Gwarantowany dostęp do maszyny przez cały czas, wyższa cena (np. $3/h dla H100).
    * **Spot:** Tańsza opcja (nawet o połowę), ale maszyna może zostać Ci odebrana, jeśli pojawi się klient płacący stawkę "On Demand". Dobre do zadań, które można przerwać i wznowić.
7.  **Skonfiguruj i uruchom:** Sprawdź podsumowanie (GPU, RAM, CPU, koszt godzinowy). Kliknij "Deploy". Maszyna zostanie utworzona w dostępnym centrum danych (np. w Kanadzie). Poczekaj kilka minut na jej zainstalowanie.

### Praca ze zdalną maszyną (Pod)

1.  **Połącz się z terminalem:** Gdy maszyna będzie gotowa (status "Running"), kliknij przycisk "Connect". Wybierz opcję "Start Web Terminal", a następnie "Connect to Web Terminal". Otworzy się terminal w przeglądarce, połączony ze zdalną maszyną.
2.  **Pobierz i uruchom model:** W web terminalu użyj komend Ollama dokładnie tak samo, jak na lokalnym komputerze.
    * Znajdź model na stronie Ollama (np. `llama3:8b`).
    * Skopiuj komendę `ollama run nazwa-modelu:wersja`.
    * Wklej i uruchom komendę w web terminalu. Model zostanie pobrany na zdalną maszynę i załadowany.
    * Przykład: `ollama run llama3:8b`
3.  **Interakcja z modelem:** Zadawaj pytania bezpośrednio w web terminalu (np. `What is sushi?`).
4.  **Dostęp przez API (Opcjonalnie):** RunPod udostępnia również adres URL (HTTP service endpoint) dla Twojej maszyny. Możesz go użyć do wysyłania zapytań do modelu Ollama działającego na tej maszynie z innych aplikacji lub skryptów, korzystając z Ollama API (dokumentacja API dostępna na stronie Ollama w sekcji "Docs").

### Zarządzanie kosztami w RunPod

1.  **Zatrzymaj maszynę:** Gdy zakończysz pracę (np. przetworzysz wszystkie dane), kliknij przycisk "Stop". Spowoduje to zatrzymanie naliczania opłat za godzinę pracy GPU/CPU. Nadal naliczana będzie niewielka opłata za zajmowany dysk.
2.  **Usuń maszynę:** Aby całkowicie zakończyć naliczanie jakichkolwiek opłat, usuń maszynę (Pod) za pomocą opcji "Terminate" (ikona kosza). Spowoduje to usunięcie wszystkich danych z tej maszyny. Przy kolejnej potrzebie trzeba będzie stworzyć i skonfigurować maszynę od nowa.

## Podsumowanie

Nauczyłeś się dwóch sposobów uruchamiania modeli językowych:

* **Lokalnie z Ollama:** Idealne do eksperymentów, mniejszych zadań i gdy posiadasz wystarczającą moc obliczeniową (RAM) na swoim komputerze. Łatwe w konfiguracji i użyciu.
* **Zdalnie z RunPod:** Przydatne do uruchamiania bardzo dużych modeli wymagających potężnych GPU, realizacji dużych zadań obliczeniowych lub gdy chcesz zoptymalizować koszty, płacąc tylko za faktyczny czas pracy maszyny.

Wiedza ta stanowi podstawę do dalszej pracy z modelami, w tym ich integracji w bardziej złożone procesy i aplikacje. 