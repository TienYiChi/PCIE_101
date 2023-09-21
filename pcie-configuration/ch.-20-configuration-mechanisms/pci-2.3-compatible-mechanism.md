# PCI Compatible Mechanism

**PCI Spec.** defined a method of performing PCI config access via **processor-initiated IO accesses**, with some constraints:

* The only practically available IO address range is **0C00h-0CFFh**
* Each PCI function (including **host/PCI bridge**) on PCI bus requires 64 DWs of configuration space.

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

***

## Configuration Address Port (0CF8h-0CFBh, 32bit)

Write the target **Bus#, Device#, Function#, DW#**, and **set Enable bit to 1**

***

## Configuration Data Port (0CFCh-0CFFh, 32bit)

Perform a 1-byte, 2-byte, or 4-byte IO read/write to the **CFGDAT address**.

***

## Host/PCI Bridge in RC

is responsible for generating Type0 or Type1 config transactions by comparing the **Bus# in CFGADR register** to its **own Bus#** and **subordinate Bus#**.
