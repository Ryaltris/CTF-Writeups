# AV Evasion: Shellcode — TryHackMe

**Platform:** TryHackMe  
**Difficulty:** Medium  
**Category:** Malware Analysis / AV Evasion  
**Date Completed:** April 2026  

---

## Overview

Explore how to build and deliver payloads, focusing on avoiding detection by common AV engines. And also look at different techniques available to attackers and discuss the pros and cons of every one of them.

---

## What is AV Evasion?

Antivirus evasion is the ability for either your program or malicious code to be delivered or run and it not get flagged by the AntiVirus on the hosts computer.

---

## Task 2

In this challenge a Windows machine is prepared for us to be able to upload out payloads into and then checked by the AV on the machine. The main goal of this challenge is to evade the AntiVirus software installed on the machine and capture the flag on the system.

## Task 3

This challenge highlights high level essential elements of PE (Portable Executable) data structure for Windows Binaries. Windows Executable file format, aka PE, is a data structure that holds informaition necessary for files. Its also a way to organise executable file code on a disk. Operating systen components, such as Widnows and DOS loaders, can load it into memory and execute it based on the parsed file infomation found in the PE.

Default file structure of Windows binaries, such as EXE, DLL, and Object code fiels, has the same PE strructure and works in the Windows operatin system for both x86 and x64 CPU architecture. 

A PE structure contains sections that hold information about the binary, such as metadata and links to a memory address of external libraries. One of these sections is the PE Header, which contains metadata information, pointers, and links to address sections in memory. Another section is the Data section, which includes containers that include the information required for the Windows loader to run a program, such as the executable code, resources, links to libraries, data variables, etc. 

<img width="762" height="555" alt="image" src="https://github.com/user-attachments/assets/c8bbb24a-f54a-493d-9d59-6f04d3ec95db" />

There are different types of data containers in the PE structure, each holding different data.

    .text stores the actual code of the program
    .data holds the initialized and defined variables
    .bss holds the uninitialized data (declared variables with no assigned values)
    .rdata contains the read-only data
    .edata: contains exportable objects and related table information
    .idata imported objects and related table information
    .reloc image relocation information
    .rsrc links external resources used by the program such as images, icons, embedded binaries, and manifest file, which has all information about program versions, authors, company, and copyright!

## Why do we need to know about PE?

AV software and malware analysts analyze EXE files based on the infomation in the PE Headerr and other PE sections. So to be able to crreate or modify malware with AV evasion capability targeting a windows machine, we need to be able to understand the structure of Windows PE files and where the malicious shellcode can be stored. 

We can control in which Data section to store our shellcode by how we define and initialise the shellcode variable. Some examples would be defining the shellcode as a local variable within the main function will store it in the .TEXT PE section

### 1. Shellcode Encoding

```bash
# commands you ran here
```

What the output showed and what it means.

### 2. Shellcode Packing
What packing does to an executable, how it changes the file signature,
and why AV struggles to detect packed payloads.
```bash
# commands you ran here
```

### 3. Binders
What binders are, how they work, and in what real-world scenarios 
an attacker would use one.
```bash
# commands you ran here
```

### 4. Crypters
How crypters differ from encoders and packers, and why they are 
considered the most effective evasion technique of the three.
```bash
# commands you ran here
```

---

## How AV Detection Works (and Why These Techniques Beat It)

This is the most important section. Explain:
- Signature-based detection and why encoding/packing defeats it
- Heuristic detection and how crypters can evade it
- What this means from a defender's perspective — how would you 
  detect these techniques if you were on the blue team?

---

## Real World Relevance

How do these techniques map to real malware families you have read 
about or analysed? Reference MITRE ATT&CK if relevant 
(e.g. T1027 - Obfuscated Files or Information).

---

## Key Takeaway

1-2 sentences on the most important thing you learned from this room 
and how it connects to your broader interest in malware analysis.

---

## References

- [MITRE ATT&CK T1027 - Obfuscated Files or Information](https://attack.mitre.org/techniques/T1027/)
- [TryHackMe AV Evasion: Shellcode Room](https://tryhackme.com/room/avevasionshellcode)
