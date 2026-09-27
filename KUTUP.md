# Kutup's fork of the x2t WebAssembly converter

This is [Kutup](https://github.com/kutupbt/kutup)'s fork of CryptPad's
[`onlyoffice-x2t-wasm`](https://github.com/cryptpad/onlyoffice-x2t-wasm):
OnlyOffice's document converter `x2t`, from
[ONLYOFFICE/core](https://github.com/ONLYOFFICE/core) (a git subtree in
`core/`), with CryptPad's changes to compile it to WebAssembly. Kutup
converts documents with it in the browser; the server never sees their
content.

- **Branch `kutup`** is what Kutup ships: CryptPad's `v9.3.0+0` (ONLYOFFICE
  core 9.3.0.140), merged in over `v7.3+1`; Kutup's own changes go on it.
- **`main`** follows CryptPad's `main`, for pulling their updates.
- **Releases** are tagged `kutup-<CryptPad version>.<n>` (for example
  `kutup-v9.3.0+0.1`). Each release notes the exact commit it was built from.

## Build

```sh
docker build --target output -o output .   # output/x2t.zip and its .sha512
```

The toolchain is pinned in the Dockerfile (emscripten, boost, gumbo,
katana). Kutup's packaging
([kutup-office-assets](https://github.com/kutupbt/kutup-office-assets))
pins the release by URL and SHA-512.

## Updating

From CryptPad: merge or rebase `kutup` onto a newer CryptPad tag. From
OnlyOffice directly: `git subtree pull --prefix core` as in
[README.md](README.md). Then build, test conversion in Kutup, and release.

## Licence

AGPL-3.0, with the ONLYOFFICE Section 7 additional terms in the source files
(keep the original product logo and legal notices; no trademark rights).
ONLYOFFICE is a trademark of its owner; this fork is not affiliated with or
endorsed by ONLYOFFICE or CryptPad.
