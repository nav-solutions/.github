RTK-rs
======

RTK-rs is a set of tools to solve the RTK Differntial GNSS positioning problem.

It is based off high quality libraries available in Rust, spanning several ecosystems:

- [Hifitime](https://github.com/nyx-space/hifitime) for accurate timing and time scale supports
- [Nyx-space](https://github.com/nyx-space/nyx) for navigation and calculations at the scale of the solar system and beyond
- [RINEX](https://github.com/georust/rinex) for space vehicles, constellations, IGS precise orrbits and RINEX data support
- [RTCM](https://github.com/martinhakansson/rtcm-rs) for RTCM messages encoding and decoding in Rust
- [Ublox-rs](https://github.com/ublox-rs/ublox) for Ublox GNSS receivers management
- NMEA for NMEA frames parsing and processing
