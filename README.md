# Asynchronous FIFO

## Overview

This repository contains the implementation of an Asynchronous FIFO (First-In-First-Out) buffer using Verilog HDL. It aims to demonstrate concepts such as FIFO buffer design, asynchronous clock domain handling, and Verilog HDL programming.

## Description

The Asynchronous FIFO implementation showcases:
- **FIFO Buffer Design**: Ensures data is processed in the order it is received.
- **Asynchronous Clock Domains**: Manages data transfer between different clock frequencies.
- **Verilog HDL Programming**: Provides a practical example of hardware design and simulation.

## Repository Contents

- **`verilog/`**: Verilog HDL source code for the Asynchronous FIFO implementation.
- **`sim_results/`**: Simulation results demonstrating the functionality and performance of the FIFO.

## Design Specifications

### FIFO Interface

- **Transmitter A**: Sends data to Receiver B.
  - **Burst Size**: 120 data units.
  - **Frequency**: 200 MHz.

- **Write Interface**:
  - `wr_clk` (200 MHz): Write clock signal.
  - `wr_en` (Active High): Write enable signal.
  - `wr_data` (8-bit): Data to be written.
  - `wr_rst` (Active High): Write reset signal.

- **Read Interface**:
  - `rd_clk` (200 MHz): Read clock signal.
  - `rd_en` (Active High): Read enable signal.
  - `rd_data` (8-bit): Data read from FIFO.
  - `rd_rst` (Active High): Read reset signal.
  - `rd_ptr = 0`: Initial read pointer value.

- **FIFO Status Interface**:
  - `O_fifo_full`: High if FIFO is full.
  - `O_fifo_empty`: High if FIFO is empty.

