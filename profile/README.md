NAV-Solutions 🛰️
================

NAv-Solutions is a framework providing GNSS libraries and applications, mostly written in Rust.  
The framework is published under the [Mozilla Public v2 license](https://www.mozilla.org/en-US/MPL/2.0/)
and [AGPLv3](https://www.gnu.org/licenses/agpl-3.0.en.html) when that applies.

## Parsers

We provide support for a few file formats, broadly used in GNSS and Geodesy applications. Some of them are
now well integrated in the Rust community. We want our parsers to go beyond providing content but truly
be the first stage of a complex processing pipeline. Most of them work both ways and allow data production as well.

- [RINEX (Receiver Independent EXchange) File parser](https://github.com/nav-solutions/rinex) that supports almost all types of RINEX files,
including RINEX file formatting. It comes with full CRINEX support. It is possible to deploy high level analysis
from just this library, by activating just a few library options

- [SP3 File parser](https://github/com/nav-solutions/sp3) for precise navigation. We support SP3 parsing and formatting.
Optionally, we provide processing methods to initialize a PPP algorithm from there.

- [CGGTTS File parser](https://github.com/nav-solutions/cggtts) supports CGGTTS file parsing and comes with an optional
CGGTTS solution solver and sky tracker, for common-view timing.

- [BINEX (Binary) parser](https://github.com/nav-solutions/binex): the only fully open-source GNSS format, is RINEX binary
equivalent. We provide basic support, both ways (encoder, decoder), for open-source real time applications.
The RINEX parser offers a BINEX to RINEX (and vice versa) bridge.

- [SINEX file parser](https://github.com/rtk-rs/sinex): for daily GNSS bias file publication processing.
Currently under development

## Community

Join us on [Discord](https://discord.gg/EqhEBXBmJh) where we discuss the latest developments, publish demos, provides FAQ and answer questions.

## Other Libraries
 
- [GNNS-Protos](https://github.com/nav-solutions/gnss-protos) to decode (and soon encode) GNSS protocols. Dedicated to real-time applications.

## Applications

- [CRX2RNX](https://github.com/nav-solutions/crx2rnx) CRINEX decompression tool
- [RNX2CRX](https://github.com/nav-solutions/rnx2crx) RINEX compression tool
- [UBX2RINEX](https://github.com/nav-solutions/ubx2rinex) capture U-Blox stream to RINEX
- [RINEX2BIN](https://github.com/nav-solutions/rinex2bin) RINEX serialization to BINEX
- [BIN2RINEX](https://github.com/nav-solutions/bin2rinex) capture BINEX stream to RINEX

## Ecosystem

This framework relies on the great libraries integrated to the Rust community, in particular:

- [Nyx-Space](https://github.com/nyx-space/)
  - `Hifitime` is our timing core and allows duration and timescales definition
  - `ANISE` is our navigation backbone
  - `Nyx` provides orbital determination (OD) and prediction anytime we need it
- [GeoRust](https://github.com/georust)
- [Nalgebra](https://github.com/dimforge/nalgebra) is used in particular in our P.V.T solver
