---
title: Installation
subtitle: Installing tfsec on your local machine
author: tfsec
tags: [installation]
---

Install with brew/linuxbrew:

```bash
brew install tfsec
```

Install with Chocolatey:

```cmd
choco install tfsec
```

You can also grab the binary for your system from the [releases page](https://github.com/tfsec/tfsec/releases).

Alternatively, install with Go:

```bash
go get -u github.com/tfsec/tfsec/cmd/tfsec
```

## Usage

tfsec will scan the specified directory. If no directory is specified, the current working directory will be used.

The exit status will be non-zero if tfsec finds problems, otherwise the exit status will be zero.

```bash
tfsec .
```

## Use with Docker

As an alternative to installing and running tfsec on your system, you may
run tfsec in a Docker container.

To run:

```bash
docker run --rm -it -v "$(pwd):/src" tfsec/tfsec /src
```
