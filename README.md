# Pajamas Inventory

Phone-friendly stock tracker for pajama patterns. Each pattern has a photo and a piece count per size:

- Kids: 4Y, 5Y, 6Y, 7Y, 8Y, 9Y, 10Y, 11Y, 12Y, 13Y
- Adults: S, M, L, XL, 2XL, 3XL

The app (`app/index.html`, photos in `app/img/`) is published as a claude.ai artifact and stores counts in the artifact's shared database, so everyone with access sees the same numbers live.

## GitHub Pages version

`docs/` is a standalone copy for GitHub Pages. Counts are saved to `data/inventory.json` on this branch through the GitHub API, so every device shows the same numbers. Each device connects once with a fine-grained GitHub token (Contents: read and write, this repo only), entered at the bottom of the patterns list. Without a token, counts stay in that browser only.
