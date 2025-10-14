# Introduction_to_Circuit_Design_SPICE_Sim: 
It included-
1. Why do we need SPICE Simulation:
    First of all, the topics we talk about such as PD, Clock Tree Syntheses, etc are not possible without spice simulation. The reason being the cmos transistor level simulation is done using SPICE which provides us with the values for all the things needed for VLSI design, and that is delay table. It provides us with the delay table for any transistor gates or designs. The delay table gives delay at the intersection of input slew and output load. SPICE simulation is the lower most simulation possible in vlsi design, it creates foundation blocks for all the layers above it. The below image shows an example of delay table.
    ![Delay_Table](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/Delay_Table.png)
    
    The SPICE Simulation answer the following questions:
    i. Where does the delay of a cell actually comes from?
    ii. Are the delay models accurate?
    iii. How do you verify, what you are doing in Static Timing Analysis is correct?

2. Introduction to basic element in Circuit design – NMOS:
    It is a 4 terminal device. It consists of P substrate, got two isolation region(SiO2), n+ diffusion region, gate oxide, Poly-Si or metal gate, Gate(G), Source(S), Drain(D), Body(B). The image below displays the structure of NMOS. 
    ![NMOS_Structure](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/NMOS_Structure.png)
    
3. Strong inversion and threshold voltage:
    Threshold Voltage- The Vgs voltage at which 'stong inversion' occurs is called threshold voltage. This forms a same type area,i.e., channel between drain and source. 
    ![Threshold_Voltage](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/Threshold_Voltage.png)
    
    When Vgs is increased further, there is no change in depletion width but the width of channel formed increases. This is because the electrons from n-type source and drain gets attracted and at some point forms a continuous n-channel formation from Source-Drain, whose conductivity is modulated by Vgs. 
    ![n_channel_formation_in_NMOS](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/n_channel_formation_in_NMOS.png)
    
    In order to derive the Threshold Voltage Equation, we consider two scenarios-
    ![scenarios](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/scenarios.png)
    
    In the second scenario where Vsb = +ve, there are very observations-
    i. The depletion layer width is more at the source side and that is because of additional reverse bias (Vsb).
    ![Source_side_increased_depletion_layer](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/S_side_increased_depletion_layer.png)
    ii. There is a delay in channel formation. Continued in 4th point.
    
4. Threshold voltage with positive substrate potential:
    ii. Due to positive voltage at source, the negative charge accumulation near the surface of gate is pulled which results in delay for the formation of channel.
    ![delay_in_channel_formation](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/delay_in_channel_formation.png)
    ![delay_in_channel_formation_2](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/delay_in_channel_formation_2.png)
    
    The Threshold Voltage Equation is given by-
    ![Threshold_Voltage_Equation](/week_4/day_1/Introduction_to_Circuit_Design_SPICE_Sim/img/Threshold_Voltage_Equation.png)

