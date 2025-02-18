RTK-rs 🛰️
==========

RTK-rs is a set of GNSS oriented tools and libraries. The core libraries are written in pure Rust.

This workspace is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/)

## Framework

`rtk-rs` hosts the following libraries

- [GNSS lib](https://github.com/rtk-rs/gnss) for high level definitions
- [GNSS Quality Control](https://github.com/rtk-rs/gnss-qc) for standardized fileset Qc and post processing
- [GNSS-RTK](https://github.com/rtk-rs/gnss-rtk) a Position Velocity TIme (PVT) solution solver

`rtk-rs` hosts the following applications

- [RT-NAVI](https://github.com/rtk-rs/rt-navi) High precision real time navigation
  
`rtk-rs` relies heavily on the following frameworks

- [Nyx-Space](https://github.com/nyx-space/)
  - Hifitime for accurate timing and time scales definition
  - ANISE for navigation
  - Nyx for complex orbital functions

`rtk-rs` is used in the following applications

- [Resolve PPP solutions](https://github.com/georust/rinex) in `rinex-cli` application
- [Resolve CGGTTS solutions](https://github.com/georust/rinex) in `rinex-cli` application
