---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Transaction Packets

## Transaction Layer Packet Types

<table><thead><tr><th width="153">Type</th><th>Behavior</th></tr></thead><tbody><tr><td>MRd</td><td></td></tr><tr><td>MRdLk</td><td>Locked</td></tr><tr><td>MWr</td><td></td></tr><tr><td>IORd</td><td>Initiated by root complex / legacy endpoints</td></tr><tr><td>IOWr</td><td>Initiated by root complex / legacy endpoints</td></tr><tr><td>CfgRd0</td><td>For EP</td></tr><tr><td>CfgRd1</td><td>For RC/Switch</td></tr><tr><td>CfgWr0</td><td>For EP</td></tr><tr><td>CfgWr1</td><td>For RC/Switch</td></tr><tr><td>Msg</td><td>Requester to completer / broadcast from root complex to all endpoints</td></tr><tr><td>MsgD</td><td>Requester to completer / broadcast from root complex to all endpoints</td></tr><tr><td>Cpl</td><td></td></tr><tr><td>CplD</td><td></td></tr><tr><td>CplLk</td><td>Locked error completion without data for MRdLk</td></tr><tr><td>CplDLk</td><td>Locked normal completion with data for MRdLk</td></tr></tbody></table>

### Locked TLP request

* Locked requests can only be initiated by **root complex** on behalf of CPU.
* **All ingress and egress ports** of the switches along the path are locked.
* The ports along the path from requester to completer **remain locked** until requester initiates an unlock message later.
