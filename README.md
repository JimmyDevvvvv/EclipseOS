# EclipseOS

EclipseOS is a custom-built operating system designed from scratch, focusing on low-level system programming, kernel development, and OS architecture. It is a learning-driven project aiming to explore protected mode, memory management, process scheduling, and system calls, while maintaining a modular and scalable design.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Boot Process](#boot-process)
- [Installation and Compilation](#installation-and-compilation)
- [Development Environment](#development-environment)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## Introduction
EclipseOS is a personal operating system project created to deeply understand OS internals and system architecture. The project includes real mode and protected mode operations, a custom bootloader, and a basic kernel with essential functionalities. Future plans include process scheduling, file system support, and networking.

## Features
- **Custom Bootloader**: Loads the kernel and sets up protected mode.
- **Real Mode & Protected Mode Transition**: Implements segmentation and switching between execution modes.
- **Memory Management**: Basic memory allocation and paging (WIP).
- **Basic Kernel Functions**: Interrupt handling, simple system calls, and screen output.
- **Filesystem (Planned)**: Development of a minimal filesystem for storing and retrieving files.
- **Multitasking (Planned)**: Implementing process scheduling and task switching.
- **Networking (Planned)**: Adding basic TCP/IP stack implementation.

## System Architecture
The OS follows a layered architecture:

1. **Bootloader (Stage 1 & 2)**: Initializes the system and loads the kernel.
2. **Kernel**: Handles memory, process scheduling, and system calls.
3. **Drivers (Planned)**: Input/output device management (e.g., keyboard, display, disk storage).
4. **Filesystem (Planned)**: A simple filesystem for storing data.
5. **Networking (Planned)**: TCP/IP stack integration.

## Boot Process
1. **BIOS Execution**: The BIOS loads the bootloader from the boot sector.
2. **Bootloader (Stage 1)**: Sets up the environment, loads the Stage 2 loader.
3. **Bootloader (Stage 2)**: Enables protected mode, loads the kernel.
4. **Kernel Execution**: Initializes memory, interrupts, and system calls.

## Installation and Compilation
### Prerequisites
- **GCC Cross Compiler**: Required for compiling low-level code.
- **NASM**: Used for assembling the bootloader and other assembly code.
- **QEMU/Bochs**: Virtualization software for testing the OS.

### Compiling EclipseOS
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/EclipseOS.git
   cd EclipseOS
   ```
2. Build the bootloader and kernel:
   ```sh
   make
   ```
3. Run it in QEMU:
   ```sh
   make run
   ```

## Development Environment
EclipseOS is primarily developed in:
- **Assembly (x86 NASM)**: For bootloader and low-level operations.
- **C**: Kernel and core system functionalities.
- **QEMU**: Testing and debugging.

## Roadmap
- [x] Implement Bootloader (Stage 1 & 2)
- [x] Enable Protected Mode
- [x] Implement Memory Segmentation
- [ ] Add Paging and Memory Management
- [ ] Implement Basic File System
- [ ] Implement Process Scheduling (Multitasking)
- [ ] Add Network Stack Support

## Contributing
This is a personal project, but contributions and suggestions are welcome! Feel free to open an issue or submit a pull request.

## License
EclipseOS is licensed under the MIT License. See the `LICENSE` file for details.

---



