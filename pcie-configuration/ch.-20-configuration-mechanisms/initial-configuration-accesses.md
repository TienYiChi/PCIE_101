# Initial Configuration Accesses

PCI/PCI-X/PCIe devices may take time to self-initialize before being able to service configuration requests.

A PCIe device may return a **Config Request Retry Status (CRS)**, and the requester terminates the configuration access process upon receiving it.

## Failure Timeout

After a PCIe device resets, RC must allow **1.0 sec (+50% / -0%)** for it to return Successful Completion before deciding the device is malfunctioned,

***

## Delay Prior to Initial Config Access

After system causes one or more PCIe devices to reset, the system must wait **at least 100ms from the end of reset** before issuing configuration requests to these devices, for they need time to complete self-initialization.

***

## Lengthy Self-Initialization

Design-specific solution for re-issuing configuration requests after 1 sec timeout has elapsed for **extra-long self-initialization devices**.

***

## RC Response to CRS during runtime

It is entirely design-specific.

* Support for completion timeout.
* Number of retries.
* Actions being taken.
