# Bus Enum

## Enum Bus 0

1. Probe BDF\_0\_0\_0

| CfgRd0 \* n | **BDF\_0\_0\_0** | -- |
| ----------- | ---------------- | -- |

2. Primary bus = 00\
   Secondary bus = 01\
   Subordinate bus = FF(255)

| CfgWr0 | **BDF\_0\_0\_0** | **\[ ee \| ff \| 01 \| 00 ]** |
| ------ | ---------------- | ----------------------------- |

3. Discovered\
   **BDF\_0\_0\_0**\
   <mark style="color:red;">**Root Port**</mark>\
   **Single-f**

***

## Enum Bus 1

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>Msg data (set slot power limit)</td><td>Implicit</td><td><strong>[ 00 | 00 | 00 | 00 ]</strong></td></tr></tbody></table>

1. Probe BDF\_1\_0\_0

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd0 * n</td><td><strong>BDF_1_0_0</strong></td><td>--</td></tr></tbody></table>

2. Primary bus = 01\
   Secondary bus = 02\
   Subordinate bus = FF(255)

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr0</td><td><strong>BDF_1_0_0</strong></td><td><strong>[ ee | ff | 02 | 01 ]</strong></td></tr></tbody></table>

3. Discovered\
   **BDF\_1\_0\_0**\
   <mark style="color:red;">**SWUP Port**</mark>\
   **Single-f**

***

## Enum Bus 2

1. Probe BDF\_2\_0\_0

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd1 * n</td><td><strong>BDF_2_0_0</strong></td><td>--</td></tr></tbody></table>

2. Primary bus = 02\
   Secondary bus = 03\
   Subordinate bus = FF(255)

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr1</td><td><strong>BDF_2_0_0</strong></td><td><strong>[ ee | ff | 03 | 02 ]</strong></td></tr></tbody></table>

3. Discovered\
   **BDF\_2\_0\_0**\
   <mark style="color:red;">**SWDN Port**</mark>\
   **Single-f**

***

## Enum Bus 3

1. Probe BDF\_3\_0\_0

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd1 * n</td><td><strong>BDF_3_0_0</strong></td><td>--</td></tr></tbody></table>

2. Discovered\
   **BDF\_3\_0\_0**\
   **EP**\
   **Multi-f**
3. Probe BDF\_3\_0\_1

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd1 * n</td><td><strong>BDF_3_0_1</strong></td><td>--</td></tr></tbody></table>

4. Discovered\
   **BDF\_3\_0\_1**\
   **EP**\
   **Multi-f**
5. Probe BDF\_3\_0\_2\
   BDF\_3\_0\_2 does not exist.

***

## Update BDF\_2\_0\_0 Headers

1. Primary bus = 02\
   Secondary bus = 03\
   Subordinate bus = 03

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr1</td><td><strong>BDF_2_0_0</strong></td><td><strong>[ ee | 03 | 03 | 02 ]</strong></td></tr></tbody></table>

2. Probe BDF\_2\_1\_0

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd1 * n</td><td><strong>BDF_2_1_0</strong></td><td>--</td></tr></tbody></table>

3. Primary bus = 02\
   Secondary bus = 04\
   Subordinate bus = FF(255)

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr1</td><td><strong>BDF_2_1_0</strong></td><td><strong>[ ee | ff | 04 | 02 ]</strong></td></tr></tbody></table>

4. Discovered\
   **BDF\_2\_1\_0**\
   **SWDN\_PORT**\
   **Single-f**

***

## Enum Bus 4

1. Probe BDF\_4\_0\_0

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgRd1 * n</td><td><strong>BDF_4_0_0</strong></td><td>--</td></tr></tbody></table>

2. Discovered\
   **BDF\_4\_0\_0**\
   **EP**\
   **Single-f**

***

## Update BDF\_2\_1\_0 Headers

1. Primary bus = 02\
   Secondary bus = 04\
   Subordinate bus = 04

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr1</td><td><strong>BDF_2_1_0</strong></td><td><strong>[ ee | 04 | 04 | 02 ]</strong></td></tr></tbody></table>

2. Probe BDF\_2\_2\_0\
   BDF\_2\_2\_0 does not exist.

***

## Update BDF\_1\_0\_0 Headers

1. Primary bus = 01\
   Secondary bus = 02\
   Subordinate bus = 04

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr0</td><td><strong>BDF_1_0_0</strong></td><td><strong>[ ee | 04 | 02 | 01 ]</strong></td></tr></tbody></table>

***

## Update BDF\_0\_0\_0 Headers

1. Primary bus = 00\
   Secondary bus = 01\
   Subordinate bus = 04

<table data-header-hidden><thead><tr><th width="305.6666666666667">TLP</th><th width="142">Target ID</th><th>Data payload</th></tr></thead><tbody><tr><td>CfgWr0</td><td><strong>BDF_1_0_0</strong></td><td><strong>[ ee | 04 | 01 | 00 ]</strong></td></tr></tbody></table>

***

## Enum BDF\_0\_1\_0

**Vendor ID** is read as **FFFh,** implying **BDF\_0\_1\_0 is not implemented**.

***

## RC Bus 0 DFS is finished.
