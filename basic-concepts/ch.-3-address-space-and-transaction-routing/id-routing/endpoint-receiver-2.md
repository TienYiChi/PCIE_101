# Endpoint Receiver (2)

* **EP device** checks **Bus#, Device#, Function#** of the packet header against its own.
* Bus#, Device# were set (and remembered by EP) by **Configuration Write Type0 TLP at Byte 8, 9.**
* **At reset**, all bus and device numbers **in the system revert to 0.**
