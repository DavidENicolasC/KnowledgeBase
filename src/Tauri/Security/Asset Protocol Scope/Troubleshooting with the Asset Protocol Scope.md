|Symptom|Things to check|
|---|---|
|“asset protocol not configured to allow the path”|Path must match an **`allow`** pattern; **`deny`** overrides **`allow`**. Use **absolute** patterns or **`$VAR`/`$HOME`** style variables that match how the path is resolved on disk.|
|Works for normal folders but not under **`.cache`** / **`.config`**|On Unix, default **`requireLiteralLeadingDot`** behavior: use a literal `.segment` in the pattern, or set **`requireLiteralLeadingDot`: `false`** in the object `scope` (see [tauri#13788](https://github.com/tauri-apps/tauri/issues/13788)).|
|User picked a folder at runtime; still blocked after restart|You may need [**persisted-scope**](https://tauri.app/plugin/persisted-scope/) with the **`protocol-asset`** feature, not only `tauri.conf.json` entries.|
|Broad `**` seems wrong|Try `**/*` for file-oriented globs; see [Embedding Additional Files](https://tauri.app/develop/resources/) for similar `**` vs `**/*` guidance in bundle resources.|
|Scope like `["*/**"]` never matches on Linux|Resolved paths are **absolute**; use **`$...` variables**, a leading **`/`**, or another pattern that matches the real path (see above).