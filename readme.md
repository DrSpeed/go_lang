## Experimenting with go embedded.
---
(aka golang)

TinyGo is a compiler for an existing programming language, the Go programming language. 

TinyGo focuses on compiling code written in Go, but for smaller kinds of systems:

* The Go compiler and tools (from golang.org) are the reference implementation of the Go programming language. They are primarily intended for server side programming but also used for command line tools and other purposes.
* The TinyGo project implements the exact same programming language. However, TinyGo uses a different compiler and tools to make it suited for embedded systems and WebAssembly. It does this primarily by creating much smaller binaries and targeting a much wider variety of systems.

### To install on OSX

With brew

`brew tap tinygo-org/tools
brew install tinygo`


### Check installation via

`tinygo version`


Should find it on your path

### To cross compile and write to device:

* Connect the Feather board to the computer and touble-click the reset button to put it in bootloader mode. You will need to do this **EVERY** time you want to flash it
* Check the path for the new USB drive `/Volumes/FEATHERBOOT`

The command to cross compile and push to (flash) device:

`tinygo build -target=feather-m0 -o=/Volumes/FEATHERBOOT/flash.uf2 feather-blink.go`

---
## The project

<https://tinygo.org/>

