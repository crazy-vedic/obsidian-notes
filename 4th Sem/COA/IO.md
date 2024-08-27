Drivers are used to allow software to interact with hardware, no accessing allowed directly.
Interface is needed because:
	Peripherals are electronic devices, conversion of signal required
	Data transfer rate is slow, so syncronization is required

IO vs memory bus
	cpu is always connected to IO and memory through address, data and control bus

Types:
	1. Programmed IO, IO can't ping the cpu, cpu needs to periodically check the status of each device, similar to petersons solution, there is a array of flags of devices that want cpu, wait on their turn
	2. Interrupt Driven IO, IO can interrupt the cpu. On receiving the interrupt, finish current instruction, then branch
	3. Direct Memory Access: Enable data transfer between IO and memory without intervention. Possible modes: Burst mode, cycle stealing, interleaving DMA

Suppose we want to read 2048 bytes in prog IO mode. bus width 32 bits, every interrupt, it takes 4 micro second to service (transfer 32 bit), how much cpu time is needed 

a dma module is transferring bytes at 76800 bps. cpu can fetch instructions at 2million ps, assume instruction size is 32 bits, how much will processor be slowed down due to dma 
76800/64000000 0.12% ans

32 bit words, cycle stealing, words assembled from a device that transmits bytes at 2400 bytes /s. cpu 1 million instruction/s
0.06%

8KB/s interrupt takes 100 micro s, interrupts the cpu for every byte. while executing ISR, processor takes 8 micro second for transfer of each byte, how much cpu is consumed by io device
108 * 8 KBps

hard disk is connected to 50 MHz using DMA, initial set up time for DMA takes 2000 clocks, assume handling of interrupt requiries 1000 clocks, transfer rate of 4000 KBps, block size transferred is 8kb, how much is consumed, as long as data is transferred during cpu idle cycles
`frequency = 50*10^6`
cycle time = 20 nano s
`dma setup time = 2000*20  = 40 micro s`
dma completion = 1000 * 20 = 20 micro s
transfer rate = 4000KB/s, 1 KB transferred in 1/4000 s
so 8kb transferred in 8/4000 s, 2 milli second
total transfer time for 8kb = (dma setup+ dma completion + transfer rate) = 40micro+20micro+2milli = 2.06 milli seconds

transfer rate = 20KBps, interrupt overhead = 6 micro second
interupt processing takes 6 microsecond for each byte, 
total overhead = 20 KB * 6 micros = 120 US
120 MS = 0.12 second
performance gain = 1-0.12 = 0.88
