# Static behavior evaluation – CMOS inverter robustness – Device variation-
It included-
    The device variation identifies the parameters that vary the length and width of CMOS Inverter.
    
1. Sources of Variation (Etching process Variation) -
    Etching is a fabrication step. It defines the width and height of structure. The etching process creates distorting while creating mask. And the W and L becomes W` and L'. The images below shows this variation properly.
    ![Etching_Process_1](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Etching_Process_1.png)
    ![Etching_Process_2](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Etching_Process_2.png)
    ![Etching_Process_3](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Etching_Process_3.png)
    ![Etching_Process_4](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Etching_Process_4.png)
  
    This Variation affects the Drain Current.
    ![Etching_Process_5](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Etching_Process_5.png)
    
2. Sources of Variation (Oxide Thickness) -
    More the Oxide Thickness Variation, more is the drain current variation. The images below explain it how-
    ![Oxide_Thickness_1](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Oxide_Thickness_1.png)
    ![Oxide_Thickness_2](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Oxide_Thickness_2.png)
    ![Oxide_Thickness_3](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Oxide_Thickness_3.png)
    
3. Smart SPICE Simulation for Device Variations-
    The image below explains what we are going to do. 
    ![Smart_SPICE_Simulation_for_Device_Variations_Explaination](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Explaination.png)
    
    Basically we'll sweep the size of nmos and pmos for device varation effects and plot the VTC for cmos inverter. Note- Strong pmos/nmos mean a very low resistance path and weak pmos/nmos mean a very high resistance path. The images below shows the program and plots.
    ![Smart_SPICE_Simulation_for_Device_Variations_Program_1](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Program_1.png)
    ![Smart_SPICE_Simulation_for_Device_Variations_Program_2](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Program_2.png)
    ![Smart_SPICE_Simulation_for_Device_Variations_Program_3](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Program_3.png)
    ![Smart_SPICE_Simulation_for_Device_Variations_Plot](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Plot.png)
    
4. Conclusion -
    The observation from the plot above is shown below in the image.
    ![Smart_SPICE_Simulation_for_Device_Variations_Conclusion](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Smart_SPICE_Simulation_for_Device_Variations_Conclusion.png)
    
    
## With this we can conclude that the cmos Inverter is robust to all kinds of variation. CMOS inverter is robust to all the parameters we discussed - Switching Threshold, Noise Margin, Power Supply Variation and Device Variation. From this we can conclude that CMOS inverter operation is intact. 
   
   ![Operation_is_Gate_Intact](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Operation_is_Gate_Intact.png)
   
5. Sky130 Device Variation Labs-
    The Lab performed for week_4 workshop day 5. And the obtained plots are shown below-
    ![Device_Variation_Lab_Plot](/week_4/day_5/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Device_Variation/img/Device_Variation_Lab_Plot.png)
    
    From the plot, we can observe that the high logic is holding for longer than low logic. This is because, the size of pmos is much higher than the size of the nmos. And the switching threshold voltage is 0.988V. 
