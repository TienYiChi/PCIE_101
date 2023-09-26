# Table of contents

## Basic Concepts

* [🏫 Ch. 2 PCIe Architecture Overview](README.md)
  * [Transaction Basics](basic-concepts/readme/transaction-basics.md)
  * [Transaction Packets](basic-concepts/readme/transaction-packets.md)
  * [Device Layers](basic-concepts/readme/device-layers/README.md)
    * [Device Core / Software Layer](basic-concepts/readme/device-layers/device-core-software-layer.md)
    * [Transaction Layer](basic-concepts/readme/device-layers/transaction-layer/README.md)
      * [TLP](basic-concepts/readme/device-layers/transaction-layer/tlp.md)
      * [Quality of Service (QoS)](basic-concepts/readme/device-layers/transaction-layer/quality-of-service-qos.md)
    * [Data Link Layer](basic-concepts/readme/device-layers/data-link-layer/README.md)
      * [TLP and DLLP (1)](basic-concepts/readme/device-layers/data-link-layer/tlp-and-dllp-1.md)
    * [Physical Layer](basic-concepts/readme/device-layers/physical-layer/README.md)
      * [TLP and DLLP (2)](basic-concepts/readme/device-layers/physical-layer/tlp-and-dllp-2.md)
      * [PLP (Ordered Sets)](basic-concepts/readme/device-layers/physical-layer/plp-ordered-sets.md)
  * [Extra Notes](basic-concepts/readme/extra-notes.md)
* [🔀 Ch. 3 Address Space & Transaction Routing](basic-concepts/ch.-3-address-space-and-transaction-routing/README.md)
  * [Device Config Registers for Routing](basic-concepts/ch.-3-address-space-and-transaction-routing/device-config-registers-for-routing/README.md)
    * [Base Address Registers (BARs)](basic-concepts/ch.-3-address-space-and-transaction-routing/device-config-registers-for-routing/base-address-registers-bars.md)
    * [Base/Limit Registers](basic-concepts/ch.-3-address-space-and-transaction-routing/device-config-registers-for-routing/base-limit-registers.md)
    * [Bus Number Registers](basic-concepts/ch.-3-address-space-and-transaction-routing/device-config-registers-for-routing/bus-number-registers.md)
  * [TLP Header](basic-concepts/ch.-3-address-space-and-transaction-routing/tlp-header.md)
  * [TLP Routing Basics](basic-concepts/ch.-3-address-space-and-transaction-routing/tlp-routing-basics.md)
  * [Address Routing](basic-concepts/ch.-3-address-space-and-transaction-routing/address-routing/README.md)
    * [Endpoint Receiver (1)](basic-concepts/ch.-3-address-space-and-transaction-routing/address-routing/endpoint-receiver-1.md)
    * [Switch Receiver (1)](basic-concepts/ch.-3-address-space-and-transaction-routing/address-routing/switch-receiver-1.md)
  * [ID Routing](basic-concepts/ch.-3-address-space-and-transaction-routing/id-routing/README.md)
    * [Endpoint Receiver (2)](basic-concepts/ch.-3-address-space-and-transaction-routing/id-routing/endpoint-receiver-2.md)
    * [Switch Receiver (2)](basic-concepts/ch.-3-address-space-and-transaction-routing/id-routing/switch-receiver-2.md)
  * [Implicit Routing](basic-concepts/ch.-3-address-space-and-transaction-routing/implicit-routing/README.md)
    * [Endpoint Receiver (3)](basic-concepts/ch.-3-address-space-and-transaction-routing/implicit-routing/endpoint-receiver-3.md)
    * [Switch Receiver (3)](basic-concepts/ch.-3-address-space-and-transaction-routing/implicit-routing/switch-receiver-3.md)

## PCIe Configuration

* [⚙ Ch. 19 Configuration Overview](pcie-configuration/ch.-19-configuration-overview/README.md)
  * [Configuration Transactions](pcie-configuration/ch.-19-configuration-overview/configuration-transactions.md)
  * [Function Discovery and Differentiation](pcie-configuration/ch.-19-configuration-overview/function-discovery-and-differentiation.md)
* [Ⓜ Ch. 20 Configuration Mechanisms](pcie-configuration/ch.-20-configuration-mechanisms/README.md)
  * [PCI Compatible Mechanism](pcie-configuration/ch.-20-configuration-mechanisms/pci-2.3-compatible-mechanism.md)
  * [PCIe Enhanced Mechanism](pcie-configuration/ch.-20-configuration-mechanisms/pcie-enhanced-mechanism.md)
  * [Initial Configuration Accesses](pcie-configuration/ch.-20-configuration-mechanisms/initial-configuration-accesses.md)
* [🌲 Ch. 21 PCIe Enumeration](pcie-configuration/ch.-21-pcie-enumeration/README.md)
  * [Single RC](pcie-configuration/ch.-21-pcie-enumeration/single-rc.md)
  * [Multiple RC](pcie-configuration/ch.-21-pcie-enumeration/multiple-rc.md)
  * [Multi-Function Device within RC/Switch](pcie-configuration/ch.-21-pcie-enumeration/multi-function-device-within-rc-switch.md)

## 🛤 TL Tracking

* [Bus Enum](tl-tracking/bus-enum.md)
* [BAR Init](tl-tracking/bar-init.md)
