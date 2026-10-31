# HSRP Verification Evidence

This folder contains HSRP command-output screenshots for the distribution switches. The `show_standby_brief.png` screenshots provide a per-VLAN summary; `show_standby.png` and `show-standby.png` contain detailed group output, including virtual IP/MAC addresses, active and standby routers, priorities, timers, and preemption state.

## Summary of the captured brief outputs

| VLAN | Virtual gateway | DWS1 captured state | DWS2 captured state |
|---:|---|---|---|
| 10 | 10.10.10.1 | Active | Standby |
| 20 | 10.10.20.1 | Standby | Active |
| 30 | 10.10.30.1 | Active | Standby |
| 40 | 10.10.40.1 | Standby | Active |
| 50 | 10.10.50.1 | Active | Standby |
| 60 | 10.10.60.1 | Standby | Active |
| 99 | 10.10.99.1 | Standby; active peer shown as `unknown` | Active; standby peer shown as `unknown` |

These are observations from the screenshots, not a guarantee of current state or a failover test. In particular, investigate why the VLAN 99 peer is reported as `unknown` on both devices, and verify the HSRP state and preemption settings directly on the switches before relying on them.

## Screenshot files

| Device folder | Summary output | Detailed output |
|---|---|---|
| [`DWS1/`](DWS1/) | [`show_standby_brief.png`](DWS1/show_standby_brief.png) | [`show_standby.png`](DWS1/show_standby.png), [`show-standby.png`](DWS1/show-standby.png) |
| [`DWS2/`](DWS2/) | [`show_standby_brief.png`](DWS2/show_standby_brief.png) | [`show_standby.png`](DWS2/show_standby.png), [`show-standby.png`](DWS2/show-standby.png) |

The folder names use `DWS1`/`DWS2`; the device configurations refer to the distribution switches as `DSW1`/`DSW2`.