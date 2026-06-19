# Water Infrastructure & Filtration Architecture

This runbook outlines the custom whole-house treatment deployment, hard-water isolation modifications, and sub-sink reverse osmosis purification configurations.

## System Topology

```mermaid
graph TD
    Main[Water Main Entry] --> TieIn{Hard Water Split}
    
    %% Hard Water Bypass Loop
    TieIn -->|Raw Unfiltered| Trunk[3/4" Hard Water Trunk]
    Trunk --> Spigot1[North Spigot]
    Trunk --> Spigot2[South Spigot]
    
    %% Soft Water Loop
    TieIn -->|Raw Domestic| PreFilter[20-Micron Sediment Filter]
    PreFilter --> Softener[Aquasure Harmony Softener]
    Softener --> HouseTaps[Whole House Soft Supply]
    HouseTaps --> KitchenSink[Kitchen Cold Feed]
    KitchenSink --> RO[6-Stage Under-Sink RO System]
    RO --> DedicatedTap[Pure Drinking Faucet]
```

## Installation & Remediation Timeline
The baseline timeline for executing the plumbing modifications and system deployment involves a targeted 12-hour main water line shutdown window.

```mermaid
gantt
    title System Installation Schedule
    dateFormat  YYYY-MM-DD
    axisFormat  %a Day %H

    section Phase 1: Prep
    Map & Label Spigot Lines       :active, p1_1, 2026-06-19, 2h
    Mount Softener & Pre-filter     : p1_3, after p1_1, 3h

    section Phase 2: Spigots
    Main Water Shutoff & Drain      :critical, p2_1, after p1_3, 1h
    Run 3/4" Hard Water Trunk       : p2_2, after p2_1, 3h
    Cut, Cap & Tie-in Spigots      :critical, p2_3, after p2_2, 3h

    section Phase 3: Softener
    Plumb Softener Loop & Bypass    :critical, p3_1, after p2_3, 4h
    Connect Drain Line              : p3_2, after p3_1, 2h
    Slow Fill & Leak Check          : p3_3, after p3_2, 1h

    section Phase 4: RO Unit
    Mount Filters & Holding Tank    : p4_1, after p3_3, 2h
    Plumb Feed & Dedicated Faucet   : p4_3, after p4_1, 2h
```

## Bill of Materials (BOM) & Costs
| Component | Target Model | Estimated Cost | Role |
| :--- | :--- | :--- | :--- |
| **Water Softener** | Aquasure Harmony (32k Grains) | \$420.00 | Whole house softening |
| **RO System** | iSpring RCC7AK (6-Stage) | \$220.00 | Fluoride & contaminant removal |
| **Pre-Filter** | 20-Micron Spun Sediment | \$25.00 | Valving protection |
| **PEX-B Supplies** | 3/4" & 1/2" Coils + Crimp Rings | \$50.00 | Hard water trunk construction |
| **Tools & Valves** | PEX Crimp Tool + Ball Valves | \$85.00 | Isolation and installation |

## Critical Runbooks
Emergency Softener Bypass Procedure
If the softener leaks or undergoes mechanical valve failure:
1. Locate the black bypass valve assembly on the rear of the Aquasure control head.
1. Turn both red dial arrows so they point inward toward each other (perpendicular to the pipes).
1. The house is now running completely on unsoftened raw municipal water; the unit is safely isolated.

