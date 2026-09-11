# BACnet Device

Canvas IO Workflows — maintained integration/fork of an independent Node-RED node package.

## Canvas IO

| | |
|--|--|
| Domain | Building / BACnet |
| Development status | Integrated in local harness (cio-wfs-dev) |
| Palette category (operational) | `Canvas IO` |
| Config nodes | remain `category: "config"` |
| Local repository | `cio-wfs-nodes/cio-wfs-node-building-bacnet-device` |
| npm package name | `node-red-contrib-bacnet-device` (unchanged) |

`cio-wfs-nodes` is an organizational parent only — not a monorepo. One node package = one Git repository.

This repository is a **Canvas IO-maintained integration/fork**. Protocol and node runtime logic originate from upstream; Canvas IO changes are limited to integration, presentation, and local development packaging.

## Nodes

### Operational (palette: Canvas IO)

- `bacnet-device`

### Configuration

- (none registered as config category)

## Development

```powershell
cd C:\GitHub\canvasio\cio-wfs-nodes\cio-wfs-node-building-bacnet-device
npm install
```

Local harness:

```powershell
cd C:\GitHub\canvasio\cio-wfs-dev
npm install
cd C:\GitHub\canvasio\cio-wfs-core
node packages/node_modules/node-red/red.js --userDir C:\GitHub\canvasio\cio-wfs-dev
```

Open http://localhost:1880

## Testing

No automated test suite in this repository.

## Upstream

| | |
|--|--|
| Original package | `node-red-contrib-bacnet-device` |
| Upstream project | https://github.com/daps1005-debug/node-red-contrib-bacnet-device |

Canvas IO does not claim authorship of the original upstream implementation.

## License

MIT — see ``LICENSE``.

---

## Upstream documentation

The following sections retain useful upstream technical documentation (adapted only where needed).

# node-red-contrib-bacnet-device

BACnet Device polling node for Node-RED using bacstack.

## Features

- Read multiple BACnet points
- BACnet/IP support
- Queue-based polling
- Async processing
- Industrial automation ready
- HVAC / SCADA integration

---

## Installation

```bash
npm install node-red-contrib-bacnet-device
```

---

## Configuration

### Device Parameters

| Field | Description |
|---|---|
| Name | Optional node name |
| IP | BACnet device IP address |
| Points | BACnet objects to read |

---

## Point Configuration

Each point requires:

| Field | Description |
|---|---|
| Name | Output property name |
| Type | BACnet object type |
| Instance | BACnet object instance |
| Property | BACnet property id |

Default property:
```text
85 = Present Value
```

---

## Example

### Input

Inject node trigger.

### Output

```json
{
  "payload": {
    "RoomTemp": 23.5,
    "Humidity": 45,
    "FanStatus": 1
  },
  "device": "192.168.1.100",
  "timestamp": 1747880000000
}
```

---

## Example BACnet Objects

| Object | Type |
|---|---|
| Analog Input | 0 |
| Analog Output | 1 |
| Analog Value | 2 |
| Binary Input | 3 |
| Binary Output | 4 |
| Binary Value | 5 |

---

## Dependencies

- bacstack

---

## Use Cases

- HVAC monitoring
- Smart buildings
- Hotel automation
- Industrial SCADA
- BACnet/IP integrations

---

## License

MIT