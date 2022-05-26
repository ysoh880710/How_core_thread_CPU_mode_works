# How core, [thread](https://en.wikipedia.org/wiki/Thread_(computing)), [CPU mode](https://en.wikipedia.org/wiki/CPU_modes) works

## What are [CPU](https://en.wikipedia.org/wiki/Central_processing_unit), [multi-core CPU](https://en.wikipedia.org/wiki/Multi-core_processor), core, and what they do?

### [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)

![CPU](https://media.geeksforgeeks.org/wp-content/uploads/20210605182444/CPUblock-660x495.jpg)

>A [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is an electronic circuit inside the computer that carries out [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) to perform arithmetic, logical, control and input/output operations. ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

>More reference about [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) : [Central processing unit, wikipedia](https://en.wikipedia.org/wiki/Central_processing_unit)

### [Multi-core CPU](https://en.wikipedia.org/wiki/Multi-core_processor)

![Multi-core CPU](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/CPU.png)

>A [multi-core CPU](https://en.wikipedia.org/wiki/Multi-core_processor) is a computer processor on a single integrated circuit with two or more separate cores, each of which reads and executes program [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)). ([Multi-core processor, wikipedia](https://en.wikipedia.org/wiki/Multi-core_processor))

>More reference about [multi-core CPU](https://en.wikipedia.org/wiki/Multi-core_processor) : [Multi-core processor, simple wikipedia](https://simple.wikipedia.org/wiki/Multi-core_processor)

### Core

![Core](https://www.baeldung.com/wp-content/uploads/sites/4/2021/11/Core-2.png)

>A Core is an execution unit inside the [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) that receives and executes [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)). ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

### Difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core

![Differences Between Core and CPU](https://www.baeldung.com/wp-content/ql-cache/quicklatex.com-c7135cdceb9b5a510d176ca7da28eb6a_l3.svg)

>While cores actually process [tasks](https://en.wikipedia.org/wiki/Task_(computing)), a [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is responsible for controlling the cores. ([Differences Between Core and CPU, baeldung](https://www.baeldung.com/cs/core-vs-cpu))

>More reference about difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core : [Difference between core and processor, stackoverflow](https://stackoverflow.com/questions/19225859/difference-between-core-and-processor)

## What are [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)), [Instruction set](https://simple.wikipedia.org/wiki/Instruction_set), [x86](https://en.wikipedia.org/wiki/X86), [x86-64](https://en.wikipedia.org/wiki/X86-64)?

### [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

>An [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) is a single operation of a processor defined by the processor [instruction set](https://simple.wikipedia.org/wiki/Instruction_set). ([Instruction (computer science), simple wikipedia](https://simple.wikipedia.org/wiki/Instruction_(computer_science)))

### [Instruction set](https://simple.wikipedia.org/wiki/Instruction_set)

>An [instruction set](https://simple.wikipedia.org/wiki/Instruction_set) is a list of all the [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) that a processor can execute. ([Instruction set, simple wikipedia](https://simple.wikipedia.org/wiki/Instruction_set))

#### Every processor or processor family has its own [instruction set](https://simple.wikipedia.org/wiki/Instruction_set). ([Machine code, wikipedia](https://en.wikipedia.org/wiki/Machine_code))

#### There are many [instruction sets](https://simple.wikipedia.org/wiki/Instruction_set). ([List of instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures))

#### I will pick [x86](https://en.wikipedia.org/wiki/X86), precisely [x86-64](https://en.wikipedia.org/wiki/X86-64), for my explanation.

#### If your [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is AMD Ryzen Series or Intel Core i3, Core i5, Core i7, Core i9, it belongs to [x86-64](https://en.wikipedia.org/wiki/X86-64).

### [x86](https://en.wikipedia.org/wiki/X86)

>[x86](https://en.wikipedia.org/wiki/X86) is a family of [complex instruction set computer (CISC)](https://en.wikipedia.org/wiki/Complex_instruction_set_computer) [instruction set](https://simple.wikipedia.org/wiki/Instruction_set) architectures initially developed by Intel based on the Intel 8086 microprocessor and its 8088 variant. ([x86, wikipedia](https://en.wikipedia.org/wiki/X86))

### [x86-64](https://en.wikipedia.org/wiki/X86-64)

>[x86-64](https://en.wikipedia.org/wiki/X86-64) is a 64-bit version of the [x86](https://en.wikipedia.org/wiki/X86) [instruction set](https://simple.wikipedia.org/wiki/Instruction_set). ([x86-64, wikipedia](https://en.wikipedia.org/wiki/X86-64))

>An [operating system](https://en.wikipedia.org/wiki/Operating_system) [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) contains a [scheduling](https://en.wikipedia.org/wiki/Kernel_(operating_system)) program which determines how much time each [process]() spends executing, and in which order execution control should be passed to programs.

## What are [operating system](https://en.wikipedia.org/wiki/Operating_system), [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware), [kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)), [scheduling](https://en.wikipedia.org/wiki/Scheduling_(computing))?

### [Operating system](https://en.wikipedia.org/wiki/Operating_system)

![operating_system](https://www.tutorialspoint.com/operating_system/images/conceptual_view.jpg)

>An [operating system (OS)](https://en.wikipedia.org/wiki/Operating_system) is system software that manages [computer hardware](https://en.wikipedia.org/wiki/Computer_hardware), software resources, and provides common services for computer programs. ([Operating system, wikipedia](https://en.wikipedia.org/wiki/Operating_system))

### [Computer hardware](https://en.wikipedia.org/wiki/Computer_hardware)

>[Computer hardware](https://en.wikipedia.org/wiki/Computer_hardware) includes the physical parts of a computer, such as the case, [central processing unit (CPU)](https://en.wikipedia.org/wiki/Central_processing_unit), random access memory (RAM), monitor, mouse, keyboard, computer data storage, graphics card, sound card, speakers and motherboard.

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
