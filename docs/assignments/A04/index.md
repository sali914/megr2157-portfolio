# A4 – Motor Mount

## Objective

The objective of this project is to design, analyze, and model a custom mount for a Brushed 24V DC Planetary Gear Motor that securely attaches to a rigid wall. The mount must safely support a **300 N point load** applied at the motor shaft. It must maintain a **safety factor of 3** against material yield and limit the **maximum deflection at the free end to 0.30 mm**.

<img width="123" height="99" alt="image" src="https://github.com/user-attachments/assets/36d23466-7629-4857-9b5a-348a88533a2f" />

## Feature 1

To design the horizontal arm that holds the motor, I treated it like a cantilever beam with a 300 N weight pushing down on the end. The design had two main rules: it couldn't break or permanently bend, and it couldn't flex downward more than 0.30 mm. For the math, I used the standard properties of ABS plastic: a **yield strength (Sy) of 44 MPa** and a **Young’s Modulus (E) of 2.3 GPa**. Assuming the **arm length (L1) is 40 mm** and the **width (b) is 35 mm**, I first checked the stress. With a **safety factor (Sf) of 3**, the **allowable stress is 14.67 MPa**, which meant the arm needed to be at least **11.84 mm thick (h1)** to keep from breaking. However, plastic is pretty flexible. When I calculated how thick it needed to be to prevent it from bending more than 0.30 mm, that number jumped to 14.71 mm. Since preventing that bending was the stricter rule, I rounded up and made the motor arm 15 mm thick.

The following image shows the process in which I got these values:

<img width="2990" height="1694" alt="Feature_1" src="https://github.com/user-attachments/assets/524dc8b7-c369-4591-87e6-db9a71a39998" />

## Feature 2

Next, I designed the vertical backplate that attaches to the wall. I also treated this like a cantilever beam, but this time bending from the top bolts. The **300 N load (P)** pushing on the horizontal arm acts like a wrench, creating a **bending moment (M1) of 12,000 N*mm** at the corner. Assuming the plate extends **50 mm (L2)** from the corner up to the bolts, this twisting translates to a **240 N pull force (F)** on the plate. Using the same ABS plastic properties and **width (b) of 35 mm**, I calculated the required thickness. To survive the stress without breaking, it needed to be 11.84 mm thick. But again, to stop it from flexing past the 0.30 mm limit, it actually needed to be **17.06 mm thick (h2)**. To make sure it was completely solid against the wall, I rounded this up to 18 mm for the CAD model.

The following image shows the process in which I got these values:

<img width="2990" height="1616" alt="Feature_2" src="https://github.com/user-attachments/assets/4f5ded9f-da93-4328-b417-5ba0c962ca9e" />


## Communicate

