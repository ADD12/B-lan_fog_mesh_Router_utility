# B-lan FOG Mesh Router Documentation

## Overview
This router has been configured as a **node** within the **B-LAN-MESH-01** B-lan Fog Mesh network.

## Network Details
- **Router Name:** FogNode-01
- **IPv6 Prefix:** fd00:b1a4::
- **Gateway:** fd00:b1a4::1
- **DTN EID:** dtn://blan.fog/node01

## Fog-to-DTN Model
This network implements a Delay Tolerant Networking (DTN) model over a Fog computing architecture. 
Data is processed at the edge (Fog nodes) and forwarded via the Bundle Protocol to the B-lan main server.

### Routing Logic
- **Local Traffic:** Handled via IPv6 mesh (802.11s).
- **Global/Server Traffic:** Encapsulated in DTN bundles and routed towards the gateway.
- **Persistence:** In case of intermittent connectivity, bundles are stored locally until a path to the next hop is available.

## Installation Instructions
1. Access your router via SSH.
2. Upload the generated `configure_blan.sh` script.
3. Run `chmod +x configure_blan.sh`.
4. Execute `./configure_blan.sh`.
5. Reboot the router.

## Joining the Mesh
Others can join this mesh by scanning the generated QR code or manually configuring their devices to use the Mesh ID: **B-LAN-MESH-01**.
