# Static behavior evaluation – CMOS inverter robustness – Power supply variation - 
It included-
1. Smart SPICE Simulation for Power Supply Variations- 
    In this, SPICE simulations are done with varying power supply and observing the effects that take place. The below images shows the program and plots for this.
    ![Power_Supply_Variation_First_Program_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Power_Supply_Variation_First_Program_1.png)
    ![Power_Supply_Variation_First_Program_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Power_Supply_Variation_First_Program_2.png)
    ![Power_Supply_Variation_First_Program_3](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Power_Supply_Variation_First_Program_3.png)
    ![Power_Supply_Variation_First_Program_Plot](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Power_Supply_Variation_First_Program_Plot.png)
  
2. Advantages and Disadvantages Using Low Supply Voltage-
    The images below explain this point-
    ![Advantage_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Advantage_Gain.png)
    ![dc_gain_power_supply_2.5V](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/dc_gain_power_supply_2o5.png)
    ![dc_gain_power_supply_o5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/dc_gain_power_supply_o5.png)
    
    ![Advantage_Energy](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Advantage_Energy.png)
    ![Energy_2o5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_2o5.png)
    ![Energy_o5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_o5.png)
    
    The disadvantage with using low supply voltage is that the inverter capacitance rise and fall delay may be bigger than what low power supply voltage can handle. The device transient operation may not work properly. The device with higher voltage has lower rise and fall time, which gives it enough time to charge and discharge the capacitor. The images below explain it very well.
    ![Energy_Disadvantage_Rise_and_Fall_Delay_2o5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_Disadvantage_Rise_and_Fall_Delay_2o5.png)
    
    The plot below shows the Vout vs Vin for 2.5V Power Supply.
    ![Energy_Disadvantage_Rise_and_Fall_Delay_2o5_Plot](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_Disadvantage_Rise_and_Fall_Delay_2o5_Plot.png)
    
    The plot below shows the Vout vs Vin for 0.5V Power Supply.
    ![Energy_Disadvantage_Rise_and_Fall_Delay_o5_Plot](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_Disadvantage_Rise_and_Fall_Delay_o5_Plot.png)
    
    The plot below shows the Vout vs Vin for 1V Power Supply.
    ![Energy_Disadvantage_Rise_and_Fall_Delay_1v_Plot](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Energy_Disadvantage_Rise_and_Fall_Delay_1v_Plot.png)
    
3. Sky130 Supply Variation Labs-
    Performing the week_4 workshop lab-
    The plots obtained are shown below-
    ![Plot_and_1o8V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_1o8V_Gain.png)
    ![Plot_and_1o6V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_1o6V_Gain.png)
    ![Plot_and_1o4V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_1o4V_Gain.png)
    ![Plot_and_1o2V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_1o2V_Gain.png)
    ![Plot_and_1V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_1V_Gain.png)
    ![Plot_and_o8V_Gain](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Power_Supply_Variation/img/Plot_and_o8V_Gain.png)
    
    From the plots, it is clear that the gain increases till 1.2V but starts decreasing after it. This is because when we consider the VTC of 1V, the supply voltage is not enough to drive the pfet and nfet transistor. The voltage is not enough for the transistor to turn ON, that's why the gain starts decreasing. 
