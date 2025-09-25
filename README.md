# Gecko's PSX Emulator

A very basic, bare bones PlayStation emulator that is capable of running BIOS (partly) and displaying some graphics. Written in D using SDL2. Mostly inspired by the great [psx-guide](https://github.com/simias/psx-guide) by Lionel Flandrin, but I used software rasterizer instead of OpenGL.

The emulation runs in a separate thread; the main loop outputs entire VRAM in a window and synchronizes using a simple atomic lock. GPU part can draw only colored triangles and quads, no textures support yet. No CD-ROM, no audio, no controller input. Don'texpect it to run any games at the current stage.

The emulator loads `bios/SCPH1001.BIN`. BIOS binary is not included in the repo for copyright reasons, you must install it yourself.

The emulation thread will stop at "unhandled store8 at address 0x1f801800", this is normal at the moment, because most of the I/O ports are not implemented yet.
