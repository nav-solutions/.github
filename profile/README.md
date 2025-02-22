RTK-rs 🛰️
==========

RTK-rs is a set of GNSS oriented tools and libraries. The core libraries are written in pure Rust.

## Framework

Our framework is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/).

1. Libraries

- [GNSS lib](https://github.com/rtk-rs/gnss) for high level definitions
- [GNSS Quality Control](https://github.com/rtk-rs/gnss-qc) for standardized fileset Qc and post processing
- [GNSS-RTK](https://github.com/rtk-rs/gnss-rtk) a Position Velocity TIme (PVT) solution solver

2. Applications

- [RT-NAVI](https://github.com/rtk-rs/rt-navi) High precision real time navigation

3. Command line utilities

- [RINEX-Cli](https://github.com/rtk-rs/rinex-cli) RINEX and SP3 post processing
  - including operations similar to TEQc
  - including a PVT solutions solver like RTKlib
  - include a CGGTTS solutions solver
- [CRX2RNX](https://github.com/rtk-rs/crx2rnx) CRINEX decompression tool
- [RNX2CRX](https://github.com/rtk-rs/crx2rnx) RINEX compression tool

## Ecosystem

`rtk-rs` relies or is closely tied to some great frameworks available
in Rust, among those we can cite

- [Nyx-Space](https://github.com/nyx-space/)
  - Hifitime for accurate timing and time scales definition
  - ANISE for navigation
  - Nyx for complex orbital functions
