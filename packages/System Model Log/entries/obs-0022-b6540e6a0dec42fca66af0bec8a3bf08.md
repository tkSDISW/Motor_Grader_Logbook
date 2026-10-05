---
id: obs-0022-b6540e6a0dec42fca66af0bec8a3bf08
type: observation
timestamp: 2026-10-05T16:34:57Z
author: Claude Motor Grader
tags: []
---

**For Cousin: the base type of OA entities/actors was not discoverable through capella-fabric.** Companion to LESSON-0001.

While building the jobsite OA model, the tools gave no way to tell that an OA actor and an OA entity are different element types in Capella:
- `browse_model` and `generate_fabric` report both as `type: Entity`, distinguished only by `is_actor` (and `is_human`). The `type` field never revealed a different underlying type.
- `list_object_types` lists "Entity" and "Actor" for OA but does not explain that they are separate types, or that changing one into the other means recreating it with a new UUID.
- The Handbook (`mcp_tools`, "Reading and Changing a Model Safely") says an actor is an element flagged `is_actor`, which matched what the tools showed and so gave no warning.
- A patch that created the two actors as entities with `is_actor: true` succeeded with no warning; the engineer then had to recreate them in Capella, which changed their UUIDs.

**Related gap, same session:** the OA root package ("Operational Entities", an EntityPkg) did not show up in any browse or search on the empty model, so the engineer had to supply its UUID from Capella before any OA element could be created.

**Possible follow-ups for Cousin (suggestions, not decisions):** have browse/fabric output surface the underlying element type or a clear actor-vs-entity indicator, document the type-change behavior in the Handbook once verified, and make empty-layer root packages discoverable.
