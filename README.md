# The B.A.S.I.S. Project (Beta-Flux Sequencer)

**B**eta-**A**ctuated **S**tepping **I**ntegrated **S**equencer. 
*A semiconductor-free analog computer architecture for extreme environments.*

## 1. What is this?
The B.A.S.I.S. is a proposed analog computer that uses radioactive beta particles (Ni-63) to perform computation. It contains **no semiconductors** (no transistors, no microchips, no software) in its decision-making path. 

It is designed for environments where modern electronics fail instantly: high-radiation zones, nuclear bunkers, or deep space. It trades the speed and programmability of silicon for absolute survivability.

## 2. Core Architecture (v0.2.1)
The machine uses a purely mechanical **stepping rotor** design.
*   **The Source:** A single Ni-63 beta source is mounted on a central rotating arm.
*   **The Gate:** As the rotor steps between discrete positions, it physically aims the source at one of four fixed lanes (or points it at a solid "park" position to block the beam).
*   **The Compute:** The particles charge a capacitor. When the voltage hits a set threshold, a mechanical comparator (a pull-in switch) physically snaps closed.
*   **The Reset:** A mechanical run-lever engages the rotor. Releasing the lever drops a spring-loaded shorting bar, instantly discharging all capacitors.

## 3. Operating Principle: "Threshold Defines the Value"
Unlike a digital computer that counts in binary, this machine integrates physical charge. The time it takes to reach the threshold depends on the source's decay rate, but **the final number is always defined by the threshold voltage**. As the Ni-63 decays over 100 years, the machine takes longer to compute, but it never produces the wrong answer.

## 4. Fail-Safe by Design
If the machine is hit by an EMP, a physical shock, or the operator releases the run-lever, the spring-loaded shorting bars instantly drop. This grounds the capacitors and returns the machine to a zeroed state. There is no software to corrupt, and no volatile memory to lose.

## 5. Relationship to Prior Art
Extensive research has been conducted on radiation-hardened MEMS logic gates and radioisotope-driven cantilevers (e.g., Purdue University, Li et al. 2002). The B.A.S.I.S. does not reinvent these switches. It proposes a **novel system-level architecture**—using a stepping rotor to sequence multiple lanes into a programmable control computer. The contribution is the *arrangement*, not the underlying physics.
