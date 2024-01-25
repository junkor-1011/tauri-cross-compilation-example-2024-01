# Tauri Cross Platform build example(Linux -> Windows)

## Requirements

OS:

- Linux(x86_64)

Rust:

- rustup@1.26.0
- cargo@1.75.0

Nodejs:

- node v20 LTS
- pnpm@8.14.3

### Tools Setup

```sh
# add target
rustup target add x86_64-pc-windows-msvc

# cross-compilation tools
cargo install cross@0.2.5
cargo install cargo-xwin@0.16.3
```

## Build

### x86_64-pc-windows-msvc

```sh
pnpm dist:win-msvc

# equivalent to
# pnpm build
# 
# cd tauri-src
# 
# cargo xwin build --release \
#     --features custom-protocol \
#     --target x86_64-pc-windows-msvc
```

### x86_64-pc-windows-gnu

```sh
pnpm dist:win-msvc

# equivalent to
# pnpm build
# 
# cd tauri-src
# 
# cross build --release \
#     --features custom-protocol \
#     --target x86_64-pc-windows-gnu
```
