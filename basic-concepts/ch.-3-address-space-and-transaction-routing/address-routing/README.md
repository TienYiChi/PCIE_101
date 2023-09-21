# Address Routing

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Address \[1:0] are always 0, since the byte address is always DW-aligned (4-bytes).
{% endhint %}

***

## Memory Read/Write, MMIO

* 3DW header for 32-bit address.
* 4DW header for 64-bit address.

***

## IO Locations

* 3DW for legacy devices.
