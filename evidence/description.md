# Network Evidence

This folder contains command-output screenshots documenting selected network states. The screenshots are snapshots of the displayed devices and VLANs; they do not by themselves prove end-to-end reachability, failover, or current device state.

## Evidence currently available

- **HSRP:** [`HSRP/`](HSRP/) contains `show standby brief` and detailed `show standby` outputs for the devices in the `DWS1` and `DWS2` subfolders. The brief outputs show gateway roles split across VLANs 10–99. The VLAN 99 output reports the peer as `unknown`; see the [HSRP description](HSRP/description.md).
- **Spanning tree:** [`STP/`](STP/) contains `show spanning-tree` outputs for DSW1, DSW2, and ASW1–ASW4. The captured distribution outputs identify DSW1 as root for VLAN 10 and DSW2 as root for VLAN 20. The access-switch screenshots show an alternate/blocked uplink in the displayed VLAN, consistent with a redundant Layer 2 path.

## Evidence not currently present

There are no OSPF-neighbor, routing-table, or failure/recovery screenshots in the current evidence files. Add those outputs before documenting OSPF adjacencies, learned routes, or observed recovery as verified results. The [test overview](../tests/overview) describes intended testing but is not a test result.
