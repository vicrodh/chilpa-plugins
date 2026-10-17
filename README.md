# chilpa-plugins

I publish Chilpa's installable plugin catalog in `index.json`. Each plugin
keeps its source and release ZIP in its own repository. The SDK and authoring
documentation live in [chilpa-plugins-sdk](https://github.com/vicrodh/chilpa-plugins-sdk).

## Catalog URL

```text
https://raw.githubusercontent.com/vicrodh/chilpa-plugins/main/index.json
```

I configure that URL by default in Chilpa 0.1.0-beta and bundle an initial
offline copy. Refresh in Settings > Plugins retrieves the current index. The host checks
the package SHA-256 before staging a release and still asks for permission
approval before enabling a plugin.

## Listed plugins

| Plugin | Source | What it does | Package |
| --- | --- | --- | --- |
| Radio | [chilpa-pg-radio](https://github.com/vicrodh/chilpa-pg-radio) | Stations from Radio Browser. No account. | WASM |
| Podcasts | [chilpa-pg-podcasts](https://github.com/vicrodh/chilpa-pg-podcasts) | Shows and episodes from PodcastIndex. No account. | WASM |
| Playlist Importer | [chilpa-pg-playlist-import](https://github.com/vicrodh/chilpa-pg-playlist-import) | Import playlist files and public playlists, then match tracks to local and connected sources. | Linux x86_64 process |
| DSP | [chilpa-pg-dsp](https://github.com/vicrodh/chilpa-pg-dsp) | Offline equalizer with vertical sliders, crossfeed and listening presets. Native DSD and DoP bypass processing. | WASM |
| Mood | [chilpa-pg-mood](https://github.com/vicrodh/chilpa-pg-mood) | **Experimental.** Local mood and similarity analysis with offline models. No audio or analysis results are uploaded. Optional model download; noncommercial model license. | Linux x86_64 process |
| Tidal | [chilpa-pg-tidal](https://github.com/vicrodh/chilpa-pg-tidal) | **Third-party, validated by Chilpa.** Library, discovery, playlists and playback. Requires a Tidal subscription. | Linux x86_64 process |

I list Tidal as an independently maintained third-party plugin by `vicrodh`,
with [validation evidence](https://github.com/vicrodh/chilpa-3rd-party-plugins/blob/177bb42dd0e147ee8d0f3659a5888304ee4e7ef2/validation/tidal-0.1.18.json)
for the published package. Inclusion in this catalog does not imply affiliation
with the service provider.

I update an entry only after publishing its matching release ZIP, checking
its manifest and SHA-256, and confirming its API version with Chilpa. The
`protocol-4` SDK tag is a source revision, not a catalog API version.
