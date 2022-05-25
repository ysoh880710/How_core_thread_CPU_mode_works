# How core, thread, CPU mode works

## Multi-core, CPU, core

![CPU_core_thread](https://www.logicbig.com/quick-info/images/multithreading.png)

### [Multi-core](https://en.wikipedia.org/wiki/Multi-core_processor)

>A [multi-core processor](https://en.wikipedia.org/wiki/Multi-core_processor) is a computer processor on a single integrated circuit with two or more separate [CPUs](https://en.wikipedia.org/wiki/Central_processing_unit), called cores, each of which reads and executes program instructions. ([Multi-core processor, wikipedia](https://en.wikipedia.org/wiki/Multi-core_processor))

>More reference about multi-core processor : [Core Processor, ScienceDirect](https://www.sciencedirect.com/topics/computer-science/core-processor)

>More reference about multiple CPU : [Multiple CPU Vs. Multi-Core, chron.com](https://smallbusiness.chron.com/jpegs-hp-thin-client-42782.html)

### [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)

>A [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is an electronic circuit inside the computer that carries out [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) to perform arithmetic, logical, control and input/output operations. ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

>More reference about [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) : [Central processing unit, wikipedia](https://en.wikipedia.org/wiki/Central_processing_unit)

### Core

>A Core is an execution unit inside the CPU that receives and executes [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science)). ([Difference Between CPU and Core, pediaa.com](https://pediaa.com/difference-between-cpu-and-core/))

### Difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core

>[CPU](https://en.wikipedia.org/wiki/Central_processing_unit) is responsible for controlling the cores. ([Differences Between Core and CPU, baeldung.com](https://www.baeldung.com/cs/core-vs-cpu))

>More reference about difference between [CPU](https://en.wikipedia.org/wiki/Central_processing_unit) and core : [Difference between core and processor, stackoverflow](https://stackoverflow.com/questions/19225859/difference-between-core-and-processor)

## [Instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture), [instructions](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

Every processor or processor family has its own [instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture). ([Machine code, wikipedia](https://en.wikipedia.org/wiki/Machine_code))

There are many [instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures). ([List of instruction sets](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures))

I will pick [x86](https://en.wikipedia.org/wiki/X86), precisely [x86-64](https://en.wikipedia.org/wiki/X86-64), for my explanation.

If your CPU is AMD Ryzen Series or Intel Core i3, Core i5, Core i7, Core i9, it belongs [x86-64]([https://en.wikipedia.org/wiki/X86](https://en.wikipedia.org/wiki/X86-64)).

### [x86](https://en.wikipedia.org/wiki/X86)

>[x86](https://en.wikipedia.org/wiki/X86) is a family of complex instruction set computer (CISC) [instruction set](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures) architectures initially developed by Intel based on the Intel 8086 microprocessor and its 8088 variant.

### [x86-64](https://en.wikipedia.org/wiki/X86-64)

>[x86-64](https://en.wikipedia.org/wiki/X86-64) is a 64-bit version of the [x86](https://en.wikipedia.org/wiki/X86) [instruction set](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures).

### [Instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science))

>An [instruction](https://simple.wikipedia.org/wiki/Instruction_(computer_science)) is a single operation of a processor defined by the processor [instruction set](https://en.wikipedia.org/wiki/Instruction_set_architecture).
