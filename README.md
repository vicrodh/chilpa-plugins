<img width="100%" alt="Chilpa Official Plugins: official plugins maintained by the project" src="assets/chilpa-official-plugins.png" />

# chilpa-plugins

The official plugin catalog of [Chilpa](https://github.com/vicrodh/chilpa), a native music player for
local libraries and self-hosted servers ([chilpa.app](https://chilpa.app)).
Plugins from independent authors are listed in the
[third-party catalog](https://github.com/vicrodh/chilpa-3rd-party-plugins).

Chilpa's installable plugin catalog is `index.json`. Each plugin
keeps its source and release ZIP in its own repository. The SDK and authoring
documentation live in [chilpa-plugins-sdk](https://github.com/vicrodh/chilpa-plugins-sdk).

## Catalog URL

```text
https://raw.githubusercontent.com/vicrodh/chilpa-plugins/main/index.json
```

Chilpa 0.1.0-beta uses that URL by default and includes an initial offline copy. Refresh in Settings > Plugins retrieves the current index. The host checks
the package SHA-256 before staging a release and still asks for permission
approval before enabling a plugin.

## Listed plugins

| Plugin | Source | What it does | Package |
| --- | --- | --- | --- |
| Radio | [chilpa-pg-radio](https://github.com/vicrodh/chilpa-pg-radio) | Stations from Radio Browser. No account. | WASM |
| Podcasts | [chilpa-pg-podcasts](https://github.com/vicrodh/chilpa-pg-podcasts) | Shows and episodes from PodcastIndex. No account. | WASM |
| Playlist Importer | [chilpa-pg-playlist-import](https://github.com/vicrodh/chilpa-pg-playlist-import) | Import playlist files and public playlists, then match tracks to local and connected sources. | Linux x86_64 / macOS Apple Silicon process |
| DSP | [chilpa-pg-dsp](https://github.com/vicrodh/chilpa-pg-dsp) | 8,772 measured headphone profiles and 53 listening presets. Expanded catalog and editor require Chilpa 0.1.3. | WASM |
| Nest | [chilpa-pg-nest](https://github.com/vicrodh/chilpa-pg-nest) | **Early-stage experimental.** CD shelves and optional player deck. Requires Chilpa 0.1.3. Ideas and feedback are welcome. | Linux x86_64 process |
| Mood | [chilpa-pg-mood](https://github.com/vicrodh/chilpa-pg-mood) | **Experimental.** Local mood and similarity analysis with offline models. No audio or analysis results are uploaded. Optional model download; noncommercial model license. | Linux x86_64 process |

Tidal and Spotify are listed in the [third-party catalog](https://github.com/vicrodh/chilpa-3rd-party-plugins).

Nest is in an early experimental stage. Share ideas, rough edges and test
results in its [issues](https://github.com/vicrodh/chilpa-pg-nest/issues).
Its trusted QML and native helper run inside Chilpa with application privileges.
Raspberry Pi builds and physical touchscreen validation remain pending.

Catalog updates require a published release ZIP, a checked manifest and
SHA-256, and a confirmed API version compatible with Chilpa. The
`protocol-4` SDK tag is a source revision, not a catalog API version.

Native plugins have separate ZIPs for each listed platform. Updated Chilpa hosts
select the current platform's `packages` entry and verify its checksum;
older Linux hosts retain the top-level package. Unsupported OS/architecture
entries are omitted from the visible catalog. The macOS native plugins
require the host build with Seatbelt process support. WASM packages remain
portable. The [SDK guide](https://github.com/vicrodh/chilpa-plugins-sdk/blob/main/wiki/Native-Plugins.md#platform-packages)
describes the package map and platform restrictions.
