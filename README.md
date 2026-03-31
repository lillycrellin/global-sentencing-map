Simple map-data package

This project is set up to build and plot country-speicifc alcohol consumption policy maps in Quarto.


## Relevant structure

- `map_world.qmd` — main Quarto workflow for map creation.
- `data/legal_alcohol_policy.csv` — policy input used by `map_world.qmd`.
- `World_Countries_(Generalized)_-573431906301700955/` — world shapefile assets.
- `UK/` — UK shapefile assets (used to replace aggregate UK polygon).
- `.gitignore`, `LICENSE`, `README.md` — project metadata.

## Quick start (maps)

1. Install required R packages: `sf`, `ggplot2`, `dplyr`.
2. Optional packages: `ggrepel`, `rmapshaper`.
3. Render from project root:

   `quarto render map_world.qmd`


## Notes

- The Quarto workflow rebuilds spatial data directly from included shapefiles (no cache dependency).
- Keep country names human-readable in `data/legal_alcohol_policy.csv`; the Quarto code normalises common aliases.



