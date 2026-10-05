---
id: dec-0010-eab696b886da4ea08e8ff63ea1a0fce8
type: decision
timestamp: 2026-10-05T16:05:24Z
author: Claude Motor Grader
tags: []
---

**New "heavy equipment jobsite" Capella model will be a higher-level system-of-systems (SoS) model.**

A new, currently empty Capella model (repo `tkSDISW/heavy_equipment_jobsite`, branch `main`, `Heavy Equipment Jobsite.aird`) has been started. Per the engineer, it will serve as a higher-level system-of-systems model, sitting above the individual equipment/subsystem models (e.g., Motor Grader, Diesel Engine, After-Treatment System).

**State at creation:** OA empty; SA contains only the default root component "System".

**Open questions:** how constituent systems (Motor Grader, etc.) are represented at the SoS level (actors vs. components), where the SoS boundary lies, and how requirements/traceability flow between this model and the lower-level models.

*Reported by the engineer; scope and boundary details still to be defined.*
