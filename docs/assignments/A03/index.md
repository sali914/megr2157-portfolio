# A3 – Parametric & FEA

## Objective

- Use axial deflection modeling to design bar dimensions.

- Use parametric design to determine the bar's length.

- Introduce FEA (Finite Element Analysis) and parameter linking in CAD.

- Compare and contrast analytical calculations with FEA results.

## Description:

Design a bar in CAD with an applied direct load between 300 lbf < F < 500 lbf. The max axial deflection of the bar is .009 inches. The bar is to be designed from Aluminum with a range of Young’s Modulus from (8.5 - 11.5) x 10^6 psi.

<img width="458" height="55" alt="image" src="https://github.com/user-attachments/assets/0bb1202b-18c2-48bf-a250-0f40d1c2ac9f" />

### 1. Design a bar in CAD

#### a.) Choose the values for the cross sectional area of the bar. (width, height, and thickness)

I decided to pick a value of 400 lbf for the applied direct load, and a value of 10 x 10^6 psi for the Young's Modulus, as they only assigned us ranges and not a specific value. Although the instructions for this step say to pick a width, height, and thickness, the instructional document mentioned that the cross-section of the bar is circular. Therefore, I will be picking a diameter of 0.45 in. Using this value, I calculated the **cross-sectional area to be 0.159 in^2** and the **nominal stress to be 2,516 psi.**

<img width="3000" height="596" alt="A3_1" src="https://github.com/user-attachments/assets/fe5fb737-b086-4056-8d1e-8f5c93904aaf" />

#### b.) Use the direct tension elongation equation in the Machinery’s Handbook to parametrically determine the length of the bar.

With all of the values I had chosen in step 1a, I rearranged the Direct Tension Elongation Equation to solve for the length, ** L = 35.775 in. **

<img width="2976" height="464" alt="A3_2" src="https://github.com/user-attachments/assets/4846f20e-8522-4f66-a480-06e18e8bfb2f" />

#### c.) Generate the bar in CAD

<img width="1992" height="902" alt="image" src="https://github.com/user-attachments/assets/c65b10e6-2550-4250-8425-398a3613782d" />

With all of the values that I have picked/solved for now assigned as global variables, as shown above, I began to design my bar in SolidWorks by assigning global variables to the dimensions.

<img width="800" height="650" alt="image" src="https://github.com/user-attachments/assets/4268ede6-59cf-42a4-bde6-0a10215f729e" />

<img width="800" height="650" alt="image" src="https://github.com/user-attachments/assets/a139deca-606d-4bf7-b8d2-abd8ae3ccc4f" />

Having extruded the bar, it was now in the correct shape. Following along with the rest of the design, I assigned the material property based off of the values chosen earlier. This resulted in me using Aluminum Alloy 6061-T6 (SS), which ended up being the closest match to the Young's Modulus and Yield Strength values that I am using.

<img width="700" height="445" alt="image" src="https://github.com/user-attachments/assets/36ee69a4-a95b-4c8d-8980-26d622684cab" />

## 2. Conduct a FEA on the bar using the same load used to generate the bar's geometry

### a. - c.) Generate a deflection map and a von Mises Stress map in the FEA. Check if the maximum stress is lower than the strength of Aluminum (Sy = 40 ksi), note the safety factor.

With the bar set up, I conducted an FEA on the bar with the same applied force of 400 lbf that I picked earlier. After fixing one side, and applying the load to the other, I ran the FEA tests for the Deflection, Stress, and Strain:

Fixed Object:

<img width="1892" height="1090" alt="image" src="https://github.com/user-attachments/assets/4b33bb7e-035c-4a91-b8b5-38149fe7659f" />

Applied Load:

<img width="1417" height="1202" alt="image" src="https://github.com/user-attachments/assets/5ee105a3-b708-42f9-9876-7e1af7dbca6d" />

Deflection Map:

<img width="2470" height="1412" alt="image" src="https://github.com/user-attachments/assets/17698b1d-df55-4edd-9480-55f19244803e" />

Von Mises Stress Map: 

<img width="2585" height="1412" alt="image" src="https://github.com/user-attachments/assets/44bae603-4e0a-4863-9950-440cc014584a" />

Maximum Stress & Safety Factor:

After running the simulations, I found that the maximum stress was 2,743 psi, which was a little higher than my initial calculation of 2,516 psi. Using this new max stress value, I calculated the Safety Factor to be 14.6.

<img width="2986" height="806" alt="A3_3" src="https://github.com/user-attachments/assets/e930fb0b-7ef3-437b-b871-1dd4186865c2" />

## 3. Design Reflection

### a.) Report the axial deflection from your parametric hand-calculation and from your FEA. Calculate the percent difference

The axial deflection from my parametric hand-calculations was given as 0.009 in, and the value I got from my FEA was 0.00899 in. I then plugged these values into the % difference formula and got a difference of about 0.11%. Given that the values are practically the same, I attributed it to the fact that it is a simple axial loading scenario with a uniform cross-section. Overall, I trust the FEA calculation more, as it can capture the real world boundary conditions at the fixture. 

<img width="3000" height="438" alt="A3_4" src="https://github.com/user-attachments/assets/46086541-4385-4f33-969a-0846616dfa7d" />

### b.) Pin Hole Estimation

After looking for the Stress Concentration Factor, I found that it was kt = 3. Using this value, I calculated the estimated peak stress by multiplying kt * nominal stress, which resulted in a value of 7,548 psi. This is still well below the safety factor of 40,000 psi.

<img width="3000" height="1110" alt="A3_5" src="https://github.com/user-attachments/assets/18d87e44-0ff4-4bde-9a58-69c565a78c88" />

## 4. Modify Design Parameters

### a.) Cycle through #2, change each of the design parameters which include load, thickness, height and width. Keep the material and the fixture the same

I decided to change the load to 350 lbf, and the diameter to 0.50 in.

### b.) Before calculations, guess if the length will increase, decrease, or stay the same

I guessed that the length would increase, because a larger diameter increases the cross-sectional area. This in turn makes the bar stiffer, and a smaller force means it is being pulled less intensely. After doing the calculations, I found that the length did in fact increase to 50.49 in. 

<img width="1985" height="897" alt="image" src="https://github.com/user-attachments/assets/60a864ad-eb12-46ca-9a81-123df567dcb9" />


## 5. Lesson Learned

Throughout this project, I ran into a few bumps that showed me why setting up my CAD files correctly is so important. When I first tried to add the diameter to my sketch, I just typed the number in. This meant it was stuck at that size and wouldn't update automatically if I changed my main settings. I had to go back, type an equals sign, and link it properly to my main list of variables. Also, when I went to test the bar using the simulation tool, I found out I couldn't just type my variable name directly into the force box. It gave me an error, so I had to figure out how to create a special simulation link first so the software would accept my force value.

Figuring these things out really showed me how much time this kind of linked modeling saves. Because I took the time to connect all my numbers at the start, updating the design at the very end was super easy. When I changed the load and diameter for the final step, the bar's length updated all by itself without me having to redraw anything or redo the math. I also learned why the computer's stress results are a little different from the math I did by hand. My hand calculation gave me 2,515 psi, but the computer showed 2,743 psi. I realized this happens because the computer simulation treats the fixed end of the bar as perfectly glued in place, which creates tiny areas of extra stress that simple hand calculations just don't account for.

The whole assignment took me about 4 hours to complete from start to finish.

