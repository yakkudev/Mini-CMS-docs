> [controllers/](controllers.md)
# `articlesController`
Moduł jest odpowiedzialny za zarządzanie zapytaniami HTTP związanymi z artykułami. Obsługuje operacje jak wyświetlanie listy artykułów, wyświetlanie pojedynczego artykułu, tworzenie nowego artykułu oraz renderowanie do formularza. Kontroler korzysta z serwisu [`articleService`](../services/articleService.md), który zapewnia interakcję z plikiem JSON.

Zobacz też: [`articles (Route)`](../routes/articles.md), [`articleService`](../services/articleService/md).

## Eksporty
`async function index(req, res)`

Wyświetla listę wszystkich artykułów.

Zapytanie GET.

**Parametry:**

- `req` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#req) zawierający informacje o zapytaniu HTTP.

- `res` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#res) służący do odesłania odpowiedzi klientowi.

---
`async function show(req, res)`

Wyświetla artykuł podany w slugu zapytania.

Zapytanie GET.


**Parametry:**

- `req` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#req) zawierający informacje o zapytaniu HTTP.

- `res` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#res) służący do odesłania odpowiedzi klientowi.


---
`async function create(req, res)`

Wyświetla formularz tworzenia artykułu, opcjonalnie błędy podane w ostatniej próbie, tworzy nowy artykuł.

Zapytanie POST.

**Parametry:**

- `req` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#req) zawierający informacje o zapytaniu HTTP.

- `res` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#res) służący do odesłania odpowiedzi klientowi.

---
`async function newForm(req, res)`

Wyświetla formularz tworzenia artykułu.

Zapytanie GET.

**Parametry:**

- `req` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#req) zawierający informacje o zapytaniu HTTP.

- `res` - [obiekt ExpressJS](https://expressjs.com/en/5x/api.html#res) służący do odesłania odpowiedzi klientowi.

--- 
#### [Mini CMS](../mini-cms.md)
