NAV-Solutions 🛰️
================

NAV-Solutions (NAV-SLS) is a framework providing GNSS libraries and applications, mostly written in Rust.  

## Community

Join us on [Discord](https://discord.gg/EqhEBXBmJh) where we discuss the latest developments, publish demos, provides FAQ and answer questions.

## Parsers

We provide support for a few file formats, broadly used in GNSS and Geodesy applications. Some of them are
now well integrated in the Rust community. We want our parsers to go beyond reading data and truly be 
the first stage of complex processing pipelines. Most of them also work both ways and allow data production as well.

- [RINEX (Receiver Independent EXchange) File parser](https://github.com/nav-solutions/rinex) supports almost all types of RINEX files,
and comes with full CRINEX support, thanks to a modern rewrite of this algorithm.

- [SP3 File parser](https://github/com/nav-solutions/sp3) for precise navigation, typically required by PPP solutions.  
We support SP3 formatting as well and new features are being developed to provide Orbital Determination (OD).

- [CGGTTS File parser](https://github.com/nav-solutions/cggtts) for Timing solutions and remote clock comparison.
This comes with a solution solver and a sky tracker to deploy the so called common-view tracking.

- [BINEX (Binary) parser](https://github.com/nav-solutions/binex): the only fully open-source GNSS format, is the
RINEX binary equivalent. We support the basic frames and we provide an encoder as well.

- [SINEX File parser](https://github.com/rtk-rs/sinex): for daily GNSS bias files.
Currently under development.

## GNSS-RTK

Our [GNSS-RTK](https://github.com/nav-solutions/gnss-rtk) is a complete PVT solution solver, that supports both
PPP and RTK algorithms. It is sort of a modern rewrite of RTKLib, with its own specificities. For example, we provide
a single solver that can do both, and the API is also compatible with real-time navigation.

## Other Libraries
 
- [GNNS-Protos](https://github.com/nav-solutions/gnss-protos) to decode (and soon encode) GNSS protocols. Dedicated to real-time applications.

## Ecosystem

This framework relies on the great libraries integrated to the Rust community, in particular:

- [Nyx-Space](https://github.com/nyx-space/)
  - `Hifitime` is our timing core and allows duration and timescales definition
  - `ANISE` is our navigation backbone
  - `Nyx` provides orbital determination (OD) and prediction anytime we need it
- [GeoRust](https://github.com/georust)
- [Nalgebra](https://github.com/dimforge/nalgebra) is used in particular in our P.V.T solver
