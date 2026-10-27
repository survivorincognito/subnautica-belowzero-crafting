# Survivor Incognito – Subnautica: Below Zero Crafting Reference

A single-file responsive HTML search and crafting planner for Below Zero. Works offline. No services, cookies, accounts, fonts or third-party JavaScript required.

## Files
- `Survivor_Incognito_Below_Zero_Crafting_Reference.html`: deployable standalone page.
- `below-zero-crafting-recipes.json`: editable source data.
- `below-zero-crafting-template.html`: HTML/JS/CSS template, with `/*__RECIPE_DATA__*/` recipe placeholder.
- `render_below_zero.py`: rebuild tool. Run `python render_below_zero.py` in the kit directory after editing the JSON.

## Functions
- Search item names and ingredients, or select one specifically.
- Filter by crafting station.
- Add recipes to a list and adjust desired quantities.
- Get combined direct materials and tick them off; batch recipes round up properly.
- Copy checklist; save progress to browser localStorage where enabled.
- Mobile-responsive with a direct jump to the checklist.

## Data & limitations
- Curated recipes and food preparations for the full game, NOT every collectable or item in the game.
- Primary 2025 game-data cross-check: https://www.subnauticadatabase.com/below-zero/items/ (Below Zero build 53872, Oct 2025).
- Historical source also consulted: https://github.com/breadthe/craftnautica2/blob/main/src/lib/items-bz.js (several historic quantities and stations corrected).
- Original Subnautica (2018) recipes MUST NOT be substituted for Below Zero recipes.
- Game PDA remains definitive. This guide does not include blueprint locations/unlock conditions or every future modded recipe.
- Checklist counts DIRECT ingredients, including fabricated components. It does NOT recursively break crafted components down into their raw materials.
- Craftable fish recipes include both Feather Fish colour variants.
- Cured/cooked fish and late-game Architect components appear in results; story spoilers are not hidden.

## Publish
- Upload the HTML to GitHub Pages (e.g., `index.html`) and link to it from the Below Zero hub. The entire planner runs within this one HTML document.
- If using WordPress, link to or embed the hosted page rather than pasting the script into a Custom HTML block that can strip JavaScript.
- Local saved lists use `si-subnautica-below-zero-crafting-list-v1`, separate from the original Subnautica guide.

This is an unofficial Survivor Incognito fan reference. Game and item names belong to Unknown Worlds Entertainment / Krafton.
