# console

[![PkgGoDev](https://pkg.go.dev/badge/github.com/charmbracelet/console)](https://pkg.go.dev/github.com/charmbracelet/console)
[![Build Status](https://github.com/charmbracelet/console/workflows/CI/badge.svg)](https://github.com/charmbracelet/console/actions?query=workflow%3ACI)
[![Go Report Card](https://goreportcard.com/badge/github.com/charmbracelet/console)](https://goreportcard.com/report/github.com/charmbracelet/console)

Golang package for dealing with consoles.  Light on deps and a simple API.

## Modifying the current process

```go
current := console.Current()
defer current.Reset()

if err := current.SetRaw(); err != nil {
}
ws, err := current.Size()
current.Resize(ws)
```

## Project details

console is a friendly fork of
[containerd/console](https://github.com/containerd/console), licensed under the
[Apache 2.0 license](./LICENSE), with the objective of supporting more operating
systems.