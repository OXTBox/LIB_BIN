# LIB_BIN

Third-party applications and binaries the LIB_ARRAY depends on (engines, servers, command-line
tools), kept in one place. **Internal only: never published.**

- One folder per tool, one sub-folder per version and platform: `livecode-server/9.6.3-linux-x64/`.
- Git tracks only this README and `MANIFEST.md`; the binaries themselves are ignored (large,
  licensed by their makers). The manifest's checksum confirms a copy is the right one.
- Tools find this folder through `$LIB_BIN` (default `~/projects/LIB_BIN`), never a hard-coded path.
- Add a tool: unpack it into its versioned folder, then add its row to `MANIFEST.md`
  (`sha256sum` of the archive you installed from).

## Licence

GPL-3.0 (see `LICENSE`), because the xTalk work here is built on the GPL-licensed LiveCode Community 9 engine. Copyright (c) 2026 xAction.
