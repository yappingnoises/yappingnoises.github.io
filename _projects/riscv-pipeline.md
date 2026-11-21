---
layout: page
title: 32-Bit Pipelined RISC-V Core
description: RV32I processor with forwarding and hazard handling
importance: 3
category: work
---

Implemented a classic 5-stage pipelined RV32I processor in Verilog.

- Included instruction fetch, decode, execute, memory, and write-back stages.
- Added operand forwarding for RAW hazard resolution.
- Implemented control-hazard flushing and load-use stalling.
