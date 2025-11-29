# ASM-Scratchpad  
**x86/x64 Assembly Language Learning Lab**

A structured, hands-on collection of assembly language examples ranging from absolute fundamentals to advanced exploitation techniques. For Curious learners, reverse engineers, exploit developers, security researchers, and anyone wanting to truly understand how software interacts with hardware.

[![GitHub Repo](https://img.shields.io/badge/GitHub-CyberForgeEx/ASM--Scratchpad-181717?logo=github)](https://github.com/CyberForgeEx/ASM-Scratchpad)
[![Stars](https://img.shields.io/github/stars/CyberForgeEx/ASM-Scratchpad?style=social)](https://github.com/CyberForgeEx/ASM-Scratchpad)

---

## Project Goal

Provide clear, commented, progressively difficult assembly examples so learners can:

- Understand CPU registers, flags, and instruction sets.
- Master stack, heap, and memory layout
- Make direct Linux system calls
- Write position-independent shellcode
- Learn real-world exploitation primitives (buffer overflow, format strings, ROP)

All code is educational and intended for legal, authorized security research and learning only.

---

#### 1. Basics
Foundation you need before anything else

- `hello-world/` – Minimal program structure, `syscall` write + exit
- `registers/`   – mov, xchg, push/pop, register preservation.
- `arithmetic/`  – add, sub, mul, div.

#### 2. Memory
How data really lives in RAM

- `stack-basics/`      – Stack frames, calling convention, local variables.
- `heap-allocation/`   – malloc/free via `brk`/`mmap` system calls.
- `buffer-overflow/`   – Classic stack smashing examples (with disabled mitigations)

#### 3. System Calls
Talking directly to the kernel

- `read-write/`   – File and stdin/stdout operations.
- `execve/`       – Spawning `/bin/sh` and arbitrary binaries.
- `socket-basics/`– TCP connect/backconnect using raw sockets.

#### 4. Advanced Exploitation
Weaponizing your knowledge

- `shellcode/`       – Polymorphic, alphanumeric, and egghunter shellcode.
- `format-strings/`  – Information leaks and arbitrary write exploits.
- `rop-gadgets/`     – Building ROP chains, bypassing NX/DEP.

---

## Quick Start (Linux x86_64)

```bash
# Clone the repo
git clone https://github.com/CyberForgeEx/ASM-Scratchpad.git
cd ASM-Scratchpad

# Example: compile and run hello-world (64-bit)
cd 1_basics/hello-world
nasm -f elf64 hello.asm -o hello.o
ld hello.o -o hello
./hello

# 32-bit example
nasm -f elf32 example.asm -o example.o
ld -m elf_i386 example.o -o example
./example
```

### Prerequisites

- Linux (Ubuntu/Kali/Arch recommended)
- `nasm` – Netwide Assembler
- `gcc` / `ld` – GNU linker
- `gdb`, `objdump`, `strace` (highly recommended)

Install everything on Debian/Ubuntu:

```bash
sudo apt update && sudo apt install nasm gcc gdb build-essential
```

---

## Recommended Learning Order

1. **Start →** `1_basics/` (master registers & program flow)  
2. **Then →** `2_memory/` (understand stack and buffer overflows)  
3. **Then →** `3_system-calls/` (learn to talk to the kernel)  
4. **Finally →** `4_advanced/` (write real shellcode & exploits)

---

## Useful Tools While Learning

| Tool       | Purpose                              |
|------------|--------------------------------------|
| `gdb` + `gef` or `pwndbg` | Best debugging experience         |
| `objdump -d`               | Disassemble binaries               |
| `strace` / `ltrace`           | Trace system calls                 |
| `readelf`                   | Inspect ELF headers                |
| Radare2 / Ghidra           | Advanced analysis                  |

---

**Enjoy learning assembly the right way - one instruction at a time.**

If this repository helps you understand low-level programming, please give it a star on GitHub, it means the world!

→ [github.com/CyberForgeEx/ASM-Scratchpad](https://github.com/CyberForgeEx/ASM-Scratchpad)
