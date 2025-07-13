RTK-rs 🛰️
==========

RTK-rs is a set of GNSS libraries and applications, mostly written in Rust.  
The framework is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/)
and [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html) when that applies.

## Navigation

- [GNSS-RTK](https://github.com/rtk-rs/gnss-rtk) is our navigation solver.
It allows manual precise navigation, typically used in post-processing but its abstract interface
makes it also compatible with real-time navigation (see our [`rt-navi` Proof of Concept using a U-Blox](https://github.com/rtk-rs/rt-navi).
Unlike RTKLib, we propose a single solver that can do both RTK and PPP, possibly changing the navigation technique for each measurement,
offering maximal flexibility to the end-user, especially in their own application.  

- [RINEX-Cli](https://github.com/rtk-rs/rinex-cli) is our command-line application, dedicated
to file post-processing and capable to deploy GNSS-RTK and/or CGGTTS, for post processed PPP, RTK and timing solutions.

- All our parsers provide the basics to post-processed navigation, see down below.

## Parsers

`rtk-rs` provides several parsers that are now well integrated in the Rust community. Most of them supporting
not only parsing, but formatting as well, so they are actually compatible with data production. They also go beyond
parsing and propose the abstraction needed to deploy the basics of GNSS/GEO algorithms.

- [RINEX (Receiver Independent EXchange) file parser](https://github.com/rtk-rs/rinex) that supports almost all types of RINEX files,
including RINEX file formatting. It comes with full CRINEX support. It is possible to deploy high level analysis
from just this library, by activating just a few library options

- [SP3 file parser](https://github/com/rtk-rs/sp3) for precise navigation. We support SP3 parsing and formatting.
Optionally, we provide processing methods to initialize a PPP algorithm from there.

- [CGGTTS file parser](https://github.com/rtk-rs/cggtts) supports CGGTTS file parsing and comes with an optional
CGGTTS solution solver and sky tracker, for common-view timing.

- [BINEX parser](https://github.com/rtk-rs/binex): the only fully open-source GNSS format, is RINEX binary
equivalent. We provide basic support, both ways (encoder, decoder), for open-source real time applications.
The RINEX parser offers a BINEX to RINEX (and vice versa) bridge.

- [SINEX file parser](https://github.com/rtk-rs/sinex): for daily GNSS bias file publication processing.
Currently under development

## Community

Join us on [Discord](https://discord.gg/EqhEBXBmJh) where we discuss the latest developments, publish demos, provides FAQ and answer questions.

## Other Libraries
 
- [GNSS Quality Control](https://github.com/rtk-rs/gnss-qc) for standardized fileset Qc and post processing
- [GNNS-Protos](https://github.com/rtk-rs/gnss-protos) to decode (and soon encode) GNSS protocols
- [NTRIP Client](https://github.com/rtk-rs/ntrip-client) for RTCM reception over TCP/HTTP using NTRIP v1 or v2 protocol
- [SINEX parser and writer](https://github.com/rtk-rs/sinex) for SINEX files management, PPP processing pipelines and constellations analysis

## Applications

- [RINEX-Cli](https://github.com/rtk-rs/rinex-cli) RINEX and SP3 post processing
  - including operations similar to TEQc
  - including a PVT solutions solver like RTKlib
  - include a CGGTTS solutions solver
- [CRX2RNX](https://github.com/rtk-rs/crx2rnx) CRINEX decompression tool
- [RNX2CRX](https://github.com/rtk-rs/rnx2crx) RINEX compression tool
- [UBX2RINEX](https://github.com/rtk-rs/ubx2rinex) capture U-Blox stream to RINEX
- [RT-NAVI](https://github.com/rtk-rs/rt-navi) Real Time Navigation, currently limited to U-Blox receivers
- [RINEX2BIN](https://github.com/rtk-rs/rinex2bin) RINEX serialization to BINEX
- [BIN2RINEX](https://github.com/rtk-rs/bin2rinex) capture BINEX stream to RINEX

## Ecosystem

`rtk-rs` relies or is closely tied to some great frameworks available, in particular:

- [Nyx-Space](https://github.com/nyx-space/)
  - Hifitime for accurate timing and time scales definition
  - ANISE for navigation
  - Nyx for complex orbital functions
- [Geo by GeoRust](https://github.com/georust/geo)
