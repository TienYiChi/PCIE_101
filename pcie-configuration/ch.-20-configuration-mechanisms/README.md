# Ⓜ Ch. 20 Configuration Mechanisms

## PCI Compatible Mechanism

***

## PCIE Enhanced Configuration Access Mechanism (ECAM)

{% hint style="info" %}
**Host Bridge** is required to translate the memory-mapped PCI Express Configuration Space accesses from the host processor to PCI Express configuration transactions.
{% endhint %}

{% hint style="info" %}
A **PCIE device** must support additional 4 bits, the **Extended Register Address \[3:0]**, for decoding configuration register access.
{% endhint %}

{% hint style="warning" %}
Device-specific register should be placed in **memory space requested by BAR**, rather than in the configuration space. The latter is <mark style="color:red;">**strongly discouraged**</mark>.
{% endhint %}
