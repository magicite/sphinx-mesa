# Sphinx Mesa
A simple Dockerfile for building a sphinx image suitable for building documentation for various projects.

# Base Image
Uses and extends the Sphinx base image as per [its image documentation](https://hub.docker.com/r/sphinxdoc/sphinx).

# Build
```
$ BUILDER=podman
$ $BUILDER build . -t sphinx-mesa:latest
```

# Usage
```
$ DOCS_ON_HOST=/Users/ben/my-docs
$ IMAGE_NAME=something
$ podman run -it --rm -v $DOCS_ON_HOST:/docs $IMAGE_NAME make -C /docs html"
```