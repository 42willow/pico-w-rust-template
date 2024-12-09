# Raspberry Pi Pico W - Rust Template

This is a template repository to help you get started with development on the Raspberry Pi Pico W using Rust.

Includes:

- A basic blink example from the [embassy-rs/embassy](https://github.com/embassy-rs/embassy/blob/main/examples/rp/src/bin/wifi_blinky.rs) repository.
- elf2uf2 tool to convert the ELF file to a UF2 file.
- A Nix flake to develop your project in a reproducible environment.

## Usage

```shell
git clone https://github.com/42willow/pico-w-rust-template
cd pico-w-rust-template
# Enter the development environment
nix develop
# Upload the UF2 file to the Pico
cargo run --release
```

## FAQ

### Error: `Unable to find mounted pico`

Make sure the Pico is in bootloader mode. You can do this by holding the `BOOTSEL` button while plugging in the Pico. Then ensure that you have mounted the Pico by running `ls /run/media/$USER`.

If the Pico is not mounted, any easy way to fix this is to open a file manager mount it manually.
