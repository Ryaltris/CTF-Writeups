# AV Evasion: Shellcode — TryHackMe

**Platform:** TryHackMe  
**Difficulty:** Medium  
**Category:** Malware Analysis / AV Evasion  
**Date Completed:** April 2026  

---

## Overview

Brief 2-3 sentence summary of what the room covered and what the learning objective was.

---

## What is AV Evasion?

Explain in your own words what antivirus evasion is, why attackers need it, 
and what the room set out to teach. 2-3 sentences is fine.

---

## Techniques Covered

### 1. Shellcode Encoding
What encoding is, how it works, and why it bypasses signature-based AV detection.
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
