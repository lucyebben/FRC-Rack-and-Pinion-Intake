# FRC-Rack-and-Pinion-Intake
*Robot intake mechanism for "Rebuilt", the 2026 FIRST Robotics Competition season*

[View Onshape CAD](https://cad.onshape.com/documents/a036a6573e37a133ac6f1799/w/2494c921d1af4438c1d661c5/e/08d2872df777d5daded781c5)
![CAD screenshot](/assets/images/CAD_5.png)


### Overview
For the first half of the season, my team had been using a 4-bar, pneumatically actuated intake (which I built in collaboration with my teammate Ruemu Otoba). But as software improved, the design's fundamental weaknesses began to bottleneck our match performance. This document details my redesign solution.

### Problem statement
Our original 4-bar pneumatic intake exhibited critical weaknesses that severely limited our match performance:

- **Inability to retract:** fixed maximum robot hitbox and moment of inertia, reducing maneuverability and making defensive collisions riskier 
- **Unreliable indexing:** any game pieces stuck in dead space behind rollers wouldn’t get indexed due to lack of agitation capability (no “chewing”)
- **Low throughput:** driven by a single x44, its three rollers were low surface speed and prone to jamming under load. Our chosen pneumatic pistons were unable to retract the weight of a beefier or additional motor
- **Structural vulnerability:** pneumatic pistons were susceptible to bending under lateral impact (sideswipes)
- **Limited reach:** the large side plates (required as bumper hard-stops) obstructed roller access to field corners
- **Poor compatibility with net hopper:** the 4-bar retraction resulted in tangling with our net hopper 

### Redesign constraints
- **Retrofit:** must integrate seamlessly with existing chassis as of Week 4 of competition season
- **Weight:** total assembly ≤12 lbs. This was really hard
- **No second chances:** zero time for prototyping. Must one-shot first design and ship

### Design solution and architecture:
- Curved MaxComposite 10DP gear racks, 1/8th inch aluminum frame
- Deployment powertrain: dual Kraken X44s, 8.8:1 reduction. Deploys or retracts in just in 0.5 seconds at 50% speed (~4000 rpm)
- Roller powertrain: two VersaRollers driven by single Kraken X60, 1.83:1 reduction

### Results and performance
- Robust to high-speed impact and sideswipes
- Improved game piece acquisition
    - High throughput while driving at full speed
    - Touch it, own it
    - Significantly less stalling and jamming
    - Improved corner reach
    - Improved indexing efficiency through “chewing” (repeated retraction and deployment)
- Improved form factor
    - Increased robot agility
    - Smaller footprint
   - Better defensive capability
- Easy repairability
   - Entire assembly can be installed/removed with just 4 bolts
   - Identical rollers (as opposed to using different pulley configurations)
   - Powertrain modules can be swapped independently of the rest of the assembly
- First pass success
   - Met strict weight requirement
   - Successfully retrofit onto robot
   - Compatible with net hopper without tangling
   - First prototype worked as intended

