# docker-vernemq

A multiarch image for Vernemq

This combines the upstream Debian Buster Dockerfile (available [here](https://github.com/vernemq/docker-vernemq)) with
the [ARM-compatible Dockerfile](https://github.com/ysoftwareab/docker-vernemq/tree/arm64-1.12.30) that was made by
[Andrei Neculau](https://github.com/andreineculau) into a single multi-arch manifest.

To build, run
```sh
docker buildx build \
  --tag <image tag> \
  --platform=linux/arm64,linux/amd64 \
  --build-arg VERNEMQ_VERSION=<vernemq version> \
  --push \
  .
```

This image is also available [here](https://hub.docker.com/r/dwsr/vernemq).
