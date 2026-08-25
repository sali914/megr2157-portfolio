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

Converts opposing user-applied hand forces at two input handles into counter-rotating mechanical torque about a pivot axis, which generates a shear stress along the overlapping cutting edges.

b. Governing Model
The system's mechanical behavior is governed by a combination of Class 1 moment equilibrium and average transverse shear stress equations:

$$M = F_{\text{hand}} \cdot d_{\text{handle}} = F_{\text{shear}} \cdot d_{\text{cut}}$$

$$\tau = \frac{F_{\text{shear}}}{A_{\text{contact}}}$$

  &nbsp;&nbsp;&nbsp; $M$: Mechanical torque applied about the central pivot axis.
  
  &nbsp;&nbsp;&nbsp; $F_{\text{hand}}$: Input manual force exerted by the user's hand at the handle grip.
  
  &nbsp;&nbsp;&nbsp; $d_{\text{handle}}$: Distance from the hand grip center to the pivot axis center.
  
  &nbsp;&nbsp;&nbsp; $F_{\text{shear}}$: Output transverse force transmitted to the target material at the blade edge.
  
  &nbsp;&nbsp;&nbsp; $d_{\text{cut}}$: Distance from the material contact point to the pivot axis center.
  
  &nbsp;&nbsp;&nbsp; $\tau$: Average shear stress developed within the material contact zone.
  
  &nbsp;&nbsp;&nbsp; $A_{\text{contact}}$: Cross-sectional shear area of the material being cut.

**Model Assumption:** The scissor blades act as perfectly rigid bodies, undergoing zero longitudinal flexure or torsional twisting under operational loads.

c. Component Photographs and Geometry Analysis

&nbsp;&nbsp;&nbsp; **Component 1 - Primary Blade & Handle**

The component features a rigid steel blade section tapering toward the tip, fused to a synthetic polymer handle loop. The large ratio of handle length ($d_{\text{handle}}$) relative to the blade cutting distance ($d_{\text{cut}}$) provides mechanical advantage, multiplying input hand forces into higher output shear forces near the pivot. The angled wedge cross-section focuses the output force across a narrow surface, concentrating shear stress along the cutting edge.

&nbsp;&nbsp;&nbsp; **Component 2 - Secondary Blade & Handle**

Mirroring the primary blade, this component features a handle loop designed to constrain finger movement relative to the primary handle. The inner face of the steel blade is manufactured with a subtle longitudinal curvature (bowing) toward the mating blade. This specific geometry ensures a continuous single-point contact interface as the blades rotate closed, maintaining localized normal contact force directly at the cutting point.

&nbsp;&nbsp;&nbsp; **Component 3 - Central Fastener**

A cylindrical threaded pin passes through concentric holes in both steel blades to establish a fixed rotational axis. The raised flange holds both blade faces in tight contact, constraining lateral separation during planar rotation.

d. Patent research and Design Analysis

*Patent Number:* US 6,493,947 B2

*Inventors/Authors:* Lars Hedstrom et al.

Design Choice Rationale:

## Decide


## Communicate

