# Gecko's PSX Emulator

A very basic, bare bones PlayStation emulator that is capable of running BIOS and displaying some graphics. 

Written in D using SDL2 + software rasterizer. The emulation runs in a separate thread; the main SDL window shows entire VRAM and synchronizes using a simple atomic lock. Most of the I/O registers is not implemented yet. GPU part can draw only colored triangles and quads, no textures support yet. Don'texpect it to run any games at the current stage.

The emulator loads `bios/SCPH1001.BIN`. BIOS binary is not included in the repo for copyright reasons, you must install it yourself.
