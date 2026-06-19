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
