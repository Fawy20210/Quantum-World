# Quantum World
A particle simulation, which tries to imitate real quarks, the things atoms are made of.

![alt Text](README-Assets/QuantumWorld-Preview.gif)
[***TRY IT OUT***](https://fawy2020.itch.io/quantum-world)

## How it works
Each particle is either an UP or DOWN quark, with the UP quarks being 2/3 positively and the DOWN quarks 1/3 negatively charged. Quarks of the same charge get repelled and those of different charge get attracted, with Up quarks pulling harder on DOWN quarks than DOWN quarks repell other DOWN quarks. For performance reasons theres a max interaction distance, past which particles ignore each other, but you can adjust it.

## Quick Start
### Windows
**Download**
- [Download on itch.io](https://fawy2020.itch.io/quantum-world)  
- [Download from Github (latest release)](https://github.com/Fawy20210/Quantum-World)

**Launch**
1. Unzip the downloaded file.
2. Open the unziped folder.
3. Execute `Quantum World.exe`


### Linux
***Linux files are provided for download, but are not tested, so they might not work or have issues.***  
***The following instructions may not be accurate, but I assume they should be.***

**Download**
- [Download from Github (latest release)](https://github.com/Fawy20210/Quantum-World/releases/latest/download/ParticleWorld-linux-1.0.zip)

**Launch**
1. Unzip the downloaded file.
2. Open the unziped folder.
3. Execute `QuantumWorld-Linux-1.0.x86_64`

## Features

- Runs on your GPU using compute shaders.
- Ability to change Simulation, Physics and Rendering Parameters.
- Input validation.
- Pause button to pause the simulation.

## Controls

### 2D
**W**: Move Up  
**A**: Move Left  
**S**: Move Down  
**D**: Move Right  
**Q**: Move Forward (zoom in)  
**E**: Move Backward (zoom out)  
**Scroll**: Adjust camera movement speed

### 3D
**W**: Move Forward  
**A**: Move Left  
**S**: Move Backward  
**D**: Move Right  
**Q**: Move Up  
**E**: Move Down  
**Scroll**: Adjust camera movement speed

## Parameters 

### Simulation Details: 

**Amount of Simulated Particles:** How many particles get simulated.  
**Up/Down Quark ratio:** What the ratio between the UP and DOWN quarks should be.
**Spawn border size:** How big the area the quarks can spawn in should be.

### Physics Details:
<details>
<summary> <b>Time Factor:</b> The size of each time step. </summary>
 Bigger steps -> -Accuracy & +Simulation speed.<br>
 Smaller steps -> +Accuracy & -Simulation speed.
</details>

<b>Particle Size:</b> Sets the size of the quarks used in calculations.

<details>
<summary> <b>Min/Max interaction distance:</b> Sets the interaction range. </summary>
 Min dist: When two quarks are closer than this distance, they won't interact.<br>
 Max dist: When two quarks are further appart than this distance, they won't interact.
</details>

<details>
<summary> <b>Dampening:</b> How much velocity the quarks lose each time step. </summary>
 Smaller value -> -Stability & +Quark speed.<br>
 Bigger value -> +Stability & -Quark speed.
</details> 

**Attraction Strength:** Scales the force that pulls *all* quarks together based on distance, that are within range.  
**Constant Attraction:** The force with which *all* quarks are pulled together constantly.



### Rendering Details:
**Particle Scale:** Scales how big the particles should be rendered.  
<details>
<summary> <b>Colors:</b> </summary>
 <i>Up color</i>: The color of the up quarks.<br>
 <i>Down Color</i>: The color of the down quarks.
</details>

### Control Details:
**Camera Movement Speed Scale:** Multiplier to how fast the camera moves.

## A small insight

<details>
<summary> <b>Why did I choose to run the computations on the GPU?</b> </summary>

I chose to run the computation on the GPU because GPUs are normally really good at doing things in parallel, which is great if you need to compute many things that are pretty much the same, and the CPU would be to slow to do the same.
 
</details>