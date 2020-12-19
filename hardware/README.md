<h1 align="center">
	IIP HARDWARE
	<br>
</h1>

<h4 align="center">Interface panels hardware project (sources, outputs, and documentation).</h4>

<p align="center">
    <a href="">
		<img src="https://img.shields.io/badge/status-development-green?style=for-the-badge">
	</a>
    <a href="">
		<img src="https://img.shields.io/badge/version-1.0-blue?style=for-the-badge">
	</a>
	<a href="">
		<img src="https://img.shields.io/badge/CAD%20tool-altium%20v19.2-9cf?style=for-the-badge">
	</a>
	<a href="">
		<img src="https://img.shields.io/badge/license-CERN-red?style=for-the-badge">
	</a>
    <!--
	<a href="https://github.com/spacelab-ufsc/obdh2/tree/dev/doc/build">
		<img src="https://img.shields.io/badge/for%20more-here-lightgray?style=for-the-badge">
	</a>
    -->
</p>

<p align="center">
  	<a href="#overview">Overview</a> •
  	<a href="#architecture">Architecture</a> •
  	<a href="#development">Development</a> •
  	<a href="#version">Version</a> •
  	<a href="#license">License</a> •
  	<a href="#notes">Notes</a>
</p>

## Overview

IIP is composed of 3 pcbs with the main components:

### Nº1 board (1_iip_charge):

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n1_top.png">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n1_bottom.png">
</p>

* Two 7x2 position pin headers for JTAG;
* One JST 2 position header for charging batteries;
* Two 6 pin PicoBlade for internal modules connection;
* One 5 pin PicoBlade for interfacing Nº1 Board to FT4232H present on Nº3 board;
* One 4 pin PicoBlade for battery charge connection to EPS module;

### Nº2 board (2_iip_rbf):

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n2_top.png">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n2_bottom.png">
</p>

* Two 7x2 position Pin Headers for JTAG;
* One 2x1 position pin header for Remove Before Flight switch;
* Two 6 pin PicoBlade for internal modules connection;
* One 5 pin PicoBlade for interfacing Nº2 Board to FT4232H present on Nº3 board;
* One 4 pin PicoBlade for RBF switch connection to EPS module;

### Nº3 board (3_IIP_QuadUART):

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n3_top.png">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n3_bottom.png">
</p>

* One FT4232HL-REEL IC for four quad channel USB to UART conversion;
* One Vertical mini B USB 2.0 port for quad UART channel debbuging;
* Two 5 pin PicoBlade for interfacing boards Nº1 and Nº2;

## Hardware architecture diagram

<p align="center">
<img src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_block_diagram.png">
</p>

## Development

TBD

## Version

#### v1.0

## License

The hardware of IIP is licensed under CERN Open Hardware License (version 2).

## Notes
Some references used:

* [NanoUtil Interstage - GOMspace](https://gomspace.com/UserFiles/Subsystems/datasheet/gs-ds-nanoutil-interstage-12.pdf)
* [Quad Serial project from Felipe Navarro](https://github.com/PY1CX/Quad-Serial)
* [FT4232H QUAD HIGH SPEED USB TO MULTIPURPOSE UART/MPSSE IC Datasheet Version 2.6](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT4232H)
