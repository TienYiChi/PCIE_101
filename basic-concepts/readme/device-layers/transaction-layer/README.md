# Transaction Layer

## Functions

### Virtual Channels (VC)

* Logically categorizes traffic into **various priorities** for the purpose of **QoS**.

### VC Buffers

* Stores inbound/outbound TLPs.
* Default set of VC buffers is called "**VC 0 buffers**".

### Flow control

* **Flow control packets (FCx DLLPs)** are sent <mark style="color:red;">**from receiver device to transmitter device**</mark> periodically to prevents receiver's VC buffers from overflow. Transmitter device keeps track of this information (called **"credits"**) and only sends a TLP out to the receiver when it has enough buffer space to accept the TLP.
* Flow control is managed at the **hardware level (for VC 0)**.
* VC 0 buffers are enabled automatically after **Link training**, thus allow **config transactions** to begin immediately after.

### Ordering

* Guarantees TLPs within a given TC is routed in correct order to prevent live-lock, and deadlock conditions.
* Different TCs have no ordering relationship.

### Configuration registers

* Configured during initialization and bus enumeration, by device drivers.
* Accessed by OS/runtime software.
* Stores "Link capabilities", such as Link width and frequency.
