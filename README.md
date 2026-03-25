Simple map-data package

This folder is set up for two tasks:

1. Building/plotting country policy maps in Quarto.
2. Maintaining a clean, hyperlinked source register.

## Relevant structure

- `map_world.qmd` — main Quarto workflow for map creation.
- `data/legal_alcohol_policy.csv` — policy input used by `map_world.qmd`.
- `World_Countries_(Generalized)_-573431906301700955/` — world shapefile assets.
- `UK/` — UK shapefile assets (used to replace aggregate UK polygon).
- `Sources_hyperlinked.csv` — References used 
- `.gitignore`, `LICENSE`, `README.md` — project metadata.

## Quick start (maps)

1. Install required R packages: `sf`, `ggplot2`, `dplyr`.
2. Optional packages: `ggrepel`, `rmapshaper`.
3. Render from project root:

   `quarto render map_world.qmd`

## Quick start (sources)

Run from project root:

`python3 tidy_sources_hyperlinked.py`

This updates both:

- `Sources_hyperlinked.csv`
- `Sources_hyperlinked.xlsx`

## Notes

- The Quarto workflow rebuilds spatial data directly from included shapefiles (no cache dependency).
- Keep country names human-readable in `data/legal_alcohol_policy.csv`; the Quarto code normalises common aliases.
- In `Sources_hyperlinked.csv`, rows marked `URL_Status = Check URL` need manual URL correction.


