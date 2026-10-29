# MFS Interview Notes
**Candidate:** Vijai (vijaiv@umich.edu)  
**Hiring Manager:** Dr. Max Fomitchev-Zamilov  
**Date:** 2026-10-29

---

## Problem 1: Reactor Interface

### My Restatement
*(to be filled in after Phase 1)*

### Given Data and Constraints
- Reactor body: 6" ConFlat (CF) vacuum nipple, mounted upright
- 6" CF flange OD: ~152 mm, face bore: ~130 mm, 16 x 1/4-20 bolts
- Bottom flange: Branson Sonifier SFX 500W, 20 kHz piezoelectric driver
- Reactor fluid: mineral oil, filled to half height
- Top flange must accommodate all of the following:
  1. KF16 vacuum port
  2. Bruker X-Flash 6 SDD Detector: 20mm vacuum nipple, compression fitting hinted
  3. IR camera (model TBD, generic) for interior monitoring
  4. Electrical feedthrough for PCB Piezotronics 113B03 piezoelectric transducer
  5. Electrical or mechanical feedthrough for immersion thermocouple
  6. HAMAMATSU H10682-110 or R928-17 photomultiplier for optical emission monitoring

### What We Learned From Photos

**System vacuum level:**
- Vacuum isolation valve on the system is a CF Manual Right Angle Valve (copper gasket, UHV rated)
- However problem specifies KF16 for the top flange vacuum port
- Estimate: rough to medium vacuum, 1–100 mTorr operating range
- O-ring seals (KF, compression fittings) are acceptable for most ports

**Bottom flange (sonifier attachment):**
- Standard 6" CF full nipple has NO openings in the tube body or flanges
- Both flanges are blank from the factory — all ports must be machined into the flanges
- Bottom blank flange is custom machined with a central blind threaded boss for sonifier horn
- Sonifier horn threads into this blind boss (no through-hole, vacuum integrity preserved)
- Vibration transfers mechanically through the flange wall into the oil above
- Branson horn thread spec: check with Dr. Max (likely 3/4"-16 UNF or Branson proprietary)
- Vacuum connection: goes through the TOP flange (KF16), NOT the bottom

**Top flange (what we are designing):**
- Existing system already has a welded cluster flange on top (visible in photos)
- Our job: design an improved/complete version carrying all 6 ports listed above
- Approach: custom-machined 6" CF blank with ports drilled/tapped + KF stubs welded on
- Black tape visible in photos = just electrical tape around the bolt ring joint, not a functional part

**Parts identified in photos:**
- CF Manual Right Angle Valve (1.33" or 2.12" CF) = vacuum isolation valve in the pump line
- Flexible stainless bellows = vacuum hose from reactor to pump/valve
- Multi-port welded cluster flange = existing top flange assembly

**Parts considered but ruled out (for now):**
- CF double-sided flange with NPT side port (shown on catalog page): correct concept but
  wrong size (1.33"/2.75" CF vs 6" CF needed). Could be used for a future bottom vacuum port.
  Filed as a useful part type to know about.

**PMT choice:**
- H10682-110: self-contained photon counting module, +5V, TTL out, plug-and-play
- R928-17: bare PMT tube, needs >1kV HV supply + divider circuit + housing
- Decision: propose H10682-110 — far simpler to integrate

### Assumptions
- A1: Operating pressure is rough vacuum, ~1–100 mTorr (based on pump hardware visible in photos)
- A2: O-ring seals (Viton) acceptable for all ports except where stated otherwise
- A3: Top flange is machined from a 316L SS blank (same material as tube body)
- A4: H10682-110 preferred over R928-17 (simpler integration)
- A5: IR camera window material TBD — pending Dr. Max specifying camera model and wavelength range

### Options Considered
*(to be filled in during Phase 3)*

### Calculations and Results
*(to be filled in during Phase 4)*

### Open Questions for Dr. Max
1. What is the actual operating vacuum level (pressure range)?
2. What IR camera model? What wavelength range (MWIR 3–5µm or LWIR 8–12µm)?
3. Should the vacuum port be KF16 or CF, given the isolation valve is CF?
4. What is the Branson horn thread spec (for bottom flange machining reference)?
5. Is the existing top flange being replaced, or are we adding to it?
6. Any constraint on top flange thickness or port spacing?

### Decisions So Far
- Design target: custom-machined 6" CF blank top flange, 316L SS
- All 6 ports go on the top flange only
- Bottom flange: blind boss for sonifier, no other ports needed
- PMT: propose H10682-110 (module), not R928-17 (bare tube)
- Seal strategy: KF16 for vacuum port, compression fittings for small sensors,
  O-ring face seal for IR viewport and PMT viewport — to be confirmed in Phase 3

---

## Problem 2: Electrostatic Charging Maximization (Bonus)

### My Restatement
*(to be filled in after Phase 1)*

### Given Data and Constraints
- Fluid: mineral oil (dielectric)
- Mechanism: charge separation when oil passes through narrow dielectric channel
- Goal: MAXIMIZE electrostatic potential (opposite of normal engineering goal)
- Deliverable: approach to maximize + method to measure the effect

### Assumptions
*(to be filled in)*

### Options Considered
*(to be filled in)*

### Calculations and Results
*(to be filled in)*

### Open Questions for Dr. Max
*(to be filled in)*

### Decisions So Far
*(to be filled in)*
