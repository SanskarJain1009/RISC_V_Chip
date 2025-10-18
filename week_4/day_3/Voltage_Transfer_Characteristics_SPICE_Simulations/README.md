# Voltage transfer characteristics – SPICE simulations
It included-
1. SPICE deck creation for CMOS inverter-
    Spice deck creation for CMOS inverter and the steps needed for it are shown below.
    ![spice_deck_connectivity](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/spice_deck_connectivity.png)
  
2. SPICE simulation for CMOS inverter-
    In this, the program for cmos is described. The code is shown below. 
    ![deck_spice_program](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/deck_spice_program.png)
    
    (Note- In this simulation the channel length is kept same for both nmos and pmos)
    The obtained plot shows that the plot is shifted a little to left.
    ![CMOS_Vin_vs_Vout_for_same_channel_length_pmos_and_nmos](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/CMOS_Vin_vs_Vout_for_same_channel_length_pmos_and_nmos.png)
    
    Now the pmos length is increased by a factor of 2.5 than the nmos. The program for this spice model is shown below-
    ![Spice_Program_for_2o5_channel_length_of_pmos](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/Spice_Program_for_2o5_channel_length_of_pmos.png)
    
    The plot obtained for vin vs vout for this configuration is shown below. In the plot one can see that the plot is somewhat around the center. 
    ![Vin_vs_Vout_for_2o5_channel_length_of_pmos](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/Vin_vs_Vout_for_2o5_channel_length_of_pmos.png)
    
    The reason for this will be explained in next lecture.

3. Labs Sky130 SPICE simulation for CMOS-
    In this lap, the sky130circuitdesignworkshop is used. The VTC of cmos inverter is plotted and along with it the switching threshold is shown. The plot obtained along with switching threshold is shown below.
    ![plot_vin_vs_vout_with_switching_threshold](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/plot_vin_vs_vout_with_switching_threshold.png)
    
    Then, the Transient Analysis is done. The obtained plot is shown below.
    The rise transient plot along with rise delay is shown below. Subtracting both the xo, the obtained Rise Delay is around 0.33ns
    ![Transient_Plot_out_vs_time_in_with_Rise_Delay](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/Transient_Plot_out_vs_time_in_with_Rise_Delay.png)
    
    Then, the fall time is also calculated using the plot obtained and is shown below. The calculation is same and it is around 0.28ns -
    ![Transient_Plot_out_vs_time_in_with_Fall_Delay](/week_4/day_3/Voltage_Transfer_Characteristics_SPICE_Simulations/img/Transient_Plot_out_vs_time_in_with_Fall_Delay.png)
