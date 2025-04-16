# Grupy Statusów HTTP

W protokole HTTP statusy odpowiedzi serwera są podzielone na pięć głównych grup, które pozwalają zrozumieć, jaki był wynik zapytania. Poniżej opisane są poszczególne grupy statusów:

## 1. 1xx – Informacyjne
- **Opis**: Te statusy oznaczają, że zapytanie zostało odebrane i jest w trakcie przetwarzania. Używane są rzadko w praktyce.
- **Przykład**: `100 Continue` – Serwer otrzymał część zapytania i oczekuje na pełną odpowiedź od klienta.

**Typowe kody**:
- `100 Continue`
- `101 Switching Protocols`

---

## 2. 2xx – Sukces
- **Opis**: Odpowiedzi z tej grupy wskazują, że zapytanie zostało pomyślnie przetworzone przez serwer. Oznaczają one różne rodzaje sukcesu, w zależności od kontekstu.
- **Przykład**: `200 OK` – Zapytanie zostało przetworzone pomyślnie, a odpowiedź zawiera żądane dane (np. stronę internetową lub JSON).

**Typowe kody**:
- `200 OK` – Żądanie zostało przetworzone poprawnie.
- `201 Created` – Zasób został pomyślnie utworzony.
- `204 No Content` – Żądanie zostało przetworzone, ale nie ma żadnej treści w odpowiedzi.

---

## 3. 3xx – Przekierowanie
- **Opis**: Kody z tej grupy wskazują, że serwer zwrócił odpowiedź, która wskazuje klientowi, że żądanie wymaga dalszego działania, np. przekierowania na inną stronę.
- **Przykład**: `301 Moved Permanently` – Zasób został na stałe przeniesiony na inny adres URL, a klient powinien używać nowego URL w przyszłości.

**Typowe kody**:
- `301 Moved Permanently` – Zasób przeniesiony na stałe.
- `302 Found` – Zasób tymczasowo przeniesiony.
- `303 See Other` – Należy wykonać inne zapytanie (np. GET) w celu uzyskania zasobu.

---

## 4. 4xx – Błąd klienta
- **Opis**: Te kody wskazują, że zapytanie było błędne lub niewłaściwe z powodu problemu po stronie klienta. Oznacza to, że klient powinien coś poprawić, aby zapytanie mogło zostać przetworzone.
- **Przykład**: `404 Not Found` – Serwer nie może znaleźć zasobu, którego klient szuka.

**Typowe kody**:
- `400 Bad Request` – Zapytanie jest niepoprawne (np. brak wymaganych parametrów).
- `401 Unauthorized` – Brak odpowiednich uprawnień do dostępu do zasobu (np. brak logowania).
- `404 Not Found` – Żądany zasób nie został znaleziony na serwerze.

---

## 5. 5xx – Błąd serwera
- **Opis**: Kody w tej grupie oznaczają, że serwer napotkał problem i nie mógł poprawnie przetworzyć zapytania. Błąd pochodzi z serwera, a nie od klienta.
- **Przykład**: `500 Internal Server Error` – Serwer napotkał niespodziewany problem i nie może przetworzyć zapytania.

**Typowe kody**:
- `500 Internal Server Error` – Ogólny błąd serwera, który może być spowodowany różnymi problemami.
- `502 Bad Gateway` – Serwer pełni rolę bramy lub proxy i otrzymał nieprawidłową odpowiedź od serwera z wyższej warstwy.
- `503 Service Unavailable` – Serwis jest chwilowo niedostępny, np. z powodu przeciążenia serwera.

---

## Podsumowanie:
- **1xx**: Informacyjne – zapytanie jest w trakcie przetwarzania.
- **2xx**: Sukces – zapytanie zostało pomyślnie przetworzone.
- **3xx**: Przekierowanie – klient musi wykonać dodatkowe kroki (np. zmienić URL).
- **4xx**: Błąd klienta – zapytanie jest błędne lub brakuje uprawnień.
- **5xx**: Błąd serwera – problem po stronie serwera, zapytanie nie mogło być przetworzone.

