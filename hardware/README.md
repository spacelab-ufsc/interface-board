<h1 align="center">
	IIP HARDWARE
	<br>
</h1>

<h4 align="center">Interface panels hardware project (sources and outputs).</h4>

<p align="center">
    <a href="https://github.com/spacelab-ufsc/spacelab#versioning">
        <img src="https://img.shields.io/badge/status-in%20development-red?style=for-the-badge">
    </a>
    <a href="https://github.com/spacelab-ufsc/interface-board/releases">
        <img alt="GitHub release (latest by date)" src="https://img.shields.io/github/v/release/spacelab-ufsc/interface-board?style=for-the-badge">
    </a>
    <a href="https://github.com/spacelab-ufsc/interface-board/releases">
        <img alt="GitHub commits since latest release (by date) for a branch" src="https://img.shields.io/github/commits-since/spacelab-ufsc/interface-board/latest/dev_hardware?style=for-the-badge">
    </a>
    <a href="https://github.com/spacelab-ufsc/interface-board/commits/master">
        <img alt="GitHub last commit (branch)" src="https://img.shields.io/github/last-commit/spacelab-ufsc/interface-board/dev_hardware?style=for-the-badge">
    </a>
    <a href="https://github.com/spacelab-ufsc/interface-board/issues">
        <img alt="GitHub last commit (branch)" src="https://img.shields.io/github/issues/spacelab-ufsc/interface-board/hardware?style=for-the-badge">
    </a>
    <a href="">
        <img src="https://img.shields.io/badge/CAD%20tool-altium%20v19.2-yellow?style=for-the-badge">
    </a>
    <a href="#license">
        <img src="https://img.shields.io/badge/license-cern%20ohl%202-yellow?style=for-the-badge">
    </a>
</p>

<p align="center">
  	<a href="#overview">Overview</a> •
  	<a href="#hardware-architecture-diagram">Architecture</a> •
  	<a href="#development">Development</a> •
  	<a href="#version">Version</a> •
  	<a href="#license">License</a> •
  	<a href="#references">References</a>
</p>

## Overview

IIP is composed of 4 pcbs with the main components:

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

### Nº3 board (3_iip_QuadUART):

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n3_top.png">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n3_bottom.png">
</p>

* One FT4232HL-REEL IC for four quad channel USB to UART conversion;
* One Vertical mini B USB 2.0 port for quad UART channel debbuging;
* Two 5 pin PicoBlade for interfacing boards Nº1 and Nº2;

### Nº4 board (4_iip):

#### Closure variant

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n4_closure_top.PNG">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n4_closure_bottom.PNG">
</p>

* Empty PCB to close the open side of the 2U/3U CubeSat structure with some easter eggs;

#### Camera variant

<p align="center">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n4_camera_top.PNG">
	<img width="45%" src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_n4_camera_bottom.PNG">
</p>

* Hole mount for a M12 lens camera;

> NOTE: The dimensions for the mouting holes follow a old [board breakout design](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwi4i8PHidLxAhXFJrkGHU2GBCQQFnoECAUQAA&url=https%3A%2F%2Fwww.robotshop.com%2Fmedia%2Ffiles%2Fpdf2%2Fmt9d111_3.2-inch_2-megapixel_module_datasheet.pdf&usg=AOvVaw37NUkZ5OMWWqNb4jGU3Vi5), they are still to be tested.

## Hardware architecture diagram

<p align="center">
<img src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/doc/figures/iip_block_diagram.png">
</p>

> This image refers to the v2.0 release.

## Development

#### Manufacture

The folder [fabrication](https://github.com/spacelab-ufsc/interface-board/tree/master/hardware/fabrication) contain 3 "ready to go" files: the gerbers and nc_drills for manufacturing the board, the BOM with all required components, and the pick_place file for automated assembly for each iip board. Additional files are avaliable in the [outputs](https://github.com/spacelab-ufsc/interface-board/tree/master/hardware/outputs) folder, which contain several useful files and documents, such as: 3D models, bill of materials, schematics, layout prints, and draftsman.

## Version

Refer to the [releases](https://github.com/spacelab-ufsc/interface-board/releases) page.

## License

The hardware project of IIP is licensed under CERN Open Hardware License (version 2).

## References

* [NanoUtil Interstage - GOMspace](https://gomspace.com/UserFiles/Subsystems/datasheet/gs-ds-nanoutil-interstage-12.pdf)
* [Quad Serial project from Felipe Navarro](https://github.com/PY1CX/Quad-Serial)
* [FT4232H QUAD HIGH SPEED USB TO MULTIPURPOSE UART/MPSSE IC Datasheet Version 2.6](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT4232H)
