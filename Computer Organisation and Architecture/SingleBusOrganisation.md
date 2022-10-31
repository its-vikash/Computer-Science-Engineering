<h2>Bus structure</hw>
<h3>Single bus structure</h3>: In computer architecture, a bus is a subsystem that transfers data between components inside a computer, or between computers. Early computer buses were literally parallel electrical wires with multiple connections, but Modern computer buses can use both parallel and bit serial connections.

![Alt text](https://media.geeksforgeeks.org/wp-content/uploads/20200427071253/singlebus.png)
<h4> Single bus structure</h4>
To achieve a reasonable speed of operation, a computer must be organized so that all its units can handle one full word of data at a given time. When a word of data is transferred between units, all its bits are transferred in parallel, that is, the bits are transferred simultaneously over many wires, or lines, one bit per line. A group of lines that serves as a connecting path for several devices is called a bus. In addition to the lines that carry the data, the bus must have lines for address and control purposes. The simplest way to interconnect functional units is to use a single bus, as shown in Figure 1.3.1. All units are connected to this bus. Because the bus can be used for only one transfer at a time, only two units can actively use the bus at any given time. Bus control lines are used to arbitrate multiple requests for use of the bus. The main virtue of the single-bus structure is its low cost and is flexibility for attaching peripheral" devices. Systems that contain multiple buses achieve more concurrency in operations by allowing two or more transfers to be carried out at the same time. This leads to better performance but at an increased cost.

Parts of a System bus: Processor, memory, Input and output devices are connected by system bus, which consists of separate busses as shown in figure 1.3.2. They are:
<h4> (i)Address bus: </h4> Address bus is used to carry the address. It is unidirectional bus. The address is sent to from CPU to memory and I/O port and hence unidirectional. It consists of 16, 20, 24 or more parallel signal lines.
<h4> (ii)Data bus: </h4> Data bus is used to carry or transfer data to and from memory and I/O ports. They are bidirectional. The processor can read on data lines from memory and I/O port and as well as it can write data to memory. It consists of 8, 16, 32 or more parallel signal lines.
<h4> (iii)Control bus: </h4> Control bus is used to carry control signals in order to regulate the control activities. They are bidirectional. The CPU sends control signals on the control bus to enable the outputs of addressed memory devices or port devices. Some of the control signals are: MEMR (memory read), MEMW (memory write), IOR (I/O read), IOW (I/O write), BR (bus request), BG (bus grant), INTR (interrupt request), INTA (interrupt acknowledge), RST (reset), RDY (ready), HLD (hold), HLDA (hold acknowledge),

<h3> Bus interconnection scheme </h4>
The devices connected to a bus vary widely in their speed of operation. Some electromechanical devices, such as keyboards and printers are relatively slow. Other devises like magnetic or optical disks, are considerably faster. Memory and processor units operate at electronic speeds, making them the fastest parts of a computer. Because all these devices must communicate with each other over a bus, an efficient transfer mechanism that is not constrained by the slow devices and that can be used to smooth out the differences in timing among processors, memories, and external devices is necessary.

A common approach is to include buffer registers with the devices to hold the information during transfers. To illustrate this technique, consider the transfer of an encoded character from a processor to a character printer. The processor sends the character over the bus to the printer buffer. Since the buffer is an electronic register, this transfer requires relatively little time. Once the buffer is loaded, the printer can start printing without further intervention by the processor. The bus and the processor are no longer needed and can be released for other activity. The printer continues printing the character in its buffer and is not available for further transfers until this process is completed. Thus, buffer registers smooth out timing differences among processors, memories, and I/O devices. They prevent a high-speed processor from being locked to a slow I/O device during a sequence of data transfers. This allows the processor to switch rapidly from one device to another, interweaving its processing activity with data transfers involving several I/O devices.