# Hi, I'm Toshit — otherwise known as Toshi.
I am an Electronics Engineering undergraduate focusing on Digital Design, RTL, Verification, FPGA Prototyping, and Open-Silicon ASIC Design. Recently, I have been working on open-source silicon flows and completed a tapeout through Tiny Tapeout.

**Focus Areas:** Computer Architecture · ASIC Design · Digital VLSI · Design Verification · RTL Design 

[GitHub](https://github.com/yappingnoises) · [CV (PDF)](./Toshit_Kumar_CV.pdf) · [Email](mailto:toshitpkumar@gmail.com)


---

#  Projects

### 1. Tiny Tapeout — 8-Bit General-Purpose Processor (TGTTOS)
*Open-Silicon ASIC Tapeout | Verilog · cocoTB · LibreLane · GF180mcu*
- Designed and verified a custom 8-bit instruction, 16-bit accumulator general-purpose processor targeting an open-source silicon shuttle via Tiny Tapeout.
- Executed RTL-to-GDSII hardening using open-source EDA flows and verified functionality across RTL and gate-level simulations using assertion-based testbenches.
- Taped out a chip successfully. 
-  [Repository](https://github.com/yappingnoises/TCPU16_LNMIIT_01_GF) ·[GDS](https://toshis.codes/TCPU16_LNMIIT_01_GF/)· [Tiny Tapeout Tile](https://app.tinytapeout.com/projects/6336)

### 2. RISC-V based Image processing hardware accelerator
*FPGA System-on-Chip | VHDL/Verilog  · Xilinx Artix-7 (Nexys 4 DDR)* · Wishbone
- Designed a custom Image processing hardware accelerator to offload the matrix calculations from a RISC-V CPU. 
- Employed the Wishbone bus architecture to enable a multiple master to slave communication. 
- Synthesized, implemented, and validated hardware acceleration on a Digilent Nexys 4 DDR board using Xilinx Vivado.
- **Links:** [Repository](#) · [Architecture Notes](#)

### 3. 32-Bit 5-Stage Pipelined RISC-V Core (RV32I)
*Computer Architecture | Verilog · Vivado · Nexys4DDR · RISC-V*
- Implemented a classic 5-stage pipelined RISC-V processor (`IF`, `ID`, `EX`, `MEM`, `WB`) supporting the RV32I base integer instruction set.
- Designed full operand forwarding paths and a hazard detection unit to resolve RAW data hazards and control hazards via pipeline stalling and flushing.
- Verified instruction-level execution and hazard edge cases against reference assembly routines via waveform inspection.
- **Links:** [Repository](#) · [Datapath Diagram](#)


---

## Technical Toolchain

| Domain                   | Tools & Languages                                                        |
| :----------------------- | :----------------------------------------------------------------------- |
| **HDLs & Verification**  | Verilog, VHDL, Assertion-Based Verification, cocotb                      |
| **FPGA & ASIC Design**   | Xilinx Vivado, Librelane, TinyTapeout, Nexys 4 DDR, Lattice iCE40, C/C++ |
| **Scripting & Workflow** | Python, Bash, Git, Linux                                                 |


---

## Experience
- **SoC Design Intern — VLSI System Design Pvt. Ltd.  *(May 2026- Jul 2026)***
	* Designed custom memory-mapped IO IP core (GPIO controller) in Verilog HDL.
	*  Integrated peripherals into a 32-bit RISC-V SoC, configuring address decode logic and resolving bus collisions.
	* Wrote bare-metal C firmware drivers and validated behavior via RTL simulations and FPGA deployment.
* **Research Intern — Indian Institute of Technology (IIT) Guwahati** *(May 2025 – Jul 2025)*
	-  Analyzed 5G New Radio (NR) synchronization procedures and implemented a low-latency Speech-to-Text processing pipeline on a Raspberry Pi 4B over an in-house 5G testbed.
* **Game Tester  — Noxcrew Ltd.** *(2026 – Present)*
	-  Participated in test sessions to minimise bugs and provide feedback for production releases on MC Championship (MCC), MCC Island,  and related projects.
	-  Collaborated with developers to document reproduction steps for technical glitches, streamlining the debugging process for the build team.

---

## Education

**B.Tech in Electronics and Communication Engineering**  
The LNM Institute of Information Technology (LNMIIT), Jaipur *(2023 – 2027)*  
***Relevant Coursework**:* Computer Architecture, Digital System Design, Digital Circuits and Systems, Fundamentals of VLSI, Microprocessors & Microcontrollers, Analog Electronics, Design for Testing.
