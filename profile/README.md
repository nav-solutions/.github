RTK-rs 🛰️
==========

RTK-rs is a set of GNSS oriented tools and libraries. The core libraries are written in pure Rust.

Join [our Discord channel](https://discord.gg/duETmeGc) for FAQ, the latest news and more learning material.

## Framework

Our framework is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/)
and [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html) when that applies.

1. Libraries

- [RINEX (Receiver Independent EXchange) parser](https://github.com/rtk-rs/rinex) for RINEX file management and processing
- [SP3 parser](https://github.com/rtk-rs/sp3) for SP3 files management and PPP processing pipelines 
- [GNSS lib](https://github.com/rtk-rs/gnss) for high level definitions
- [GNSS-RTK](https://github.com/rtk-rs/gnss-rtk) a Position Velocity TIme (PVT) solution solver
- [GNSS Quality Control](https://github.com/rtk-rs/gnss-qc) for standardized fileset Qc and post processing
- [BINEX (Binary EXchange) parser](https://github.com/rtk-rs/binex) the only open source real-time GNSS streaming format
- [SINEX parser and writer](https://github.com/rtk-rs/sinex) for SINEX files management, PPP processing pipelines and constellations analysis

2. Applications

- [RT-NAVI](https://github.com/rtk-rs/rt-navi) High precision real time navigation

3. Command line utilities

- [RINEX-Cli](https://github.com/rtk-rs/rinex-cli) RINEX and SP3 post processing
  - including operations similar to TEQc
  - including a PVT solutions solver like RTKlib
  - include a CGGTTS solutions solver
- [CRX2RNX](https://github.com/rtk-rs/crx2rnx) CRINEX decompression tool
- [RNX2CRX](https://github.com/rtk-rs/crx2rnx) RINEX compression tool
- [RINEX2BIN](https://github.com/rtk-rs/rinex2bin) RINEX serialization to BINEX
- [UBX2RINEX](https://github.com/rtk-rs/ubx2rinex) capture U-Blox stream to RINEX
- [BIN2RINEX](https://github.com/rtk-rs/bin2rinex) capture BINEX stream to RINEX

## Ecosystem

`rtk-rs` relies or is closely tied to some great frameworks available
in Rust, among those we can cite

- [Nyx-Space](https://github.com/nyx-space/)
  - Hifitime for accurate timing and time scales definition
  - ANISE for navigation
  - Nyx for complex orbital functions
