RTK-rs
======

RTK-rs is a set of tools (applications) and libraries to work with GNSS and resolve precise positions in Rust.

## Ecosystem :crab:

`rtk-rs` hosts the following Rust libraries

- [GNSS](https://github.com/rtk-rs/gnss) for high level definitions to work with GNSS in Rust

`rtk-rs` relies heavily on the following ecosystems

- [Hifitime](https://github.com/nyx-space/hifitime) for accurate timing and time scales support
- [Nyx-space](https://github.com/nyx-space/nyx) for navigation at the scale of the Solar System and beyond

`rtk-rs` is used in the following applications

- [RINEX Processing](https://github.com/georust/rinex) to post process RINEX and resolve positions
- [RNX2CGGTTS](https://github.com/georust/rinex) generate CGGTTS data for high accuracy time transfer
