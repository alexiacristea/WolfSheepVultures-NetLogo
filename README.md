WolfSheepVultures-NetLogo

An agent-based simulation of an ecosystem with sheep, wolves, vultures and grass, built in NetLogo.

The project started as an assignment for the Fundamentals of Economic Cybernetics course at the Bucharest University of Economic Studies (ASE, CSIE). It extends the classic Wolf Sheep Predation model with a third predator, a disease affecting wolves and a seasonal cycle, and was later debugged and calibrated so that all species can coexist.

Simulation

Key Functionality
Simulate four interacting populations: sheep, wolves, vultures and grass
Choose between three model versions:
sheep-wolves – predators and prey only
sheep-wolves-grass – sheep depend on grass that regrows over time
sheep-wolves-vultures – the extended ecosystem
Model a disease that stops sick wolves from hunting and reproducing (shown in red)
Introduce vultures that prey only on sick or weakened wolves
Alternate summer and winter every 100 ticks, with slower grass regrowth in winter
Track populations, sick wolves and the current season through live plots and monitors
Adjust every parameter from the interface without changing the code
Built With
NetLogo 7 (agent-based modeling language)
Agent breeds, agent and patch variables, reporters and procedures
Interface widgets: sliders, chooser, plots and monitors
Repository Layout
text
.
├── WolfSheepVultures.nlogox     # NetLogo model (code, interface and documentation)
├── docs/
│   ├── simulation.gif           # Recording of the simulation
│   └── Documentatie_BCE.pdf     # Original project documentation (Romanian)
└── README.md
Getting Started
Install NetLogo 7 (free, available for Windows, macOS and Linux).
Open WolfSheepVultures.nlogox.
Select sheep-wolves-vultures in model-version.
Press setup, then go.

The default slider values are calibrated so that all species coexist over long runs.

Model Rules
Sheep move randomly, lose energy at every step and regain it by eating green grass
Eaten grass turns brown and regrows after grass-regrowth-time ticks; winter slows regrowth
Healthy wolves hunt sheep; each healthy wolf can become sick with probability sickness-chance per tick
Sick wolves cannot hunt or reproduce and lose energy faster
Vultures lose little energy, behave like scavengers and attack sick or weak wolves with a 60% success rate
Every agent reproduces with a configurable probability and dies when its energy reaches zero
Improvements Over the Original Coursework

The documentation in docs/ reflects the original submission. The model was improved afterwards:

Fixed the sheep-wolves-grass version, which did not model grass and stopped with a runtime error
Fixed grass regrowth so that only eaten grass regrows, making the winter effect consistent
Made the simulation start in summer instead of switching to winter at tick 0
Limited the disease to healthy wolves and prevented sick wolves from reproducing
Recalibrated disease, winter and vulture parameters so that all four populations persist
Fixed the vulture monitor, which displayed the agent set instead of the count
Skills Demonstrated
Agent-based modeling and simulation of complex systems
Debugging emergent behavior and tracing it back to specific rules
Calibrating model parameters to obtain a stable equilibrium
Designing an interactive interface for running experiments
Credits and License

This model is based on Wolf Sheep Predation by Uri Wilensky (1997), Center for Connected Learning and Computer-Based Modeling, Northwestern University. The original model is licensed under CC BY-NC-SA 3.0; this derivative work is shared under the same license.