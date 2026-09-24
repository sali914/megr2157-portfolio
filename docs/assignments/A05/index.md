# A5 – Bracket Design and Analysis

## Objective

The objective of this project was to design, analyze, and model a bracket that can safely support a horizontal load. The bracket needed to satisfy both strength and stiffness requirements. The design had to maintain a **safety factor of 4** against yielding while keeping the maximum deflection below **0.005 in**.

For the analysis, I selected **6061-T6 aluminum** because it provided a good combination of strength, stiffness, and manufacturability. I used a **yield strength (Sy) of 40,000 psi** and a **Young's Modulus (E) of 10,000,000 psi**. The applied force was chosen as **750 lbf**, which is within the required 500–800 lbf range. With a safety factor of 4, the **allowable stress was: 10,000 psi**. The bracket was divided into five main features so that each section could be analyzed separately for both stress and stiffness.

## Feature A

The first feature I analyzed was the large circular section where the load enters the bracket. I treated this section as a **circular cantilever** with the force acting at the end. The length of the section was assumed to be **2.00 in**. The first step was finding the bending moment created by the 750 lbf load. I then used the bending stress equation for a circular cross section, setting the stress equal to the allowable stress of **10,000 psi**, the minimum diameter required from the strength analysis was **1.152 in**. I also checked the diameter based on the **0.005 in deflection limit**. Using the cantilever deflection equation,
and found that the diameter required for stiffness was approximately **0.950 in**.

Since the stress requirement required a larger diameter than the stiffness requirement, **stress governed the design**. I therefore used a final Feature A diameter of **1.152 in**.

The following image shows my Feature A free-body diagram and calculations:

<img width="1000" height="900" alt="A5_1" src="https://github.com/user-attachments/assets/1b806d6c-62fa-4092-9223-e24dd14d6d21" />

## Feature B

The next section was Feature B. I treated this feature as an **axial member** carrying the full **750 lbf load** from Feature A. The width of Feature B was based on the diameter found for Feature A, so I used a width of **1.152 in**.

The first step was checking the required thickness based on stress. Since the load is axial, the stress was equal to F / A, where A = b * t. Using the allowable stress here let me set up an equation for the thickness, which came out to be 0.0651 in. I then checked the thickness required to keep the axial deflection below **0.005 in** and found that the stiffness requirement was smaller than the stress requirement, so stress once again controlled the design.

I therefore used a final Feature B thickness of **0.0651 in** and a width of **1.152 in**. At this thickness, the stress is approximately **10,000 psi**, while the calculated deflection is approximately **0.003 in**, which is below the maximum allowed value.

The following image shows my Feature B analysis:

<img width="1000" height="900" alt="A5_2" src="https://github.com/user-attachments/assets/47f65430-0eec-4c04-ab4c-7b01a9b0d658" />

## Feature C

Feature C was the long central section of the bracket. Unlike Feature B, this section behaves like a **simply supported beam with the 750 lbf load acting at the center**. I used a length of **4.00 in** and kept the width at **1.152 in**.

The following image shows the Feature C free-body diagram and calculations:

<img width="1000" height="900" alt="A5_3" src="https://github.com/user-attachments/assets/b9f88ec8-49cb-4d86-ba09-ef3fd05b163c" />

## Feature D

Feature D is another axial section of the bracket. Because of the symmetry of the bracket, I only needed to analyze one side of the load path. The load carried by this feature is **375 lbf**. I used the same **1.152 in width** as the other sections. The thickness required from the stiffness calculation was approximately **0.020 in**, so the stress requirement was again larger.

The final Feature D dimensions were therefore **1.152 in wide** and **0.033 in thick**. At this thickness, the calculated stress is approximately **9,864 psi**, which is below the allowable stress, and the deflection is approximately **0.003 in**.

The following image shows my Feature D calculations:

<img width="1000" height="900" alt="A5_4" src="https://github.com/user-attachments/assets/bf5f7741-0af1-4b7f-93fd-9914504e871a" />

## Feature E

Feature E was slightly different from the other sections because it rests directly against a rigid surface. I initially considered treating this feature like a cantilever, but after looking more closely at the geometry and the direction of the force, I realized that this was not the correct model. The feature is primarily being loaded in **compression against the supporting surface**.

The load carried by Feature E is **375 lbf**, and I used a length of **1.000 in** and a width of **1.152 in**. For the stress calculation, I used the bearing/compressive stress relationship with the allowable stress and got a **thickness of 0.033 in**.

I also checked the axial compression deflection and found the stiffness requirement only required a thickness of approximately **0.0065 in**, so stress clearly governed this feature.

I therefore used a final Feature E thickness of **0.033 in**. The resulting stress is approximately **9,864 psi**, and the calculated deflection is approximately **0.001 in**.

The following image shows the Feature E analysis:

<img width="1000" height="900" alt="A5_5" src="https://github.com/user-attachments/assets/e18f7b62-c104-4068-b498-fd8f6eb93273" />

## Multiview Hand Drawing

I also created a multiview sketch showing the different views of the bracket.

<img width="1000" height="1200" alt="A5_6" src="https://github.com/user-attachments/assets/e0d4f969-c4d7-4d02-974e-e6b471073008" />

# 2157 Students Only – Linkage and Fits

## Linkage Design

For the 2157-only portion of the assignment, I designed a separate linkage that connects Feature A of the bracket to a **1-inch shaft**. The linkage needed to carry the same **750 lbf force** as the bracket while still satisfying the same strength and stiffness requirements.

I continued using **6061-T6 aluminum**, with an allowable stress of **10,000 psi** and a Young's Modulus of **10,000,000 psi**.

The linkage was designed with a **1.750 in overall width** and a **3.000 in center-to-center distance** between the two holes. The larger hole connects to Feature A, so its diameter was set to the previously calculated **1.152 in** diameter.

### Linkage Stress and Stiffness Analysis

The most important part of the linkage was the material remaining around the larger Feature A hole. Since the hole removes material from the middle of the cross section, I used the net width through the hole as the critical section. After checking strength, I checked the linkage for axial deflection. Since the linkage is primarily carrying the force along its length, I used the axial deformation equation.

The following image shows my linkage stress and stiffness calculations:

<img width="1000" height="700" alt="A5_7" src="https://github.com/user-attachments/assets/986bddd9-7539-46d9-9f63-bab4324c061c" />

## Selecting the Fit for Feature A

The first fit I needed to select was the hole where the linkage connects to Feature A. The assignment requires this connection to be a **running/sliding fit**, meaning the hole and mating cylindrical feature need enough clearance for the linkage to move without being pressed onto the feature.

To select the fit, I used **Machinery's Handbook, 32nd Edition**, specifically the fit tables in the assigned section on pages **646–660**. I compared the available running and sliding fit classes and selected the class that best matched the required function of the connection.

The Feature A diameter is **1.152 in**, so the fit needs to be selected based on the diameter range containing 1.152 in rather than simply using the nominal 1.152 in value as the tolerance.

After selecting the fit class, I used the corresponding hole and shaft tolerance values from the table to determine the actual allowable size range for the Feature A connection.

The important part of this fit is that the smallest possible hole must still be larger than the largest possible mating feature so that the parts can slide together without interference.

## Manufacturing Process for Feature A

For the Feature A connection, the fit requires a relatively controlled hole size because the amount of clearance affects how freely the linkage can move.

I would manufacture the hole using a drilling operation followed by a more accurate finishing operation such as **reaming**. Drilling alone would not provide the same level of dimensional control as a finished reamed hole.

The hole would first be drilled undersize and then brought to the required tolerance using the appropriate reamer. The final hole would then be inspected using the appropriate measuring equipment to make sure it falls within the tolerance range specified by the selected fit.

## Selecting the Fit for the 1-inch Shaft

The second fit was for the **1.000 in shaft**. Unlike Feature A, this connection requires a **light assembly pressure fit**. The shaft should be able to be assembled into the linkage using light pressure, but it should not be loose enough to freely slide around during operation.

I again used **Machinery's Handbook, 32nd Edition**, using the fit tables on pages **646–660** to select the appropriate fit class.

The selected fit needs to provide a small amount of interference between the shaft and hole. This means the shaft can be slightly larger than the hole depending on the tolerance limits, creating the light assembly pressure required by the assignment.

After selecting the fit class, I used the table's tolerance values for the **1.000 in nominal diameter** to determine the allowable hole and shaft sizes.

## Manufacturing Process for the 1-inch Shaft

The manufacturing process for this connection needs to produce a much more controlled hole than a basic drilled hole. I would drill the hole undersize first and then use a finishing operation such as **reaming** to bring it to the required tolerance.

The shaft itself would also need to be manufactured or finished to its specified tolerance. After both parts are manufactured, the actual dimensions can be checked before assembly to make sure the hole and shaft fall within the selected fit limits.

## Mistakes and Corrections

One of the biggest things I had to correct during the project was the way I modeled **Feature E**. I initially treated it like another cantilever section, but after looking at the actual geometry and the direction of the force, I realized that it was resting against a rigid surface. This meant that the better model was a compression/bearing analysis rather than a cantilever bending analysis. Changing the model also changed which equations were appropriate for the feature.

I also had to be careful with rounding. For the linkage, the calculated minimum thickness was **0.1254 in**. Simply rounding this down to **0.125 in** would make the calculated stress slightly exceed the allowable 10,000 psi. This showed me that calculated dimensions should not automatically be rounded down just because the difference appears small.

Another important correction was making sure that the Feature A diameter was carried into the linkage design. Since the linkage hole is based on the **1.152 in Feature A diameter**, changing Feature A would also change the amount of material remaining around the hole in the linkage.

## Lessons Learned & Time Spent

This project helped me understand how important it is to choose the correct physical model before starting the calculations. The equations themselves are not usually the hardest part. The harder part is figuring out what the part is actually doing and deciding whether the feature should be modeled as a cantilever, axial member, beam, or compression/bearing section.

I also learned that **stress and stiffness can give very different required dimensions**. For the linkage, the stress calculation required **0.1254 in** of thickness, while the stiffness calculation only required **0.0753 in**. This meant that strength was the governing requirement. The same comparison was made for each of the five bracket features.

Another thing I learned was how errors can carry through an entire design. The **1.152 in Feature A diameter** was not just a dimension for one feature. It also determined how much material remained around the linkage hole. If the Feature A diameter changed, the linkage stress calculation would also change.

Finally, I learned more about how engineering fits are actually selected. The nominal diameter alone does not tell you whether two parts will slide together, run freely, or require pressing. The tolerance limits of both mating parts have to be considered together.

Overall, I spent approximately **7 hours** completing the assignment, including the initial calculations, hand sketches, linkage design, fit research, and final documentation.
