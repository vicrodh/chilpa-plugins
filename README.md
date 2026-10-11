# chilpa-plugins

I publish Chilpa's installable plugin catalog in `index.json`. Each plugin
keeps its source and release ZIP in its own repository. The SDK and authoring
documentation live in [chilpa-plugins-sdk](https://github.com/vicrodh/chilpa-plugins-sdk).

## Catalog URL

```text
https://raw.githubusercontent.com/vicrodh/chilpa-plugins/main/index.json
```

I add that URL in Chilpa's **Plugin repository URL** field. The host checks
the package SHA-256 before staging a release and still asks for permission
approval before enabling a plugin. The current host does not add this URL
automatically; making it the built-in default requires a separate host change.

## Listed plugins

| Plugin | Source | Package |
| --- | --- | --- |
| Radio | [chilpa-pg-radio](https://github.com/vicrodh/chilpa-pg-radio) | WASM |
| Podcasts | [chilpa-pg-podcasts](https://github.com/vicrodh/chilpa-pg-podcasts) | WASM |
| Playlist Importer | [chilpa-pg-playlist-import](https://github.com/vicrodh/chilpa-pg-playlist-import) | Linux x86_64 process |

I update an entry only after publishing its matching release ZIP, checking
its manifest and SHA-256, and confirming its API version with Chilpa. The
`protocol-4` SDK tag is a source revision, not a catalog API version.
