# Ⓜ Ch. 20 Configuration Mechanisms

## PCI Compatible Mechanism

* Read/Write via IO Address Space

***

## PCIE Enhanced Configuration Access Mechanism (ECAM)

{% hint style="info" %}
**Host Bridge** is required to translate the memory-mapped PCI Express Configuration Space accesses from the host processor to PCI Express configuration transactions.
{% endhint %}

{% hint style="info" %}
A **PCIE device** must support decoding additional 4 bits, the **Extended Register Address \[3:0] = Upper 4 bits of DW offset**.
{% endhint %}

{% hint style="warning" %}
Device-specific register should be placed in **memory space requested by BAR**, rather than in the configuration space. The latter is <mark style="color:red;">**strongly discouraged**</mark>.
{% endhint %}
