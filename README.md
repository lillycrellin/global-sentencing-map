Simple map-data package

Contents:
- map_world.qmd — Quarto document that builds a working spatial dataset and plots highlighted countries.
- data.xlsx — spreadsheet listing countries to highlight (must contain a `Country` column).
- World_Countries_(Generalized)_-573431906301700955/ — world shapefile used by the workflow.
- UK/ — UK subdivisions shapefile (used to replace the aggregate United Kingdom polygon).
- .gitignore — ignores caches, outputs and OS/editor files.

Quick start
1. Install required R packages: `readxl`, `sf`, `ggplot2`. Optional: `ggrepel`, `rmapshaper`.
2. Render the Quarto document from the project root:

	quarto render map_world.qmd

	or open `map_world.qmd` in RStudio and run the chunks.

Notes
- The document rebuilds the working spatial dataset from the included shapefiles (no cache).
- Edit `data.xlsx` (the `Country` column) to change which countries are highlighted.
- To share this repo on GitHub, create a remote and push from this folder.


