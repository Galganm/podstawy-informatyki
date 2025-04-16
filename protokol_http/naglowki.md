# Nagłówki HTTP

## Nagłówki zapytania (Request):
1. **Accept** – Określa, jakie typy mediów są akceptowane przez klienta (np. tekst, HTML, JSON, itp.). W tym przypadku klient akceptuje wszystkie typy: `*/*`.
2. **Accept-Encoding** – Mówi serwerowi, jakie algorytmy kompresji mogą być używane do przesyłania danych. W tym przypadku klient obsługuje kompresję `gzip, deflate, br, zstd`.
3. **User-Agent** – Zawiera informacje o przeglądarce i systemie operacyjnym klienta. Przykład: `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/135.0.0.0 Safari/537.36 Edg/135.0.0.0`.

## Nagłówki odpowiedzi (Response):
1. **Content-Type** – Określa typ danych, które są wysyłane przez serwer. W tym przypadku jest to `application/json`, co oznacza, że odpowiedź jest w formacie JSON.
2. **Date** – Zawiera datę i czas, kiedy odpowiedź została wysłana przez serwer. Przykład: `Wed, 16 Apr 2025 11:47:37 GMT`.
3. **Server** – Określa serwer, który obsługuje zapytanie. W tym przypadku serwer to `gunicorn/19.9.0`, co oznacza, że jest używana wersja 19.9.0 Gunicorn.
