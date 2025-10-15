# CMOS_Voltage_Transfer_Characteristics_VTC:
It included-
1. MOSFET as a Switch-
    The MOS Device Characteristics are shown in the image below- 
    ![MOS_Device_Characteristics](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/MOS_Device_Characteristics.png)
    
2. Introduction to standard MOS voltage current parameters-
    The CMOS structure is shown, it comprises of pmos and nmos with same common gate and drain connected to each other. The Source of pmos is connected to Vdd and the source of nmos is connected to ground(GND). Note- The pmos turns ON when -Vgs < -Vt and nmos turns ON when Vgs > Vt.
    The structure of cmos along with it's operation when input is high is shown below-
    ![cmos_high_input](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/cmos_high_input.png)
    ![cmos_low_input](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/cmos_low_input.png)
    
    The Vout of CMOS for both the inputs is shown below-
    ![vout](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/vout.png)
    
    The structure of CMOS after naming convention is shown below-
    ![Naming_Convention](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/Naming_Convention.png)
    
    From the above info. we can clearly see and conclude that the shown cmos structure acts as an Inverter.
    Now, for deriving the Voltage Transfer Characteristics of the cmos inverter, we observed few things in the structure which are shown below-
    ![Observations_for_VTC](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/Observations_for_VTC.png)
    
3. PMOS/NMOS drain current v/s drain voltage
    The Ids and Vds Curve with sweeping Vgs for both the pmos and nmos is shown below-
    ![pmos_nmos_Ids_vs_Vds_const_Vgs](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/pmos_nmos_Ids_vs_Vds_const_Vgs.png)

4. Step 1- Convert PMOS gate-source-voltage to Vin
    Steps to obtain Voltage-Transfer Characteristics for Static CMOS Inverter-
    For VTC, we need to bring pmos and nmos plot shown above in same plot (same x and y axis). We will try to bring the graph under same Vin and Vout and they have one common current (IdsN) as IdsP = -IdsN. So, for that we will first alter the pmos graph. We tried bringing pmos graph in terms of Vin and IdsN and the plot is shown in the image below.
    ![pmos_graph_in_terms_of_IdsN_and_Vin](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/pmos_graph_in_terms_of_IdsN_and_Vin.png)

5. Step2 & Step3 – Convert PMOS and NMOS drain-source-voltage to vout
    Next, we will bring pmos plot under the Vout terms. It is shown below-
    ![pmos_graph_in_terms_of_Vout](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/pmos_graph_in_terms_of_Vout.png)
    
    Now, same thing we will similarly bring nmos plot under the Vin, Vout and IdsN terms.
    ![load_curve_for_nmos](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/load_curve_for_nmos.png)
    
6. Step4 – Merge PMOS – NMOS load curves and plot VTC
    After merging the pmos and nmos load curve and plotting the Vin and Vout plot for the intersection points of nmos and pmos gives us the VTC plot. The VTC is shown below.
    ![VTC_Inverter](/week_4/day_2/CMOS_Voltage_Transfer_Characteristics_VTC/img/VTC_Inverter.png)
    
    
    
