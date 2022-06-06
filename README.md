# How core, [thread](https://en.wikipedia.org/wiki/Thread_(computing)), [CPU mode](https://en.wikipedia.org/wiki/CPU_modes) works

#### I will explain in **[bottom up](https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design) order**, because [top down](https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design) order was more difficult to avoid mentioning other topics. I felt mentioning more topics is eventually making more difficult to understand.

#### Understanding of [operating system](https://en.wikipedia.org/wiki/Operating_system) is inevitable. So I will begin with a brief explanation of [operating system](https://en.wikipedia.org/wiki/Operating_system).

## What is [operating system](https://en.wikipedia.org/wiki/Operating_system)?

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Operating_system_placement.svg/165px-Operating_system_placement.svg.png">
</p>

>An [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is system **[software](https://en.wikipedia.org/wiki/Software) that manages computer [hardware](https://en.wikipedia.org/wiki/Computer_hardware), software resources, and provides common services for computer programs**.
><div align="right">https://en.wikipedia.org/wiki/Operating_system</div>

>An [operating system](https://en.wikipedia.org/wiki/Operating_system) is **[software](https://en.wikipedia.org/wiki/Software) that manages a computer’s [hardware](https://en.wikipedia.org/wiki/Computer_hardware)**.
><div align="right">3p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

>A more common definition, and the one that we usually follow, is that the [operating system](https://en.wikipedia.org/wiki/Operating_system) is **the one program running at all times on the computer**—usually called the [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)).
><div align="right">6p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

>An [operating system](https://en.wikipedia.org/wiki/Operating_system) is a **resource manager**. The system’s CPU, memory space, file-storage space, and I/O devices are among the resources that the operating system must manage.
><div align="right">27p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

### Summary

**- An [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is a [software](https://en.wikipedia.org/wiki/Software) that manages computer [hardware](https://en.wikipedia.org/wiki/Computer_hardware), software resources, and provides common services for computer programs.**

## What are the types of [operating system](https://en.wikipedia.org/wiki/Operating_system)?

>- Single-tasking and [multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking)
>- Single-user and multi-user
>- Distributed
>- Templated
>- Embedded
>- Real-time
>- Library
><div align="right">https://en.wikipedia.org/wiki/Operating_system#Types_of_operating_systems</div>

>- Batch
>- [Multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking)
>- Distributed
>- Network
>- Real-Time
><div align="right">https://www.geeksforgeeks.org/types-of-operating-systems/</div>

>- Batch
>- [Multi-Tasking](https://en.wikipedia.org/wiki/Computer_multitasking)
>- Real time
>- Distributed
>- Network
>- Mobile
><div align="right">https://www.guru99.com/operating-system-tutorial.html#types-of-operating-system</div>

### Summary

- Single-tasking and [multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking)
- Single-user and multi-user
- Distributed
- Templated
- Embedded
- Real time
- Batch
- Network
- Mobile

#### I will handle [multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) [operating system](https://en.wikipedia.org/wiki/Operating_system) in this article.

## What is [multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) in [operating system](https://en.wikipedia.org/wiki/Operating_system)?

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20200426073127/Multitasking1-300x300.png">
</p>

>[Multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) is the **[concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) execution of multiple tasks** (also known as processes) over a certain period of time.
><div align="right">https://en.wikipedia.org/wiki/Computer_multitasking</div>

>[Multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) is an extension of multiprogramming wherein [CPU scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)#Short-term_scheduling) algorithms rapidly switch between [processes](https://en.wikipedia.org/wiki/Process_(computing)), providing users with a fast response time.
><div align="right">52p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

#### [Multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) leads to having multiple [processes](https://en.wikipedia.org/wiki/Process_(computing)) in memory at the same time. If several processes are ready to run at the same time, the system must choose which process will run next. Making this decision is [CPU scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)#Short-term_scheduling).
<div align="right">24p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

### Summary

**- [Multi-tasking](https://en.wikipedia.org/wiki/Computer_multitasking) is the [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) execution of multiple tasks (also known as processes) over a certain period of time.**

#### For more detail about concurrency, read Parallel Computing.

## What are the functions of [operating system](https://en.wikipedia.org/wiki/Operating_system)?

>- Security
>- Control over system performance
>- Job accounting
>- Error detecting aids
>- Coordination between other software and users
>- Memory Management
>- [Processor Management](https://en.wikipedia.org/wiki/Process_management_(computing))
>- Device Management
>- File Management
><div align="right">https://www.geeksforgeeks.org/functions-of-operating-system/</div>

>- [Process management](https://en.wikipedia.org/wiki/Process_management_(computing))
>- Memory management
>- File management
>- Device Management
>- I/O System Management
>- Secondary-Storage Management
>- Security
>- Command interpretation
>- Networking
>- Job accounting
>- Communication management
><div align="right">https://www.guru99.com/operating-system-tutorial.html#functions-of-operating-system/</div>

>- [Process Management](https://en.wikipedia.org/wiki/Process_management_(computing))
>- Memory Management
>- File-System Management
>- Mass-Storage Management
>- Cache Management
>- I/O System Management
>- Security and Protection
>- Virtualization
><div align="right">27p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

### Summary

- [Process Management](https://en.wikipedia.org/wiki/Process_management_(computing))
- Memory Management
- File-System Management
- Mass-Storage Management
- Cache Management
- I/O System Management
- Security and Protection
- Virtualization

## Why does the definition, types, and functions of [operating system](https://en.wikipedia.org/wiki/Operating_system) vary?

>In general,we have **no completely adequate definition of an operating system**.
><div align="right">5p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

>In addition, we have **no universally accepted definition of what is part of the operating system**.
><div align="right">6p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

## CPU scheduling

CPU - The hardware that executes instructions.
Processor - Aphysical chip that contains one or more CPUs.
Core - The basic computation unit of the CPU.
Multicore - Including multiple computing cores on the same CPU.
Multiprocessor - Including multiple processors.
<div align="right">18p, Operating System Concepts 10th edition, Abraham Silberschatz</div>

## What are [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware), [integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit), [processor](https://en.wikipedia.org/wiki/Processor_(computing)), [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor), core?

### [Computer hardware](https://en.wikipedia.org/wiki/Computer_hardware)

![Computer hardware](https://scontent-gmp1-1.xx.fbcdn.net/v/t1.6435-9/176067216_1813918015455920_2474979289003788370_n.jpg?stp=cp0_dst-jpg_e15_q65_s320x320&_nc_cat=105&ccb=1-7&_nc_sid=110474&_nc_ohc=H8i6zv687LUAX9p3zZu&_nc_ht=scontent-gmp1-1.xx&oh=00_AT8-8th1QddD70eFq1w9WqrgTgDP9ZnV0LlovbidhYv_bA&oe=62B83238)

>[Computer hardware](https://en.wikipedia.org/wiki/Computer_hardware) includes the physical parts of a computer, such as the case, **[central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit)**, random access memory (RAM), monitor, mouse, keyboard, computer data storage, graphics card, sound card, speakers and motherboard.
><div align="right">https://en.wikipedia.org/wiki/Computer_hardware</div>

>[Hardware](https://en.wikipedia.org/wiki/Computer_hardware) is typically directed by the software to execute any command or [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)).
><div align="right">https://en.wikipedia.org/wiki/Computer_hardware</div>

### [Integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit)

>An [integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit) or monolithic [integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit) (also referred to as an IC, a chip, or a microchip) is a set of electronic circuits on one small flat piece (or "chip") of semiconductor material, usually silicon.
><div align="right">https://en.wikipedia.org/wiki/Integrated_circuit</div>

### [Processor](https://en.wikipedia.org/wiki/Processor_(computing))

>A [processor](https://en.wikipedia.org/wiki/Processor_(computing)) or processing unit is an electrical component (digital circuit) that performs operations on an external data source, usually memory or some other data stream.
><div align="right">https://en.wikipedia.org/wiki/Processor_(computing)</div>

>The term is frequently used to refer to the [central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit) in a system. However, it can also refer to other coprocessors, such as a graphics processing unit (GPU).
><div align="right">https://en.wikipedia.org/wiki/Processor_(computing)</div>

### [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)

|![Intel](https://assets.hardwarezone.com/img/2021/11/Corei9_02.jpg)|![AMD](https://cdn.mos.cms.futurecdn.net/mnzNfoMcmVXme8vxENcyjm-970-80.jpg)|
|---|---|
|<div align="center">Intel i9 12900K</div>|<div align="center">AMD Ryzen 9 5950X</div>|

>A [central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit), also called a central [processor](https://en.wikipedia.org/wiki/Processor_(computing)), main [processor](https://en.wikipedia.org/wiki/Processor_(computing)) or just [processor](https://en.wikipedia.org/wiki/Processor_(computing)), is the electronic circuitry that **executes [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))** comprising a computer program. The [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) performs basic **arithmetic, logic, controlling, and input/output (I/O) operations specified by the [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))** in the program.
><div align="right">https://en.wikipedia.org/wiki/Central_processing_unit</div>

### [Multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor)

>A [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor) is a computer **[processor](https://en.wikipedia.org/wiki/Processor_(computing))** on a single [integrated circuit](https://en.wikipedia.org/wiki/Integrated_circuit) with two or more separate processing units, called **cores**, each of which **reads and executes program [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))**. The **[instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) are ordinary [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))** (such as add, move data, and branch) but the single [processor](https://en.wikipedia.org/wiki/Processor_(computing)) can run [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) on separate cores at the same time, increasing overall speed for programs that support multithreading or other parallel computing techniques.
><div align="right">https://en.wikipedia.org/wiki/Multi-core_processor</div>

>A [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor) is **a single [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)** that contains more than one microprocessor core.
><div align="right">https://en.wikipedia.org/wiki/Microprocessor</div>

### Core

>A core is **an execution unit inside the [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) that receives and executes [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))**.
><div align="right">https://pediaa.com/difference-between-cpu-and-core</div>

### Difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core

|<div align="center">![CPU diagram](https://media.geeksforgeeks.org/wp-content/uploads/20210605182444/CPUblock-660x495.jpg)</div>|<div align="center">![Multi-core CPU diagram](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/CPU.png)</div>|
|---|---|
|<div align="center">CPU diagram</div>|<div align="center">Multi-core CPU diagram</div>|
|<div align="center">![Core diagram 1](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/Core-2.png)</div>|<div align="center">![Core diagram 2](https://ars.els-cdn.com/content/image/3-s2.0-B9780128014134000118-f11-15-9780128014134.jpg)</div>|
|<div align="center">Core diagram 1</div>|<div align="center">Core diagram 2</div>|

#### [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core are different. (Compare multi-core CPU diagram and Core diagram 1)

![Differences Between Core and CPU](https://www.baeldung.com/wp-content/ql-cache/quicklatex.com-c7135cdceb9b5a510d176ca7da28eb6a_l3.svg)

>**While cores actually process [tasks](https://en.wikipedia.org/wiki/Task_(computing)), a [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is responsible for controlling the cores**.
><div align="right">https://www.baeldung.com/cs/core-vs-cpu</div>

#### Core is [CPU](https://en.wikipedia.org/wiki/Central_processing_unit). (Compare CPU diagram, Core diagram 1, and Core diagram 2)

>**A core is a small [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) or [processor](https://en.wikipedia.org/wiki/Processor_(computing)) built into a big [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) or [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) socket.**
><div align="right">https://www.sciencedirect.com/topics/computer-science/core-processor</div>

>More reference about difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core : [Difference between core and processor, stackoverflow](https://stackoverflow.com/questions/19225859/difference-between-core-and-processor)

#### In conclusion, [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core are different from perspective of [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) meaning [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor). [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core are same from perspective of definition and components of [CPU](https://en.wikipedia.org/wiki/Central_processing_unit).

### Summary

#### - [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is a type of [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware).

#### - [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is a type of [processor](https://en.wikipedia.org/wiki/Processor_(computing)).

#### - [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) executes arithmetic, logic, controlling, and input/output (I/O) [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)).

#### - [Multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor) is a big [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) that contains more than one core, which is a small [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) executing [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)).

## What are [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)), [instruction set](https://simple.wikipedia.org/wiki/Instruction_set), [x86](https://en.wikipedia.org/wiki/X86), [x86-64](https://en.wikipedia.org/wiki/X86-64), [thread](https://en.wikipedia.org/wiki/Thread_(computing))?

### [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

>An [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) is a single operation of a [processor](https://en.wikipedia.org/wiki/Processor_(computing)) defined by the [processor](https://en.wikipedia.org/wiki/Processor_(computing)) [instruction set](https://simple.wikipedia.org/wiki/Instruction_set).
><div align="right">https://simple.wikipedia.org/wiki/Instruction_(computer_science)</div>

### [Instruction set](https://simple.wikipedia.org/wiki/Instruction_set)

>An [instruction set](https://simple.wikipedia.org/wiki/Instruction_set) is a list of all the [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) that a [processor](https://en.wikipedia.org/wiki/Processor_(computing)) can execute.
><div align="right">https://simple.wikipedia.org/wiki/Instruction_set</div>

#### Every [processor](https://en.wikipedia.org/wiki/Processor_(computing)) or [processor](https://en.wikipedia.org/wiki/Processor_(computing)) family has its own [instruction set](https://simple.wikipedia.org/wiki/Instruction_set).
<div align="right">https://en.wikipedia.org/wiki/Machine_code</div>

#### There are many [instruction sets](https://simple.wikipedia.org/wiki/Instruction_set). ([List of instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures))

#### [x86](https://en.wikipedia.org/wiki/X86) and [x86-64](https://en.wikipedia.org/wiki/X86-64) are examples of [instruction sets](https://simple.wikipedia.org/wiki/Instruction_set).

### [x86](https://en.wikipedia.org/wiki/X86)

>[x86](https://en.wikipedia.org/wiki/X86) is a family of [complex instruction set computer (CISC)](https://en.wikipedia.org/wiki/Complex_instruction_set_computer) [instruction set](https://simple.wikipedia.org/wiki/Instruction_set) architectures initially developed by Intel based on the Intel 8086 microprocessor and its 8088 variant.
><div align="right">https://en.wikipedia.org/wiki/X86</div>

### [x86-64](https://en.wikipedia.org/wiki/X86-64)

>[x86-64](https://en.wikipedia.org/wiki/X86-64) is a 64-bit version of the [x86](https://en.wikipedia.org/wiki/X86) [instruction set](https://simple.wikipedia.org/wiki/Instruction_set).
><div align="right">https://en.wikipedia.org/wiki/X86-64</div>

#### If your [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is AMD Ryzen Series or Intel Core i3, Core i5, Core i7, Core i9, it belongs to [x86-64](https://en.wikipedia.org/wiki/X86-64).

### [Thread](https://en.wikipedia.org/wiki/Thread_(computing))

![Thread](https://upload.wikimedia.org/wikipedia/commons/a/a5/Multithreaded_process.svg)

>A [thread](https://en.wikipedia.org/wiki/Thread_(computing)) of execution is **the smallest sequence of programmed [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))** that can be managed independently by a **scheduler**, which is typically a part of the **[operating system](https://en.wikipedia.org/wiki/Operating_system)**.

### Summary

#### [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) is a single operation of a [processor](https://en.wikipedia.org/wiki/Processor_(computing)).

#### [Instruction set](https://simple.wikipedia.org/wiki/Instruction_set) is a list of all the [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)).

#### [x86](https://en.wikipedia.org/wiki/X86) and [x86-64](https://en.wikipedia.org/wiki/X86-64) are examples of [instruction set](https://simple.wikipedia.org/wiki/Instruction_set).

#### [Thread](https://en.wikipedia.org/wiki/Thread_(computing)) is the smallest sequence of programmed [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) that can be managed independently by a **scheduler**, which is typically a part of the **[operating system](https://en.wikipedia.org/wiki/Operating_system)**.

## What are scheduler, [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)), [operating system](https://en.wikipedia.org/wiki/Operating_system)?

### [Operating system](https://en.wikipedia.org/wiki/Operating_system)

![operating_system](https://www.tutorialspoint.com/operating_system/images/conceptual_view.jpg)

>An [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is system software that manages [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware), software resources, and provides common services for computer programs. ([Operating system, wikipedia](https://en.wikipedia.org/wiki/Operating_system))

>An [operating system](https://en.wikipedia.org/wiki/Operating_system) [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) contains a [scheduling](https://en.wikipedia.org/wiki/Kernel_(operating_system)) program which determines how much time each [process]() spends executing, and in which order execution control should be passed to programs.

### [Kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system))

![kernel](https://miro.medium.com/max/1400/1*iuW845pwRhd49KEUYvzsmg.png)

>The [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) is a computer program at the core of a computer's [operating system](https://en.wikipedia.org/wiki/Operating_system) and generally has complete control over everything in the system. ([Kernel (operating system), wikipedia](https://en.wikipedia.org/wiki/Kernel_(operating_system)))

### [Scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))

>[Scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) is the action of assigning resources to perform [tasks](https://en.wikipedia.org/wiki/Task_(computing)). The resources may be [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), network links or expansion cards. The [tasks](https://en.wikipedia.org/wiki/Task_(computing)) may be [threads](https://en.wikipedia.org/wiki/Thread_(computing)), [processes](https://en.wikipedia.org/wiki/Process_(computing)) or data flows. ([Scheduling (computing), wikipedia](https://en.wikipedia.org/wiki/Scheduling_(computing)))

#### An [operating system](https://en.wikipedia.org/wiki/Operating_system) [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) contains a [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) program which determines how much time each [process](https://en.wikipedia.org/wiki/Process_(computing)) spends executing, and in which order execution control should be passed to programs. ([Operating system, wikipedia](https://en.wikipedia.org/wiki/Operating_system#Multitasking))

#### There are many types of [operating systems](https://en.wikipedia.org/wiki/Operating_system). ([Types of operating systems](https://en.wikipedia.org/wiki/Operating_system#Types_of_operating_systems))

#### I will pick [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking), precisely [preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)#Preemptive_multitasking), for my explanation.

#### If your [operating system](https://en.wikipedia.org/wiki/Operating_system) is [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows), it belongs to [preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)#Preemptive_multitasking) [operating system](https://en.wikipedia.org/wiki/Operating_system).

## What are [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking), [preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)#Preemptive_multitasking)?

### [Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking)

![multitasking](https://media.geeksforgeeks.org/wp-content/uploads/20200426073127/Multitasking1-300x300.png)

>[Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) is the [concurrent](https://en.wikipedia.org/wiki/Concurrency_(computer_science)) execution of multiple [tasks](https://en.wikipedia.org/wiki/Task_(computing)) (also known as processes) over a certain period of time. ([Computer multitasking, wikipedia](https://en.wikipedia.org/wiki/Computer_multitasking))

>[Multitasking](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking) in [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) allocates a processor [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) to each [thread](https://en.wikipedia.org/wiki/Thread_(computing)) it executes. ([Multitasking, microsoft docs](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking))

### [Preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)#Preemptive_multitasking)

>The term [preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)#Preemptive_multitasking) is used to distinguish a multitasking operating system, which permits preemption of tasks, from a cooperative multitasking system wherein processes or tasks must be explicitly programmed to yield when they do not need system resources.

## [Process](https://en.wikipedia.org/wiki/Process_(computing)), [thread](https://en.wikipedia.org/wiki/Thread_(computing)), [operating system](https://en.wikipedia.org/wiki/Operating_system), [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)), [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))

### [Process](https://en.wikipedia.org/wiki/Process_(computing))

### [Thread](https://en.wikipedia.org/wiki/Thread_(computing))

>A [thread](https://en.wikipedia.org/wiki/Thread_(computing)) is the sequence of [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) given to cores. ([CPU Cores VS Threads Explained, youtube](https://youtu.be/hwTYDQ0zZOw))

>[Thread](https://en.wikipedia.org/wiki/Thread_(computing)) in [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) is the basic unit to which an operating system allocates processor time. ([Threads and threading, microsoft docs](https://docs.microsoft.com/en-us/dotnet/standard/threading/threads-and-threading))

>More reference about [thread](https://en.wikipedia.org/wiki/Thread_(computing)) : [Thread (computing), wikipedia](https://en.wikipedia.org/wiki/Thread_(computing))

### Difference between [Process](https://en.wikipedia.org/wiki/Process_(computing)) and [Thread](https://en.wikipedia.org/wiki/Thread_(computing))

## [Operating system](https://en.wikipedia.org/wiki/Operating_system), [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)), [Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking), [Preemptive multitasking](https://en.wikipedia.org/wiki/Preemption_(computing)), [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))

![Scheduling](http://beyondthegeek.com/wp-content/uploads/2017/09/Screen-Shot-2017-09-29-at-12.39.17-AM-500x484.png)

- An [operating system](https://en.wikipedia.org/wiki/Operating_system) [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) contains a [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) program which determines how much time each process spends executing, and in which order execution control should be passed to programs. ([Operating system, wikipedia](https://en.wikipedia.org/wiki/Operating_system#Multitasking))

- There are many [operating systems](https://en.wikipedia.org/wiki/Operating_system). ([List of operating systems](https://en.wikipedia.org/wiki/List_of_operating_systems))

- I will pick [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) for my explanation.

- Microsoft Windows supports preemptive multitasking, which creates the effect of simultaneous execution of multiple threads from multiple processes. ([About Processes and Threads](https://docs.microsoft.com/en-us/windows/win32/procthread/about-processes-and-threads))

## [Multitasking](https://en.wikipedia.org/wiki/Computer_multitasking), [task](https://en.wikipedia.org/wiki/Task_(computing)), [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice)

The concept of [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing)) makes it possible to have computer [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) with a single [central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit).

Most modern [operating systems](https://en.wikipedia.org/wiki/Operating_system) have [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [kernels](https://en.wikipedia.org/wiki/Kernel_(operating_system)), which are designed to permit [tasks](https://en.wikipedia.org/wiki/Task_(computing)) to be preempted even when in kernel mode. ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)))

[Preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) allocates a processor [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) to each [thread](https://en.wikipedia.org/wiki/Thread_(computing)) it executes. ([Multitasking, ](https://docs.microsoft.com/en-us/windows/win32/procthread/multitasking))

If your [operating systems](https://en.wikipedia.org/wiki/Operating_system) is [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows), it belongs [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking).

### [Task](https://en.wikipedia.org/wiki/Task_(computing))

>A [task](https://en.wikipedia.org/wiki/Task_(computing)) is a unit of execution or a unit of work. The term is ambiguous; precise alternative terms include process, light-weight process, [thread (for execution)](https://en.wikipedia.org/wiki/Thread_(computing)), step, request, or query (for work). ([Task (computing), wikipedia](https://en.wikipedia.org/wiki/Task_(computing)))

### [Time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice)

>The period of time for which a process is allowed to run in a [preemptive](https://en.wikipedia.org/wiki/Preemption_(computing)) [multitasking](https://en.wikipedia.org/wiki/Computer_multitasking) system is generally called the [time slice](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice) or quantum. ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)#Time_slice))

## [Context switch](https://en.wikipedia.org/wiki/Context_switch), [protection ring](https://en.wikipedia.org/wiki/Protection_ring), [CPU modes](https://en.wikipedia.org/wiki/CPU_modes)

![Kernel level multi-thread process model](https://d8it4huxumps7.cloudfront.net/uploads/images/621c698b9abab_kernel_level_multi_thread_process_model.jpg)
![Context_switch](https://www.bogotobogo.com/cplusplus/images/multithread/Context_switch.png)

A change in the currently executing [task](https://en.wikipedia.org/wiki/Task_(computing)) of a [processor](https://en.wikipedia.org/wiki/Processor_(computing)) is known as [context switching](https://en.wikipedia.org/wiki/Context_switch). ([Preemption (computing), wikipedia](https://en.wikipedia.org/wiki/Preemption_(computing)))

[Protection rings](https://en.wikipedia.org/wiki/Protection_ring) are generally hardware-enforced by some [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) architectures that provide different [CPU modes](https://en.wikipedia.org/wiki/CPU_modes) at the hardware or microcode level. ([Protection ring, wikipedia](https://en.wikipedia.org/wiki/Protection_ring))

Many modern [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) architectures (including the popular Intel x86 architecture) include some form of ring protection, although the [Windows NT](https://en.wikipedia.org/wiki/Windows_NT) [operating system](https://en.wikipedia.org/wiki/Operating_system), like Unix, does not fully utilize this feature. OS/2 does to some extent, using three rings: ring 0 for kernel code and device drivers, ring 2 for privileged code (user programs with I/O access permissions), and ring 3 for unprivileged code (nearly all user programs). ([Protection ring, wikipedia](https://en.wikipedia.org/wiki/Protection_ring))

**[Context switches](https://en.wikipedia.org/wiki/Context_switch) can occur only in [kernel mode](https://en.wikipedia.org/wiki/CPU_modes)**. ([Context Switch Definition, linfo](http://www.linfo.org/context_switch.html))

More reference about [Context switches](https://en.wikipedia.org/wiki/Context_switch) can occur only in [kernel mode](https://en.wikipedia.org/wiki/CPU_modes) are as follows.
- [Context Switch implies Mode Switch, stackoverflow](https://stackoverflow.com/questions/41359896/context-switch-implies-mode-switch)
- [Does context switching happen in the the kernel mode?, quora](https://www.quora.com/Does-context-switching-happen-in-the-the-kernel-mode)
- [What happens to CPU mode if CPU time slice expires during CPU mode switch?](https://stackoverflow.com/questions/72351560/what-happens-to-cpu-mode-if-cpu-time-slice-expires-during-cpu-mode-switch)

Also, **all [threads](https://en.wikipedia.org/wiki/Thread_(computing)) start off in [kernel space](https://en.wikipedia.org/wiki/CPU_modes), because the clone() operation happens in [kernel space](https://en.wikipedia.org/wiki/CPU_modes)**. ([Difference between user-level and kernel-supported threads?, stackoverflow](https://stackoverflow.com/questions/15983872/difference-between-user-level-and-kernel-supported-threads))

In processes on x86 Windows, **[threads](https://en.wikipedia.org/wiki/Thread_(computing)) alternate between the [user and kernel modes](https://en.wikipedia.org/wiki/CPU_modes) (between the program and the OS/system calls)**. ([Difference between user-level and kernel-supported threads?, stackoverflow](https://stackoverflow.com/questions/15983872/difference-between-user-level-and-kernel-supported-threads))

**[CPU](https://en.wikipedia.org/wiki/Central_processing_unit) must enter [kernel mode](https://en.wikipedia.org/wiki/CPU_modes) before [context switch](https://en.wikipedia.org/wiki/Context_switch)**. ([Core execution flow in the point of thread context switch and CPU mode switch](https://stackoverflow.com/questions/72367424/core-execution-flow-in-the-point-of-thread-context-switch-and-cpu-mode-switch))

The execution flow in core from timer interrupt is as follows.
- 1. A thread enters kernel mode because of an timer interrupt.
- 2. Context switch occur in kernel mode.
- 3. Current thread context is stored.
- 4. Next thread context is restored.
- 5. The thread returns at exactly the place where next thread last called it.
- 6. The thread returns from the interrupt to application code running in user-mode.

### [Context switch](https://en.wikipedia.org/wiki/Context_switch)

>A [context switch](https://en.wikipedia.org/wiki/Context_switch) (also sometimes referred to as a process switch or a task switch) is the switching of the [CPU (central processing unit)](https://en.wikipedia.org/wiki/Central_processing_unit) from one process or [thread](https://en.wikipedia.org/wiki/Thread_(computing)) to another. ([Context Switch Definition, linfo](http://www.linfo.org/context_switch.html))

>A [context switch](https://en.wikipedia.org/wiki/Context_switch) is the process of storing the state of a process or [thread](https://en.wikipedia.org/wiki/Thread_(computing)), so that it can be restored and resume execution at a later point. ([Context switch, wikipedia](https://en.wikipedia.org/wiki/Context_switch))

### [Protection rings](https://en.wikipedia.org/wiki/Protection_ring)

>[Protection rings](https://en.wikipedia.org/wiki/Protection_ring) are mechanisms to protect data and functionality from faults (by improving fault tolerance) and malicious behavior (by providing computer security). ([Protection ring, wikipedia](https://en.wikipedia.org/wiki/Protection_ring))

### [CPU modes](https://en.wikipedia.org/wiki/CPU_modes)

>[CPU modes](https://en.wikipedia.org/wiki/CPU_modes) (also called processor modes, CPU states, CPU privilege levels and other names) are operating modes for the [central processing unit](https://en.wikipedia.org/wiki/Central_processing_unit) of some computer architectures that place restrictions on the type and scope of operations that can be performed by certain processes being run by the CPU. ([CPU modes, wikipedia](https://en.wikipedia.org/wiki/CPU_modes))

![CPU_core_thread](https://www.logicbig.com/quick-info/images/multithreading.png)

# Organized by ysoh880710
