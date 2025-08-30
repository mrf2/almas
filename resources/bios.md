# BIOS - Basic Input Output System
 * 512 bytes in size, where last two byte is the boot signature (also called *magic number*) **`0xaa55`**.
 * BIOS loops through each storage devices (*e.g. floppy drive, hard disk, CD drive, etc.*), reads the boot sector into memory, and instructs the CPU to begin executing the first boot sector it finds that ends with the **magic number**.


## CPU Operation
 * CPU does not differentiate between code and data: bot can be interpreted as CPU instructions where code is simply instructions that have been crafted by a programmer into some useful algorithm.
