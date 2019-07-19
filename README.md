vhcaddrgen
====

[![Build Status](https://travis-ci.org/valhallacoin/vhcaddrgen.png?branch=master)](https://travis-ci.org/valhallacoin/vhcaddrgen)
[![GoDoc](https://godoc.org/github.com/valhallacoin/vhcaddrgen?status.png)](http://godoc.org/github.com/valhallacoin/vhcaddrgen)


vhcaddrgen is a simple offline address generator for [valhallacoin](https://valhallacoin.org/).

It allows one to generate an address (along with either the private
key or a wallet seed) without a running wallet or daemon.

## Installation and updating

### Windows/Linux/BSD/POSIX - Build from source

Building or updating from source requires the following build dependencies:

- **Go 1.11**

  Installation instructions can be found here: http://golang.org/doc/install.
  It is recommended to add `$GOPATH/bin` to your `PATH` at this point.

**Getting the source**:

For a first time installation, the project and dependency sources can be
obtained manually with `git` and `dep` (create directories as needed):

```
git clone https://github.com/valhallacoin/vhcaddrgen $GOPATH/src/github.com/valhallacoin/vhcaddrgen
cd $GOPATH/src/github.com/valhallacoin/vhcaddrgen
```

To update an existing source tree, pull the latest changes and install the
matching dependencies:

```
cd $GOPATH/src/github.com/valhallacoin/vhcaddrgen
git pull
```

**Building/Installing**:

The `go` tool is used to build or install (to `GOPATH`) the project.  Some
example build instructions are provided below (all must run from the `vhcaddrgen`
project directory).

To build a `vhcaddrgen` executable and install it to `$GOPATH/bin/`:

```
go install
```

To build a `vhcaddrgen` executable and place it in the current directory:

```
go build
```

## Usage

```
Usage: vhcaddrgen [-testnet] [-simnet] [-regtest] [-noseed] [-h] filename
Generate a Valhalla private and public key or wallet seed.
These are output to the file 'filename'.

  -h 		    Print this message
  -testnet 	    Generate a testnet key instead of mainnet
  -simnet       Generate a simnet key instead of mainnet
  -regtest      Generate a regtest key instead of mainnet
  -noseed       Generate a single keypair instead of a seed
  -verify 	    Verify a seed by generating the first address
```
