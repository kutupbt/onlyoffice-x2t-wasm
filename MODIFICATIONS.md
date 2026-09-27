# Modifications

This is a **modified version** of ONLYOFFICE's document converter `x2t`
(`core`), originally developed by **Ascensio System SIA**
(<https://github.com/ONLYOFFICE/core>). It is based on ONLYOFFICE core
**9.4.0** (tag `v9.4.0.131`), compiled to WebAssembly.

The code carries ONLYOFFICE's copyright and licence notices, which must be
kept: GNU AGPL v3 with the additional terms in `core/LICENSE`. ONLYOFFICE is
a trademark of Ascensio System SIA; this version is not affiliated with or
endorsed by it.

## Changes by CryptPad (2019-12-20 – 2026-04-23)

From [cryptpad/onlyoffice-x2t-wasm](https://github.com/cryptpad/onlyoffice-x2t-wasm),
to compile `x2t` to WebAssembly with emscripten: build and linker settings
for emscripten, code adjusted where the WebAssembly toolchain differs (for
example `BinaryReader` made header-only), a wrapper entry point
(`wrap-main.cpp`, `pre-js.js`), and the Docker build. Changed code is
marked with `CryptPad` comments; the full history is in this repository.

## Changes by Kutup

- **2026-09-27:** fork notice (`KUTUP.md`); boost taken from its release
  tarball, checked by SHA-256, instead of cloning its submodules.
- **2026-09-27:** updated from ONLYOFFICE core 9.3.0.140 to 9.4.0 (`git
  subtree pull`), carrying CryptPad's changes across; built with ONLYOFFICE
  `build_tools` `v9.4.0.131`.

Every change is a commit on the `kutup` branch.
