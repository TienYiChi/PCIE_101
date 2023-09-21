# Switch Receiver (1)

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

1. **Switch device** checks if it is the intended completer.\
   It checks the address in the packet header against the **target addresses programmed in its 2 BARs,** and if it falls within the range, it consumes the packet.
2. If not, it then checks Type1 configuration space header **for each downstream**. If it falls in the range of one of its **secondary bridge interface Base/Limit register sets**, it will forward the packet downstream.
3. Otherwise, the packet will be handled as **Unsupported Request** on the primary link.
