---
description: PCIe System Architecture Vol. I Ch. 3
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🔀 Ch. 3 Address Space & Transaction Routing

## Transaction Layer Traffic

* Originates in the Transaction Layer of one device targeting the the Transaction Layer of another device.
* Gets forwarded if necessary, thus routing mechanism is required.

***

## Local Link Traffic

Local Link Traffic is never forwarded or flow controlled, and must be accepted once sent.

{% hint style="warning" %}
Because **Ordered sets and DLLPs** do <mark style="color:red;">**NOT**</mark> get forwarded, the routing rules only apply to **TLPs**.
{% endhint %}
