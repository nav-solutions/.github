RTK-rs 🛰️
==========

RTK-rs is a set of GNSS oriented tools and libraries. The core libraries are written in pure Rust.

This workspace is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/)

## Ecosystem

`rtk-rs` hosts the following libraries

- [GNSS lib](https://github.com/rtk-rs/gnss) for high level definitions
- [GNSS-RTK](https://github.com/rtk-rs/gnss-rtk) a Position Velocity TIme (PVT) solution solver

`rtk-rs` hosts the following applications

- [RT-NAVI](https://github.com/rtk-rs/rt-navi) High precision real time navigation
  
`rtk-rs` relies heavily on the following ecosystems

- [Hifitime](https://github.com/nyx-space/hifitime) for accurate timing and time scales support
- [ANISE](https://github.com/nyx-space/nyx) for high precision navigation
- [Nyx-space](https://github.com/nyx-space/nyx) for complex orbital features

`rtk-rs` is used in the following applications

- [Resolve PPP solutions](https://github.com/georust/rinex) in `rinex-cli` application
- [Resolve CGGTTS solutions](https://github.com/georust/rinex) in `rinex-cli` application
