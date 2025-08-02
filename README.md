# Synchronous FIFO Buffer – OpenLane Macro

## Overview

This project implements a parameterized, synchronous First-In, First-Out (FIFO) buffer in Verilog. The FIFO supports configurable data width and depth, offers standard status flags (full, empty, almost full/empty), and safely queues data between digital system modules operating at different speeds.

## Features

- Parameterized data width (e.g., 32 bits) and depth (e.g., 4 entries)
- Synchronous operation with active-low read/write/clear controls
- Full, empty, last/almost full/almost empty flag outputs
- Modular design: separates control logic and storage block

## Hardware Implementation

The Verilog design is synthesized and hardened as a reusable macro (IP block) using the OpenLane open-source ASIC flow, targeting the SKY130 process. The macro approach is industry standard, enabling flexible integration of the FIFO buffer within larger digital systems (ASICs/SoCs):

1. **Design Preparation**: RTL Verilog for FIFO logic and memory array.  
2. **OpenLane Flow**: Synthesis, floorplanning, placement, routing, and signoff, producing a technology-mapped, DRC/LVS-clean GDS and LEF macro.  
3. **Reuse**: The generated macro (GDS/LEF) can be integrated with other IP blocks in system-level hardware projects.

## Viewing the Final Design

The final **GDS file** for this project can be found at: runs/FinalFlow/results/final/gds/FIFO_Model.gds


You can conveniently view this GDS layout online using the Tiny Tapeout GDS viewer at:

https://gds-viewer.tinytapeout.com/

Download the GDS file and upload it to the link above to view it in 3D.



