---
title: A1 - Computer Fundamentals
layout: page
description: About
bodyClass: page-about
---


# Lesson 1 - Von Neumann architecture

The Von Neumann architecture is the design used in most everday computers. The main idea before the design is that instructions and data are stored within the same memory, simplifying hardware design and making them easy to reprogram meaning they can be used for many tasks and can therefore be used for whatever the user requires. 

<p align="center">
<img src="/images/illustrations/IBA1_L1.png" alt="My Logo" width="63%" height="auto">
</p>

The modern Von Neumann architecture contains the followed components:

## 🖥️ Central Processing Unit (CPU)
The CPU is the core of the computer system. It executes instructions, performs calculations, and manages data flow between components. It includes the Control Unit, ALU, and various registers.
## 💾 Primary Memory (RAM)
Primary memory stores data and instructions currently in use. It is volatile, meaning its contents are lost when power is turned off. The CPU fetches instructions and data from RAM during processing.
## 🔗 Buses – Overview
Buses are communication pathways that transfer data and signals between components. They are essential for the CPU to interact with memory and other parts of the system.
## 🧭 Address Bus
Carries memory addresses from the CPU to RAM. It is unidirectional (CPU → Memory).
## 🔄 Data Bus
Transfers actual data between the CPU and memory. It is bidirectional (CPU ↔ Memory).
## 🧵 Control Bus
Carries control signals from the Control Unit to other components. These signals manage operations like read, write, and instruction execution.
## 📦 Registers – Overview
Registers are small, fast storage locations inside the CPU. They temporarily hold data, instructions, and addresses during processing. Each register plays a specific role in the fetch–decode–execute cycle.
## 🎛️ Control Unit (CU)
The Control Unit manages the execution of instructions. It decodes instructions in the Instruction Register and sends control signals via the control bus to coordinate operations.
## ➕ Arithmetic Logic Unit (ALU)
Performs arithmetic operations (e.g., addition, subtraction) and logical operations (e.g., AND, OR, NOT). Works closely with the accumulator to process data.
## 📜 Instruction Register (IR)
Holds the current instruction that has been fetched from memory. The Control Unit decodes this instruction to determine the required action.
## 📍 Program Counter (PC)
Stores the address of the next instruction to be fetched from memory. It usually increments automatically unless modified by a jump or branch instruction.
## 🧭 Memory Address Register (MAR)
Holds the address of the memory location to be accessed. This address is sent to RAM via the address bus.
## 📥 Memory Data Register (MDR)
Holds the actual data being transferred to or from memory. It communicates with RAM via the data bus.
## 🧮 Accumulator
Stores intermediate results of calculations performed by the ALU. Often used as the default destination for ALU outputs.

## Lesson Resources:

- <a href="https://nordanglia-my.sharepoint.com/:w:/g/personal/elliott_rees_nais_hk/EYAb8dEbeypHmX6pGt2MIysBDezDLFZl3uNWHibq40IhkA?download=1">Lesson Worksheet</a>
- <a href="https://nordanglia-my.sharepoint.com/:w:/g/personal/elliott_rees_nais_hk/ETeBkfkr5-tDnu2GuzyJoYcBrO_bCvyqSJ13ifbyK5hr5A?download=1">Lesson Worksheet Answers</a>



<hr>

# Lesson 2 - Graphics Processing Units & Cores

## What is a core?
A core is the fundamental processing unit within a computer’s central processing unit (CPU) or graphics processing unit (GPU). It performs the basic operations required to run programs—such as fetching instructions, executing calculations, and managing data flow.

In CPU's, Each core can independently execute tasks. Most modern CPU's have multiple cores which allow the CPU to handle several tasks simultaneously (called parallel processing). This improves performance in multitasking, gaming, video editing, and more.

Example: A quad-core CPU can run four separate threads at once—like streaming music, browsing the web, and running background updates without slowing down.



<p align="center">
<img src="/images/illustrations/cores.svg" alt="My Logo" width="75%" height="auto">
</p>


## What is the role of a Graphics Processing Unit?
The Graphics Processing Unit (GPU) is a specialized processor designed to handle complex visual and mathematical tasks—especially those related to rendering images, video, and animations. But its role goes far beyond just making things look pretty:
- Rendering Images: Converts digital data into pixels on your screen.
- 3D Graphics: Handles geometry, lighting, shading, and textures in games and simulations.
- Video Playback: Accelerates decoding and smooth playback of high-resolution video.

## 🧠 Parallel Processing Power
Unlike a CPU, which has a few powerful cores for general tasks, a GPU has hundreds or thousands of smaller cores optimized for doing many calculations at once. This makes it ideal for:
- Scientific simulations
- Machine learning and AI
- Cryptocurrency mining
- Data visualization

Example: Rendering a 3D scene in a video game involves calculating lighting, textures, and movement for millions of pixels—GPU cores do this in parallel.

<hr>

# Lesson 2.5 (HL Only) - The difference between a CPU and a GPU

The central processing unit (CPU) and the graphical processing unit (GPU) are both core
components of modern computers. They are designed differently, which is why they are used
for different kinds of tasks. The CPU is great for handling various jobs, but the GPU is better for
doing the same job many times on a lot of data at once.

## Design Philosophies

CPUs are generally called “general-purpose processors” because they can handle many types
of tasks. They are designed to run the operating system, process user input and manage
programs. CPUs are good at tasks where decisions need to be made quickly, and where
different types of work are being done at the same time.
GPUs are specialized processors because they tocus on specific types of tasks. They are
made for processing large amounts of data in parallel. This means they can work on many
calculations at the same time. For example, GPUs are used to process images and videos
because they can work on thousands of pixels at once. 

## Core Architecture

The CPU has only a few cores, but these cores are very powerful. Each core can handle many
different instructions, but it works best when doing one task at a time. This makes the CPU
very good for such tasks as running the operating system, where quick responses are needed.
CPUs also have features including branch prediction (where the CPU tries to guess what will
happen next) and out-of-order execution (where the CPU can work on tasks that are ready
before others).
The GPU has many smaller cores. These cores are not as powerful as the CPU cores, but there
are thousands of them, and they all work at the same time. This is why the GPU is very good
for tasks such as rendering 3D images, where many similar calculations need to happen at
once. The GPU’s architecture is designed to work on large sets of data all at the same time. 

## Memory access and power efficiency 

The CPU and GPU access memory differently. The CPU uses a smaller, high-speed memory
cache to get data quickly. This is useful when the CPU needs to access small amounts of data
many times, such as when running programs or handling user inputs.
The GPU uses its own special memory called VRAM (video RAM). VRAM has a very high
bandwidth, meaning it can move large amounts of data at once, such as images and videos.
However, the GPU uses more power because it must process a lot of data at the same time,
especially when rendering videos or running complex simulations. 


<p align="center">
<img src="/images/illustrations/HLI1.png" alt="My Logo" width="75%" height="auto">
</p>

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/h9Z4oGN89MU?si=bVyrwfzZKMvihRg2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</p>

<hr>


# Lesson 3 - Visualsation of the Fetch - Decode - Execution Cycle


The fetch—decode—execute cycle, also known as the “instruction cycle”, is the fundamental
process that a CPU uses to execute instructions. The cycle consists of three main stages:
- 1 Fetch: The CPU fetches an instruction from the memory.
- 2 Decode: The CPU interprets the instruction and prepares the necessary operations to execute it.
- 3 Execute: The CPU performs the actions required by the instruction. 


An easier way to see these stages carried out in more detail is to use an educational CPU model
known as Little Man Computer, which you can search for online or use the one available
here: https://peterhigginson.co.uk/Imc. This model uses assembly language — a simple set of
instructions, each represented by three letters, which is stored as a three-digit code in the
memory. The full set of instructions is: 

<p align="center">
<img src="/images/illustrations/lmc.png" alt="My Logo" width= "auto" height="auto">
</p>



## Activity 1: Copy and run the following code in the LMC. 
<p align="center">
<img src="/images/illustrations/lmc1.png" alt="My Logo" width="50%" height="auto">
</p>

After hitting submit, you should see the memory the instructions loaded into memory address 1, memory address 2 and memory address three. There are now three isntructions for our Program counter to work through, which will take three instruction cycles in our single core CPU to work through.

Hit run to see each instruction be fetched, decoded and executed. The INP command waits for the user to input a value which will be held temporarily in the accumulator. The STA 10 command will store the content of the accumulator into memory location 10.


## Activity 2: Ammend your code to look like the following:
<p align="center">
<img src="/images/illustrations/lmc2.png" alt="My Logo" width="50%" height="auto">
</p>

Can you see what this program is doing?


## Challenges
- Write a program that adds three number together and outputs the result.
- Write a program that takes two inputers and subtracts the second from the first.
- Write a program which outputs the larger of two input values.
- Write a program that outputs the largest of three input values.
- Write a program which takes three numbers and outputs them in ascending order.
- Write a program which takes in two numbers and subtracts the second from the first. If the result is negative, the program should output the value 0.
- Write a program which counts down from any input value.
- Write a program which multiplies two numbers.


<hr>


# Lesson 4 - Primary Memory

Primary memory is memory which is directly accessed by the CPU. It generally stores instructions for the CPU to fetch, decode and execute as well data (numbers,  text, images, sound ect...) which the user currently has open. Some primary memory is volatile (loses memory when the power is removed) and some is non-volatile (rememebrs even after power is lost.)

Most programs and data are stored in secondary memory in order to be stored permanently and moved to primary memory when openned. We will explore secondary memory in lesson 5!

## Random Access Memory
RAM (random access memory) holds instructions and data for programs that are currently running. For example, when you open an app on your phone or computer, it loads into RAM so that is can be accessed quickly by the CPU.
RAM is volatile, meaning that it loses its contents when the power to the computer is turned off. This is why, when playing a game, you lose your progress unless you save the
game (which is then stored in secondary memory).

## Cache (L1, L2 and L3) 
Cache memory is small, high speed memory which is located both within and near to the CPU.  It acts as a buffer between the CPU and the slower RAM, storing frequently used data
and instructions.

<p align="center">
<img src="/images/illustrations/cache.png" alt="My Logo" width="75%" height="auto">
</p>

There are three types of cache: L1, L2 and L3, each with different sizes and speeds. The closer
to the CPU, the faster it is.

- L1 cache is located directly on the CPU, making it the fastest type of cache. It can be
accessed almost instantly due to its location. However, it is also the smallest, often only
a few kilobytes in size (32KB to 128KB per core). Each CPU core usually has its own
L1 cache, which is typically split into two sections: L1i to store instructions and L1d to
store data.
- L2 cache can either be on the CPU, like L1, or situated very close to the CPU. L2 cache
is larger than L1 and can be up to several megabytes in size (256KB to 2MB per core),
providing more storage for frequently used instructions. It is faster than L3, but slightly
slower than L1, though it still significantly speeds up processing by reducing the need to
fetch data from the slower RAM.
- L3 cache is often located the furthest from the CPU chip. L3 cache may be shared on
multiple-core CPUs, whereas L1 and L2 are usually exclusive to a single core. It is the largest
of the three, and can be up to tens of megabytes in size (2MB to 64MB shared across all
cores). It is the slowest of the three types of caches, but is still significantly faster than RAM.


<p align="center">
<img src="/images/illustrations/cache2.png" alt="My Logo" width="50%" height="auto">
</p>


# Cache Hit and Cache Miss

The terms cache hit and cache miss are used to describe the efficiency of the CPU’s cache
memory when retrieving data. A cache hit is the ideal scenario, where the CPU requests data
and it is found in the cache memory. A cache miss means it was not found, necessitating
retrieval from the slower main memory (RAM) or even slower storage (SSD / HDD).

The percentage of hit rate determines the efficiency and effectiveness of the cache. A low
percentage means the system would suffer more from latency, where the data has to be fetched
from elsewhere, hindering pertormance speed. Systems with a larger cache size will generally
perform better, as well as systems with more intelligent prefetching techniques that can predict
which data will be needed soon and load it into cache ahead of time. 

Imagine you are playing a video game on a computer. The CPU frequently checks the L1, 1.2
and L3 cache to find the data it needs to run the game smoothly. The game’s core functions,
such as player controls and game logic, might be stored in the L1 cache, while the less
frequently accessed data, such as background textures, may be in the L3 cache. The layering
system helps to ensure that the game runs smoothly, without interruptions.
A CPU with a larger cache or more advanced prefetching (a technique where the CPU predicts
what data it will need and loads it into cache ahead of time) has fewer cache misses and
performs better overall. 



## Read Only Memory

 The Read Only Memory (ROM) is a type of primary memory which can only be read and stores the Basic Input / Output System (BIOS). The BIOS is an essential piece of software which is required get the computer system running when powering on. It has two main roles:
- Number 1: To initialize the system hardware components and tast that they work properly. If any key hardware is found to not function as expected, the BIOS will display an error message and not allow the startup of the computer system to proceed.
- Number 2: To locate the operating system and move it into RAM to allow the OS to run the entire computer system.

ROM is non-volatile to ensure that the BIOS is never deleted or overwritten.



<hr>

# Lesson 4 - Visualsation of the Fetch - Decode - Execution Cycle


The fetch—decode—execute cycle, also known as the “instruction cycle”, is the fundamental
process that a CPU uses to execute instructions. The cycle consists of three main stages:
- 1 Fetch: The CPU fetches an instruction from the memory.
- 2 Decode: The CPU interprets the instruction and prepares the necessary operations to execute it.
- 3 Execute: The CPU performs the actions required by the instruction. 


An easier way to see these stages carried out in more detail is to use an educational CPU model
known as Little Man Computer, which you can search for online or use the one available
here: https://peterhigginson.co.uk/Imc. This model uses assembly language — a simple set of
instructions, each represented by three letters, which is stored as a three-digit code in the
memory. The full set of instructions is: 

<p align="center">
<img src="/images/illustrations/lmc.png" alt="My Logo" width= "auto" height="auto">
</p>



## Activity 1: Copy and run the following code in the LMC. 
<p align="center">
<img src="/images/illustrations/lmc1.png" alt="My Logo" width="50%" height="auto">
</p>

After hitting submit, you should see the memory the instructions loaded into memory address 1, memory address 2 and memory address three. There are now three isntructions for our Program counter to work through, which will take three instruction cycles in our single core CPU to work through.

Hit run to see each instruction be fetched, decoded and executed. The INP command waits for the user to input a value which will be held temporarily in the accumulator. The STA 10 command will store the content of the accumulator into memory location 10.


## Activity 2: Ammend your code to look like the following:
<p align="center">
<img src="/images/illustrations/lmc2.png" alt="My Logo" width="50%" height="auto">
</p>

Can you see what this program is doing?


## Challenges
- Write a program that adds three number together and outputs the result.
- Write a program that takes two inputers and subtracts the second from the first.
- Write a program which outputs the larger of two input values.
- Write a program that outputs the largest of three input values.
- Write a program which takes three numbers and outputs them in ascending order.
- Write a program which takes in two numbers and subtracts the second from the first. If the result is negative, the program should output the value 0.
- Write a program which counts down from any input value.
- Write a program which multiplies two numbers.


<hr>

# Lesson 4.5 (HL Only) - The Process of Pipelining in Multi-Core Architectures

<hr>

# Lesson 5 - Secondary Storage Devices & Cloud Computing

<hr>

# Lesson 6 - Data Compression

<hr>