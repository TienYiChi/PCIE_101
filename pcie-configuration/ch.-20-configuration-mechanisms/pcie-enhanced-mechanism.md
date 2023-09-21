# PCIe Enhanced Mechanism

## Configuration Space

#### 256 Buses \* 32 Devices \* 8 Functions \* 4KB = 256MB

* Bits \[63:28] = 256MB-aligned base address
* Bits \[27:20] = target bus number
* Bits \[19:15] = target device number
* Bits \[14:12] = target function number
* Bits \[11:2] = **target DW** within the configuration
* Bits \[2:0] = **target byte location** within the DW (1 DW = 4 bytes)

***

## Difference of Type0 / Type1

* When the request **ARRIVES** on the destination bus.
* When it is performed on **EACH BUS ON THE WAY** to the destination bus.

***

## In the TLP header...

### Format Field

* 00 = Read
* 10 = Write

### Type Field

* 00100 = Type 0
* 00101 = Type 1

***

## For a switch/bridge device receiving Type 1 request...

* If target bus <mark style="color:red;">**IS**</mark> the bridge's secondary bus, this Type 1 request **converted to a Type 0 request** and then forwarded downstream.
* If not, but is a downstream bus below this port, the Type 1 request is passed as is.
