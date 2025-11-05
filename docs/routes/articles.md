> [routes/](routes.md)
# `articles (Route)`
Moduł jest odpowiedzialny przekierowanie zapytań do odpowiednich kontrolerów.

Zobacz też: [`articlesController`](../controllers/articlesController.md).

## Eksporty

`router`

Jest obiektem [Router ExpressJS](https://expressjs.com/en/5x/api.html#router).

Zawiera następujące routingi:

- `GET "/"` - [`articlesController.index()`](../controllers/articlesController.md)

- `GET "/articles/new"` - [`articlesController.newForm()`](../controllers/articlesController.md)

- `POST "/articles"` - [`articlesController.create()`](../controllers/articlesController.md)

- `GET "/articles/:slug"` - [`articlesController.show()`](../controllers/articlesController.md)


--- 
#### [Mini CMS](../mini-cms.md)
