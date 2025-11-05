# Dokumentacja Mini CMS

Przykład aplikacji CMS zbudowany przy użyciu Node.js, Express i EJS. Pozwala na przeglądanie listy artykułów, podgląd pojedynczego artykułu oraz
tworzenie nowych wpisów zapisywanych w pliku JSON.

## Podstawowa struktura projektu

### `src/`
- [`controllers/`](controllers/controllers.md) - kontrolery zapytań HTTP: walidacja wejścia, wywołanie serwisów i zwracanie odpowiedzi

- [`models/`](models/models.md) - warstwa dostępu do danych: operacje na plikach 

- [`routes/`](routes/routes.md) - przypisanie endpointów do kontrolerów

- [`services/`](services/services.md) - logika biznesowa aplikacji: operacje operacje niezależne od HTTP.

- [`views/`](views/views.md) - widoki, szablony EJS stron renderowanych po stronie serwera

- [`server.js`](server.md) - entry point aplikacji, włącza serwer na porcie

- [`app.js`](app.md) - konfiguracja ExpressJS

### `public/`
Pliki statyczne, takie jak arkusze stylów, bez żadnego wcześniejszego przetwarzania przez serwer.

### `data/`
Zapisane dane aplikacji.


## Schemat zależności projektu
```
server.js -> app.js -> routes -> controllers -> services -> models -> storage
                                      ↓
                                    views
```

---

**Mini CMS**: [Michał Spilkowski](https://github.com/MichalSpilkowski),
**Dokumentacja**: [Dominik Brewka](https://github.com/yakkudev)