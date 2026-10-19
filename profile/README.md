<div align="center">

<img src="https://raw.githubusercontent.com/JSI-Mines-Collaboration/.github/main/profile/banner.svg" alt="JSI x Mines: modeling and simulation toolbench for the JSI TRIGA Mark-II" width="100%"/>

### 🔵 Where a 60-year-old research reactor meets modern open-source simulation

[![JSI](https://img.shields.io/badge/Jo%C5%BEef_Stefan_Institute-0077b6?style=for-the-badge&logoColor=white)](https://www.ijs.si)
[![Colorado School of Mines](https://img.shields.io/badge/Colorado_School_of_Mines-002554?style=for-the-badge&logoColor=white)](https://www.mines.edu)
[![OpenMC](https://img.shields.io/badge/OpenMC-48cae4?style=for-the-badge&logo=python&logoColor=white)](https://openmc.org)
[![Reactor](https://img.shields.io/badge/TRIGA_Mark--II-250_kW-03045e?style=for-the-badge&logoColor=white)](#-the-reactor)

</div>

---

## 🤝 About this collaboration

A long-running partnership between the **Reactor Physics Department of the Jožef Stefan Institute (Ljubljana, Slovenia)** and the **M-PRISM group at the Colorado School of Mines**. Its home is one reactor, the **JSI TRIGA Mark-II**, which has become the most extensively used experimental validation facility for the **fission-matrix (FM)** family of fast transport methods.

This organization collects the **models, scripts and tools** that come out of that work, so the experiments, the simulation models and the validation studies stay connected.

<div align="center">

| 🏛️ **JSI, Ljubljana** | 🏔️ **Colorado School of Mines** |
|:---:|:---:|
| Reactor operation, experiments, Serpent reference models, burnup (bRAPID) | Fission-matrix methods, OpenMC models, kinetics (TFM), control rods (FM-CRd) |

</div>

---

## ⚛️ The reactor

<table>
<tr>
<td width="50%">

**JSI TRIGA Mark-II**, an open-top, pool-type research reactor.

- 🗓️ First critical **31 May 1966**; reconstructed in 1991 (transient rod, pulse mode)
- ⚡ **250 kW** steady state, up to **~1 GW** in pulse mode
- 🔵 **91** lattice positions in **6 rings** (A–F), graphite radial reflector
- 🧱 U-ZrH fuel, 12 wt% U, **19.9–20 %** ²³⁵U, 38.1 cm active height
- 🎛️ Four B₄C control rods: **SAFE · REGU · SHIM · TRAN**

</td>
<td width="50%">

| Ring | A | B | C | D | E | F | **Total** |
|:---:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Positions | 1 | 6 | 12 | 18 | 24 | 30 | **91** |

<sub>Concentric-ring lattice around the central position, surrounded by the graphite reflector.</sub>

</td>
</tr>
</table>

---

## 📦 What's here

| Repository | Description |
|---|---|
| 🧬 [**jsi_triga_mark2_openmc**](https://github.com/JSI-Mines-Collaboration/jsi_triga_mark2_openmc) | Static **OpenMC** models of the reactor as self-contained Jupyter notebooks: **Core 133** (the ICSBEP benchmark core, 40 fresh fuel rods) and **Core 189** (56 fresh rods, in-core carousel and dosimetry channels). Detailed fuel, control-rod, grid-plate, reflector, beam-port and biological-shield geometry. MIT-licensed. |

> 🔒 Some repositories in this organization are private while work is in progress.

---

## 🧭 Research thread, at a glance

```mermaid
flowchart LR
    A["🎯 Dosimetry<br/>Al-Au wires"] --> B["🎚️ Control rods<br/>FM-CRd · Core 133"]
    B --> C["⏱️ Kinetics<br/>rod swap & insertion · TFM"]
    C --> D["🔥 Burnup<br/>bRAPID · fuel swaps"]
    D --> E["🧮 OpenMC fission matrix<br/>FM approaches · UQ"]
    classDef n fill:#03045e,stroke:#48cae4,color:#fff,stroke-width:2px;
    class A,B,C,D,E n;
```

### ✅ Published results

| Topic | Publication |
|---|---|
| 🎯 **Dosimetry** | *Experimental Validation of RAPID Based on JSI TRIGA Reactor Dosimetry*, Mascolino, Haghighat, Radulović & Snoj (NENE 2020) |
| 🎚️ **Control rods** | *Development and Validation of New Algorithms for Control Rods Insertion Modeling in RAPID*, Mascolino, Haghighat & Snoj, **Ann. Nucl. Energy** 166 (2022) |
| ⏱️ **3-D kinetics** | *Experimental Validation of the 3-D Neutron Kinetics Algorithm of RAPID using the JSI TRIGA Mark-II Reactor*, Mascolino, Pungerčič, Snoj & Haghighat, **Prog. Nucl. Energy** 176 (2024) |
| 🔥 **Burnup** | *Verification of a Novel Fuel Burnup Algorithm in RAPID…*, Pungerčič, Mascolino, Haghighat & Snoj, **Nucl. Eng. Technol.** 55 (2023) |
| 🪙 **Fuel worth** | *JSI TRIGA Fuel Rod Reactivity Worth Experiments for Validation of Serpent-2 and RAPID Fuel Burnup Calculations*, Pungerčič, Haghighat & Snoj, **Nucl. Eng. Technol.** 56 (2024) |
| 🧮 **OpenMC fission matrix** | *Comparing Fission Matrix Approaches using a JSI TRIGA Mark-II Reactor Model*, Balouza, Krašovic, Pungerčič & Mascolino (2026, preliminary comparison) |
| 🛰️ **Flux reconstruction** | *Evaluation of the Effect of Control Rod Positioning on One-Group Effective Nuclear Data for Ex-Core Flux Reconstruction in the JSI TRIGA Mark-II Reactor*, Lafore et al. (2026, preliminary extended summary) |
| 🕰️ **Facility history** | *A half-century of nuclear research, education and training: Story of the JSI TRIGA reactor*, Snoj et al., **Ann. Nucl. Energy** 214 (2025) |

### 🛠️ In progress

> These threads are active work, not yet published results.

- 🔬 **Uncertainty quantification** for the fission-matrix method on Core 133 using the OpenMC model developed with JSI (manuscript submitted, under review).
- 🌀 **Higher-order eigenmode analysis** on Core 133, studying flux-tilt harmonics beyond k₀ under control-rod perturbation.

---

## 🚀 Using the models

```bash
git clone https://github.com/JSI-Mines-Collaboration/jsi_triga_mark2_openmc
cd jsi_triga_mark2_openmc
jupyter lab core133.ipynb      # needs OpenMC and a cross-section library with TRIGA thermal-scattering data
```

Control-rod positions are set in the first code cell of each notebook; all lengths are in cm.

---

<div align="center">

<sub>🌐 Part of the [M-PRISM](https://github.com/M-PRISM-Colorado-School-of-Mines) research network</sub>

<img src="https://raw.githubusercontent.com/JSI-Mines-Collaboration/.github/main/profile/footer.svg" alt="JSI x Mines" width="100%"/>

</div>
