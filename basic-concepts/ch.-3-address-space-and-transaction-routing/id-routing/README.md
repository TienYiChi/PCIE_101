# ID Routing

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

## Bus Number, Device Number, Function Number

* Suitable for **Completions and Messages.**
* **Bus number** is contained in **Byte 8**
* **Device number (5-bit) and Function number (3-bit)** is contained in **Byte 9**

## Basic Topology Limits

1. Maximum of **256 buses/links** in a system, including buses created by **PCI-compatible bridges.**
2. Maximum of **32 devices** per bus/link.
3. Maximum of **8 internal functions** per device.
