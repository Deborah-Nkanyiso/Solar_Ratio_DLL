# Solar Ratio Calculator DLL (PE3)

A Windows Dynamic Link Library (DLL) written in x86 Assembly (MASM) that computes the **solar ratio** for a solar power system.

**Author:** DN MBOYI (MBOYI DN)  
**Student Number:** 222019179  
**Subject:** CSC03B3  
**Practical Exercise:** PE3  
**Year:** 2025  

---

## Problem Description

The DLL exports a single function:

- **`solarRatio(coverage, solarOutput, capacity)`**

This function calculates the ratio of actual solar energy produced relative to the maximum possible capacity:

**Formula:**

solarRatio = (coverage × solarOutput) / capacity



- All three parameters are integers.
- The function uses the **x87 FPU** to perform floating-point division and returns the result as a **float** (single precision).

---

## Features

- Simple and efficient implementation using integer multiplication followed by FPU division
- Proper use of `FILD`, `FDIVP`, and stack management for floating-point operations
- Clean stack frame setup and parameter cleanup (`RET 12`)
- Exported via `.def` file for easy integration with C/C++ or other programs
- Includes basic `LibMain` for DLL loading

---

## Technologies Used

- **x86 Assembly Language**
- **MASM** (Microsoft Macro Assembler)
- **x87 Floating Point Unit (FPU)**
- DLL Development with module definition (`.def`) file

---

## Files Included

- `222019179_PE3.asm` – Main assembly source with `solarRatio` function
- `PE3.def` – Module definition file exporting the function
- `createdll.bat` – Batch file for assembling and linking the DLL
- `README.md`

---

## How to Build

You can build the DLL using the provided batch file:

```batch
createdll.bat 222019179_PE3 PE3
