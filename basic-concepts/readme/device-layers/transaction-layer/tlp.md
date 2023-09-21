# TLP

## Header

* **Address** (Transaction routing)
  * Memory req.: 32/64-bit
  * IO req.: 32-bit
  * Config req.: Bus# + Device# + Func# + Config register address.
  * Completion req.: requester ID of the original requester
  * Message req.: Bus# + Device# + Func# / Root complex or upstream port for broadcasting
* **TLP type**
  * [#transaction-layer-packet-types](../../transaction-packets.md#transaction-layer-packet-types "mention")
* **Transfer size**
  * 1-1024 doublewords, signifying the data transfer length.
* **Requester/completer ID**
  * Bus# + Device# + Func#
* **Tag**
  * Memorized and used by the completer.
* **Traffic class**
  * Priority
* **Byte enables**
* **Completion codes**
* **Attributes** ("no snoop", "relaxed ordering" bits)
* **TLP Digest bit**
  * Indicates whether this packet contains ECRC

***

## ECRC

* 32-bit field.
* Generated from the 1st byte of header to last byte of data payload, with the exception of **EP bit** and **bit 0 of Type field (always considered to be 1)**.
* Receiver side checks this field for CRC errors. If none, ECRC is stripped and **header + data payload** is forwarded to the **device core**.

***

## Transmit side:

* Receives core section **(Header - Data)** from the **software layer/device core**.
* Assembly of the core section:\
  **Header - Data - ECRC**(Optional).
* ECRC = End-to-end Cyclic Redundancy Check.

## Receive side:

* Checks for ECRC errors.
* Strips ECRC field away, and then forwards the **Header - Data** to the software layer/device core.
