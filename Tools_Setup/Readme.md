# RTL to GDS Flow Setup on Ubuntu

## 📘 Overview

This repository documents the **complete open-source RTL to GDSII VLSI flow setup on Ubuntu**, intended for:
- Undergraduate students
- Beginners in VLSI / Digital Design
- Juniors learning RTL design and physical design tools

The goal of this documentation is not only to **install tools**, but also to **understand why each tool is used and where it fits in the flow**.

---

## 🧠 RTL → GDS Flow at a Glance

The standard digital ASIC design flow consists of the following stages:

1. RTL Design (Verilog)
2. RTL Simulation & Verification
3. Logic Synthesis
4. Static Timing Analysis
5. Floorplanning, Placement & Routing
6. Physical Verification (DRC/LVS)
7. GDSII Generation

📌 **This document covers Stage 2: RTL Simulation & Verification**

---

## 🔍 Stage 2: RTL Simulation & Verification

Before synthesis or physical design, RTL code must be:
- Functionally correct
- Free from logical errors
- Verified against a testbench

For this purpose, we use:
- **Icarus Verilog** – Verilog compiler & simulator
- **GTKWave** – Waveform viewer

These tools are lightweight, open-source, and ideal for academic use.

---

# 🔧 Icarus Verilog & GTKWave Installation (Ubuntu)

## 📌 Tool Description

### Icarus Verilog
Icarus Verilog (`iverilog`) is an open-source Verilog HDL compiler used to:
- Compile RTL and testbench code
- Perform event-driven simulation
- Generate waveform dump files (`.vcd`)

### GTKWave
GTKWave is a waveform visualization tool used to:
- View signal transitions over time
- Debug RTL behavior
- Analyze simulation results graphically

---

## 🖥️ System Requirements

- OS: Ubuntu 20.04 / 22.04 (Recommended)
- Architecture: x86_64
- Internet connection
- Basic Linux terminal knowledge

---

### 🔄 Step 1: Update Package List

Before installing any tool, update the Ubuntu package list:

```bash
sudo apt update
```
---
### 📦 Step 2: Install Icarus Verilog

- Install Icarus Verilog using the APT package manager:
```bash
sudo apt install iverilog   
```
---
### ✅ Verify Installation

```bash
iverilog -V 
``` 
- Expected output (version may vary):

```bash
Icarus Verilog version 11.x   
```
---
### 📦 Step 3: Install GTKWave

- Install GTKWave for waveform viewing:
```bash
sudo apt install gtkwave   
```
---
### ✅ Verify Installation

```bash
gtkwave --version   
```
---
# 🔧 Yosys Setup (RTL Synthesis Tool)

## 📌 Purpose

This document describes the installation and verification of **Yosys**, an open-source **RTL synthesis tool**, on Ubuntu.

---
### 🔄 Step 1: Update Package List

Before installing Yosys, update the Ubuntu package index:

```bash
sudo apt update
```
---
### 📦 Step 2: Install Yosys

- Install Yosys using the Ubuntu APT package manager:

```bash
sudo apt install yosys   
```
---
### ✅ Step 3: Verify Installation

- Check whether Yosys is installed correctly:

```bash
yosys -V   
```
- Expected output (version may vary):
```bash
Yosys 0.xx
```
---

### 🧪 Step 4: Launch Yosys Shell (Optional Check)

- Start the interactive Yosys shell:

```bash
yosys 
```
- You should see:

```bash
yosys>   
```
- Exit the shell using:

```bash
exit   
```
---
#### 📁 Optional: Check Installation Path

```bash
which yosys   
 ```
- Expected output:

```bash
/usr/bin/yosys   
```
---