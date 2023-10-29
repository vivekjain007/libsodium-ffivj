## libsodium-ffivj

This crate is based on libsodium-ffi crate sources. This crate only upgrades the rust edition to 2021 & zip and bindgen dependencies.  

Rust native binding to [libsodium](https://github.com/jedisct1/libsodium)

```toml
# Cargo.toml
[dependencies]
libsodium-ffivj = "0.2"
```

## Usage

Environement variables

- `SODIUM_LIB_DIR=/path/to/libsodium` for telling cargo where to find libsodium (Work with `SODIUM_INCLUDE_DIR`)

- `SODIUM_INCLUDE_DIR=/path/to/libsodium/include` for telling `bindgen` where to find libsodium's headers (Work with `SODIUM_LIB_DIR`)

- `SODIUM_STATIC=yes` for telling cargo to static-link libsodium

- `SODIUM_BUILD_STATIC=yes` force build from source instead of trying to find libsodium in system-wide

Examples

```bash
## Specify paths by hand
# This is the path to the directory of `/usr/local/lib/libsodium.a`
export SODIUM_LIB_DIR=/usr/local/lib
# This is the path to the directory of `/usr/local/include/sodium.h`
export SODIUM_INCLUDE_DIR=/usr/local/include

## Uses system-wide libsodium
# Statically link system-wide libsodium
export SODIUM_STATIC=yes

## Build libsodium from source
export SODIUM_BUILD_STATIC=yes
```

## Thanks

- This is borrowed from [libsodium-ffi](https://github.com/zonyitoo/libsodium-ffi.git) project.
