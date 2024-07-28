RTK-rs 🛰️
==========

RTK-rs is a set of tools and libraries to work with GNSS. The core libraries are written in pure Rust.

## Ecosystem

`rtk-rs` hosts the following libraries

- [GNSS](https://github.com/rtk-rs/gnss) for high level definitions to work with GNSS in Rust
- [RTK](https://github.com/rtk-rs/gnss-rtk) is a position solver, to resolve precise positions

`rtk-rs` hosts the following applications

- [RT-NAVI](https://github.com/rtk-rs/rt-navi) High precision real time navigation
  
`rtk-rs` relies heavily on the following ecosystems

- [Hifitime](https://github.com/nyx-space/hifitime) for accurate timing and time scales support
- [ANISE](https://github.com/nyx-space/nyx) for high precision navigation
- [Nyx-space](https://github.com/nyx-space/nyx) for complex orbital features

`rtk-rs` is used in the following applications

- [Resolve PPP solutions](https://github.com/georust/rinex) in the `rinex-cli` application
- [Resolve CGGTTS solutions](https://github.com/georust/rinex) in the `rinex-cli` applications
