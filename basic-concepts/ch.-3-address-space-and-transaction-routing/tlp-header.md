# TLP Header

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

## Format (2-bit), Type (5-bit)

<table><thead><tr><th width="134">TLP</th><th width="180.33333333333331">Fmt Field</th><th width="424">Type Field</th></tr></thead><tbody><tr><td>MRd</td><td>00 = 3DW, no data<br>01 = 4DW, no data</td><td>0 0000</td></tr><tr><td>MRdLk</td><td>00<br>01</td><td>0 0001</td></tr><tr><td>MWr</td><td>10 = 3DW, w/ data<br>11 = 4DW, w/ data</td><td>0 0000</td></tr><tr><td>IORd</td><td>00</td><td>0 0010</td></tr><tr><td>IOWr</td><td>10</td><td>0 0010</td></tr><tr><td>CfgRd0</td><td>00</td><td>0 0100</td></tr><tr><td>CfgWr0</td><td>10</td><td>0 0100</td></tr><tr><td>CfgRd1</td><td>00</td><td>0 0101</td></tr><tr><td>CfgWr1</td><td>10</td><td>0 0101</td></tr><tr><td>Msg</td><td>01</td><td>1 0RRR (RRR = Msg TLP routing subfield)</td></tr><tr><td>MsgD</td><td>11</td><td>1 0RRR (RRR = Msg TLP routing subfield)</td></tr><tr><td>Cpl</td><td>00</td><td>0 1010</td></tr><tr><td>CplD</td><td>10</td><td>0 1010</td></tr><tr><td>CplLk</td><td>00</td><td>0 1011</td></tr><tr><td>CplDLk</td><td>10</td><td>0 1011</td></tr></tbody></table>

***

## Address Field

### 32 bit addressing

* Byte \[11:8]: 30 bits, 2 bits reserved.

### 64 bit addressing

* Byte \[11:8] = Upper 32 bits
* Byte \[15:12] = Lower 30 bits of bits, 2 bits reserved.
