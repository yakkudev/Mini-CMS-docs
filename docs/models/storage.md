> [models/](models.md)
# `storage`
Moduł jest odpowiedzialny za zapis i odczyt artykułów z pliku `data/articles.json`.


## Eksporty
`async function readArticles()`

Odczytuje artykuły zapisane w pliku `data/articles.json`, zwraca je jako tablicę obiektów. W przypadku błędu zwraca pustą tablicę.

**Użycie**
```js
const articles = await storage.readArticles();
console.log(articles);
```

---
`async function writeArticles(articles)`

Nadpisuje artykuły zapisane w `data/articles.json` nowymi.

**Parametry:**

- `articles` - obiekt który ma być zamieniony na JSON i zapisany do pliku.
> Artykuł powinien przyjmować podobną formę:
```
{
    "id": "123456789",
    "title": "Tytuł artykułu",
    "content": "Lorem ipsum dolor sit amet",
    "author": "Jan Kowalski",
    "slug": "slug-artykulu",
    "createdAt": "2025-10-27T12:24:25.288Z"
},
```

**Użycie:**

```js
const newArticle = { id: 123456, title: "lorem", /* ... */ };
let articles = await storage.readArticles();
articles = [...articles, newArticle];

await storage.writeArticles(articles);
```

--- 
#### [Mini CMS](../mini-cms.md)
