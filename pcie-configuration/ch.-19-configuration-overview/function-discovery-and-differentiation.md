# Function Discovery and Differentiation

## Discovery of Functions

RC discovers by functions by reading/probing hardwired **Vendor ID** assigned by PCI-SIG in each function's config register.

Receiving value **FFFFh** indicates a non-existent function.

***

## &#x20;Single/Multi Function Device

The highest bit of the Header Type register identifies the type of device:

* 0: Single-function device
* 1: Multi-function device

***

## PCI-to-PCI Bridge / Non-Bridge Function

The lower 7 bits of the Header Type register identifies the category of the function:

* 0 = Non-bridge function
* 1 = PCI-to-PCI bridge
* 2 = CardBus bridge
