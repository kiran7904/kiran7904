<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&pause=1000&color=00D4FF&center=true&vCenter=true&width=750&lines=Hi%2C+I'm+Kiran+Kumar+Siripurapu+%F0%9F%91%8B;RTL+Design+%7C+Physical+Design+%7C+RISC-V+Engineer;Full+RTL-to-GDS+Flow+%E2%80%94+Sky130+%C2%B7+Nangate45+%C2%B7+ASAP7;Open+to+RTL+%2F+PD+%2F+Verification+Roles" alt="Typing SVG" />

<br/>

[

![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)

](https://www.linkedin.com/in/kiran-kumar-siripurapu)
[

![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)

](https://kiran-mu.vercel.app/)
[

![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)

](mailto:kirankumarsiripurapu93@gmail.com)

</div>

---

## 👨‍💻 About Me

RTL Design & Physical Design Engineer, B.Tech ECE (2026), with hands-on experience taking silicon designs from **microarchitecture spec to timing-clean GDSII** across Sky130, Nangate45, and ASAP7. I own blocks end-to-end — HDL, SDC constraints, synthesis, floorplanning, CTS, routing, STA, and tape-out.

- 🏭 **6 months @ DeepGrid Semi Pvt. Ltd.** as RTL owner of the **AXI4 interconnect fabric and 16-region IOPMP security module** for a dual-hart RISC-V edge-AI SoC — wrote production SystemVerilog, authored SDC constraints and SVA assertions, achieved timing signoff, and debugged 7 integration issues across IP boundaries using GTKWave

- ⚙️ Took the **Ariane 64-bit RISC-V CPU** through a full RTL-to-GDSII physical design flow on **Nangate45 using OpenROAD** — floorplanning, PDN, macro placement, CTS, and detailed routing, plus Tcl-scripted multicycle-path SDC constraints across 8 pipeline blocks (multiplier, scoreboard, and others), closing timing at **450 MHz with zero hold violations**

- ⚙️ Designed two complex SoC-facing RTL blocks independently:
  - **Parameterized N:M AXI4 crossbar** — weighted round-robin arbitration, per-master outstanding-transaction tracking, AXI-ID response routing, register slices on all 5 channels, 2FF CDC synchronizers, deadlock-free microarchitecture
  - **RV32I pipelined processor** — dual AXI4-Lite master ports, complete hazard resolution (RAW stall, EX-EX/MEM-EX forwarding, branch flush), all 37 base integer instructions, verified against a Python ISA reference model

- 🔬 **Research Intern @ NIT Warangal** — characterized sub-3nm Fishbone FETs in Sentaurus TCAD; **co-author on IEEE Transactions on Electron Devices (accepted)**

- 🎯 **Every RTL project independently taped out** on Sky130B PDK via OpenLane — 100 MHz, zero timing violations across all designs

- 🛠️ Full-flow tooling: **OpenROAD, OpenSTA, Yosys, Vivado, KLayout, GTKWave, Verible**; NPTEL-certified in VLSI Physical Design and RTL-to-GDS flow

- 🎓 B.Tech Electronics & Communication Engineering, RGUKT Srikakulam (AP IIIT) — 2022–2026, CGPA 8.2/10

---

## 🛠️ Technical Skills

<div align="center">

| Category | Skills |
|---|---|
| **HDL** | SystemVerilog (IEEE 1800-2017) · Verilog |
| **Architectures & Protocols** | RISC-V RV32I · Ariane (64-bit RISC-V) · AMBA AXI4 / AXI4-Lite · APB · IOPMP · Systolic Arrays |
| **Verification** | SVA · Cocotb · Verilator · OOP Testbenches · Scoreboards · Functional Coverage |
| **Physical Design Flow** | Floorplanning · PDN · Standard Cell Placement · Clock Tree Synthesis (CTS) · Global & Detailed Routing · STA · Setup/Hold Timing Closure |
| **EDA / Synthesis Tools** | OpenROAD · OpenLane · Yosys · Vivado · OpenSTA · QuestaSim / ModelSim · KLayout · GTKWave · Verible |
| **PDKs / Process Nodes** | Sky130 (A/B) · Nangate45 (45nm) · ASAP7 (7nm Predictive FinFET) |
| **Scripting** | Python · Tcl (SDC constraints) · MATLAB (DSP) |
| **Other** | FSM Design · Pipelined Architectures · Clock Domain Crossing (CDC) · Linux · Git |

</div>

---

## 🚀 Featured Projects

> Full-stack silicon engineering — RTL through physical design, with several designs carried all the way to a clean tape-out.

---

### 🔷 [Ariane RISC-V CPU — Physical Design & Timing Closure (450 MHz)](https://github.com/kiran7904/Ariane-133)

> End-to-end RTL-to-GDSII physical design for the 64-bit Ariane CPU on Nangate45 using OpenROAD.

| Aspect | Detail |
|---|---|
| **PDK / Node** | Nangate45 (45nm) |
| **Flow Steps** | Floorplanning · PDN · Macro placement · CTS · Global & Detailed Routing |
| **Constraints** | Tcl-scripted multicycle-path SDC across 8 pipeline blocks (multiplier, scoreboard, etc.) |
| **Result** | Closed setup TNS from −67k ns to **+0.4 ns positive slack**, zero hold violations, at 450 MHz |

---

### 🔷 [RISC-V-RV32I-Pipeline](https://github.com/kiran7904/RISC-V-RV32I-Pipeline) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)

 · `Updated 11 hours ago`

> In-order 5-stage RISC-V RV32I pipeline with dual AXI4-Lite master ports (IMEM + DMEM).  
> The latest evolution of my processor design — actively maintained.

**Also see the public reference:** [RTL-Implementation-of-an-In-Order-5-Stage-RV32I-Pipeline](https://github.com/kiran7904/RTL-Implementation-of-an-In-Order-5-Stage-RV32I-Pipeline) ⭐ 1

| Aspect | Detail |
|---|---|
| **Stages** | IF → ID → EX → MEM → WB, with inter-stage pipeline registers |
| **Hazard Unit** | Load-use stall (1 cycle) · EX-EX & MEM-EX data forwarding · Branch flush (2 cycles) |
| **Memory Interface** | Dual AXI4-Lite master ports with handshake FSMs (IF + DM) |
| **ISA** | Full RV32I — 37 instructions across R/I/S/B/U/J types |
| **Verification** | Self-checking SV testbench · 6 SVA properties · Python ISA reference model |
| **Modules** | 11 RTL modules (per-stage + hazard unit + register file + ALU + decoder) |
| **Tapeout** | ✅ 199 cells · 1,836 µm² · Sky130B |

---

### 🔷 [AXI4-N-M-Crossbar-Interconnect](https://github.com/kiran7904/AXI4-N-M-Crossbar-Interconnect) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)

 · `Updated last week`

> Multi-master, multi-slave AXI4 crossbar interconnect — plug-compatible with the RV32I core.

| Aspect | Detail |
|---|---|
| **Architecture** | N-master : M-slave non-blocking crossbar with round-robin arbitration |
| **Protocol** | Full AXI4 channel compliance (AW/W/B/AR/R) |
| **Integration** | Designed to accept `rv32i_core`'s AXI4-Lite master ports as slave inputs |
| **Backend** | Gate-level synthesis via Yosys; placement, routing, PPA analysis in OpenROAD |
| **Tapeout** | ✅ Sky130B · 100 MHz · zero timing violations |

---

### 🔷 [GIFT-64-Cryptographic-Core](https://github.com/kiran7904/GIFT-64-Cryptographic-Core) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)

 · `Updated last week`

**Also public:** [gift64-crypto-core](https://github.com/kiran7904/gift64-crypto-core)

> Area-optimized round-based hardware implementation of the GIFT-64 lightweight block cipher — RTL through backend tapeout.

| Aspect | Detail |
|---|---|
| **Algorithm** | GIFT-64: 64-bit block · 128-bit key · 28 rounds · nibble S-box + bit permutation |
| **Mode** | Runtime encrypt/decrypt selection with inverse S-box & permutation |
| **Verification** | Cocotb + self-checking SV testbench — full encrypt → decrypt → plaintext recovery check |
| **Backend** | Floorplanning, placement density tuning, CTS buffer insertion; validated via OpenSTA |
| **Tapeout** | ✅ 3,409 cells · 36,036 µm² · Sky130B · zero DRC/LVS violations |

---

### 🔷 [axi4-lite-slave-ip](https://github.com/kiran7904/axi4-lite-slave-ip) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)



> Parameterized AMBA AXI4-Lite slave IP with byte-enable and SLVERR support.

| Aspect | Detail |
|---|---|
| **Features** | Full AW/W/B/AR/R channel handling · WSTRB byte-lane masking · SLVERR on invalid access |
| **Verification** | Self-checking testbench: full-word R/W, byte-enable, invalid address, pass/fail summary |
| **Tapeout** | ✅ 512 cells · 7,767 µm² · Sky130B |

---

### 🔷 [Systolic-Mac-Array-Verification-Using-SystemVerilog](https://github.com/kiran7904/Systolic-Mac-Array-Verification-Using-SystemVerilog) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)



> 4×4 weight-stationary systolic MAC array with a full OOP-style verification environment.

| Aspect | Detail |
|---|---|
| **RTL** | `mac_4x4.sv` · `pe_top.v` (processing element) · `input_buffer` · `output_buffer` · `mac_controll` |
| **Verification** | Transaction class · Generator · BFM · Monitor · Scoreboard · SVA · Functional Coverage |
| **Scoreboard** | Computes expected matrix multiplication result and compares against DUT output |
| **Simulator** | QuestaSim / ModelSim (`.do` script provided) |
| **Tapeout** | ✅ Sky130B · 100 MHz · zero timing violations |

---

### 🔷 [Low-Pass-Butterworth-FIR-Filter](https://github.com/kiran7904/Low-Pass-Butterworth-FIR-Filter) · 

![SystemVerilog](https://img.shields.io/badge/-SystemVerilog-blue?style=flat-square)

 

![MATLAB](https://img.shields.io/badge/-MATLAB-orange?style=flat-square)



> Butterworth low-pass FIR filter design — coefficients generated in MATLAB, RTL implemented in SystemVerilog/Verilog.

| Aspect | Detail |
|---|---|
| **Design** | FIR filter with Butterworth response · MATLAB coefficient generation · fixed-point RTL |
| **Tapeout** | ✅ Sky130B · 100 MHz · zero timing violations |

---

### 🔷 [VeriLogicLab](https://github.com/kiran7904/VeriLogicLab) · 

![Verilog](https://img.shields.io/badge/-Verilog-green?style=flat-square)

 · ⭐ 2 · `160 commits`

> My RTL learning lab — a growing collection of digital design implementations.

<details>
<summary>📂 Click to see all projects inside VeriLogicLab</summary>

| Category | Projects |
|---|---|
| **Processors** | 16-bit RISC-V · 5-Stage Pipeline RISC-V |
| **Bus Protocols** | AXI Slave · AHB Protocol · APB Protocol · SPI · I2C Master-Slave · UART |
| **Memory** | Async FIFO · Basic FIFO · 64-bit SRAM · Dual Port RAM |
| **Cryptography** | GIFT-64 Lightweight Algorithm · GIFT-64 using LFSR |
| **Clock / CDC** | Async FIFO CDC · High-Freq to Low-Freq domain · Clock Gating · Clock Divider |
| **Arithmetic** | Carry Lookahead Adder · Booth's Multiplier · BCD Adder · Barrel Shifter |
| **Controllers** | Traffic Light · Fuzzy Logic Traffic Light · Elevator Controller · 1010 Counter |
| **Misc** | Sequence Detector · Ring Counter · Shift Registers · Seven Segment |

</details>

---

### 🔷 [kraken_soc](https://github.com/kiran7904/kraken_soc) · `Updated Mar 2026`

> SoC integration project — bringing together the processor core, interconnect, and peripherals.

---

## 📊 GitHub Stats

<div align="center">

<img height="175em" src="https://github-readme-stats.vercel.app/api?username=kiran7904&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true" />
<img height="175em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kiran7904&layout=compact&langs_count=6&theme=tokyonight&hide_border=true" />

</div>

<div align="center">

[

![GitHub Streak](https://streak-stats.demolab.com?user=kiran7904&theme=tokyonight&hide_border=true)

](https://git.io/streak-stats)

</div>

---

## 🏆 Achievements

| | Achievement |
|---|---|
| 🎯 | **Every RTL project independently taped out** on Sky130B PDK via OpenLane — RV32I Core · AXI4 Crossbar · GIFT-64 · AXI4-Lite Slave · Systolic MAC · FIR Filter — all at 100 MHz, zero violations |
| ⚙️ | **Physical design timing closure** on the Ariane RISC-V CPU (Nangate45, OpenROAD) — closed setup TNS from −67k ns to +0.4 ns positive slack, zero hold violations, at 450 MHz |
| 📄 | **Co-author**: *Interface Trap-Induced Performance Degradation in Fishbone FET* — **IEEE Transactions on Electron Devices** (Accepted) |
| 💡 | **160 commits** in VeriLogicLab · **18 commits** in RV32I pipeline · **70+ HDLBits** problems solved |
| 🎓 | NPTEL: VLSI Design Flow (RTL-to-GDS) · VLSI Physical Design with Timing Analysis · Siemens EDA: SystemVerilog for Design & Verification |

---

## 💼 Experience

**Digital IC Design Intern — DeepGrid Semi Pvt. Ltd., T-Hub, Hyderabad**  `Nov 2025 – Apr 2026`
- Designed the **AXI4 interconnect fabric** for a dual-hart RISC-V edge-AI SoC — weighted round-robin arbitration and address-based routing, resolving data-width mismatches across multiple IP blocks
- Implemented a **16-region IOPMP** hardware security module per the RISC-V IOPMP spec to enforce memory access policies
- Authored timing-driven **SDC constraints** and embedded **SVA assertions**; ran logic synthesis and STA to confirm layout timing feasibility ahead of floorplanning
- Debugged **7 integration issues** at subsystem boundaries by analyzing GTKWave waveforms to align AXI channel handshakes
- Automated RTL linting and synthesis scripts with **Verible** and **Tcl**

**Device Modeling Research Intern — NIT Warangal** `May 2025 – Jul 2025`
- Conducted TCAD electrical characterization of **sub-3nm Fishbone FET** devices — interface trap analysis, subthreshold swing, transistor-level electrostatics
- Co-authored a manuscript accepted by **IEEE Transactions on Electron Devices**

---

## 📫 Let's Connect

I'm actively looking for **RTL Design / Physical Design / SoC Architecture / Verification** roles.
If you're working on RISC-V, digital design, physical implementation, or open-source EDA — I'd love to talk.

<div align="center">

[

![Email](https://img.shields.io/badge/kirankumarsiripurapu93%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)

](mailto:kirankumarsiripurapu93@gmail.com)
[

![LinkedIn](https://img.shields.io/badge/kiran--kumar--siripurapu-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)

](https://www.linkedin.com/in/kiran-kumar-siripurapu)
[

![Portfolio](https://img.shields.io/badge/kiran--mu.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)

](https://kiran-mu.vercel.app/)



![Profile Views](https://komarev.com/ghpvc/?username=kiran7904&color=0e75b6&style=flat-square)



</div>

---

<div align="center">

*Made with ❤️ for open-source silicon · RTL-to-GDS across Sky130, Nangate45 & ASAP7*

</div>