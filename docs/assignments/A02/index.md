# A2 – Truss Stress Analysis

## Objective

- Design a lightweight planar truss using A500 steel or an alternative material.
- Create free body diagrams (FBDs) for joints and critical pins.
- Calculate the required cross-sectional area of truss elements with a safety factor.
- Determine pin sizes based on shear forces with a safety factor.
- Solve equations symbolically and numerically for both truss and pin design.
- Estimate the total weight of the truss and pins.
- Create a CAD model with accurate dimensions and connections.
- Compare CAD weight predictions with hand calculations.
- Document key engineering lessons learned from the process.

## Analyze

<img width="317" height="215" alt="image" src="https://github.com/user-attachments/assets/f389b006-cea0-4655-9882-89db2c3ef784" />

The image above, Figure #1, showcases the geometric constraints of the truss. The values provided are: P = any force between 20 and 30 kN, a = 0.4 m, and b = 0.3 m. The cross sectional area of each element needs to be identical. 

## 2. Design the Overall truss Geometry:

### a. Design the truss structure using the parameters in Figure #1

#### i. To efficiently support the applied 20 kN load ($P$) at points C and D, I decided to design a standard W-truss configuration for its balance of strength and simplicity. The overall dimensions were established by the given parameters, a 0.4 m width spacing ($a$) and a 0.3 m height ($b$). Using the Pythagorean theorem, the lengths of the diagonal members were calculated to establish the exact geometry of the framework. These specific dimensions assisted the calculations needed to find the external forces.

<img width="2344" height="1020" alt="p-1" src="https://github.com/user-attachments/assets/a38dd26e-1d50-448a-9d2a-55bbbda3c2b3" />

<img width="2624" height="1086" alt="p-2" src="https://github.com/user-attachments/assets/7ceb4416-a986-49d7-a6f5-9774aeb9aeaf" />


#### ii - iv. To visualize the forces interacting within the structure, I sketched up isolated Free Body Diagrams for each pin-connected joint. Each diagram details the applied external loads, reaction forces at the supports, and the unknown internal member forces. The forces were broken down into their respective x and y components based on the calculated geometric angles of the truss. Then, I applied the Method of Joints was using static equilibrium equations ($\Sigma F_x = 0$ and $\Sigma F_y = 0$) at each individual node. Before plugging in any given numbers, algebraic expressions were written to isolate the unknown tension or compression force in each member. The system of equations was then solved sequentially, starting from the support reactions and moving joint-by-joint to find the exact internal force for every beam. This resulted in me finding the maximum internal force of **16.07 kN**.

<img width="750" height="1000" alt="p-3" src="https://github.com/user-attachments/assets/e148c585-475e-4d4a-b52c-559a9d191e32" />

### b. Use the largest internal force to calculate the required cross-sectional area of the elements using a safety factor of 3.5, and the yield strength. 

#### i - iii. Before sizing the physical beams, all known constraints, such as the yield strength, safety factor, and maximum internal force, were clearly listed alongside the target unknown variables in the image below. The normal stress equation ($\sigma = F/A$) was then rearranged symbolically to isolate the minimum required cross-sectional area. I chose to increase the minimum cross-sectional area to a more standard number of 225 $mm^2$, which I then used to calculate the actual safety factor of 3.51.

<img width="2238" height="628" alt="p-4" src="https://github.com/user-attachments/assets/ec94af90-5074-46ff-ba29-4cd9f349b733" />

#### iv. The exact maximum internal force, the 250 MPa yield strength, and the safety factor of 3.5 were used in the symbolic area formula resulted in a minimum cross-sectional area of 224.28 mm², which was practically achieved by selecting a 10 mm by 22.5 mm rectangular beam profile. The total length of the members were calculated to determine the volume. Finally, multiplying this volume and the density of ASTM A36 steel yielded an approximate truss weight of 57.39 N.

<img width="2532" height="1038" alt="p-5" src="https://github.com/user-attachments/assets/584990a3-4214-4ff0-a56d-ef40e5bf280b" />

## 3. Determine the cross-sectional area of the connecting pins

### a. Calculate the required cross-sectional area of the pins to withstand the expected shear forces. Design a single shear connection. Use a safety factor of 4.

#### i. Before starting the pin design process, material properties for the hardened tool steel, such as the yield shear strength (170 ksi) and density (7695 kg/ $m^3$) were explicitly listed alongside the required safety factor of 4. The unknown variables, including the minimum required cross-sectional area, pin diameter, and total combined weight, were clearly identified to structure the upcoming calculations.

#### ii - iv. A specific Free Body Diagram was sketched for the pin experiencing the largest reaction load within the truss structure. This diagram visually isolated the single-shear connection, showing exactly how the maximum 20 kN force attempts to slice through the pin's cross-section between the structural members. Along with that, the basic shear stress equation ($\tau = V/A$) was rearranged to isolate the minimum area. The specific project values, like the 20 kN maximum shear force, 1172 MPa yield shear strength, and safety factor of 4, were inserted into the symbolic formula to find the exact numerical requirement. This calculation helped to determine a minimum required cross-sectional area of 68.26 mm², which was then safely satisfied by selecting a standard 10 mm diameter pin . Finally, the total volume of all five 45 mm-long pins was multiplied by the tool steel's density to calculate a lightweight combined mass of approximately 0.136 kg, or 1.33 N.

<img width="2532" height="1634" alt="p-6" src="https://github.com/user-attachments/assets/d4ab5b63-8386-4106-b934-bcb592415392" />

## 4. Utilize CAD software to generate a 3D model of the truss. Model the pins as cylinders with the appropriate cross-sectional areas and lengths.

### a. Represent the truss minus the pins as one part in CAD.

I needed to model the main frame of the truss as one single piece to match the project rules. To do this in SolidWorks, I drew a flat 2D layout and used the software to build solid beams along those lines, fusing them all together into one object. This gave me a single, continuous 3D part for the truss itself, keeping the pins separate for later.

<img width="2782" height="937" alt="Screenshot 2026-09-03 010306" src="https://github.com/user-attachments/assets/521555bf-6467-44e1-9fb3-763f62cd61cd" />


### b. Maintain the cross-sectional area of each element at the intersection of the pin joint.

Drilling holes for the pins removes material, which weakens the joints and violates the project's area rules. To fix this, I added extra circular hubs of material around every joint before cutting the 10 mm holes through them. This extra padding made sure the joints stayed strong and kept the exact same amount of material as the rest of the beams.

<img width="750" height="500" alt="Screenshot 2026-09-03 010512" src="https://github.com/user-attachments/assets/7794d313-1058-419a-bb16-ae3809adbb56" />

### c. Ensure that the truss design satisfies the safety factor, weight optimization goal, and geometric constraints while maintaining structural integrity and stability.

I had to make sure the 3D model exactly matched the math and size rules from the earlier steps. I carefully typed in the required 0.4 m width and 0.3 m height, and set all the beams to the safe 10 mm by 22.5 mm size we calculated. By following these exact numbers, the final model is as light as possible while still being strong enough to hold the 20 kN load safely.

<img width="643" height="314" alt="Screenshot 2026-09-03 010911" src="https://github.com/user-attachments/assets/d28309c5-e9aa-4938-8875-b2ace72f4f47" />
<img width="564" height="245" alt="Screenshot 2026-09-03 011049" src="https://github.com/user-attachments/assets/65263fdb-c354-46a5-b606-283941fdeb38" />

### d. Implement mass properties in the CAD model and determine the predicted weight, accordingly.

Finally, I needed to check if my hand-calculated weight matched what the computer predicted. I told SolidWorks that the truss was made of A36 Steel and the pins were Tool Steel so it knew exactly how heavy the materials should be. Then, I used the software's Mass Properties tool to find the mass of the final assembly, which was a value of m = 5.919 kg, which was off from my hand-calculated value of m = 5.986 kg.

<img width="605" height="350" alt="Screenshot 2026-09-03 011747" src="https://github.com/user-attachments/assets/cff04eef-6a78-433a-9dde-efb37108465d" />

## 5. Engineering Lesson Learned

Throughout this project, I gained a deeper understanding of how local geometric features impact global structural integrity, specifically regarding joint design. I learned that simply removing material for a connection pin critically reduces the cross-sectional area, which creates a high-stress concentration highly susceptible to tear-out or bearing failure. To mitigate this mechanical vulnerability, I learned how to strategically design material hubs around the pin joints to compensate for the internal void and maintain the uniform cross-sectional area. Furthermore, translating the theoretical static equations into a functional CAD assembly taught me how to effectively validate manual weight optimization calculations against computationally predicted mass properties.

