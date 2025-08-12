# Sights from the Wired – Real-Time Network Traffic Social Simulation

Note: Source code is included in Releases tab not within the repo.

> A zero-player Unreal Engine simulation that transforms real-time network traffic into an emergent social ecosystem, where each IP address becomes an autonomous agent navigating a retro cyberdimension.

**Full project write-up:** [Read on my portfolio](https://samirsfolder.com)  
**Demo video:** Working on it !

|  |  |
|--|--|
| <img src="https://github.com/user-attachments/assets/b0aa9ee2-346b-43d0-b2d0-9614855bb108" width="500px"/> | <img src="https://github.com/user-attachments/assets/1f7de6f3-2fee-42ca-84c1-5a6a84f0f5f5" width="500px"/> |
| <img src="https://github.com/user-attachments/assets/a5c0a0b3-75a7-4dab-a0cb-1767f9242968" width="500px"/> | <img src="https://github.com/user-attachments/assets/a3e7f18d-cf52-445f-96e3-66a07105126e" width="500px"/> |

---

## Overview
Sights from the Wired captures live Wi-Fi network packets using **tshark** and streams them to **Unreal Engine** via the **Remote Control API**. Each unique IP address detected spawns an autonomous agent with procedural personality traits, which interact based on both packet-level events and proximity-based social behavior.

The simulation is inspired by *Serial Experiments Lain*, reimagining networked devices as sentient entities that experience narrative arcs, crises of faith, and ideological shifts based on the protocols and failures they encounter. Agent attributes such as faith, trust, and influence are updated using weighted-average rules loosely based on **DeGroot** and **Deffuant** opinion dynamics models.

---

## Features
- **Live Packet Capture:** Real-time data from tshark to UE over HTTP.
- **Agent Spawning:** Each unique IP spawns an Unreal Engine AI controller.
- **Personality System:** Dynamic traits updated from protocol-specific interactions.
- **Autonomous Movement & Socialization:** NavMesh-driven wandering and interactions between idle agents.
- **Retro Aesthetic:** Custom post-process shader for PS1-style pixelation, vertex jitter, and color quantization.
- **Emergent Narrative Potential:** Narrative arcs evolve from network conditions and agent interactions.

---

## Tech Stack
- **Engine:** Unreal Engine (C++ + Blueprints)
- **Networking:** tshark (via Wireshark CLI), bash scripting, Unreal Remote Control API
- **Programming Languages:** C++, Bash
- **AI & Navigation:** UE AI Controllers, Nav Mesh volumes
- **Shaders:** Custom material functions for pixelation, color quantization, vertex jitter
- **OS Compatibility:** Developed on macOS; Unreal Engine 4.27

---

## How to Run

1. **Download**
   - From the [Releases](https://github.com/YOUR_USERNAME/sights-from-the-wired/releases) page, download:
     - `PacketStream.zip`
     - `send_packets.sh`

2. **Set up Unreal Project**
   - Unzip `PacketStream.zip` into your Unreal Projects directory (e.g., `Documents/Unreal Projects`).
   - Open the `.uproject` file in Unreal Engine.
   - **Mac users:** If blocked, go to **System Settings > Privacy & Security** and click **Allow/Open Anyway**.

3. **Install Prerequisites**
   - Install [Wireshark](https://www.wireshark.org/) (includes tshark).

4. **Run Packet Script**
   ```bash
   chmod +x send_packets.sh
   cd /path/to/script
   ./send_packets.sh
   ```
   - This streams live packet data into Unreal Engine.

> **Note:** Blueprints for agent definitions are in `Content/Cube`.  
> C++ scripts are in `C++ Classes/PacketStream/Public`.

---

## Authors
- **Samir Rajesh** – Networking pipeline, C++ agent logic, shader programming
- **Portia Summers** – Environment/world design, narrative structure
