# Hardware implementation of the McCulloch-Pitts Neuron model
# Analog Implementation of McCulloch & Pitts Neuron Using Op-Amps
## Project Overview
This project explores how analog circuits can mimic the behavior of a simplified biological neuron, based on the 1943 McCulloch & Pitts model. By using op-amps in summing and comparator configurations, we implement a threshold logic unit (TLU) that fires when the weighted sum of inputs exceeds a defined threshold. This behavior is visualized using an LED and verified through simulation and real-world testing.
The circuit demonstrates how logic operations (AND, OR) can be realized with resistive weighting and op-amp thresholding—offering a hardware perspective on neuron-like decision-making.

## Problem Statement
Biological neurons make binary decisions by firing when their inputs cross a threshold. Inspired by this, our project uses simple analog components to simulate such behavior. It connects neuroscience-inspired logic with real-world op-amp circuits, showcasing how analog electronics can emulate threshold-based decision-making.

## Objectives
1. Design and build an analog circuit that behaves like a binary threshold neuron.
2. Demonstrate logic gates (AND, OR) by tuning weights and threshold voltages.
3. Extend the design toward multi-neuron setups to emulate basic neural networks.
4. Analyze circuit response through both simulation and hardware validation.

## System Architecture
### Signal Flow:
* Inputs are applied as binary voltages (0V or 5V).
* A summing amplifier computes the weighted sum.
* A comparator checks the sum against a threshold (Vref).
* If the sum exceeds the threshold, the neuron “fires”, lighting an LED.

## Block Diagram
(Schematic or block image goes here, e.g. input → summing amp → comparator → LED)

## List of Materials
| Component           | Quantity | Role                                  |
| ------------------- | -------- | ------------------------------------- |
| LM324 Op-Amp        | 1        | Summing amplifier and comparator      |
| Resistors (1k–100k) | 6+       | Weighting inputs and setting feedback |
| Potentiometer       | 1        | Adjust Vref (threshold)               |
| LED + 330Ω          | 1        | Output indication (neuron firing)     |
| Breadboard          | 1        | Prototyping                           |
| Jumper Wires        | -        | Circuit connections                   |
| 5V Power Supply     | 1        | Power source for op-amp and LED       |


## Tools & Technologies
* Hardware: LM324 op-amp, resistors, potentiometer, LED
* Simulation: LTSpice / Multisim
* PCB Design: KiCAD

## Working Principle
The circuit mimics a McCulloch-Pitts neuron by:
* Adding input voltages using a summing amplifier
* Comparing the summed result to a reference using a comparator
* Lighting the LED only when the threshold is crossed
This models the basic “fire if input sum ≥ threshold” behavior of neurons.

## Simulation & Testing
* LTSpice simulations validate expected behavior: comparator output switches high when sum > Vref.
* On hardware, input combinations like (5V, 5V) vs (5V, 0V) are tested.
* Oscilloscope used to visualize transitions and validate threshold detection.

## Results
* The LED turns on only when the combined input signal crosses the comparator’s threshold.
* Successfully replicates AND and OR logic gates using analog components.
* Validates that simple op-amp circuits can mimic neuron-like decisions.

## Challenges & Learnings
* Selecting appropriate resistors to match input weights and Vref range.
* Dealing with offset voltage and noise in comparator stage.
* Gained insight into how analog systems can implement threshold logic without digital components.

## Future Scope
* Extend to multi-layer threshold logic circuits to simulate neural networks.
* Use microcontrollers (e.g., Arduino) to dynamically change weights via digital potentiometers.
* Explore learning mechanisms (e.g., resistor switching, memristors) for analog adaptation.
