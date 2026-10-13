# chilpa-plugins

The list of plugins Chilpa offers to install, in `index.json`. Each plugin
lives in its own repository with its source and release ZIP. To write one,
start with [chilpa-plugins-sdk](https://github.com/vicrodh/chilpa-plugins-sdk).

```text
https://raw.githubusercontent.com/vicrodh/chilpa-plugins/main/index.json
```

Chilpa reads this catalog by default. Before installing, it checks the ZIP
against the SHA-256 listed here, and it asks you to approve the plugin's
permissions before enabling it.

| Plugin | Source | Package |
| --- | --- | --- |
| Radio | [chilpa-pg-radio](https://github.com/vicrodh/chilpa-pg-radio) | WASM |
| Podcasts | [chilpa-pg-podcasts](https://github.com/vicrodh/chilpa-pg-podcasts) | WASM |
| Playlist Importer | [chilpa-pg-playlist-import](https://github.com/vicrodh/chilpa-pg-playlist-import) | Linux x86_64 process |

An entry changes only after its release ZIP is published and its manifest,
SHA-256 and API version are checked against Chilpa. The `api` range is the
manifest's `api_version`; the SDK's `protocol-4` tag is a source revision,
not an API version.
