# Quality of Service (QoS)

{% hint style="warning" %}
QoS was not supported by PCI/PCI-X.
{% endhint %}

## Traffic Class (TC)

* 3-bit field in the header, given by the software layer based on performance requirements.
* TC0 must be supported by any PCIe devices.

## Virtual Channels (VC)

* Up to 8 channels (VC0\~VC7)
* By default, VC0 must be implemented by any PCIe devices.

### TC/VC Mapping

* In the simplest form, TC-VC mapping is one-to-one.
* In practice, multiple TCs as a group can be mapped onto a single VC (to reduce cost).
* Within a TC group, TLPs will flow with equal priority.

## Port Arbitration

* 2 packets arrive on different ingress ports, but mapped to the same VC of a common egress port.
* RR, weighted-RR, programmable time-based RR

## VC Arbitration

* Coming after port arbitration, VC arbitration resolves the order in which TLPs from different VC are forwarded.
* Strict priority, RR, Weighted RR
