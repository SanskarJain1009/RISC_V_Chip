# Static behavior evaluation – CMOS inverter robustness – Switching Threshold-
It included-
1. Switching Threshold, Vm- 
    Previously we shown that when pmos and nmos has same channel length the plot for vin and vout was little shifted to left and when the channel length is made 2.5x of nmos, it was somewhere around the center of Vin voltage. The reason for that will be explained. And the concept of switching threshold(Vm) will be described here. 
    Both the plots are shown below-
    ![same_channel_length_and_2o5x_pmos_vtc_plot](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/same_channel_length_and_2o5x_pmos_vtc_plot.png)
    
    One of the parameter that describes the robustness of the cmos inverter is the switching threshold. Vm is the point where Vin = Vout. The Vm lies at a region where both nmos and pmos are in saturation region. This may lead to current leakage. The Vm for both the configuration along with the boundary conditions required for deriving the Vm is shown below-
    ![Vm_for_both_the_Configurations](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Vm_for_both_the_Configurations.png)
    
    ![Boundary_Conditions](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Boundary_Conditions.png)

2. Analytical expression of Vm as a function of (W/L)p and (W/L)n-
    The derivation of the Vm is shown in series in the images below- (Note- The drain current is considered in velocity saturation region)
    ![Derivation_Vm_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_Vm_1.png)
    ![Derivation_Vm_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_Vm_2.png)
    ![Derivation_Vm_3](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_Vm_3.png)
    
    In the above derivation, we set the value of W/L and then found the Vm. Conversely we can do the opposite, by setting the Vm, we can reach to W/L ratios.
    
3. Analytical expression of (W/L)p and (W/L)n as a function of Vm-
    The derivation of the Vm is shown in series in the images below- (Note- The drain current is considered in velocity saturation region)
    ![Derivation_W_by_L_in_terms_of_Vm_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_1.png)
    ![Derivation_W_by_L_in_terms_of_Vm_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_2.png)
    ![Derivation_W_by_L_in_terms_of_Vm_3](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_3.png)
    ![Derivation_W_by_L_in_terms_of_Vm_4](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_4.png)
    ![Derivation_W_by_L_in_terms_of_Vm_5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_5.png)
    ![Derivation_W_by_L_in_terms_of_Vm_6](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Derivation_W_by_L_in_terms_of_Vm_6.png)

4. Static and dynamic simulation of CMOS inverter-
    The images below shows the simulation plots and resultant values-
    Static Simulation-
    ![program_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/program_1.png)
    ![plot_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_1.png)
    
    Dynamic Simulation-
    ![program_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/program_2.png)
    ![Transient_Analysis_Pulse_Description](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Transient_Analysis_Pulse_Description.png)
    ![plot_2_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_2_1.png)
    ![plot_2_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_2_2.png)
    ![plot_2_3](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_2_3.png)
    ![plot_2_4](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_2_4.png)
    ![plot_2_5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/plot_2_5.png)
    
    ![Switching_Threshold_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Switching_Threshold_1.png)
    
5. Static and dynamic simulation of CMOS inverter with increased PMOS width-
    ![Increased_pmos_width_2x_program_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Increased_pmos_width_2x_program_1.png)
    ![Increased_pmos_width_2x_program_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Increased_pmos_width_2x_program_2.png)
    
    The plot below shows that the VTC curve is shifted to right. And as a result we have more area in the pmos for the load capacitor to get charged faster.
    ![Increased_pmos_width_2x_plot_1](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Increased_pmos_width_2x_plot_1.png)
    ![Increased_pmos_width_2x_plot_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Increased_pmos_width_2x_plot_2.png)
    ![program_2_rise_delay](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/program_2_rise_delay.png)
    ![program_2_fall_delay](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/program_2_fall_delay.png)
 
    ![Switching_Threshold_2](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Switching_Threshold_2.png)
    
    Now, we again increase the pmos size to 3x, 4x and 5x. And do the same steps again. The results found are shown below for the respective sizes-
    ![Switching_Threshold_3](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Switching_Threshold_3.png)
    ![Switching_Threshold_4](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Switching_Threshold_4.png)
    ![Switching_Threshold_5](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Switching_Threshold_5.png)
    
    The observations found are tabulated and shown below. 
    ![Observations_for_Increased_pmos_width](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Observations_for_Increased_pmos_width.png)
    
6. Applications of CMOS inverter in clock network and STA-
    Concluding the switching threshold-
    i. The first advantage of having CMOS inverter kind of structure is that the power increase when the size of pmos increases is not much.
    ii. There might be size of nmos and pmos where rise delay and fall delay is approximately same.
    ![Approximate_equal_rise_and_fall_time](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Approximate_equal_rise_and_fall_time.png)
    
    The Equal Rise and Fall time has an application in clock tree synthesis. It is visually shown in the image below.
    ![Application_for_equal_rise_and_fall_time](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Application_for_equal_rise_and_fall_time.png)
    
    iii. The other sized cmos inverter can be used in data paths. The reason being they are regular inverter/buffer.
    ![Regular_Inverter_or_Buffer](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Regular_Inverter_or_Buffer.png)
    ![Application_as_regular_inverter_or_buffer](/week_4/day_3/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Switching_Threshold/img/Application_as_regular_inverter_or_buffer.png)
    
    
