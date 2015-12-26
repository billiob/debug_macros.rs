debug_macros
============

A simple set of macros (only one so far) to help debugging.

Currently it contains:
 * `dbg!()` is a macro to print line only when a crate is compiled in debug
   mode. In release mode, `dbg!()` is a noop.
   It prints the crate, the file and and the line where `dbg!()` is called.

### Installation

This crate is fully compatible with Cargo. Just add it to your `Cargo.toml`:

```toml
[dependencies]
debug_macros = "*"
```

### Quick example

```rust
#[macro_use]
extern crate debug_macros;

fn main() {
    dbg!("2+2={}", 2+2);
}
```

