# A8 – Gears

## Objective

Design a mechanical gearbox with a 24:9 gear ratio capable of delivering an output torque of 1.25 in-lbf at 1100 rpm. This portfolio documents the engineering analysis of shaft shear stresses and gear forces, the selection of standard journal bearings based on maximum PV ratings, and the creation of a fully parametric CAD assembly and ASME Y14.5 compliant engineering drawings.

## Design Calculations

### Design of the Shafts

To determine the input parameters, the system was analyzed assuming an ideal gear train (power in equals power out). With an output torque of 1.25 in-lbf and an output speed of 1100 rpm, the 24:9 gear ratio dictates that the smaller input gear must rotate faster with less torque.

#### Gear Ratio Calculations

To determine the input parameters, the system was analyzed assuming an ideal gear train where power in equals power out. With an output torque of 1.25 in-lbf and an output speed of 1100 rpm, the 24:9 gear ratio dictates that the smaller input gear must rotate faster with less torque. This results in an input torque of 0.46875 in-lbf and an input speed of 2933.33 rpm. The total transmitted power is approximately 0.02182 hp.

#### Shaft Shear Stress Calculations

The given shafts were analyzed as solid circular members under pure torsion to ensure the specified diameters could handle the rotational loads. The simplified equation $\tau = 16T / \pi d^3$ was used. The input shaft, with a 0.125-inch diameter, has a calculated shear stress of 1,222.31 psi. This is well below the allowable limit of 4,000 psi for standard plain carbon steel. The output shaft, with a 0.250-inch diameter, has a calculated shear stress of 407.44 psi, which is also well below the allowable limit of 8,500 psi. Based on these results, both assigned diameters are structurally sufficient.

<img width="1050" height="1550" alt="A8_1" src="https://github.com/user-attachments/assets/998bb405-6623-4dee-a46a-5b8faf8241fd" />

#### Gear Force Calculations

To determine the loads acting on the bearings, the gear contact forces were calculated based on the pitch diameters and a standard 20° pressure angle. The tangential force was calculated as 2.5 lbf, and the radial force was calculated as 0.91 lbf. These two vectors combine for a total resultant force of 2.66 lbf. For a conservative bearing design, the full resultant load of 2.66 lbf was applied to size each bearing, representing a worst-case load distribution scenario.

Journal Bearing Pressure, Surface Velocity, and PVOperating parameters were calculated using the full conservative load and a selected bearing length of 0.250 inches. For the input bearing, the calculated pressure is 85.13 psi, the surface velocity is 95.99 ft/min, and the resulting PV rating is 8,172.30. For the output bearing, the calculated pressure is 42.57 psi, the surface velocity is 71.99 ft/min, and the resulting PV rating is 3,064.61.

#### Material Selection

SAE 841 Oil-Embedded Porous Bronze was selected from the lecture slide material table. Both calculated PV ratings of 8,172.30 and 3,064.61 fall well below the porous bronze limits of 4,500 psi for pressure, 1,500 sfpm for velocity, and 50,000 for PV.Journal Bearing ThicknessA simplified compression model was used to determine the minimum required wall thickness to prevent the bearing from crushing. Applying a Factor of Safety of 2 against a compressive yield strength of 11,000 psi gives an allowable stress of 5,500 psi. The minimum calculated thickness required is 0.000967 inches. The standard 1/16-inch wall thickness of the selected McMaster-Carr bearings massively exceeds this required minimum, ensuring structural failure will not occur under compression.

<img width="1250" height="1500" alt="A8_2" src="https://github.com/user-attachments/assets/ea676bcc-748e-4400-a162-455b9316cbd2" />

Bronze Sleeve Bearings
I selected the McMaster-Carr 9368T96 and the 9368T13 bronze sleeve bearing for the 0.125-inch input shaft and 0.250-inch output shaft respectfully. Both lengths matches the calculations, and the dimensions perfectly accommodate the required running sliding fit and pressure ratings for the output side.

<img width="1490" height="147" alt="Screenshot 2026-10-29 080524" src="https://github.com/user-attachments/assets/f01334e4-9fbc-4439-98b0-301087f895b1" />
<img width="1485" height="147" alt="Screenshot 2026-10-29 080515" src="https://github.com/user-attachments/assets/f7a519e6-3915-455e-bc9f-200576771543" />

### Design CAD Model

#### Gearbox Housing Model

The custom gearbox housing was designed as a two-part clam-shell assembly modeled in ABS plastic. The center-to-center distance between the bearing bores was explicitly modeled at 0.6875 inches to ensure ideal gear mesh.

<img width="700" height="450" alt="image" src="https://github.com/user-attachments/assets/47be4775-7157-48e0-b54f-89f5eda18a5a" />

#### 2157 Gearbox Housing Drawing

<img width="500" height="425" alt="image" src="https://github.com/user-attachments/assets/8711e3cc-36f2-441c-9eaf-0d4442beab7d" />

#### Input Shaft Model

The input shaft was modeled parametrically in SolidWorks using a global variable for the 0.125-inch diameter and a length of 1 inch. The material was set to Plain Carbon Steel to validate the allowable shear stress limits used in the calculations.

![[Image Placeholder: Screenshot of the Input Shaft CAD Model]]

#### 2157 Input Shaft Drawing

![[Image Placeholder: Drawing Sheet - Input Shaft]]

Output Shaft Model

The output shaft was modeled parametrically using a global variable for the 0.250-inch diameter and a length of 1 inch. It was similarly assigned Plain Carbon Steel.

![[Image Placeholder: Screenshot of the Output Shaft CAD Model]]

2157 Output Shaft Drawing

![[Image Placeholder: Drawing Sheet - Output Shaft]]

Final Assembly

In the SolidWorks assembly, the bearings were mated concentrically and coincident to the housing bores. The shafts were mated concentrically to the bearings with rotation unlocked, and centered via distance mates. The gears were mated concentrically to the shafts with rotation locked, and aligned linearly. Finally, a mechanical gear mate with a 24:9 ratio was applied to the shafts to simulate the kinematic rotation of the system.

![[Image Placeholder: Screenshot of the Assembled Gearbox]]

2157 Final Assembly Drawing

![[Image Placeholder: Drawing Sheet - Final Assembly]]

Lessons Learned

Throughout this project, the most significant lesson learned was the critical importance of validating theoretical calculations before beginning any CAD modeling. By confirming the shaft shear stresses and bearing PV limits early on, I avoided the need to redesign the housing components later in the process. Additionally, navigating the McMaster-Carr catalog to source standard off-the-shelf bearings and gears highlighted how engineers balance custom design with existing manufacturing solutions to save time and reduce costs. On the software side, implementing mechanical gear mates in SolidWorks proved to be a highly valuable skill for simulating true kinematic motion and verifying that the calculated 0.6875-inch center-to-center distance resulted in perfect gear mesh without interference.

Time Taken

The entire project took approximately twelve hours to complete. The initial mathematical modeling, including the gear force analysis and journal bearing sizing, required about three hours of focused work. Sourcing the appropriate standard components and modeling the parametric shafts, bearings, and custom aluminum housing in SolidWorks took another four hours. The most meticulous phase was generating the ASME Y14.5 compliant engineering drawings and formatting the specific MEGR 2157 title blocks, which took approximately three hours to ensure all manufacturing tolerances were properly communicated. The final two hours were spent compiling the calculations, CAD renderings, and written analysis into this cohesive design portfolio.

CAD Files:

