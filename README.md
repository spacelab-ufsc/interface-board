# Interstage Interface Panels (IIP)

This repository contains the hardware project of the external interface to be used in SpaceLab's second mission envolving a 2U CubeSat.

## Summary

IIP are vertical mounted PCBs designed to give external access to the modules inside of a 2U CubeSat during final assembly, integration and testing. IIP is composed by 3 different boards, the complete set allows for the nanosatellite to be charged, programed and debugged.

Currently the project has finished the "Semi USB" variant, which needs the use of the [MSP-FET
](https://www.ti.com/tool/MSP-FET#2) for JTAG programming and debbuging up to 4 modules. The "Full USB" variant doesn't have yet a date to begin development. 

## Hardware features

### Semi USB Variant

#### Full system block diagram

<p align="center">
<img src="https://github.com/spacelab-ufsc/interface-board/blob/documentation/semi_usb_interface/doc/figures/IIP_SemiUSB_BlockDiagram.png">
</p>

#### Nº1 Board (1_IIP_Charge):

* Two [7x2 position pin headers]() for JTAG;
* One [JST 2 position header]() for charging batteries;
* Two [6 pin PicoBlade]() for internal modules connection;
* One [5 pin PicoBlade]() for interfacing Nº1 Board to FT4232H present on Nº3 board;
* One [4 pin PicoBlade]() for battery charge connection to EPS module;

#### Nº2 Board (2_IIP_RBF):

* Two [7x2 position Pin Headers]() for JTAG;
* One [2x1 position pin header]() for Remove Before Flight switch;
* Two [6 pin PicoBlade]() for internal modules connection;
* One [5 pin PicoBlade]() for interfacing Nº2 Board to FT4232H present on Nº3 board;
* One [4 pin PicoBlade]() for RBF switch connection to EPS module;

#### Nº3 Board (3_IIP_QuadUART):

* One [FT4232HL-REEL]() IC for four quad channel USB to UART conversion;
* One [Vertical mini B USB 2.0 port]() for quad channel UART debbuging;
* Two [5 pin PicoBlade]() for interfacing boards Nº1 and Nº2;

## Software used

This hardware project was done using Altium Designer.

## References

* [NanoUtil Interstage - GOMspace](https://gomspace.com/UserFiles/Subsystems/datasheet/gs-ds-nanoutil-interstage-12.pdf)
* [Quad Serial project from Felipe Navarro](https://github.com/PY1CX/Quad-Serial)
* [FT4232H QUAD HIGH SPEED USB TO MULTIPURPOSE UART/MPSSE IC Datasheet Version 2.6](https://www.ftdichip.com/Support/Documents/DataSheets/ICs/DS_FT4232H.pdf)


## License

This project is licensed under GPL license, version 3.