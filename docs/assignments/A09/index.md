# A9 – Pulley System

## Objective

The objective of this assignment was to design a pulley system capable of transferring power between two parallel shafts separated by a center distance of 4 to 6 inches. The system was required to use two 3-inch diameter pulleys, operate between 1000 and 2000 rpm, and maintain an initial belt tension between 4 and 6 lbf. All components needed to satisfy a minimum safety factor of 3.

For my design, I selected ABS for the pulleys, polyurethane rubber for the belt, and 1060 hardened steel for the shafts. I also designed a supporting frame and evaluated journal bearing materials using the Machinery's Handbook.

<img width="295" height="100" alt="image" src="https://github.com/user-attachments/assets/e39193cc-d460-40b6-92fa-ab58c38c7d8c" />


### 1. Belt Design

#### Knowns and Unknowns

I began by identifying the known and unknown variables for the belt system. I selected a center distance of 5 inches, an operating speed of 1500 rpm, and an initial belt tension of 5 lbf. These values fall within the specified design requirements.

#### Free-Body Diagram

I created free-body diagrams to identify the forces acting on the driver and driven pulleys. The belt experiences different tensions on its tight and loose sides when transmitting power.

For my analysis, I used a sign convention where counterclockwise moments are positive and clockwise moments are negative.

<img width="1000" height="450" alt="A9_1" src="https://github.com/user-attachments/assets/73815b56-2075-44ab-89f8-29f8e375daea" />

#### Solving

I began with the relationship between the initial static belt tension and the operating tensions:

T0 = T1 + T2

I then used the belt friction equation at impending slip with an assumed friction coefficient of 0.26  and an angle of pi radians to solve for T2 and T1, which were 3.064 lbf and 6.936 lbf respectfully. After determining these forces, I used the normal stress equation and the required safety factor to calculate the minimum belt cross-sectional area. Since the belt has a circular cross-section, I rearranged the area equation to determine the minimum diameter.

Using the selected operating conditions, I obtained the following preliminary values:

<img width="1250" height="1000" alt="A9_2" src="https://github.com/user-attachments/assets/11801772-f9d7-4e3c-a9d5-498410c17170" />


#### Belt Selection

After completing the calculations, I used McMaster-Carr to find a polyurethane round belt that closely matched my required dimensions.

I initially considered a larger belt diameter for an additional safety margin. However, I decided to use a standard 1/4-inch diameter belt rather than a custom-sized option.

The selected belt was McMaster-Carr Part #3044K606, with a diameter of 0.250 inches and a nominal outer circumference of 20.25 inches.

Using the preliminary calculated tight-side tension, the belt has a tensile safety factor of approximately 3.33. This result depends on the assumed operating tensions, and the installed belt tension would need to be verified.

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/fe9e56e8-2276-4b80-a3a4-2ab497cbf735" />


### 2. Shaft Design

#### Knowns and Unknowns

After completing the belt design, I moved on to calculating the minimum shaft diameter. The shafts were required to be made from 1060 hardened steel.

I used the previously calculated belt tensions to determine the torque transmitted through the system.

<img width="900" height="350" alt="A9_3" src="https://github.com/user-attachments/assets/82b1fe12-6eb7-40ea-8075-f8938aade831" />

#### Free-Body Diagram

I created a free-body diagram to identify the forces and torque acting on the shaft. The belt tensions produce a net torque, while the combined belt forces produce a transverse load on the shaft.

For the preliminary design, I assumed the pulley was centered between two bearing supports.

<img width="1000" height="500" alt="A9_4" src="https://github.com/user-attachments/assets/fd36549b-1ea4-4410-b478-b6df6d5cf5dc" />

####  Solving

I began by calculating the transmitted torque, Mt = 5.808 lbf - in. I then used the torsional shear stress equation for a solid circular shaft. After substituting the geometric relationships for the area of a circular shaft, I solved for an area of 0.01098 in^2. Once the minimum area was determined, I calculated the corresponding shaft diameter of 0.1182. Using a tensile yield strength of 93,000 psi for the selected hardened steel condition, I applied the von Mises criterion and a safety factor of 3.

I then chose to select a more standard 1/8-inch shaft diameter because it exceeded the calculated torsional minimum.

<img width="900" height="500" alt="A9_5" src="https://github.com/user-attachments/assets/bad9912a-8e26-4d08-bd2e-45ea0df74e4c" />

### 3. Journal Bearing Design

#### Knowns and Unknowns

The next portion of the assignment involved selecting a journal bearing capable of supporting the rotating shaft. I used the shaft diameter of 0.125 inches, rotational speed of 1500 rpm, and the bearing reactions determined from the belt forces. I assumed that each shaft was supported by two bearings, with the pulley centered between them. This arrangement distributes the 10 lbf transverse belt load equally, resulting in 5 lbf per bearing.

<img width="1000" height="450" alt="A9_6" src="https://github.com/user-attachments/assets/c4cf5cc5-4ff6-4fae-8330-681779f0ce1b" />

### Free-Body Diagram

I created a free-body diagram showing the pulley load acting on the shaft and the reactions at both journal bearings. With the pulley centered between the supports, the bearing reactions were calculated as RA = RB = 5 lbf

<img width="1200" height="600" alt="A9_7" src="https://github.com/user-attachments/assets/422dea1c-c201-47f0-bf61-c3e075525554" />

### Solving

I began with the projected bearing area, Ap = 0.03125 in^2. The bearing pressure was then calculated using P = Fr / Ap, which was equal to 160 psi. Next, I determined the shaft's linear surface velocity as v = 49.09 ft/min. Finally, I multiplied the bearing pressure by the surface velocity to calculate the PV rating, PV = 7854.4 psi - ft/min.

<img width="1100" height="700" alt="A9_8" src="https://github.com/user-attachments/assets/17447dbb-57e5-43c9-9baa-06007fdf98a3" />

### Material Selection

After calculating the operating pressure, velocity, and PV rating, I compared my results with Table 4, Application Limits: Sintered Metal and Nonmetallic Bearings, from Machinery's Handbook. I selected porous bronze because it satisfied the required operating conditions while maintaining a safety factor greater than 3 for both pressure and PV. The material has a maximum pressure rating of 4,500 psi and a PV limit of 50,000 psi·ft/min. The calculated pressure safety factor was 28.13, while the calculated PV safety factor was 6.37.

Porous bronze also offers self-lubricating properties when properly oil-impregnated, making it suitable for a journal bearing application.

<img width="636" height="465" alt="image" src="https://github.com/user-attachments/assets/23291055-acfd-4b07-a9cd-d4839edeacd8" />


### 4. Frame Design

For the final portion of the mechanical design, I developed a supporting frame for the pulley system. I wanted to create a relatively simple structure that would maintain the required pulley spacing while providing support for the rotating shafts. I decided to use a two-plate frame design with rounded ends. Each plate contains two bearing locations, allowing the shafts to be supported on opposite sides of the pulley assembly. The design incorporates a 5-inch center distance between the shaft axes to maintain the required pulley spacing. The frame concept was developed using hand sketches showing the front, side, and isometric views.

<img width="2500" height="1800" alt="A9_9" src="https://github.com/user-attachments/assets/0062f1fa-1b4c-4a39-b79d-7e3a5671f7de" />

### 5. Lessons Learned

Throughout this assignment, I developed a better understanding of how several mechanical design concepts work together in a pulley system. One of the most important things I learned was how the tight-side and loose-side belt tensions change when power is transmitted and how their difference determines the torque acting on the shaft. I also gained experience calculating the minimum cross-sectional area required to resist torsional loading. This helped me understand why shaft diameter is an important design consideration, even when the transmitted torque is relatively small. Another useful part of the assignment was learning how journal bearing pressure and surface velocity are combined into a PV rating. Before this project, I had limited experience using PV ratings to compare bearing materials. One challenge I encountered was selecting a belt that matched my calculated dimensions. I initially considered a larger diameter but ultimately selected a standard 1/4-inch polyurethane belt based on the available catalog options. I also had to distinguish between the initial static belt tension and the different tensions that develop during operation.

Finally, designing the frame helped me consider how shaft alignment, bearing placement, and structural support affect the overall assembly.

Total Time Spent: Approximately 5 hours.

### References:

Dunn, D. J. Solid Mechanics - Dynamics: Tutorial - Pulley Drive Systems.

Machinery's Handbook, 32nd Edition. Simple Stresses, Table 2.

Machinery's Handbook, 32nd Edition. Plain Bearing Materials, Table 4, p. 2442.

[McMaster-Carr. Polyurethane Round Belts. Part #3044K606.](https://www.mcmaster.com/3044K606-1835T385/)
