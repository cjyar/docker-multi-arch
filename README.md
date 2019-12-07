# Travis and Docker multi-architecture builds

This is one way to publish multi-architecture Docker builds. It may not be the best way.

Travis uses its build matrix to build on 4 different architectures in parallel. Each build pushes its own docker image
to the same repository, using a tag with the architecture name embedded in it.

A final build step creates a manifest list, aka fat image, aka multi-architecture image. That final product gets pushed
to the same repository as the per-architecture images.
