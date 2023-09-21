# Implicit Routing

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

## Only messages use implicit routing

**Bit\[2:0] of Type field = RRR = Msg TLP routing subfield**, where message header indicates that this packet is intended for:

* **000b: Route to RC**
* 001b: Address routing
* 010b: ID routing
* **011b: Downstream broadcast**
* **100b: Terminates at receiver (neighbor device)**
* **101b: Gather & route to RC**
