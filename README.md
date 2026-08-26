# Basalt Extensions

The extension store feed for the Basalt launcher.

Paste this URL into the launcher at **Settings → Extensions → Discover**:

```
https://raw.githubusercontent.com/closedsrc/basalt-extensions/main/feed.json
```

The launcher reads [`feed.json`](./feed.json), shows what each package can do, and
installs the `.basaltext` from its release asset. No backend — this is just a
static file plus release downloads.

## Available extensions

| Extension | Version | What it does |
|-----------|---------|--------------|
| **Basaltify** | 1.0.0 | Music player — searches/streams via yt-dlp, trending chart, local playlists, persistent now-playing bar. |

## Publishing an update

1. Rebuild the package: `node scripts/pack-extension.mjs extensions/<name>` (in the launcher repo).
2. Upload the new `.basaltext` to a GitHub release here.
3. Bump the `version` and `url` in `feed.json` and push.
