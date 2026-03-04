Simple map-data package

Contents:
- map_world.qmd — Quarto document that builds a working spatial dataset and plots highlighted countries.
- data/legal_alcohol_policy.csv — single source dataset for countries, legal system, and alcohol policy indicators.
- World_Countries_(Generalized)_-573431906301700955/ — world shapefile used by the workflow.
- UK/ — UK subdivisions shapefile (used to replace the aggregate United Kingdom polygon).
- .gitignore — ignores caches, outputs and OS/editor files.

Quick start
1. Install required R packages: `sf`, `ggplot2`, `dplyr`. Optional: `ggrepel`, `rmapshaper`.
2. Render the Quarto document from the project root:

	quarto render map_world.qmd

	or open `map_world.qmd` in RStudio and run the chunks.

Notes
- The document rebuilds the working spatial dataset from the included shapefiles (no cache).
- Edit `data/legal_alcohol_policy.csv` directly to change highlighted countries and indicators.
- The Quarto file auto-loads `data/legal_alcohol_policy.csv` and will render additional maps for:
	- `legal_system_family`
	- `alcohol_policy_status`
- Keep country names in the spreadsheet human-readable (e.g. Turkey, Czech Republic, United States); the script normalises common aliases to shapefile names.
- To share this repo on GitHub, create a remote and push from this folder.


