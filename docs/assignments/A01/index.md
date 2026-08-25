# A1 – Building Your Professional Portfolio

## Objective
Establishing a professional baseline for documenting and evaluating engineering work. Along with demonstrating the ability to apply analytical models to physical systems, make and justify technical design decisions using functional criteria, and communicate your reasoning clearly through a live, web-hosted documentation portfolio.

## Analyze
### Task A - Analyzing Portfolios

Portfolio 1 - https://nhoong.github.io/

Navigability:
This portfolio utilized a single-page layout with a navigation menu fixed to the top, which includes links for the portfolio, work experience, resume, and other social links. A reviewer will be able to easy find any specific project header within 30 seconds, either by scrolling or selecting the main navigation bar. However, locating underlying CAD source files or executable code repositories requires visiting a linked GitHub profile or external PDF viewer.

Reproducibility:
The degree to which another engineer could replicate the work varies drastically depending on the project segment. For example, the Shock Top Assembly entry is highly reproductible for drawing interpretation as the SolidWorks orthographic projections and a complete Bill of Materials with labeled callouts is embedded. On the other hand, the PILF Surgical Tool and Butterfly Valve entries both only provide high-level rendered projections without any dimensional tolerances, material callouts, or manufacturing restraints. All of which would make the physical reproduction impossible without directly requesting the source files. 

Evidence of Reasoning:
This portfolio presents final performance metrics instead of documenting the design process itself. Quantitative outcomes are explicitly stated, such as the Glaukos fixture measuring applied forces within a 1% margin of error, or even the Wobbler Engine running at a minimum pressure of 1.3 psi. However, the entries do not include stress simulations, material trade-off matrices, and failed early prototypes.

Professional Tone:
The writing itself follows a formal technical register, suitable for a hiring manager. The descriptions throughout rely on precise domain specific language to outline hardware interfaces and software logic. The narrative also avoids conversational phrasing, ensuring the focus remains on system inputs, outputs, and physical constraints.

Portfolio 2 - https://thanhvtran.com/

Navigability:
This website utilized a top level navigation menu with dedicated tabs for Home, Resume, Projects, About, and Contact. Navigating over to the Projects page allows a reviewer to locate any specific project within 20 seconds. The site also provides a category filter in order to isolate specific subsects of work. However, accessing the underlying calculation files, raw CAD repositories, or even FEA datasets requires navigating through individual projects that link out selectively, instead of displaying primary files to the top-level site. 

Reproducibility:
Once again, the degree to which an external reviewer can replicate the documented systems depends on the specific project. The FSAE Suspension Uprights and Plastic Injection Mold entries can both be moderately reproduced due to the documentation detailing the structural material selection, specific tooling operations, and explicit design mechanisms. 

Evidence of Reasoning:
The portfolio consistently demonstrates how analytical methods impacted physical design choices. Take the FSAE Suspension Uprights entry, in which the documentation showcased a clear transition between the initial boundary calculations to the hand calculations. Similarly, the Plastic Injection Mold entry compared three distinct mechanical solutions for molding undercuts and documented the exact cost and time trade-offs that led to selecting said mechanical solutions. 

Professional Tone: 
The writing follows a technical voice suitable for an engineering recruiter or lead designer. The narrative incorporated domain specific language, such as GD&T or topology optimization, to explain physical constraints and failure modes. The site tended to avoid a more casual blog-like style of story telling in favor of grounding project descriptions in physical parameters, manufacturing constraints, and verified structural behaviors. 

### Task B - Product Analysis

a. Primary engineering Function

Converts opposing user-applied hand forces at two input handles into counter-rotating mechanical torque about a detachable pivot axis, which generates a shear stress along the overlapping cutting edges.

b. Governing Model
The system's mechanical behavior is governed by a combination of Class 1 moment equilibrium and average transverse shear stress equations.

**Model Assumption:** The individual steel blade components act as perfectly rigid bodies, undergoing zero flexure or torsional twist during force transmission.

c. Component Photographs and Geometry Analysis

<img width="3000" height="4000" alt="Full_Scissor" src="https://github.com/user-attachments/assets/813e35ff-66b7-4478-9934-436d1f5a36e3" />

*Patent Number:* US 6,493,947 B2 | *Inventors/Authors:* Lars Hedstrom et al. | *Filed:* Jan. 22, 2001 | *Granted:* Dec. 17, 2002

&nbsp;&nbsp;&nbsp; **Component 1 - Primary Blade & Keyed Pivot Post**
<img width="3000" height="4000" alt="Comp_1" src="https://github.com/user-attachments/assets/2d969dd3-2c6b-4ae5-8573-4f615bc2d600" />

This component integrates a steel blade, an ergonomic handle loop, and an asymmetric raised pivot post welded or stamped near the fulcrum. The post geometry features two parallel flat edges that align with the mating component's slot at a specific rotation angle (typically open at $90^\circ$). When rotated into normal cutting angles ($0^\circ$ to $45^\circ$), the raised shoulder overlaps the mating blade's recessed track, converting input handle forces into planar rotation while preventing axial separation.

&nbsp;&nbsp;&nbsp; **Component 2 - Secondary Blade & Keyed Slot Hole**
<img width="3000" height="4000" alt="Comp_2" src="https://github.com/user-attachments/assets/425152c0-7e6c-4660-a7f0-ed082eed2068" />

This component features the mating blade edge, handle loop, and a specially profiled keyhole aperture. The aperture consists of a circular central bore with a keyway slot matched to the pivot post of Component 1. The circular bore constrains radial movement during rotation, while the keyway geometry allows complete axial separation only when manually aligned at a designated angle, satisfying sanitation and maintenance requirements.

d. Patent research and Design Analysis

**Alternative Solutions for Primary Function:**

Fixed Threaded Pivot Shears: Uses a permanent threaded fastener or rivet to hold the blades together, preventing non-destructive disassembly.

Spring-Loaded Bypass Shears: Employs a single pivot pin with an external coil spring pushing the handles open, using a mechanical thumb latch to lock the blades closed.

**Design Choice Rationale:**

*Observed Feature -* The asymmetric keyed slip-joint profile (requiring the blades to be opened to $90^\circ$ for separation).

*Engineering Rationale -* The designer selected a keyed slip-joint over a permanent threaded rivet to enable complete disassembly without tools. This geometric feature ensures that during normal operational cutting angles ($0^\circ$ to $45^\circ$), the blade shoulders remain locked together to resist transverse separation forces, while still allowing full separation for washing and sanitizing trapped material along the pivot interface.

## Decide


## Communicate

