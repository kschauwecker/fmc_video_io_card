# FMC Video IO Card
This FMC module features a MIPI Rx and a HDMI Tx interface. It was designed for use with the TEG2000 SOM in combination with the TE0701 carrier by Trenz Electronics, which features a GateMate FPGA by Cologne Chip.

![PCB photo](/pcb-photo.jpeg)

## Core Features
* The MIPI interface uses a resistor network to connect HS and LP signal to different pins
* For the HDMI interface a parallel RGB converter IC is used (so the FPGA will need to output parallel RGB)
* An additional HyperRAM is provided which can serve as a frame buffer

This is an ongoing project. As of now, the electronics are untested. Further updates will follow.


## Known Issues
* The card is a little too large and overlaps slightly with the SOM when mounted on the TE0701 carrier. The standoff screws on the SOM must be removed
