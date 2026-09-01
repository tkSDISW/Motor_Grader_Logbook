---
id: dec-0003-d5b544cffec44017aebe9d6aecbe47f4
type: decision
timestamp: 2026-09-01T15:52:57Z
author: Claude Motor Grader
tags: []
---

## Decision: Adopt PMEI Prefix Convention for Component Exchange Names

### Decision
Going forward, all Component Exchange names in this model will carry a prefix indicating which of the four Design Structure Matrix (DSM) interaction categories the exchange represents:

- **P (Physical)**: spatial/mechanical connections, geometric constraints, physical mating or contact between components.
- **M (Material)**: flow, transfer, or exchange of physical substances, fluids, or raw materials through channels or ducts.
- **E (Energy)**: transfer or transformation of power, electrical current, thermal energy, or mechanical force.
- **I (Information)**: transmission of data, control signals, logic commands, or feedback between nodes.

### Rationale
PMEI classification is a recognized systems-engineering/product-architecture convention for categorizing component interfaces in a Design Structure Matrix (source: https://vbn.aau.dk/ws/files/549531421/Thesis_trykning.pdf). Tagging each Component Exchange with its PMEI category at the naming level makes the interface type immediately legible in diagrams and browsers without opening the exchange to check what it carries — useful both for engineering review and for the eventual product-configurator/BOM work (dec-0005), where physical/material/energy/information interfaces often have different downstream implications (e.g. energy and material interfaces tend to map to physical connectors/ports on a BOM; information interfaces often don't).

### Naming format
`[X] Existing Name` — single-letter bracketed prefix, consistent with the project's existing bracketed diagram-naming convention (`[OCB]`, `[OAB]`, `[OPD]`, `[LAB]`, `[SAB]`, `[MCB]`).

### Next step
Full pass over all existing Component Exchanges to classify and rename per this convention — to follow in this same session.
