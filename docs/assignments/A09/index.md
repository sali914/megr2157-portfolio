# A9 – Pulley System

## Objective

The objective of this assignment was to design a pulley system capable of transferring power between two parallel shafts separated by a center distance of 4 to 6 inches. The system was required to use two 3-inch diameter pulleys, operate between 1000 and 2000 rpm, and maintain an initial belt tension between 4 and 6 lbf. All components needed to satisfy a minimum safety factor of 3.

For my design, I selected ABS for the pulleys, polyurethane rubber for the belt, and 1060 hardened steel for the shafts. I also designed a supporting frame and evaluated journal bearing materials using the Machinery's Handbook.

<img width="295" height="100" alt="image" src="https://github.com/user-attachments/assets/e39193cc-d460-40b6-92fa-ab58c38c7d8c" />


### Belt Design

#### Knowns and Unknowns

I began by identifying the known and unknown variables for the belt system. I selected a center distance of 5 inches, an operating speed of 1500 rpm, and an initial belt tension of 5 lbf. These values fall within the specified design requirements.

[Insert Image: Belt Design Knowns and Unknowns]

#### Free-Body Diagram

I created free-body diagrams to identify the forces acting on the driver and driven pulleys. The belt experiences different tensions on its tight and loose sides when transmitting power.

For my analysis, I used a sign convention where counterclockwise moments are positive and clockwise moments are negative.

[Insert Image: Belt and Pulley Free-Body Diagrams]

#### Solving

I began with the relationship between the initial static belt tension and the operating tensions:

T0 = T1 + T2

I then used the belt friction equation at impending slip with an assumed friction coefficient of 0.26  and an angle of pi radians to solve for T2 and T1, which were 3.064 lbf and 6.936 lbf respectfully. After determining these forces, I used the normal stress equation and the required safety factor to calculate the minimum belt cross-sectional area. Since the belt has a circular cross-section, I rearranged the area equation to determine the minimum diameter.

Using the selected operating conditions, I obtained the following preliminary values:


#### Belt Selection

After completing the calculations, I used McMaster-Carr to find a polyurethane round belt that closely matched my required dimensions.

I initially considered a larger belt diameter for an additional safety margin. However, I decided to use a standard 1/4-inch diameter belt rather than a custom-sized option.

The selected belt was McMaster-Carr Part #3044K606, with a diameter of 0.250 inches and a nominal outer circumference of 20.25 inches.

Using the preliminary calculated tight-side tension, the belt has a tensile safety factor of approximately 3.33. This result depends on the assumed operating tensions, and the installed belt tension would need to be verified.

<img width="797" height="607" alt="image" src="https://github.com/user-attachments/assets/fe9e56e8-2276-4b80-a3a4-2ab497cbf735" />


### 2. Shaft Design

Knowns and Unknowns

After completing the belt design, I moved on to calculating the minimum shaft diameter. The shafts were required to be made from 1060 hardened steel.

I used the previously calculated belt tensions to determine the torque transmitted through the system.

[Insert Image: Shaft Design Knowns and Unknowns]

Free-Body Diagram

I created a free-body diagram to identify the forces and torque acting on the shaft. The belt tensions produce a net torque, while the combined belt forces produce a transverse load on the shaft.

For the preliminary design, I assumed the pulley was centered between two bearing supports.

[Insert Image: Shaft Free-Body Diagram]

Symbolically Solving

I began by calculating the transmitted torque:

$$
M_t=(T_1-T_2)r
$$

I then used the torsional shear stress equation for a solid circular shaft:

$$
\tau_{\max}=\frac{M_tc}{J}
$$

After substituting the geometric relationships for a circular shaft, the equation becomes:

$$
\tau_{\max}=\frac{16M_t}{\pi d^3}
$$

Since the assignment requested the minimum cross-sectional area, I rearranged the torsion equation in terms of area:

$$
A_{\min}=\left(\frac{2\sqrt{\pi}M_t}{\tau_{\text{allow}}}\right)^{2/3}
$$

Once the minimum area was determined, I calculated the corresponding shaft diameter.

$$
d_{\min}=\sqrt{\frac{4A_{\min}}{\pi}}
$$

[Insert Image: Shaft Design Symbolic Calculations]

Numerically Solving

Using the calculated belt tensions, I determined the transmitted torque to be:

$$
M_t=(6.936-3.064)(1.5)=5.808\text{ lbf}\cdot\text{in}
$$

Using a tensile yield strength of 93,000 psi for the selected hardened steel condition, I applied the von Mises criterion and a safety factor of 3.

Parameter

Value

Transmitted torque

5.808 lbf·in

Assumed tensile yield strength

93,000 psi

Allowable shear stress

17,897.86 psi

Minimum shaft area

0.01098 in²

Minimum shaft diameter

0.1182 in

Selected shaft diameter

0.125 in

I selected a standard 1/8-inch shaft diameter because it exceeded the calculated torsional minimum.

The selected shaft satisfies the preliminary torsional stress requirement. However, the calculation does not include bending from the belt forces, so the final shaft design would require an additional combined-loading analysis.

[Insert Image: Shaft Design Numerical Calculations]

3. Journal Bearing Design

Knowns and Unknowns

The next portion of the assignment involved selecting a journal bearing capable of supporting the rotating shaft.

I used the shaft diameter of 0.125 inches, rotational speed of 1500 rpm, and the bearing reactions determined from the belt forces.

I assumed that each shaft was supported by two bearings, with the pulley centered between them. This arrangement distributes the 10 lbf transverse belt load equally, resulting in 5 lbf per bearing.

[Insert Image: Journal Bearing Knowns and Unknowns]

Free-Body Diagram

I created a free-body diagram showing the pulley load acting on the shaft and the reactions at both journal bearings.

With the pulley centered between the supports, the bearing reactions were calculated as:

$$
R_A=R_B=\frac{10}{2}=5\text{ lbf}
$$

[Insert Image: Journal Bearing Free-Body Diagram]

Symbolically Solving

I began with the projected bearing area:

$$
A_p=d_sL
$$

The bearing pressure was then calculated using:

$$
P=\frac{F_r}{d_sL}
$$

Next, I determined the shaft's linear surface velocity:

$$
V=\frac{\pi d_sN}{12}
$$

Finally, I multiplied the bearing pressure by the surface velocity to calculate the PV rating.

$$
PV=P\times V
$$

These values would allow me to compare the operating conditions against the material limits provided in Machinery's Handbook.

[Insert Image: Journal Bearing Symbolic Calculations]

Numerically Solving

I selected a preliminary bearing length of 0.250 inches and used the 0.125-inch shaft diameter to calculate the projected bearing area.

$$
A_p=(0.125)(0.250)=0.03125\text{ in}^2
$$

The bearing pressure was:

$$
P=\frac{5}{0.03125}=160\text{ psi}
$$

The surface velocity was:

$$
V=\frac{\pi(0.125)(1500)}{12}=49.087\text{ ft/min}
$$

The resulting PV rating was:

$$
PV=(160)(49.087)=7853.98\text{ psi}\cdot\text{ft/min}
$$

Parameter

Value

Shaft diameter

0.125 in

Bearing length

0.250 in

Load per bearing

5 lbf

Bearing pressure

160 psi

Surface velocity

49.087 ft/min

PV rating

7,853.98 psi·ft/min

[Insert Image: Journal Bearing Numerical Calculations]

Material Selection

After calculating the operating pressure, velocity, and PV rating, I compared my results with Table 4, Application Limits: Sintered Metal and Nonmetallic Bearings, from Machinery's Handbook.

I selected porous bronze because it satisfied the required operating conditions while maintaining a safety factor greater than 3 for both pressure and PV.

The material has a maximum pressure rating of 4,500 psi and a PV limit of 50,000 psi·ft/min.

The calculated pressure safety factor was 28.13, while the calculated PV safety factor was 6.37.

Porous bronze also offers self-lubricating properties when properly oil-impregnated, making it suitable for a journal bearing application.

[Insert Image: Machinery's Handbook Table 4 with Porous Bronze Highlighted]

4. Frame Design

For the final portion of the mechanical design, I developed a supporting frame for the pulley system.

I wanted to create a relatively simple structure that would maintain the required pulley spacing while providing support for the rotating shafts.

I decided to use a two-plate frame design with rounded ends. Each plate contains two bearing locations, allowing the shafts to be supported on opposite sides of the pulley assembly.

The design incorporates a 5-inch center distance between the shaft axes to maintain the required pulley spacing.

The frame concept was developed using hand sketches showing the front, side, and isometric views.

Design Considerations

The primary considerations for the frame were shaft alignment, bearing placement, and the forces transmitted from the pulleys to the supports.

The belt produces a combined transverse load of 10 lbf on each shaft. With the pulleys centered between two supports, each bearing transfers approximately 5 lbf to the frame.

This loading arrangement allows the frame to distribute the forces through the two side plates.

The frame would still require a detailed stress and deflection analysis to confirm that its dimensions satisfy the overall safety factor requirement.

[Insert Image: Frame Design Front View]

[Insert Image: Frame Design Side View]

[Insert Image: Frame Design Isometric View]

5. Lessons Learned

Throughout this assignment, I developed a better understanding of how several mechanical design concepts work together in a pulley system. One of the most important things I learned was how the tight-side and loose-side belt tensions change when power is transmitted and how their difference determines the torque acting on the shaft.

I also gained experience calculating the minimum cross-sectional area required to resist torsional loading. This helped me understand why shaft diameter is an important design consideration, even when the transmitted torque is relatively small.

Another useful part of the assignment was learning how journal bearing pressure and surface velocity are combined into a PV rating. Before this project, I had limited experience using PV ratings to compare bearing materials.

One challenge I encountered was selecting a belt that matched my calculated dimensions. I initially considered a larger diameter but ultimately selected a standard 1/4-inch polyurethane belt based on the available catalog options. I also had to distinguish between the initial static belt tension and the different tensions that develop during operation.

Finally, designing the frame helped me consider how shaft alignment, bearing placement, and structural support affect the overall assembly.

Total Time Spent: Approximately 5 hours.

References

Dunn, D. J. Solid Mechanics - Dynamics: Tutorial - Pulley Drive Systems.

Machinery's Handbook, 32nd Edition. Simple Stresses, Table 2.

Machinery's Handbook, 32nd Edition. Plain Bearing Materials, Table 4, p. 2442.

McMaster-Carr. Polyurethane Round Belts. Part #3044K606.

Wanga, Chena, Wua, Zhangb, and Suna. Strain-induced Structural and Dynamic Changes in Segmented Polyurethane Elastomers.
