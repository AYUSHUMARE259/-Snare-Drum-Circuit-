# Snare Drum Circuit — PCB Design (EE 322 AMSC Project)

**Course:** EE 322 – Analog and Mixed Signal Circuits
**Term:** Semester 1, 2025–26
**Team:** Team Behzad

## The Team

| Member | Roll No. |
|---|---|
| Yash Sonone | 23110318 |
| Sumedh Wankhede | 23110364 |
| Ayush Umare | 23110346 |

---

## What This Project Is

An electronic snare drum circuit, designed from schematic to soldered board and demonstrated live. The circuit synthesizes a snare-drum sound purely through analog circuitry — no samples, no microcontroller — and the final PCB played back an audible, recognizable snare hit.

Everything here was built the way a real hardware project should be: simulate first, prove it on a breadboard, then commit to copper.

## How We Got There

1. **Simulate** — Modeled the snare drum circuit in LTspice to confirm the topology would actually produce a snare-like waveform before touching hardware.
2. **Prototype** — Built the circuit on a breadboard to validate it worked with real components and real noise, not just an idealized simulation.
3. **Design the PCB** — Captured the schematic in KiCad, assigned footprints, ran ERC to catch wiring issues, then placed and routed the layout.
4. **Verify** — Ran DRC to check the layout against fabrication constraints, and reviewed the board in 3D before export.
5. **Fabricate** — Generated Gerber and drill files and sent them to LionsCircuit for manufacturing.
6. **Build & Demo** — Hand-soldered every component onto the fabricated board and demonstrated the finished circuit producing live snare drum audio.

---

## Repository Layout

```
├── Team_Behzad_Project_Proposal            # project proposal
├── full_schematic_kicad.kicad_pcb_final.kicad_pcb   # PCB layout (KiCad)
├── full_schematic_kicad.kicad_pcb_final.kicad_pro   # KiCad project file
├── gerber_files_amsc_project/                        # Fabrication-ready Gerbers
│   ├── *-F_Cu.gbr / *-B_Cu.gbr            # Copper layers (front/back)
│   ├── *-F_Mask.gbr / *-B_Mask.gbr        # Solder mask layers
│   ├── *-F_Silkscreen.gbr / *-B_Silkscreen.gbr  # Silkscreen layers
│   ├── *-Edge_Cuts.gbr                    # Board outline
│   ├── *-PTH.drl / *-NPTH.drl             # Drill files (plated/non-plated)
│   └── *-job.gbrjob                       # Gerber job file
└── Team Behzad_AMSC.pdf                              # Full written report
```

---

## Toolchain

- **LTspice** — pre-layout circuit simulation
- **KiCad** (v7+ recommended) — schematic capture and PCB layout
- **LionsCircuit** — PCB fabrication

## Getting the Project Running Locally

1. Install [KiCad](https://www.kicad.org/) (v7 or newer).
2. Clone the repo:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Team-Behzad-AMSC.git
   ```
3. Open `full_schematic_kicad.kicad_pcb_final.kicad_pro` in KiCad to view the schematic and layout.
