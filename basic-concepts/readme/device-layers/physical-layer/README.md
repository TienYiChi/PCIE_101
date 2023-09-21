# Physical Layer

## Logical Physical Layer

* Digital logic

## Electrical Physical Layer

* **Differential driver/receiver,** an analog interface that connects to the Link.

***

## Encoding Logic

To achieve **DC balance** which prevents **signal loss**<mark style="color:red;">**(?):**</mark>

* Gen 1/2: 8b/10b
* Gen 3/4/5: 128b/130b

***

## Other Functions

### Link training and initialization

Determines the following:

* **Link width**
  * x1, x2, x4, x8, x16 (power of 2)
* **Link data rate**
  * Initializes with **the highest common frequency** between the opposite ends of the Link.
* **Lane reversal**
  * In multi-Lane Link, Lane numbers can be reversed in case of difficult wire routing.
* **Polarity inversion**
  * In a single Lane, designated positive and negative (D+/D-) can be inverted.
* **Bit lock per Lane**
* **Symbol lock per Lane**
* **Lane-to-Lane de skew**
  * Due to wire length variations or driver/receiver characteristics on a **multi-Lane Link.**

### Link power management

* L0: Power-on state
* L0s: Entered when a time-out occurred after inactivity.
* L1, L2:
* L3: Off power state, the device **CANNOT** generate a wake up event.

### Reset

* Cold/warm reset (Fundamental reset)
* Hot reset (protocol reset)

{% hint style="info" %}
On exit from reset, all state machines and config registers are initialized.
{% endhint %}
