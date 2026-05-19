# Malware Behavior Comparison
### Remote Access Trojan · Fileless · Living-off-the-Land

Static analysis and behavioral classification of three malware categories using 
Ghidra, MITRE ATT&CK mapping, and IOC extraction.

📄 [Read the Report](./Malware_Analysis_Report.pdf)

## Overview

This project compares how RATs, fileless malware, and living-off-the-land attacks 
differ in execution strategy, evasion technique, and persistence mechanism—and 
what that means for detection.

| Category | Execution | Evasion | Persistence |
|----------|-----------|---------|-------------|
| Remcos RAT | Compiled PE | Dynamic API loading | Registry Run key |
| Fileless | PowerShell IEX | Memory-only | Registry (PS) |
| LotL | Trusted binaries | Signed bins | Scheduled tasks |

## Artifacts

- `report/` → LaTeX source and compiled PDF
- `samples/` → Pseudocode representations of fileless and LotL techniques 
  (commented out to prevent reproducibility)

## Remcos RAT Sample

Obtained from [MalwareBazaar](https://bazaar.abuse.ch/).  
SHA256: `32aa0546c952a980435c113eeb04b6f9a82bf2b260e0b7b261010eaa585d55f1`

> ⚠️ All analysis was conducted in an isolated VM. No live malware is stored in this repository.
