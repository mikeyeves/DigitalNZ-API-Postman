# DigitalNZ API v3 — Postman Collection (incl. Papers Past)

A Postman (v2.1) collection for the **[DigitalNZ Records API v3](https://digitalnz.org/developers/api-docs-v3)** (10 requests). It searches 30M+ items from New Zealand libraries, archives, museums and media, including **Papers Past**: New Zealand newspapers from 1839 to the 1980s, with full text.

**Import link** (Postman → Import → Link):
```
https://raw.githubusercontent.com/mikeyeves/DigitalNZ-API-Postman/main/DigitalNZ_API.postman_collection.json
```
**No key is needed** for public content. A free DigitalNZ key (account → *My API key*) gives you more throughput; put it in `dnz_key` and enable the `api_key` parameter.

## Folders
| Folder | Requests |
|---|---|
| ★ Search | 8 |
| Record metadata | 2 |

Search requests show results in a **Visualizer** table with title, date, collection, category and partner.

## Useful parameters
- **`and[display_collection][]=Papers Past`:** newspapers only.
- **Filters:** `and[year][]`, `and[decade][]`, `and[placename][]`, `and[category][]`. Use `or[...]` to match any of several values and `without[...]` to exclude.
- **Facets:** `facets=display_collection,decade,category,placename` with `per_page=0` gives counts only.
- **Sorting and area:** `sort=date&direction=asc`; `geo_bbox=north,west,south,east` limits results to a region.

## Tested at build time
- Papers Past search for "Bukovsky": 2 hits.
- "Barbarossa" in 1905: 10 hits.
- "Barna": 987 records.

## Related collections
[Trove (Australia)](https://github.com/mikeyeves/Trove-API-Postman) · [Library of Congress](https://github.com/mikeyeves/Library-of-Congress-API-Postman) · [WikiTree](https://github.com/mikeyeves/WikiTree-API-Postman) · [Open Archives](https://github.com/mikeyeves/Open-Archives-API-Postman)

*Unofficial. Not affiliated with DigitalNZ or the National Library of New Zealand. Built from the public API documentation.*
