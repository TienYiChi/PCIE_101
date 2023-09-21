---
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

# Transaction Basics

## Memory, IO, Configuration, Message

## Transaction types:

| Type                          | Behavior   |
| ----------------------------- | ---------- |
| Mem Read                      | Non-posted |
| Mem Read Lock                 | Non-posted |
| Mem Write                     | Posted     |
| IO Read                       | Non-posted |
| IO Write                      | Non-posted |
| Config Read (Type 0, Type 1)  | Non-posted |
| Config Write (Type 0, Type 1) | Non-posted |
| Message                       | Posted     |

***

## Posted vs. Non-posted:

#### Non-posted

* A completion TLP must be sent back to the requester, which notifies the requester of the status.

#### Posted

* No completion packet is needed, thus less time being wasted compared to non-posted transactions.
* Completer may initiate an message TLP to the root complex for further error handling.

***

{% hint style="warning" %}
Transactions <mark style="color:red;">**CANNOT**</mark> cross two different ports of the root complex.
{% endhint %}
