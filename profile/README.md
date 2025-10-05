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

- [IONEX (Ionosphere Maps) parser](https://github.com/nav-solutions/ionex), a snapshot of the ionosphere state, in 2D or 3D

- [DORIS (special Observation) RINEX parser](https://github.com/nav-solutions/doris), the DORIS measurement network is operated
and maintained by CNES.

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

## RINEX CLI (Command line)

[RINEX-Cli](https://github.com/nav-solutions/rinex-cli) is our post-processing command line application.
It wraps the RINEX and SP3 parsers, our P.V.T and CGGTTS solvers to allow three major workflows:
- the Quality Check (Qc) pre-navigation analysis
- P.V.T solutions solving
- CGGTTS solutions solving

## Other Libraries
 
- [GNNS-Protos](https://github.com/nav-solutions/gnss-protos) to decode (and soon encode) GNSS protocols. Dedicated to real-time applications.
- [NTRIP client](https://github.com/nav-solutions/ntrip-client) is a small object that facilitates connecting to NTRIP servers
for real-time RTCM messaging. It uses `tokio` to handle the socket.

## Other tools

- [UBX2RINEX](https://github.com/nav-solutions/ubx2rinex) a command-line tool to collect RINEX files from U-Blox receivers (or UBX captures).
- [RINEX2BIN](https://github.com/nav-solutions/ubx2rinex) a command-line tool to serialize RINEX to all protocols we support
- [RT-NAVI (Real-Time Navigation)](https://github.com/nav-solutions/rt-navi) is a proof-of-contept that our `GNSS-RTK` solver applies to real-time navigation as well.
We do this by operating a U-Blox receiver in "raw" mode.

## Ecosystem

This framework relies on the great libraries integrated to the Rust community, in particular:

- [Nyx-Space](https://github.com/nyx-space/)
  - `Hifitime` is our timing core and allows duration and timescales definition
  - `ANISE` is our navigation backbone
  - `Nyx` provides orbital determination (OD) and prediction anytime we need it
- [GeoRust](https://github.com/georust)
- [Nalgebra](https://github.com/dimforge/nalgebra) is used in particular in our P.V.T solver
