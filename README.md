# Recipe Finder

A small, fast, searchable cookbook in one HTML file: recipes sorted onto shelves by meal, search by recipe, ingredient or mood, filters, favourites, and shareable links to single recipes.

**See it with the full collection:** [sarvineshaghi.com/hobbies/recipes](https://sarvineshaghi.com/hobbies/recipes/)

## Features

- **Shelves** by meal: Breakfast, Lunch & dinner, Snacks, Desserts & baking, Sauces & marinades, Drinks, Tips & techniques.
- **Search** across titles, summaries and ingredients (all words must match).
- **Filters** for meal, style (healthy, balanced, indulgent, meal prep), recipe detail (complete / partial) and your saved recipes.
- **Sort** complete recipes first, or A–Z.
- **Surprise me** opens a random complete recipe.
- **Save** favourites with ♥ (kept in your own browser).
- **Recipe view** with ingredients, method, a link back to the original creator, *Copy ingredients* (a quick shopping list) and *Copy link* (`#recipe-id`).
- Keyboard friendly, works on phones, no build step, no dependencies.

## Run it

Serve the folder with any static server, for example:

```sh
python3 -m http.server 8000
```

then open <http://localhost:8000>. Replace `recipes.json` with your own collection.

## Data format

```json
{
  "updated": "YYYY-MM-DD",
  "recipes": [
    {
      "id": "recipe-01",
      "title": "Oat-Date Chocolate Bars",
      "types": ["snack", "dessert"],
      "styles": ["healthy"],
      "detail": "complete",
      "summary": "One short sentence.",
      "ingredients": ["…"],
      "method": ["step 1", "step 2"],
      "source_url": "https://…",
      "source_name": "creator"
    }
  ]
}
```

## About the data

This repository ships the app with two demo recipes created for me. The full collection on my site is compiled from cooking posts I've saved; those recipes belong to their creators, and every one links back to the original post, so they aren't redistributed here.

## Credits

Made by [Sarvin Eshaghi](https://sarvineshaghi.com/). The collection was compiled with Muse.

## Licence

No open-source licence is granted yet. You're welcome to read the code and try the demo.
