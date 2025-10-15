# SPICE Simulation for Lower Nodes and Velocity Saturation Effect:
It included-
1. SPICE Simulation for Lower Nodes-
    First, a plot was shown for describing the regions - Cutoff, saturation and linear.
    ![spice_waveform](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/spice_waveform.png)
    
    Then, W/L is kept constant and two different spice models are simulated and plotted. The plotted graphs are displayed below.
    ![Observed_Plot_for_constant_W_by_L](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Observed_Plot_for_constant_W_by_L.png)
    
2. Drain current vs gate voltage for long and short channel device-
    Observation 1:
    In longer channel device, the current has quadratic dependency as expected (drain current equation is quadratic) at higher drain voltage. Whereas in shorter channel device, the current has quadratic dependency at lower values of Vgs and linear dependency for higher values of Vgs. The reason being the velocity saturation effect takes place at short channel. This is one of the short channel effect. 
    The plot below (gate voltage v/s drain current) displays the varying Vgs and Constant Vds. The plot clearly shows that the plot with longer channel is somewhat quadratic and the plot with shorter channel length is quadratic at lower values of Vgs and linear at higher values of Vgs.
    ![V_I_Plot_const_Vds_varying_Vgs](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/V_I_Plot_const_Vds_varying_Vgs.png)
    
3. Velocity saturation at lower and higher electric fields- 
    For short channel transistors, we have 4 region of operation- cutoff, linear, saturation and velocity saturation region.
    The velocity saturation effect basically tells us that at lower electric field, it follows a certain trend and at higher electric field velocity becomes constant and the reason being the scattering effect. The images below explain velocity saturation in better sense and derive the drain current also. 
    ![velocity_saturation_effect_1](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_1.png)
    ![velocity_saturation_effect_2](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_2.png)
    ![velocity_saturation_effect_3](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_3.png)
    ![velocity_saturation_effect_4](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_4.png)
    ![velocity_saturation_effect_5](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_5.png)
    ![velocity_saturation_effect_6](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_6.png)
    ![velocity_saturation_effect_7](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/velocity_saturation_effect_7.png)
    
4. Velocity saturation drain current model-
    By substituting different values of Vmin, the drain current equation is obtained for different regions. The images shown below, shows all these obtained equations.
    ![Saturation_Region_Drain_Current_Equation](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Saturation_Region_Drain_Current_Equation.png)
    ![Resistive_Region_Drain_Current_Equation](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Resistive_Region_Drain_Current_Equation.png)
    ![Velocity_Saturation_Region_Drain_Current_Equation](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Velocity_Saturation_Region_Drain_Current_Equation.png)
    
    Observation 2:
    We observed that the device saturate early and the peak current for same W/L ration is different and less, this is due to the velocity saturation effect in short channels. The image below shows this observation graphically.
    ![Observation_2](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Observation_2.png)
    
5. Labs Sky130 Id-Vgs
    The obtained plots for both the vds and vgs constant separately is shown below.
    ![Labs_Sky130_Id_Vds](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Labs_Sky130_Id_Vds.png)
    ![Labs_Sky130_Id_Vgs](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Labs_Sky130_Id_Vgs.png)
    
6. Labs Sky130 Vt-
    This lab showed how to find the Vt of the device. Using the just above plot, if we go along the linear region and where this tangential extension cuts the x-axis is the Vt of the device. The image below shows the Vt of the device.
    ![Labs_Sky130_Vt](/week_4/day_2/SPICE_Simulation_for_Lower_Nodes_and_Velocity_Saturation_Effect/img/Labs_Sky130_Vt.png)
