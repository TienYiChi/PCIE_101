# TLP Routing Basics

## General Concept

### 4 Address Spaces

* Memory
* IO
* Configuration
* Message: Eliminates the need of **sideband signals** related to **interrupts, error handling, and power management**.

### TLP routing steps include:

1. Examining **Type and Format** and deciding **which routing rule is used**.
2. Consuming or forwarding the TLP depending on who the recipient is.
3. Rejecting the TLP as an **Unsupported Request (UR)**, if neither the device nor any one in the path to it is the recipient.

{% hint style="info" %}
**Split Transactions**: Request TLP and Completion TLP is **separated in time**, thus the link is free for other activity in the time between.
{% endhint %}

***

## Routing Rules

| TLP Type                                  | Routing Method                                           |
| ----------------------------------------- | -------------------------------------------------------- |
| <p>MRd<br>MRdLk<br>MWr</p>                | Address Routing                                          |
| <p>IORd<br>IOWr</p>                       | Address Routing                                          |
| <p>CfgRd0 / CfgRd1<br>CfgWr0 / CfgWr1</p> | ID Routing                                               |
| Msg / MsgD                                | <p>Address Routing<br>ID Routing<br>Implicit Routing</p> |
| Cpl / CplD                                | ID Routing                                               |

{% hint style="info" %}
PCIe routing is compatible with PCI.
{% endhint %}
