# Static behavior evaluation – CMOS inverter robustness – Noise margin
It included-
1. Introduction to noise margin-
    Ideally the slope of inverter is infinite but in reality the slope of inverter transition is finite. This is shown in the image below.
    ![Noise_Margin_Ideal_And_Practical](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Ideal_And_Practical.png)
  
2. Noise margin voltage parameters-
    The actual and practical Vin vs Vout is shown below for the inverter.
    ![Noise_Margin_Practical_and_Actual](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Practical_and_Actual.png)

3. Noise margin equation and summary- 
    Basically, noise margin implies for a set of range for input and output such that the local high or low can be inferred. The noise margin makes the device tolerable to noise. We have three margins in total, noise high margin, noise low margin and undefined margin. The images below shows them properly.
    ![Noise_Margin_for_Logic_High](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_for_Logic_High.png)
    ![Noise_Margin_for_Logic_Low](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_for_Logic_Low.png)
    ![Undefined_Margin](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Undefined_Margin.png)
    
    Noise Margin Summary is shown in the image below-
    ![Noise_Margin_Summary](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Summary.png)
    
4. Noise margin variation with respect to PMOS width-
    In this, we will find the variation in Noise Margin of a CMOS Inverter when the pmos width is varied. Below are the images showcasing this-
    ![Noise_Margin_Variation_with_pmos_width_1x](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Variation_with_pmos_width_1x.png)
    ![Noise_Margin_Variation_with_pmos_width_2x](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Variation_with_pmos_width_2x.png)
    ![Noise_Margin_Variation_with_pmos_width_3x](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Variation_with_pmos_width_3x.png)
    ![Noise_Margin_Variation_with_pmos_width_4x](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Variation_with_pmos_width_4x.png)
    ![Noise_Margin_Variation_with_pmos_width_5x](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Variation_with_pmos_width_5x.png)
    
    The noise margin area can be used for digital design and the undefined region is used for analog design. It is shown below-
    ![Region_For_Digital_Design](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Region_For_Digital_Design.png)
    ![Region_For_Analog_Design](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Region_For_Analog_Design.png)
    
5. Sky130 Noise margin labs-
    The image shown below shows the plot and the VIL, VOH, VIH and VOL values respectively. The NMH (Noise Margin High, VOH - VIH) value is 0.75V and the NML (Noise Margin Low, VIL - VOL) value is 0.64V. 
    ![Noise_Margin_Lab](/week_4/day_4/Static_Behavior_Evaluation_CMOS_Inverter_Robustness_Noise_Margin/img/Noise_Margin_Lab.png)
