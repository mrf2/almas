# UEFI - Unified Extensible Firmware Inferface

 * **Boot Services**
   * Disk access
   * Memory allocation
   * Protocol handling
 * **Runtime Services**
   * variables
   * real-time clock
   * Reset
   * Shutdown, etc.

## **Operating Systems Expectations:**
   * Interrupt latency
   * Memory configuration
   * Peripheral usage
## Differences vs BIOS/DOS:
 * No `INT 13h`, `INT 10h` style interrupts. Everything is **function calls via memory pointers**.
 * 32/64-bit clean interface (not limited to **1MB** or real mode).
 * Extensible with drivers (**protocols**).

