# Travis and Docker multi-architecture builds

This is one way to publish multi-architecture Docker builds. It may not be the best way.

The build runs on a single machine, which installs QEMU and a recent version of Docker with
[buildx](https://docs.docker.com/buildx/working-with-buildx/) support. Buildx runs the build in parallel on multiple
emulated architectures, then pushes the resulting images and manifest list.
