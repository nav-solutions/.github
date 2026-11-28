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

- [IONEX (Ionosphere Maps) parser](https://github.com/nav-solutions/ionex), a snapshot of the ionosphere state, in 2D or 3D.
The library offers several post-processing features, such as spatial interpolation.

- [DORIS (special Observation) RINEX parser](https://github.com/nav-solutions/doris), the DORIS measurement network is operated
and maintained by CNES.

- [SP3 File parser](https://github/com/nav-solutions/sp3) for precise navigation, typically required by PPP solutions.  
We support SP3 formatting as well and new features are being developed to provide Orbital Determination (OD).

- [CGGTTS File parser](https://github.com/nav-solutions/cggtts) for Timing solutions and remote clock comparison.
This comes with a solution solver and a sky tracker to deploy the so called common-view tracking.

- [SINEX File parser](https://github.com/rtk-rs/sinex): for daily GNSS bias files.
Currently under development.

## `GNSS-RTK`: navigation solver 🌏

[GNSS-RTK](https://github.com/nav-solutions/gnss-rtk) is a complete PVT solution solver,
it supports both absolute or differential techniques (so called Real Time Kinematics), with simple
configuration and a lot of flexibility. It is abstract and can apply to either real-time or post-processing.

- [GNSS-Qc](https://github.com/nav-solutions/gnss-qc) takes advantage of that to support both real-time
or post-processed navigation and provide advanced operations, such as PPP solutions solving or CGGTTS track post fitting,
from all support input streams
- [rinex-cli](https://github.com/nav-solutions/rinex-cli) applies it to post-processed workflow
- [rt-navi](https://github.com/nav-solutions/rt-navi) applies `GNSS-RTK` to an U-Blox receiver operated
in "manual" mode
- [gnss-rcv](https://github.com/mx4/gnss-rcv) applies `GNSS-RTK` to symbols sampled by a RTL-SDR

## `GNSS-Qc`: an abstract and powerful processor 📈

[`GNSS-Qc`](https://github.com/nav-solutions/gnss-qc) is an abstract and complex library which regroups the core processing algorithms (or geo "pipelines) required by
GNSS navigation, timing applications and much more. It works is Multi Input Single Output (`MISO`) engine that deploys complex
algorithms and streams solutions into a single output. 

## RINEX CLI (Command line) 📈

[`rinex-cli`](https://github.com/nav-solutions/rinex-cli) is our post-processing command line application.
It deploys the `GNSS-Qc` processor dedicated to post-processing workflows, so remains mostly limited to input text/gzip files.
It can perform Qc analysis, sort of like `TEQc`.
It integrates the position solver and is able to solve CPP, SPP, PPP or RTK-PPP solutions, similar to some of the `RTKLlib` toolbox.
It is also capable of post-fitting CGGTTS tracks for post-processed common-view time comparison.
It offers several Ionosphere related analysis, such as `tec` projection from IONEX files.

## `NTRIP` Client 💻

I created a small [NTRIP client](https://github.com/nav-solutions/ntrip-client) wrapped as a minimalistic library that anyone could import into their application.
The client conntects to any server and supports secure connections. Helpers for Centipede network exist. The client deploys the `rtcm-rs` parser and forwards them
to the external application. The client relies on `tokio` to handle the socket.

## GNSS Radio protocols 🔭

This framework offers a few options to deal with the GNSS radio protocols, mostly navigation messages,
which are the binary mesasges sent by satellites enabling real-time navigation.

- [`GNSS-protos`](https://github.com/nav-solutions/gnss-protos) provides encoder and decoders for some of the most
common navigation messages. It currently suppports (both ways)
  - GPS L1 C/A navigation messages
  - QZSS L1 C/A navigation messages (same protocol)
  - Galileo I-NAV navigation messages

## `BINEX` 

BINEX is the binary equivalent of the (ASCII) RINEX format, mostly in the sense that it is fully open-source.
This framework proposes three options to dealing with that format:

- The [BINEX parser](https://github.com/nav-solutions/binex) to encode and parse BINEX streams
- [UBX2RINEX](https://github.com/nav-solutions/ubx2rinex) a command-line tool to collect RINEX files from U-Blox receivers (or UBX captures).
- [RINEX2BIN](https://github.com/nav-solutions/ubx2rinex) a command-line tool to serialize RINEX to all protocols we support

## `rt-navi`

[RT-NAVI (Real-Time Navigation)](https://github.com/nav-solutions/rt-navi) is a proof-of-contept that our `GNSS-RTK` solver applies to real-time navigation as well.
We do this by operating a U-Blox receiver in "raw" mode.

## Ecosystem

This framework relies on the great libraries integrated to the Rust community, in particular:

- [Nyx-Space](https://github.com/nyx-space/)
  - `Hifitime` is our timing core and allows duration and timescales definition
  - `ANISE` is our navigation backbone
  - `Nyx` provides orbital determination (OD) and prediction anytime we need it
- [GeoRust](https://github.com/georust)
- [Nalgebra](https://github.com/dimforge/nalgebra) is used in particular in our P.V.T solver
