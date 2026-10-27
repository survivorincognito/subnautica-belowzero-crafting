# Survivor Incognito — Subnautica Crafting Reference

## Files

- `subnautica-crafting-reference.html`: ready-to-host, self-contained interactive reference. This is the only file required for visitors.
- `subnautica-crafting-recipes.json`: editable recipe database used to build the HTML.
- `crafting_template.html`: the CSS/JavaScript layout with a data placeholder.
- `render_from_json.py`: regenerates the HTML from the JSON and template.

## Publishing via GitHub Pages

1. Upload `subnautica-crafting-reference.html` to your GitHub Pages repository.
2. Enable GitHub Pages for that repository if you have not already.
3. Visit the published file URL, e.g. `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/subnautica-crafting-reference.html`. Replace both placeholders with your actual names.
4. Link to the hosted tool from the existing Subnautica Crafting Reference page, or embed it using the code below if your WordPress setup supports iframes.

```html
<iframe
  src="https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/subnautica-crafting-reference.html"
  title="Subnautica interactive crafting reference"
  loading="lazy"
  style="width:100%; height:1100px; border:0; border-radius:12px;"
></iframe>
```

The iframe height is fixed, so it has its own scrolling area. A plain link to the hosted HTML is an alternative if you prefer a full-screen tool or your WordPress setup disallows iframes.

## Updating recipe data

Edit the JSON recipe array, then run `python render_from_json.py` in this folder and re-upload the HTML. The page itself contains the data; it does not load the JSON from a server.

Each entry contains `id`, `name`, `station`, `category`, and `ingredients`. Each ingredient has `name` and `qty`. `note` is optional. Keep `id` unique.

## Behaviour and limitations

- Searches recipe names, crafting stations, categories and ingredient names.
- Ingredient pills search all recipes that use that ingredient.
- Preparation list totals **direct recipe ingredients**, not fully broken-down raw material costs.
- List and checkbox state are saved with browser local storage, when available. Other browsers/devices do not sync.
- The page works offline when opened as a file in an unrestricted browser. No external stylesheets, frameworks or API requests are required.
- This is for the original Subnautica, not Below Zero.
- Audited against published original Subnautica recipe references and the recipe-module data on 26 October 2026. Changes are recorded in `subnautica-recipe-audit.md`. This is a documentation-based verification, not a direct in-game PDA capture. Check doubtful entries against the PDA if the game version differs.

## Verification and batch quantities

- `subnautica-recipe-audit.md` lists the corrected, removed, added and clarified entries.
- Recipes marked `outputQty` in JSON make multiple items per craft (e.g., 2 Disinfected Waters or 5 Pipes). The planner rounds up the desired number of items to whole crafting batches.
- Generic cooked fish and cured fish entries summarize the many separate fish variants listed in the game.
- Decorative pickup-only items such as posters are not listed as craftable building recipes.
