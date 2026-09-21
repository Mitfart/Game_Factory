# `/gf-start` asset intake

Read this file only when the Operator supplies assets.

1. Resolve only paths explicitly supplied by the Operator. Never browse adjacent Asset Library content.
2. Precompute the complete mapping before copying: a file maps to `assets/<filename>`; a directory maps to `assets/<directory-name>/<relative source path>`. Preserve every filename and relative path.
3. If two sources map to one destination, or any destination exists without a matching completed-copy record, stop before copying. Never overwrite, rename, convert, deduplicate, or mutate either side.
4. Copy every file byte-for-byte and verify it with a cryptographic hash or byte comparison.
5. Delegate inspection to a Builder only after copying. It may read only paths under this Game Project's `assets/` tree, may not search the Asset Library, and reports likely use/technical observations without inferring licensing.
6. Write one `ASSETS.md` row per file: absolute source path, project-relative destination, Operator-supplied purpose, supplied license/attribution, and byte-verification result.

On resume, verify recorded source/destination pairs and reuse exact verified copies. A mismatch or unrecorded collision is a stop, not permission to overwrite.
