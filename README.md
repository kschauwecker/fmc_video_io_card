# FMC Video IO Card
This FMC module features a MIPI Rx and a HDMI Tx interface. It was designed for use with the TEG2000 SOM in combination with the TE0701 carrier by Trenz Electronics, which features a GateMate FPGA by Cologne Chip.

Please see the [blog post on Elektronaut](https://elektronaut.tech/en/fpga/driving-full-hd-video-with-the-cologne-chip-gatemate-fpga/)
for more details on this project.

![PCB photo](/pcb-photo.jpeg)

## Core Features
* The MIPI interface uses a resistor network to connect HS and LP signal to different pins
* For the HDMI interface a parallel RGB converter IC is used (so the FPGA will need to output parallel RGB)
* An additional HyperRAM is provided which can serve as a frame buffer

## Project Status
This is an ongoing project. Only the following hardware parts have been tested and are confirmed to work

* HDMI interface running at 720p @ 60Hz
* HDMI interface running at 1080p @ 60Hz

Test for the MIPI interface and HyperRAM are still pending.

## Known Issues
* The card is a little too large and overlaps slightly with the SOM when mounted on the TE0701 carrier. The standoff screws on the SOM must be removed

## FPGA Software
The FPGA-implementation for the parallel RGB interface is available here:

https://github.com/kschauwecker/gatemate_parallel_rgb
