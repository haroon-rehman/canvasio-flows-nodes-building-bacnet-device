# BACnet Device (RETIRED)

> **RETIRED** — BACnet Device (`bacnet-device`) is now maintained in
> `canvasio-flows-node-building-bacnet` (`@halsystems/red-bacnet`).
>
> Do not install this package in the Canvas IO harness or Node Pack.
> This repository is retained for historical reference only.

---

## Historical notes

Previously this package provided a standalone BACnet Device node using
`bacstack@0.0.1-beta.14`. That implementation has been replaced by a
HAL-backed Device that shares the `bacnet client` / BACnet Network config
with Discover, Read, and Write.

| | |
|--|--|
| Domain | Building / BACnet |
| Status | **Retired** |
| Successor | `canvasio-flows-nodes/canvasio-flows-node-building-bacnet` |
| npm package name | `node-red-contrib-bacnet-device` (do not use) |
| Registered type (historical) | `bacnet-device` |

`canvasio-flows-nodes` is an organizational parent only — not a monorepo.
