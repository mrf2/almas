# pic - Programmable Interrupt Controller (PIC)

## **Intel 8259A**
Intel 8259A Programmable Interrupt Controller (8259A/8259A-2)
 * 8086, 8088 Compatible
 * MCS-80, MCS-85 Compatible
 * Eight-Level Priority Controller
 * Expandable to 64 Levels
 * Programmable Interrupt Modes
 * Invidual Request Mask Capability
 * Single $+5V$ Supply (No Clocks)
 * Available in 28-Pin DIP and 28-Lead PLCC Package
 * Available in EXPRESS
   * Standard Temperature Range
   * Extended Temperature Range
## Pin Description
|Symbol|Pin No.|Type|Name and Function|
|:---|---|---|:--|
|$V_{CC}$|28|I|**Supply:** +5V Supply.|
|GND|14|I|**GROUND**|
|$\overline{CS}$|1|I|**CHIP SELECT:** A low on this pin enables $\overline{RD}$ and $\overline{WR}$ communication between the CPU and the 8259A. INTA functions are independent of CS.|
|$\overline{WR}$|2|I|**WRITE:** A low on this pin when CS is low enables the 8259A to accept command words fromt he CPU.|
|$\overline{RD}$|2|I|**READ:** A low on this pin when CS is low enables the 8259A to release status onto the data bus for the CPU.|
|$D_7 - D_0$|4-11|I/O|**BIDIRECTIONAL DATA BUS:** Control, status and interrupt-vector information is transferred via this bus.|
|$CAS_0 - CAS_2$|12, 13, 15|I/O|**CASCADE LINES:** The CAS lines form a private 8259A buto to control a multiple 8259A structure. These pins are outputs for a master 8259A and inputs for a slave 8259A|
|$\overline{SP}/\overline{EN}$|16|I/O|**SLAVE PROGRAM/ENABLE BUFFER:** This is a dual function pin. When in the Buffered Mode it can be used as an output to control buffer transceivers (EN). When not in the buffered mode it is used as an input to designate a master (SP = 1) or slave (SP = 0)|
|INT|17|0|**INTERRUPT:** This pin goes high whenever a valid interrupt request is asserted. It is used to interrupt the CPU, thus it is connected to the CPU's interrupt pin.|
|$IR_0 - IR_7$|18-25|I|**INTERRUPT REQUESTS:** Asynchronous inputs. An interrupt request is executed by raising an IR input (low to high), and holding it high until it is acknowledged (Edge Triggered Mode), or just by a high level on an IR input (Level Triggered Mode).|
|$\overline{INTA}$|26|I|**INTERRUPT ACKNOWLEDGE:** This pin is used to enable 8259A interrupt-vector data onto the data bus by a sequence of interrupt acknowledge pulses issued by the CPU.|
|$A_0$|27|I|**AO ADDRESS LINE:** This pin acts in conjuction with the $\overline{CS}, \overline{WR}, and \overline{RD}$ pins. It is used by the 8259A to decipher various Command Words the CPU writes and status the CPU wishes to read. It is typically connected to the CPU A0 address line (A1 for 8086, 8088).|
## Abbreviation
 * **ISR** - In Service Register
 * **IRR** - Interrupt Request Register
 * **IMR** - Interrupt Mask Register


 * [osdev.org](https://wiki.osdev.org/8259_PIC)

