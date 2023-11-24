# GoBump
GoBump is a simple command-line tool written in Go that allows you to update the versions of your Go dependencies.

## Usage

```shell
gobump -packages=<package@version>,... -modroot=<path to go mod>
```

**NOTE**: This tool does not run `go mod tidy` at the end, you must run that yourself.

### Flags

* `-packages`: A comma-separated list of packages to update. Each package should be in the format package@version.
* `-modroot`: Path to the go.mod root. If not specified, it defaults to the current directory.

## Example

```shell
gobump -packages=github.com/pkg/errors@v0.9.1,golang.org/x/mod@v0.4.2 -modroot=/path/to/your/project
```

This will update the versions of `github.com/pkg/errors` and `golang.org/x/mod` in your `go.mod` file.

## Requirements

Go 1.20 or later

## Installation
To install gobump, you can use go install:

```shell
go install github.com/dlorenc/gobump@latest
```

## Contributing
Contributions are welcome! Please submit a pull request on GitHub.

