# MANIFEST

| tool | version | platform | folder | from (archive) | licence | sha256 of archive | added |
|---|---|---|---|---|---|---|---|
| LiveCode Community Server | 7.1.4 | Windows 32-bit (runs from WSL) | `livecode-server/7.1.4-win-x86/` | `Installers/LiveCodeCommunityServer-7_1_4-Windows.zip` | GPLv3 (Community) | 8e4ffd1256b283aabf77cb8444b4e78b6474a1d367c1dd0d4ff979fc982d20d7 | 2026-11-13 |
| LiveCode Community Server | 9.6.3 | Windows x86_64 (runs from WSL) | `livecode-server/9.6.3-win-x64/` | `Installers/LiveCodeCommunityServer-9_6_3-Windows-x86_64.zip` | GPLv3 (Community) | 78fb1ab0ad695d0111733e2d38c3be952fca12dcfbfd2e6a1870aa45073e10bb | 2026-11-13 |
| LiveCode Community Server | 9.6.3 | **Linux x86_64 (native in WSL)** | `livecode-server/9.6.3-linux-x64/` | `Installers/LiveCodeCommunityServer-9_6_3-Linux-x86_64.zip` | GPLv3 (Community) | e7f92cf82074b69349307c1b904014d3949284546659ce72fb032972d99dcb76 | 2026-11-13 |
| iGame3D Pro external + its DLLs, Player, Data | 2007 (051707) | Windows 32-bit | `igame3d_last_working_Livecode_6_version/` | the owner's archive | the owner's own (iGame3D); Newton, OpenAL, Ogg Vorbis, Lua: their own licences | - | 2026-11-13 |

## Use

```bash
cd ~/projects/LIB_BIN/livecode-server/9.6.3-linux-x64 && ./livecode-community-server ../../tests/linux_generica.lc
cd ~/projects/LIB_BIN/livecode-server/7.1.4-win-x86 && ./livecode-community-server.exe "$(wslpath -w ../../tests/version.lc)"
```
Prints `engine 7.1.4 | platform Win32 | processor x86`. A server script is `<?lc ... ?>` text.

- **7.1.4 (32-bit)** is the only one that can load the iGame3D external (32-bit DLL): see
  `~/projects/LIB_ig3d/IGAME3D_EXTERNAL.md`; tests `tests/ig3d_probe.lc` (load: 123 commands,
  53 functions) and `tests/ig3d_lua.lc` (init + Lua: prints 42; crashes on exit, no shutdown yet).
- **9.6.3 Linux** runs natively in WSL, no Windows hop: tested 2026-11-13, `tests/linux_generica.lc` loads
  LIB_GENERICA (`start using`) and reads the genetic_anomaly ranks. Use it first for headless xTalk.
- **9.6.3 (64-bit)** is the one for harvesting stacks one process at a time (LIB_XTJSON A-11).
