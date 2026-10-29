# MVT Decoder

A single static page that decodes a Mapbox Vector Tile and shows it on a MapLibre map.

## Input

- **URL**: fetches the tile. The server must send CORS headers. `z/x/y` is read from paths ending in `/{z}/{x}/{y}[.ext]`.
- **Paste**: hex (spaces, commas, `0x` and `\x` prefixes allowed) or base64/base64url.
- **File**: a `.pbf` or `.mvt` file.

Gzipped tiles are decompressed automatically.

Link to a tile directly with `?url=`:

```
https://<user>.github.io/<repo>/?url=https://demotiles.maplibre.org/tiles/2/2/1.pbf
```

## Run locally

```sh
python3 -m http.server 8000
```

Open http://localhost:8000.

## Publish on GitHub Pages

1. Push `index.html` to the default branch.
2. In the repository, open **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**, branch `main`, folder `/ (root)`.
