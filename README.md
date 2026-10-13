# Learn-SecByte-CTF-Labs-Collection-Shellcode-Dev-Ret2libc-ROP-SEH-Overwrite-Practice
A curated collection of hands-on binary exploitation CTF labs covering Position-Independent Shellcode, Ret2libc, Ret2csu, Ret2dlresolve, Stack Pivoting, SEH Overwrites, Vtable Drift, and Memory Leak Cascades from Learn SecByte.
# Learn SecByte CTF & Cybersecurity Labs Collection

Welcome to the **Learn SecByte CTF & Cybersecurity Labs Collection**. This repository is a dedicated, searchable index of hands-on binary exploitation, advanced return-oriented programming (ROP), control flow hijacking, information disclosure chaining, and shellcode engineering labs designed for cybersecurity students, CTF players, exploit developers, reverse engineers, and vulnerability researchers.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Redirecting execution flows through memory corruption requires mastering advanced control flow primitives and chaining information leaks. Hosted on [Learn SecByte](https://learn.secbyte.org/), this collection of CTF challenge labs provides rigorous hands-on training across modern exploit engineering techniques.

From writing custom Position-Independent Shellcode (PIC) and null-free payloads to exploiting structured exception handlers (SEH), corrupting C++ virtual function tables (vtables), hijacking function pointers, executing partial pointer overwrites, pivoting constrained stacks, chaining memory leaks, and executing `ret2libc`, `ret2csu`, and `ret2dlresolve` attacks, these labs establish complete binary exploitation proficiency.

---

## Lab Collection & Index

Below is the complete, searchable index of all shellcode engineering, ROP, pointer hijacking, and memory leak challenges in this collection:

| # | Lab / Challenge Name | Category | Focus / Key Topics | Lab Link |
|---|----------------------|----------|---------------------|----------|
| 1 | **Position-Independent Shellcode Lab** | Shellcode Engineering | Delta technique / GetPC routines, PEB/TEB scanning, API hashing, position-independent execution | [Access Lab](https://learn.secbyte.org/ctf/position-independent-shellcode-lab) |
| 2 | **Advanced Shellcode Development Lab** | Shellcode Engineering | Custom assembly stagers, alphanumeric encoding, null-byte elimination, constrained byte filters | [Access Lab](https://learn.secbyte.org/ctf/advanced-shellcode-development-lab) |
| 3 | **Exception Handler Overwrite Techniques** | Control Flow Hijacking | Windows Structured Exception Handling (SEH), SEH chain corruption, `pop-pop-ret` gadgets, SafeSEH bypasses | [Access Lab](https://learn.secbyte.org/ctf/exception-handler-overwrite-techniques) |
| 4 | **Vtable Drift: Exploiting Virtual Function Tables** | Control Flow Hijacking | C++ object memory layout, virtual method tables (vtables), vtable pointers (`vptr`), indirect call hijacking | [Access Lab](https://learn.secbyte.org/ctf/vtable-drift-exploiting-virtual-function-tables) |
| 5 | **Function Pointer Hijacking** | Control Flow Hijacking | Function pointer arrays, callback structures, dynamic function overwrites, `system()` redirection | [Access Lab](https://learn.secbyte.org/ctf/function-pointer-hijacking) |
| 6 | **Partial Pointer Overwrite Exploitation** | Control Flow Hijacking | Partial byte overwrites, page boundary alignment, ASLR entropy reduction, relative jump redirection | [Access Lab](https://learn.secbyte.org/ctf/partial-pointer-overwrite-exploitation) |
| 7 | **Ret2csu Techniques: From Theory to Exploit** | ROP & Advanced Reusing | Universal `__libc_csu_init` gadgets, populate RDI/RSI/RDX registers, 64-bit function call preparation | [Access Lab](https://learn.secbyte.org/ctf/ret2csu-techniques-from-theory-to-exploit) |
| 8 | **Ret2dlresolve: Resolving the Unresolved** | ROP & Advanced Reusing | Dynamic symbol resolution, fake `Elf64_Rela`/`Elf64_Sym` structures, Lazy binding abuse, `system()` invocation | [Access Lab](https://learn.secbyte.org/ctf/ret2dlresolve-resolving-the-unresolved) |
| 9 | **Return-to-Libc: The Service Desk Breach** | ROP & Advanced Reusing | Stack buffer overflow, glibc address calculation, `system("/bin/sh")` execution, stack alignment (`movaps`) | [Access Lab](https://learn.secbyte.org/ctf/return-to-libc-the-service-desk-breach) |
| 10 | **Stack Pivoting: Rescue the Overflow** | ROP & Advanced Reusing | Limited buffer space, `leave; ret` gadgets, ESP/RSP register redirection, fake stack pivot | [Access Lab](https://learn.secbyte.org/ctf/stack-pivoting-rescue-the-overflow) |
| 11 | **Leak Cascade: Information Leak Chaining** | Memory Leaks & Information Disclosure | Format string leaks, uninitialized memory reads, multi-stage leak chains, ASLR base calculation | [Access Lab](https://learn.secbyte.org/ctf/leak-cascade-information-leak-chaining) |
| 12 | **Memory Leak Maze** | Memory Leaks & Information Disclosure | Out-of-bounds reads, heap pointer leaks, glibc base resolution, stack canary extraction | [Access Lab](https://learn.secbyte.org/ctf/memory-leak-maze) |

---

## Categories

### 1. Shellcode Development & Position-Independent Code
Master low-level assembly payload engineering, API hash resolution, and encoder design for constrained memory buffers.
- [Position-Independent Shellcode Lab](https://learn.secbyte.org/ctf/position-independent-shellcode-lab)
- [Advanced Shellcode Development Lab](https://learn.secbyte.org/ctf/advanced-shellcode-development-lab)

### 2. Control Flow Hijacking & Pointer Corruptions
Corrupt function pointers, C++ vtables, Windows SEH structures, and execute partial pointer overwrites to bypass ASLR.
- [Function Pointer Hijacking](https://learn.secbyte.org/ctf/function-pointer-hijacking)
- [Partial Pointer Overwrite Exploitation](https://learn.secbyte.org/ctf/partial-pointer-overwrite-exploitation)
- [Vtable Drift: Exploiting Virtual Function Tables](https://learn.secbyte.org/ctf/vtable-drift-exploiting-virtual-function-tables)
- [Exception Handler Overwrite Techniques](https://learn.secbyte.org/ctf/exception-handler-overwrite-techniques)

### 3. Advanced ROP, Ret2Libc & Dynamic Resolution
Construct return-oriented programming chains, leverage universal binary gadgets (`ret2csu`), pivot stack pointers, and trigger `ret2dlresolve`.
- [Return-to-Libc: The Service Desk Breach](https://learn.secbyte.org/ctf/return-to-libc-the-service-desk-breach)
- [Stack Pivoting: Rescue the Overflow](https://learn.secbyte.org/ctf/stack-pivoting-rescue-the-overflow)
- [Ret2csu Techniques: From Theory to Exploit](https://learn.secbyte.org/ctf/ret2csu-techniques-from-theory-to-exploit)
- [Ret2dlresolve: Resolving the Unresolved](https://learn.secbyte.org/ctf/ret2dlresolve-resolving-the-unresolved)

### 4. Memory Leaks & Information Disclosure Chaining
Exploit out-of-bounds reads and format string vulnerabilities to defeat ASLR, leak stack canaries, and calculate library offsets.
- [Memory Leak Maze](https://learn.secbyte.org/ctf/memory-leak-maze)
- [Leak Cascade: Information Leak Chaining](https://learn.secbyte.org/ctf/leak-cascade-information-leak-chaining)

---

## Learning Path

Follow this structured learning pathway to master control flow hijacking and advanced ROP payload development:

1. **Phase 1: Shellcode Engineering & Pointer Hijacking** — Develop position-independent payloads and hijack indirect pointers:
   - [Position-Independent Shellcode Lab](https://learn.secbyte.org/ctf/position-independent-shellcode-lab)
   - [Advanced Shellcode Development Lab](https://learn.secbyte.org/ctf/advanced-shellcode-development-lab)
   - [Function Pointer Hijacking](https://learn.secbyte.org/ctf/function-pointer-hijacking)
   - [Partial Pointer Overwrite Exploitation](https://learn.secbyte.org/ctf/partial-pointer-overwrite-exploitation)

2. **Phase 2: Information Leaks & Windows SEH / Vtables** — Chain memory leaks to break ASLR and exploit object layouts:
   - [Memory Leak Maze](https://learn.secbyte.org/ctf/memory-leak-maze)
   - [Leak Cascade: Information Leak Chaining](https://learn.secbyte.org/ctf/leak-cascade-information-leak-chaining)
   - [Vtable Drift: Exploiting Virtual Function Tables](https://learn.secbyte.org/ctf/vtable-drift-exploiting-virtual-function-tables)
   - [Exception Handler Overwrite Techniques](https://learn.secbyte.org/ctf/exception-handler-overwrite-techniques)

3. **Phase 3: Classic ROP & Stack Pivoting** — Execute return-to-libc attacks and pivot execution to controlled memory:
   - [Return-to-Libc: The Service Desk Breach](https://learn.secbyte.org/ctf/return-to-libc-the-service-desk-breach)
   - [Stack Pivoting: Rescue the Overflow](https://learn.secbyte.org/ctf/stack-pivoting-rescue-the-overflow)

4. **Phase 4: Advanced Universal Gadgets & Dynamic Resolution** — Utilize `ret2csu` and trigger `ret2dlresolve` symbol resolution:
   - [Ret2csu Techniques: From Theory to Exploit](https://learn.secbyte.org/ctf/ret2csu-techniques-from-theory-to-exploit)
   - [Ret2dlresolve: Resolving the Unresolved](https://learn.secbyte.org/ctf/ret2dlresolve-resolving-the-unresolved)

---

## How to Use the Labs

1. Select a challenge link from the index or category sections above.
2. Read the scenario requirements and target binary specifications on [Learn SecByte](https://learn.secbyte.org/).
3. Deploy binary exploitation frameworks (GDB-GEF/pwndbg, Pwntools, ROPgadget, Ropper, x64dbg) inside an isolated Linux/Windows research VM.
4. Craft information leak chains, compute libc base addresses, build ROP/pivoting payloads, overwrite control structures, and retrieve target flags.

---

## Disclaimer

This repository and its linked resources are strictly designed for educational, threat research, and authorized technical security training purposes. Never test, deploy, or execute binary exploitation payloads against production environments, unauthorized applications, or unapproved systems.
