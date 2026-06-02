# go-deltasync

🌐 **[Website](https://go-deltasync.github.io)** · 📚 **[Documentation](https://go-deltasync.github.io/docs/)**

**Pure-Go, cgo-free building blocks for delta synchronization** — move and store
only the bytes that actually change between two versions of a file.

Each tool is a clean-room reimplementation that is **wire-compatible with its
reference implementation** (verified by cross-implementation tests in CI), ships
as a single static binary **and** an importable Go package, and is held to
**100% test coverage** by a CI gate.

## Tools

| Repo | What it is | Interoperates with |
|------|------------|--------------------|
| [**zsync2**](https://github.com/go-deltasync/zsync2) | zsync — download only the changed bytes from a vanilla HTTP server | zsync |
| [**rdiff**](https://github.com/go-deltasync/rdiff) | rsync signature / delta / patch workflow | librsync |
| [**zchunk**](https://github.com/go-deltasync/zchunk) | content-defined chunked container + HTTP-Range delta | zchunk (Fedora/DNF) |
| [**vcdiff**](https://github.com/go-deltasync/vcdiff) | VCDIFF (RFC 3284) delta encode/decode | xdelta3 |
| [**bita**](https://github.com/go-deltasync/bita) | differential file synchronization over HTTP (`.cba` archives) | [oll3/bita](https://github.com/oll3/bita) |

## Principles

- **Pure Go, no cgo** — one static cross-platform binary, always buildable from source.
- **Wire-compatible** — interoperates with the reference tool, checked by `-tags=compat` tests.
- **100% test coverage** — enforced as a CI gate on every repository.
- **Reusable** — every tool is both a command and an importable library package.

## Links

- **Website (landing):** <https://go-deltasync.github.io> — built with Hugo.
- **Documentation:** <https://go-deltasync.github.io/docs/> — MkDocs Material,
  versioned with [mike]; source in [go-deltasync/docs](https://github.com/go-deltasync/docs).

[mike]: https://github.com/jimporter/mike
