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

#### i. To efficiently support the applied 20 kN load ($P$) at points C and D, I decided to design a standard W-truss configuration for its balance of strength and simplicity. The overall dimensions were established by the given parameters, a 0.4 m width spacing ($a$) and a 0.3 m height ($b$). Using the Pythagorean theorem, the lengths of the diagonal members were calculated to establish the exact geometry of the framework. These specific dimensions ensure the applied forces are safely distributed throughout the entire structure.

<img width="2344" height="1020" alt="p-1" src="https://github.com/user-attachments/assets/a38dd26e-1d50-448a-9d2a-55bbbda3c2b3" />

#### ii - iv. To visualize the forces interacting within the structure, I sketched up isolated Free Body Diagrams for each pin-connected joint. Each diagram details the applied external loads, reaction forces at the supports, and the unknown internal member forces. The forces were broken down into their respective x and y components based on the calculated geometric angles of the truss. Then, I applied the Method of Joints was using static equilibrium equations ($\Sigma F_x = 0$ and $\Sigma F_y = 0$) at each individual node. Before plugging in any given numbers, algebraic expressions were written to isolate the unknown tension or compression force in each member. The system of equations was then solved sequentially, starting from the support reactions and moving joint-by-joint to find the exact internal force for every beam. This resulted in me finding the maximum internal force of **16.07 kN**.

## Communicate

