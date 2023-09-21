# PLP (Ordered Sets)

<table><thead><tr><th width="129">Type</th><th width="250">Symbols</th><th>Purpose</th></tr></thead><tbody><tr><td>FTS</td><td>COM + 3 FTS</td><td></td></tr><tr><td>TS1</td><td>COM + LaneID + 14 more</td><td></td></tr><tr><td>TS2</td><td>COM + LaneID + 14 more</td><td></td></tr><tr><td>IDLE</td><td>COM + 3 IDLE</td><td></td></tr><tr><td>Skip</td><td>COM + 3 SKP</td><td></td></tr></tbody></table>

***

## Notes

* PLP is a **multiple of 4 bytes (doublewords = DW)** in size.
* PLPs <mark style="color:red;">**DO NOT**</mark> pass through **switches**.
* Example 1: Used during the **Link Training** process.
* Example 2: Used to place a Link into the **electrical idle low power state** / wake up a link from such state.
