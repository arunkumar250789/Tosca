# `Tosca`

This repository is organized as a Cargo workspace that includes several crates.
The main create is [tosca](./crates/tosca), a Rust library that provides a set of
APIs and interfaces to:

- Create and manage HTTP `Rest` routes
- Define a device and its methods
- Associate some hazards to a device

It can even run on an embedded system since it is a `no_std` library.

The [tosca-os](./crates/tosca-os) and [tosca-esp32c3](./crates/tosca-esp32c3)
are two Rust libraries which make use of the `tosca` library as dependency to
define the APIs for their respective architectures.

The `tosca-os` library is thought for firmware which run on operating systems.
In the [tosca-os/examples](./crates/tosca-os/examples) directory, a simple
device firmware has been implemented as examples: a [light](./crates/tosca-os/examples/light).

The `tosca-esp32c3` library is thought for firmware which run on a `ESP32-C3`
board.
In the [tosca-esp32c3/examples](./crates/tosca-esp32c3/examples) directory,
various device firmware have been implemented.
