# Endpoint Receiver (1)

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

**EP device** checks the address in the packet header against each of its implemented BARs.

1. It checks the address in the packet header against the target addresses programmed in its **6 BARs,** if it falls within the range, it consumes the packet.
2. Otherwise, it will **reject** the packet.
