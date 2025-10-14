# NMOS_Resistive_Region_and_Saturation_Region_of_Operation: 
There are basically three modes of operation-
  i. Cut-off region
  ii. Resistive region
  iii. Saturation region.
  
  Earlier we discussed about the cutoff region. Here we will discuss about the resistive and saturation region. 
  
1. Resistive region of operation with small drain-source voltage-
    Resistive region -> Vgs > Vt (Vt = Threshold Voltage)
    The NMOS structure at resistive region is studied as follow-
    ![nmos_in_physics_pov](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/nmos_in_physics_pov.png)
    
2. Drift current theory-
    The derivation for the drift current is shown in the images below-
    ![Vt_derivation_1](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_1.png)
    ![Vt_derivation_2](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_2.png)
    
    From device point of view, we have two types of current-
    i. Drift current- Current due to potential difference.
    ii. Diffusion current- Current due to difference in carrier concentration.
    
    And in the structure of NMOS drawn in the above images, we can see that there is voltage difference at V(L) (Vds) and V(0) (0). So, we will only derive drift current equation and it explains the model in a very simple manner. 
    ![Vt_derivation_3](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_3.png)
    ![Vt_derivation_4](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_4.png)
    ![Vt_derivation_5](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_5.png)

3. Drain current model for linear region of operation-
    ![Vt_derivation_6](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Vt_derivation_6.png)

4. SPICE conclusion to resistive operation-
    Now, we need to check the Id with varying Vgs to find the range of Vds at which the resistive operation withholds. So, for this we need SPICE. SPICE simulation answers the question -"How do we calculate Id for different values of Vgs and at every value of Vgs, sweep Vds till (Vgs-Vt) using linear equation for Id?"
    
5. Pinch-off region condition-
    At Vds >= (Vgs - Vt), the channel starts disappearing. And this region is called as Pinch-off Region. The images below shows and explains the pinch-off region.
    ![Pinch_off_Region_1](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Pinch_off_Region_1.png)
    ![Pinch_off_Region_2](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Pinch_off_Region_2.png)
    
6. Drain current model for saturation region of operation-
    Here, we will make a simple model of NMOS transistor and derive the drain current equation for it. The images below derives the drain current for saturation region.
    ![Pinch_off_Region_Drain_Current_Model](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Pinch_off_Region_Drain_Current_Model.png)
    
    Although the equations shows that by reducing the channel length the drain current increases but that's not what actually happens and the reason being is velocity saturation (which is discussed later). In contrast by decreasing the channel length, the drain current also decreases. It looks like that at this region, the transistor acts as a perfect current source but this is also not true. Vds is still a factor for drain current equation at pinch off region. The image below shows it in a better sense along with the correct drain current equation for pinch-off region by taking channel length modulation in account.
    ![Pinch_off_Region_Channel_Length_Mod](/week_4/day_1/NMOS_Resistive_Region_and_Saturation_Region_of_Operation/img/Pinch_off_Region_Channel_Length_Mod.png)
