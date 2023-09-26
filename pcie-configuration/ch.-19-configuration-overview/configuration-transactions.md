# Configuration Transactions

## Configuration Registers of a Device

4KB = 1024 DW in total.

### PCI-Compatible Space

First 256B = 64DW, accessible via both PCI-compatible mechanism or ECAM.

### PCI Express Extended Configuration Space

Remaining 960DW, only accessible by ECAM.

***

## Properties of Configuration Transaction

* Only **RC** can originate configuration transactions.
* Only move downstream.
* No P2P.

***

## Routing Rules

* Configuration transactions use **ID routing** (Bus#, Device#, Function#).
