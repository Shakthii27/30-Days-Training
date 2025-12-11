## Read/Write throughput:
- L1 Cache	~1000–2000 GB/s	= 1000× faster
- L2 Cache	~500–1000 GB/s	= 500× faster
- L3 Cache	~100–400 GB/s	= 100× faster
- RAM (DDR4)	20–25 GB/s	= 10× faster (double data transfer)  
- NVMe SSD	2–3 GB/s	baseline (Non-volatile memory express)
- SATA SSD	0.5 GB/s = 0.6x slower

## Computer Memory devices 

L1 - Fastest, smallest, immediate data  
L2 - Fast, medium, data needed soon  
L3 - Moderate ,largest ,reduce RAM usage  

RAM DDR - double data rate -> RAM can transfer data two times per clock cycle - Once on the rising edge of the clock signal, once on the falling edge  

ATA - advanced technology attachment 
used to connect storage devices to motherboard  
PATA - parallel ATA - wide ribbon cables - very slow 
SATA - serial ATA - thin small cable used to connect SSD HDD - faster than PATA  
SATA SSD uses SATA cable  
NVMe - faster than SATA SSD as it does not use SATA port, it uses PCIe bus which is faster   

## Memory Management in Python
In Python, memory is divided mainly into two parts: Stack Memory, Heap Memory
Stack memory is temporary and is only alive until the function or method call is running.  
Heap memory is like a storage area where all values and stack memory just keeps directions (references) to them.  

## Memory allocation  
Allocate memory for list in heap  
Allocate memory for ints in heap  
Put pointer in stack  
Manage memory through reference counting  
If object is unused -> garbage collector frees it  
Python may reuse freed memory internally and not always return to OS - Python keeps some memory blocks for future reuse, only when entire arenas become unused, memory returns to OS  

## Exploring TOP command  
Swaping - move some inactive RAM pages to the SSD to free real RAM for active apps.  
Swapout - from RAM to SSD, if RAM getting full or inactive pages  
Swapin - from SSD to RAM - when an app you previously swapped out becomes active again, S needs that memory immediately  
Processes: 782 total, 3 running, 779 sleeping, 3390 threads - 782 total processes out of which 3 processes are actively running
Load Avg: 1.93, 2.05, 2.02 avg CPU load in 1 min, 5 min and 15 mins, at any moment, about 2 tasks were waiting for the CPU  
Process - a program that is being executed 
Threads - used when mutiple tasks happen in same program 

