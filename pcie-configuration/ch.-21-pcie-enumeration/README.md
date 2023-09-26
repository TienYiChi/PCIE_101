# 🌲 Ch. 21 PCIe Enumeration

## Enumeration:

* The process of discovering the **existing buses and devices** behind them.
* Assign BDF ID to each function.

***

## In PCIE Capabilities Register:

#### Device/Port type field:

1. 0000b: EP
2. 0001b: Legacy EP
3. 0100b: Root port of RC
4. 0101b: Upstream port
5. 0110b: Downstream port
6. 0111b: PCIe to PCI/PCI-X bridge
7. 1000b: PCI/PCI-X to PCIe bridge
