# Week 5 Task – OpenROAD Flow Setup and Floorplan + Placement

## Objective
To set up the **OpenROAD Flow Scripts** environment and execute the **Floorplan** and **Placement** stages of the physical design flow.  
This task transitions from SPICE-level transistor design (Week 4) to backend implementation, where logic is transformed into an actual physical layout.

## Why This Task Is Important
After understanding timing at the transistor level, it’s essential to see how those circuits are physically realized on silicon.  
This task introduces **OpenROAD**, an open-source **RTL-to-GDSII** flow widely used in both academic and industrial VLSI design research.

Learning to perform floorplanning and placement provides insight into:
- How design constraints are applied before routing.
- How standard cells are arranged to minimize delay, area, and congestion.
- How physical design choices affect timing, area, and manufacturability.

---

## Summary
The **OpenROAD Flow** was successfully installed, verified, and executed.  
The snapshots below confirm successful installation and completion of the **Floorplan** and **Placement** stages.

### Installation Verification
![yosys_Installed](/week_5/Deliverables_Images/yosys_Installed.png)  
![OpenRoad_Installed](/week_5/Deliverables_Images/OpenRoad_Installed.png)

### Floorplan and Placement Outputs
- **Floorplan View & Placement Layout (Standard Cells Visible)**  
  ![Task5_GDSII](/week_5/Deliverables_Images/Task5_GDSII.png)  
- **Floorplan and Placement Log**  
  ![Report_Floorplan_Placement](/week_5/Deliverables_Images/Report_Floorplan_Placement.png)

---

## Challenges Faced
Initially, OpenROAD could not be set up on my **local system** — the `./setup.sh` script would repeatedly freeze midway.  
To resolve this, I opted for the **Docker-based installation**, which executed successfully and provided a stable environment for flow execution.

---

## Deliverables
1. **Installation Proof**
   - Verified installation of `yosys` and `openroad`.
   - Screenshots confirming setup success.

2. **Execution Proof**
   - Successfully generated Floorplan and Placement layouts.

3. **Logs and Visual Evidence**
   - Screenshots of flow completion and placement view.
   - Logs confirming execution up to placement stage.

---

## References
- [OpenROAD Official Documentation – Build with Docker](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts/blob/master/docs/user/BuildWithDocker.md)  
- [Reference Repository – spatha_vsd-hdp (Day 14)](https://github.com/spatha0011/spatha_vsd-hdp/blob/main/Day14/README.md)

---

## Outcome
By completing this task, I successfully:
- Installed and configured the **OpenROAD Flow Scripts** using Docker.  
- Executed and verified the **Floorplan** and **Placement** stages of the physical design flow.  
- Produced clear visual and logged evidence of a working OpenROAD setup.  

This marks the first successful step toward a **complete physical implementation flow** in **VLSI design**, bridging the gap between logic-level and layout-level understanding.


---

## Commands Executed

```bash
# 1. Clone the repository
git clone --recursive https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts

# 2. Enter the cloned directory
cd OpenROAD-flow-scripts/

# 3. Build OpenROAD (2 threads)
./build_openroad.sh -t 2

# 4. Enable X11 display access for Docker
xhost +local:docker

# 5. Create and run the OpenROAD Docker container with GUI support
docker run -it --name OpenRoad_Docker_Complete \
    -v $(pwd)/:/workspace \
    -e DISPLAY=$DISPLAY \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -v ${HOME}/.Xauthority:/.Xauthority \
    --network host \
    --security-opt seccomp=unconfined \
    openroad/flow-ubuntu22.04-builder:ee5a20

# 6. Exit from container after initial setup
exit

# 7. Start the container again
docker start OpenRoad_Docker_Complete

# 8. Re-enter the container
docker exec -it OpenRoad_Docker_Complete /bin/bash

# 9. Source environment
source ./env.sh

# 10–12. Verify installations
yosys -help
yosys -m slang -p "slang_version"
openroad -help

# 13. Move to flow directory
cd flow

# 14. Run the flow
make

# 15. Launch GUI to view floorplan and placement
make gui_final


