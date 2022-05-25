# How core, thread, CPU mode works

## [Multi-core](https://en.wikipedia.org/wiki/Multi-core_processor), [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), core

![CPU_core_thread](https://www.logicbig.com/quick-info/images/multithreading.png)

### [Multi-core](https://en.wikipedia.org/wiki/Multi-core_processor)

>A [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor) is a computer processor on a single integrated circuit with two or more separate [CPUs](https://en.wikipedia.org/wiki/Central_processing_unit), called cores, each of which reads and executes program instructions. ([Multi-core processor, wikipedia](https://en.wikipedia.org/wiki/Multi-core_processor))

>More reference about multi-core processor : [Core Processor, ScienceDirect](https://www.sciencedirect.com/topics/computer-science/core-processor)

>More reference about multiple CPU : [Multiple CPU Vs. Multi-Core, chron](https://smallbusiness.chron.com/jpegs-hp-thin-client-42782.html)

### [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)

>A [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is an electronic circuit inside the computer that carries out [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) to perform arithmetic, logical, control and input/output operations. ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

>More reference about [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) : [Central processing unit, wikipedia](https://en.wikipedia.org/wiki/Central_processing_unit)

### Core

>A Core is an execution unit inside the CPU that receives and executes [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)). ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

### Difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core

>[CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is responsible for controlling the cores. ([Differences Between Core and CPU, baeldung](https://www.baeldung.com/cs/core-vs-cpu))

>More reference about difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core : [Difference between core and processor, stackoverflow](https://stackoverflow.com/questions/19225859/difference-between-core-and-processor)

## [Instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture), [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

Every processor or processor family has its own [instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture). ([Machine code, wikipedia](https://en.wikipedia.org/wiki/Machine_code))

There are many [instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures). ([List of instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures))

I will pick [x86](https://en.wikipedia.org/wiki/X86), precisely [x86-64](https://en.wikipedia.org/wiki/X86-64), for my explanation.

If your [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is AMD Ryzen Series or Intel Core i3, Core i5, Core i7, Core i9, it belongs [x86-64](https://en.wikipedia.org/wiki/X86-64).

### [x86](https://en.wikipedia.org/wiki/X86)

>[x86](https://en.wikipedia.org/wiki/X86) is a family of complex instruction set computer (CISC) [instruction set](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures) architectures initially developed by Intel based on the Intel 8086 microprocessor and its 8088 variant. ([x86, wikipedia](https://en.wikipedia.org/wiki/X86))

### [x86-64](https://en.wikipedia.org/wiki/X86-64)

>[x86-64](https://en.wikipedia.org/wiki/X86-64) is a 64-bit version of the [x86](https://en.wikipedia.org/wiki/X86) [instruction set](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures). ([x86-64, wikipedia](https://en.wikipedia.org/wiki/X86-64))

### [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

>An [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) is a single operation of a processor defined by the processor [instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture). ([Instruction (computer science), simple wikipedia](https://simple.wikipedia.org/wiki/Instruction_(computer_science)))

## [Thread](https://en.wikipedia.org/wiki/Thread_(computing)), [operating system](https://en.wikipedia.org/wiki/Operating_system), [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)), [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))

An [operating system](https://en.wikipedia.org/wiki/Operating_system) [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) contains a [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) program which determines how much time each process spends executing, and in which order execution control should be passed to programs.

There are many [operating systems](https://en.wikipedia.org/wiki/Operating_system). ([List of operating systems](https://en.wikipedia.org/wiki/List_of_operating_systems))

I will pick [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) for my explanation.

### [Thread](https://en.wikipedia.org/wiki/Thread_(computing))

>A [thread](https://en.wikipedia.org/wiki/Thread_(computing)) is the sequence of [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) given to cores. ([CPU Cores VS Threads Explained, youtube](https://youtu.be/hwTYDQ0zZOw))

>[Thread](https://en.wikipedia.org/wiki/Thread_(computing)) in [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) is the basic unit to which an operating system allocates processor time. ([Threads and threading, microsoft docs](https://docs.microsoft.com/en-us/dotnet/standard/threading/threads-and-threading))

>More reference about [thread](https://en.wikipedia.org/wiki/Thread_(computing)) : [Thread (computing), wikipedia](https://en.wikipedia.org/wiki/Thread_(computing))

### [Operating system](https://en.wikipedia.org/wiki/Operating_system)

>An [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is system software that manages computer hardware, software resources, and provides common services for computer programs. ([Operating system, wikipedia](https://en.wikipedia.org/wiki/Operating_system))

### [Kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system))

>The [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) is a computer program at the core of a computer's [operating system](https://en.wikipedia.org/wiki/Operating_system) and generally has complete control over everything in the system. ([Kernel (operating system), wikipedia](https://en.wikipedia.org/wiki/Kernel_(operating_system)))

### [Scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))

>[Scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) is the action of assigning resources to perform tasks. The resources may be [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), network links or expansion cards. The tasks may be [threads](), processes or data flows. ([Scheduling (computing), wikipedia](https://en.wikipedia.org/wiki/Scheduling_(computing)))

## [Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking), [task](https://en.wikipedia.org/wiki/Task_(computing)), [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice)

The concept of [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) makes it possible to have computer [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) with a single [central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit).

Most modern [operating systems](https://en.wikipedia.org/wiki/Operating_system) have [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [kernels](https://en.wikipedia.org/wiki/Kernel_(operating_system)), which are designed to permit [tasks](https://en.wikipedia.org/wiki/Task_(computing)) to be preempted even when in kernel mode. ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)))

[Preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) allocates a processor [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) to each [thread](https://en.wikipedia.org/wiki/Thread_(computing)) it executes. ([Multitasking, ](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking))

If your [operating systems](https://en.wikipedia.org/wiki/Operating_system) is [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows), it belongs [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking).

### [Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking)

>[Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) is the [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) execution of multiple [tasks](https://en.wikipedia.org/wiki/Task_(computing)) (also known as processes) over a certain period of time. ([Computer multitasking, wikipedia](https://en.wikipedia.org/wiki/Computer_multitasking))

>[Multitasking](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking) in [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) allocates a processor [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) to each [thread](https://en.wikipedia.org/wiki/Thread_(computing)) it executes. ([Multitasking, microsoft docs](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking))

### [Task](https://en.wikipedia.org/wiki/Task_(computing))

>A [task](https://en.wikipedia.org/wiki/Task_(computing)) is a unit of execution or a unit of work. The term is ambiguous; precise alternative terms include process, light-weight process, [thread (for execution)](https://en.wikipedia.org/wiki/Thread_(computing)), step, request, or query (for work). ([Task (computing), wikipedia](https://en.wikipedia.org/wiki/Task_(computing)))

### [Time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice)

>The period of time for which a process is allowed to run in a [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) system is generally called the [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) or quantum. ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice))

## [Context switch](https://en.wikipedia.org/wiki/Context_switch), [protection rings](https://en.wikipedia.org/wiki/Protection_ring), [CPU modes](https://en.wikipedia.org/wiki/CPU_modes)

A change in the currently executing task of a [processor](https://en.wikipedia.org/wiki/Processor_(computing)) is known as [context switching](https://en.wikipedia.org/wiki/Context_switch). ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)))

[Protection rings](https://en.wikipedia.org/wiki/Protection_ring) are generally hardware-enforced by some [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) architectures that provide different [CPU modes](https://en.wikipedia.org/wiki/CPU_modes) at the hardware or microcode level. ([Protection ring, wikipedia](https://en.wikipedia.org/wiki/Protection_ring))

### [Context switch](https://en.wikipedia.org/wiki/Context_switch)

>A [context switch](https://en.wikipedia.org/wiki/Context_switch) is the process of storing the state of a process or [thread](https://en.wikipedia.org/wiki/Thread_(computing)), so that it can be restored and resume execution at a later point. ([Context switch, wikipedia](https://en.wikipedia.org/wiki/Context_switch))

### [Protection rings](https://en.wikipedia.org/wiki/Protection_ring)

>[Protection rings](https://en.wikipedia.org/wiki/Protection_ring) are mechanisms to protect data and functionality from faults (by improving fault tolerance) and malicious behavior (by providing computer security). ([Protection ring, wikipedia](https://en.wikipedia.org/wiki/Protection_ring))

### [CPU modes](https://en.wikipedia.org/wiki/CPU_modes)

>[CPU modes](https://en.wikipedia.org/wiki/CPU_modes) (also called processor modes, CPU states, CPU privilege levels and other names) are operating modes for the [central processing unit](https://en.wikipedia.org/wiki/Central_processing_unit) of some computer architectures that place restrictions on the type and scope of operations that can be performed by certain processes being run by the CPU. ([CPU modes, wikipedia](https://en.wikipedia.org/wiki/CPU_modes))

When a processor becomes available, the system performs a context switch.
