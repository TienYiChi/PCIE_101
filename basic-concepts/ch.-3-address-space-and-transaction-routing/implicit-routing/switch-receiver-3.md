# Switch Receiver (3)

## Based on bit \[2:0] of Type field:

#### Use address routing / ID routing

#### Implicit routing:

* Checks the legitimacy of the packet regarding its **destination and arriving port.**
* Example 1. **"Broadcast"** packets can only come from upstream (primary side, RC).
* Example 2. **"Route to RC"** packets can only come from downstream.

If routing indicates **"terminate at receiver"**, the switch may consume it.
