# Data Link Layer

{% hint style="info" %}
The primary function of Data Link Layer is to ensure **data integrity**.\
**Error detection and auto replay erroneous packets mechanism** makes PCIe ideal for low error rate, high availability systems.
{% endhint %}

## Functions

### ACK/NAK mechanism

* Sequence ID and a LCRC is generated and appended to the TLP, and a copy of this TLP is preserved in a **replay buffer**.
* If <mark style="color:red;">**NO**</mark> CRC error is detected, the receiver device returns a **ACK DLLP containing a sequence ID** to confirm that a TLP has reached at the receiving end (not necessarily the final destination). As a consequence, the stored TLP is cleared from replay buffer.
* If CRC error is detected, the receiver device returns a **NAK DLLP containing a sequence ID and eliminates the TLP**, and the transmitter device then replays the TLP from the replay buffer\*\*.\*\*
* If transmitter device **gets NAK 4 times, i.e. TLP is relayed 3 times**, the Data Link Layer logs the error, reports a correctable error, and re-trains the Link.

### Power management

* PMx DLLP

### Flow control

* FCx DLLP
* Accomplished at hardware level.

***

## Notes

* DLLPs <mark style="color:red;">**DO NOT**</mark> pass through **switches**.
