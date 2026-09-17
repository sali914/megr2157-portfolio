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


## Isometric Hand Drawing

Before jumping into the CAD software, I drew a 3D isometric sketch by hand:

<img width="507" height="407" alt="Iso_Hand" src="https://github.com/user-attachments/assets/2b279684-ff31-47ab-9090-c874f64c705c" />

## CAD Model (Parametric)

Right before I built the motor mount in SolidWorks, I set up the global variables in order to make changing dimension at a later time easier.

<img width="2152" height="560" alt="image" src="https://github.com/user-attachments/assets/f671aac7-12e0-4c6d-af8c-70ee5dcab50c" />

I then sketched the basic "L" shape on the Right Plane and extruded it out from the middle. Doing it this way means if I ever need to change the length or material later, I can just change the variables and the whole 3D model updates automatically.

<img width="600" height="800" alt="image" src="https://github.com/user-attachments/assets/947dd3b8-64fd-48b0-89a3-cd38499b4ee0" />

Lastly, I cut out a pocket and a through-hole for the motor shaft, plus four 3.4 mm holes on the backplate for the M3 wall bolts.

<img width="650" height="850" alt="image" src="https://github.com/user-attachments/assets/dc3de99a-b538-493e-8efd-ab5e0e78d5ca" />


## Drawings

Once I finished designing the part, I generated a full multiview engineering drawing from my 3D model. It uses third-angle projection to show the Front, Top, and Right views, plus a shaded 3D isometric view in the corner. I added all the necessary size dimensions and hole callouts so the part could be easily manufactured.

<img width="1100" height="850" alt="image" src="https://github.com/user-attachments/assets/53b67991-ae9a-4422-ac78-c2bae7338afd" />

## Lesson Learned & Time Spent

I learned that when designing with 3D-printed plastics like ABS, you usually do not have to worry about the part snapping, you have to worry about it bending too much. Plastic is not very stiff, so the deflection limit usually dictates how thick the part needs to be. I also saw firsthand how mechanical leverage is tricky. When calculating the wall plate, making the part longer gave it more mechanical leverage to lower the pulling force on the bolts, but it made the plate itself easier to bend, meaning I had to make it thicker to compensate. Finally, I realized that using parametric variables saves a massive amount of time. Drawing the whole side-profile in one sketch and controlling it with variables was way better than stacking a bunch of separate blocks, allowing the model to update automatically if my math changed.

Overall I spent approximately **7 hours** to complete the assignment, from the initial calculations to the final CAD drawings.

## CAD Files

[Motor Mount Pack & Go File](https://drive.google.com/file/d/14jaOXrgmG7dQGNsxFxW4z6iMQIBNkSLW/view?usp=sharing)
