# Building a OCI-native Container Image CI/CD Pipeline

The [Open Container Initiative](https://opencontainers.org/) is an open
governance structure for the express purpose of creating open industry
standards around container formats and runtimes [1].

This document describes a step-by-step procedure towards achieving a OCI-native
secure software supply chain.

## Build Images

[`stacker`](https://github.com/project-stacker/stacker) is a standalone tool
for building OCI images via a declarative yaml format. The output of the build
process is a container image in a OCI layout.

[`skopeo`](https://github.com/containers/skopeo) is a command line utility that
performs various operations on container images and image repositories.

## Image Registry

[`zot`](https://github.com/project-zot/zot) is a production-ready
vendor-neutral OCI image registry server purely based on OCI Distribution
Specification.

## Signing Images

[`cosign`](https://github.com/sigstore/cosign) is a tool that performs
container Signing, verification and storage in an OCI registry.

## Deploying Container Images

[`cri-o`](https://github.com/cri-o/cri-o) is an implementation of the
Kubernetes CRI (Container Runtime Interface) to enable using OCI (Open
Container Initiative) compatible runtimes. It is a lightweight alternative to
using Docker as the runtime for kubernetes.

## Container Image Verification

[`cosigned`](https://github.com/sigstore/cosign) is a image admission
controller that validates container images before deploying them.

# References

[1] https://opencontainers.org/

[2] https://github.com/project-stacker/stacker

[3] https://github.com/containers/skopeo

[4] https://github.com/project-zot/zot

[5] https://github.com/cri-o/cri-o
