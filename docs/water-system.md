# Water Infrastructure & Filtration Architecture

This runbook outlines the custom whole-house treatment deployment, hard-water isolation modifications, and sub-sink reverse osmosis purification configurations.

## System Topology

```mermaid
graph TD 
    Main[Water Main Entry] --> TieIn{Hard Water Split} 

    TieIn -->|Raw Unfiltered| Trunk[3/4 inch Hard Water Trunk] 
    Trunk --> Spigot1[East Spigot] 
    Trunk --> Spigot2[West Spigot] 

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
    dateFormat YYYY-MM-DD-HH:mm
    axisFormat %H:%M

    section Phase 1: Prep
    Map and Label Spigot Lines       :active, p1, 2026-06-19-07:00, 2026-06-19-09:00
    Mount Softener and Pre-filter     :p2, 2026-06-19-09:00, 2026-06-19-12:00

    section Phase 2: Spigots
    Main Water Shutoff and Drain      :crit, p3, 2026-06-19-12:00, 2026-06-19-13:00
    Run 3-4 inch Hard Water Trunk     :p4, 2026-06-19-13:00, 2026-06-19-16:00
    Cut Cap and Tie-in Spigots        :crit, p5, 2026-06-19-16:00, 2026-06-19-19:00

    section Phase 3: Softener
    Plumb Softener Loop and Bypass    :crit, p6, 2026-06-19-19:00, 2026-06-19-23:00
    Connect Drain Line                :p7, 2026-06-19-23:00, 2026-06-20-01:00
    Slow Fill and Leak Check          :p8, 2026-06-20-01:00, 2026-06-20-02:00

    section Phase 4: RO Unit
    Mount Filters and Holding Tank    :p9, 2026-06-20-02:00, 2026-06-20-04:00
    Plumb Feed and Dedicated Faucet   :p10, 2026-06-20-04:00, 2026-06-20-06:00
```

## Bill of Materials (BOM) & Costs
| Component | Target Model | Estimated Cost | Role |
| :--- | :--- | :--- | :--- |
| **Water Softener** | Aquasure Harmony (32k Grains) | '$420.00' | Whole house softening |
| **RO System** | iSpring RCC7AK (6-Stage) | '$220.00' | Fluoride & contaminant removal |
| **Pre-Filter** | 20-Micron Spun Sediment | '$25.00' | Valving protection |
| **PEX-B Supplies** | 3/4" & 1/2" Coils + Crimp Rings | '$50.00' | Hard water trunk construction |
| **Tools & Valves** | PEX Crimp Tool + Ball Valves | '$85.00' | Isolation and installation |

## Critical Runbooks

### Emergency Softener Bypass Procedure

If the softener leaks or undergoes mechanical valve failure:
1. Locate the black bypass valve assembly on the rear of the Aquasure control head.
1. Turn both red dial arrows so they point inward toward each other (perpendicular to the pipes).
1. The house is now running completely on unsoftened raw municipal water; the unit is safely isolated.

