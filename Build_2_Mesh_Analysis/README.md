## Mesh Analysis Verification - Two-Mesh Resistor Circuit
## Objective

Comparing theoretical mesh analysis calculations with real circuit measurements from a multimeter, to see if mesh analysis actually holds up in practice.

## Parts List
5V DC power supply
100Ω resistor (1/2W)
220Ω resistor (1/2W)
330Ω resistor (1/2W)
470Ω resistor x2 (1/2W)
Breadboard
Jumper wires
Fluke 15B+ Digital Multimeter
## Procedure

I designed a two-mesh circuit using resistor values I actually had in my kit (100Ω, 220Ω, 330Ω, and two 470Ω). Before building anything, I checked the power dissipation for each resistor to make sure everything stayed safely under the 1/2W rating.

Next, I set up KVL equations for Mesh a and Mesh b based on the circuit layout and solved for the two mesh currents. Then I built the circuit on a breadboard, with node A and node B the two junctions where the mesh currents split and combine.

Once it was built, I measured voltage across each resistor with the multimeter and used Ohm's Law (I = V/R) to calculate the current through each one.

## Circuit Diagram

(See attached photo of hand-drawn circuit diagram, labeled with node A, node B, Mesh a, Mesh b, and all resistor values)

## Mesh Equations

Mesh a: 790Ω·I_a - 470Ω·I_b = 5V

Mesh b: -470Ω·I_a + 1270Ω·I_b = 0V

## Solving the system:

I_a = 8.1 mA I_b = 3.0 mA

The shared 470Ω resistor carries the difference between the two mesh currents, since I_a and I_b flow through it in opposite directions:

I_R4(shared) = I_a - I_b = 8.1 mA - 3.0 mA = 5.1 mA

## Current Calculations

Using I = V/R with the measured voltage across each resistor:

I_100Ω = 0.808V / 100Ω = 8.08 mA 
I_220Ω = 1.78V / 220Ω = 8.09 mA 
I_330Ω = 0.99V / 330Ω = 3.00 mA 
I_470Ω(mesh b) = 1.41V / 470Ω = 3.00 mA 
I_470Ω(shared) = 2.39V / 470Ω = 5.09 mA

## Results
|Resistor|Theoretical Voltage|Measured Voltage|Theoretical Current|	Measured Current|	% Error|
|--------|-------------------|----------------|-------------------|-----------------|--------|
|100Ω (Mesh a)|	0.81 V|	0.808 V|	8.1 mA|	8.08 mA|	0.25%|
|220Ω (Mesh a)|	1.78 V|	1.78 V|	8.1 mA|	8.09 mA|	0.11%|
|330Ω (Mesh b)|	0.99 V|	0.99 V|	3.0 mA|	3.00 mA|	0.00%|
|470Ω (Mesh b only)|	1.41 V|	1.41 V|	3.0 mA|	3.00 mA|	0.00%|
|470Ω (Shared, R4)|	2.40 V|	2.39 V|	5.1 mA|	5.09 mA|	0.29%|
## Conclusion

Mesh analysis is a solid way to break down a complicated circuit using KVL and get accurate current readings without touching a single component. Every measured voltage came in close to what I calculated, with the worst error under 0.3%. Proving that mesh analysis is a viable method to get accurate circuit  values.
