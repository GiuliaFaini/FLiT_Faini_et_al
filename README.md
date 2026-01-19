# FLiT_Faini_et_al

This repository provides basic MATLAB code to implement **FLiT photostimulation protocols**, as described in:

> **Faini et al., Nature Communications (2023)**  
> https://www.nature.com/articles/s41467-023-37416-w

The scripts allow control and synchronization of the **galvomirror system** and **laser power attenuator**, implement essential calibration procedures, define stimulation parameters and pipelines, and execute FLiT photostimulation events.

---

## Repository contents

### Main MATLAB scripts

#### `FLiTcalibration.m`
This script is used to:
- Define basic setup parameters and hardware configuration
- Implement and define calibration procedures, including:
  - Diffraction efficiency calibration
  - Tiled hologram efficiency calibration
  - Spatial calibration of stimulation spots

---

#### `FLiT_stimulation_MAIN.m`
This script is used to:
- Define stimulation patterns (i.e. spot coordinates and their distribution across tiled holograms)
- Set stimulation parameters
- Generate waveforms to drive:
  - Galvomirrors
  - Laser power control
- Execute FLiT photostimulation experiments

The current version implements a **cyclic stimulation protocol**, but it can be easily adapted to other photostimulation paradigms.

---

## Meadowlark SLM control software

In addition to the MATLAB scripts, we provide a home-made GUI-based application called **`meadowlarkFeeder`**, developed by *Vincent de Sars*, to control the **Meadowlark SLM** model used in the paper.

Key features:
- Built on the manufacturer-provided SDK
- Optimized graphical interface
- Additional tools to simplify SLM addressing for photostimulation pipelines

---

## Notes

Although this material was developed for a specific hardware configuration, it is **easily adaptable** and can serve as a **starting point** for users interested in setting up their own FLiT-based photostimulation pipeline.
