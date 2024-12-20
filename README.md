# Modeling-and-Design

 Gishushu Traffic Light System Specification
 -------------------------------------------
1. Normal Operation Cycle
-------------------------
North-South Green: 45 seconds. During this phase, vehicles traveling in the North-South direction have a green light, and all East-West lanes remain stopped (red light). This ensures smooth traffic flow for North-South vehicles.
North-South Yellow: 5 seconds. The yellow light signals to North-South vehicles that the green light is ending, allowing drivers to prepare to stop. East-West lanes remain red to clear the intersection.
North-South Red (Transition Delay): 2 seconds. All directions hold a red light briefly to allow the intersection to clear, preventing any overlap of moving vehicles from different directions.
East-West Green: 45 seconds. During this phase, East-West traffic has a green light, and North-South lanes are stopped (red light), allowing East-West vehicles to pass safely.
East-West Yellow: 5 seconds. The yellow light signals to East-West vehicles that the green light is ending. This phase allows vehicles to prepare to stop, while North-South lanes remain red.
East-West Red (Transition Delay): 2 seconds. All directions hold a red light for a brief period, ensuring that all vehicles have stopped before moving to the next phase.
Pedestrian Crossing (if active): 20 seconds (adjustable). During this phase, all traffic is stopped (red lights for all directions), allowing pedestrians to cross safely. Pedestrian walk signals are activated.

2. Pedestrian Crossing
----------------------
State: When a pedestrian crossing request is made, the system switches to a phase where all vehicle directions are red, and the pedestrian walk light is on. This ensures the safety of pedestrians while they cross.
Duration: Typically 20 seconds (this can be adjusted based on pedestrian volume and intersection size).
Transition: After the pedestrian timer expires, vehicle lights return to NorthSouth_Green or EastWest_Green based on the cycle.

3. Emergency Mode
-----------------
State: When an emergency signal is received (from emergency vehicles like ambulances or fire trucks), all traffic lights flash red. This gives priority to emergency vehicles, allowing them to pass through the intersection without delay.
Condition: The emergency mode is triggered when a signal is received from emergency services (via sensors or manual override).
Transition: After the emergency is cleared, the system will resume normal operation starting from the NorthSouth_Green phase to continue the traffic cycle.

4. Cycle Flow
-------------
The system follows a continuous, repeating sequence to regulate traffic safely:
NorthSouth_Green → NorthSouth_Yellow → NorthSouth_Red → EastWest_Green → EastWest_Yellow → EastWest_Red → Pedestrian_Crossing (if active).
