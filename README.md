# Knowledge Graph Reader — release feed

Public download and update feed for **Knowledge Graph Reader**, a local-first
knowledge-graph reader for macOS (Apple silicon). The app itself is developed in a
private repository; this one holds only what the app has to fetch anonymously:

- `latest.json` — the manifest Tauri's updater reads
  (`…/releases/latest/download/latest.json`): the version, the `.app.tar.gz`, and the
  minisign signature of that archive.
- the update archive and its `.sig`.

The app verifies the signature against the public key compiled into it, and installs
nothing unless that check passes.
