> [services/](services.md)
# `articleService`

Moduł odpowiedzialny za zarządzanie danymi artykułów, w tym ich odczytem, tworzeniem oraz generowaniem slugów. Serwis interaktuje z plikiem JSON artykułów poprzez funkcje [`storage.readArticles()`](../models/storage.md) i [`storage.writeArticles()`](../models/storage.md).

Zobacz też: [`articleController`](../controllers/articlesController.md), [`storage`](../models/storage.md).

## Eksporty
`async function getAllArticles()`

Zwraca tablicę obiektów ze wszystkimi artykułami.

**Użycie**
```js
const articles = await articleService.getAllArticles();
console.log(articles);
```

---
`async function getArticlesBySlug(slug)`

Zwraca artykuły z podanym slugiem.

**Parametry:**
- `slug` - identyfikator artykułu (string)

**Użycie**
```js
const article = await articleService.getArticlesBySlug("test-article");
console.log(article);
```

---
`async function createArticle({title, content, author})`

Tworzy nowy artykuł generując dla niego unikalny slug. Zapisuje artykuł w pliku i zwraca nowo utworzony obiekt artykułu.

**Parametry:**
- `title` - tytuł artykułu (string)
- `content` - treść artykułu (string)
- `author` - autor artykułu (string, opcjonalnie, domyślnie `"Unknown"`)

**Użycie:**
```js
const { title, content, author } = req.body;
const article = await articleService.createArticle({
    title,
    content,
    author,
});

res.status(300).redirect(`/articles/${article.slug}`);
```

---

#### [Mini CMS](../mini-cms.md)