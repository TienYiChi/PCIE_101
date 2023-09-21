# Single RC

## An Example, Device 0 on Bus 0:

<figure><img src="../../.gitbook/assets/image (12).png" alt="" width="480"><figcaption></figcaption></figure>

### Step 1: Read Vendor ID (Probing)

* If a valid vendor ID is returned, the device is implemented and **contains at least one function**.
* If **FFFF**h is returned as vendor ID, function 0 is not implemented in the device. The enumeration process will proceed to probe the next device.

### Step 2: Series of Configuration Writes

* Primary Bus # = 0.
* Secondary Bus # = 1.
* Subordinate Bus # = 1.

### Step 3: Updates Subordinate Bus \#

* Set subordinate bus # to 1 in the Host/PCI bridge.
* In the cases of devices further down the tree, subordinate bus # on **all devices along the path** back to Host/PCI bridge must be updated.

### Step 4: Checks Port Type

* The enumeration process reads the device's **"capability registers"** to check the port type field.
* In such case, **0100b** means **"root port"** on the RC.

### Step 5: Searches Buses/Devices/Functions by DFS

* Recursively by the order of **Bus -> Device -> Function.**
