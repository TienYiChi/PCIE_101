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

# Base Address Registers (BARs)

**BARs** is the way in which a device makes **resource (system memory, IO, MMIO) allocation** request to the system.

### Type 0 Non-bridge Functions

* Have 6 BARs

### Type 1 Switch/Bridge Functions

* Have 2 BARs

{% hint style="info" %}
**64 bit BAR** requires additional one DW; in this case, **two consecutive DWs** will be merged as one.
{% endhint %}

***

## BARs Setup

1. Uninitialized BARs were **hard-coded at lower bits** to indicate resource type, address bit length, pre-fetchability... etc\*\*.\*\*
2. RC then writes **all read-write bits as 1's.** Hard-coded lower bits were not affected.
3. The first non-zero bit indicates the size of the requested resource, e.g. 10th bit indicates $$2^{10}$$ = 1MB of memory address.
4. After resource allocation, RC then writes the starting address back to **the upper BAR**.

<figure><img src="../../../.gitbook/assets/BARs.drawio (1).png" alt=""><figcaption></figcaption></figure>
