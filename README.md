# @io/flate2 — Gzip/Deflate/Zlib Compression for Zeta

Auto-converted from [flate2](https://crates.io/crates/flate2) v1.1.9 via [Dark Factory](https://github.com/murphsicles/dark-factory).

## Features
| Format | Read | Write | BufRead |
|--------|------|-------|---------|
| **Gzip** | GzDecoder | GzEncoder | MultiGzDecoder |
| **Zlib** | ZlibDecoder | ZlibEncoder | — |
| **Deflate** | DeflateDecoder | DeflateEncoder | — |

All formats support streaming compression/decompression with configurable compression levels (0-9) and strategies.

## Usage
```zeta
let data = b"hello world";
let mut encoder = GzEncoder::new(data.as_slice(), Compression::default());
let mut compressed = Vec::new();
encoder.read_to_end(&mut compressed);
```

## Stats: ~4,655 lines across 21 source files, 0 unsupported items

## License
MIT