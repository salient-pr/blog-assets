# Salient PR — blog image assets

Interim public host for the images used by the Salient PR blog during the
Squarespace → Webflow migration.

**Why this exists.** Webflow's CSV import downloads a remote image into Assets
only for a mapped *Image field*. Images inside a Rich Text body stay as external
`<img src>` references pointing at whatever host they came from. Ours pointed at
the Squarespace CDN, which stops answering when that subscription ends — so the
blog needed a home for them that survives the cutover, before we have access to
the Webflow site's own Assets.

**Contents.** 86 images, WebP, capped at 1920px wide, 15.9 MB total. Converted
from the original Squarespace files; the mapping from every original URL to its
file here is in `IMAGE_MAP.csv` in the migration workspace.

**This is temporary.** Once the Webflow site is handed over, the images move into
Webflow's own Assets via `upload_images_to_webflow.py`, the CSVs are repointed at
the webflow.com URLs, and this repository can be archived.

Served via GitHub Pages at `https://salient-pr.github.io/blog-assets/blog/<file>.webp`.
