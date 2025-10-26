# SoC design and OpenLANE:
   
1. Introduction to all components of open-source digital ASIC design-
    The main components for Digital ASIC Design are - RTL IPs, EDA Toold and PDK Data. 
    The below images shows this flow along with the open-source tools.
    ![Open_Source_Digital_IC_Design_Components_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Open_Source_Digital_IC_Design_Components_1.png)
    ![Open_Source_Digital_IC_Design_Components_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Open_Source_Digital_IC_Design_Components_2.png)
    
    PDK (Process Development Kit), it acts as a bridge between design and fabrication process. It is a collection of files used to model a fabrication process for the EDA tools used to design an IC. The images below explain it in a better sense. 
    ![PDK_1](/week_6/day_1/SoC_design_and_OpenLANE/img/PDK_1.png)
    ![PDK_2](/week_6/day_1/SoC_design_and_OpenLANE/img/PDK_2.png)
    
2. Simplified RTL2GDS flow-
    The RTL to GDSII Flow is simplified into 6 steps-
    i. Synthesis.
    ii. Floor Planning and Power Planning.
    iii. Placement.
    iv. Clock Tree Synthesis.
    v. Routing.
    vi. Sign Off. 
    
    The above steps are shown and explained in the series of images below-
    ![RTL_to_GDSII_Flow](/week_6/day_1/SoC_design_and_OpenLANE/img/RTL_to_GDSII_Flow.png)
    ![Synthesis](/week_6/day_1/SoC_design_and_OpenLANE/img/Synthesis.png)
    ![Floor_Planning_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Floor_Planning_1.png)
    ![Floor_Planning_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Floor_Planning_2.png)
    ![Floor_Planning_3](/week_6/day_1/SoC_design_and_OpenLANE/img/Floor_Planning_3.png)
    ![Synthesis](/week_6/day_1/SoC_design_and_OpenLANE/img/Synthesis.png)
    ![Placement_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Placement_1.png)
    ![Placement_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Placement_2.png)
    ![Clock_Tree_Synthesis](/week_6/day_1/SoC_design_and_OpenLANE/img/Clock_Tree_Synthesis.png)
    ![Routing_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Routing_1.png)
    ![Routing_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Routing_2.png)
    ![Signoff](/week_6/day_1/SoC_design_and_OpenLANE/img/Signoff.png)
    
3. Introduction to OpenLANE and Strive chipsets-
    The images below briefs about the OpenLANE and Strive. After this, the images shows the main goals of OpenLANE.
    ![OpenLANE](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE.png)
    ![Strive_Family](/week_6/day_1/SoC_design_and_OpenLANE/img/Strive_Family.png)
    ![OpenLANE_Main_Goals_1](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Main_Goals_1.png)
    ![OpenLANE_Main_Goals_2](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Main_Goals_2.png)
    ![OpenLANE_Main_Goals_3](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Main_Goals_3.png)
    ![OpenLANE_Main_Goals_4](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Main_Goals_4.png)
    ![OpenLANE_Main_Goals_5](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Main_Goals_5.png)
    
4. Introduction to OpenLANE detailed ASIC design flow-
    The image below shows the OpenLANE detailed ASIC Deisgn flow.
    ![OpenLane_Design_ASIC_Flow](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLane_Design_ASIC_Flow.png)
    
    The image below shows the projects on which OpenLANE based on.
    ![OpenLANE_Based_On](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Based_On.png)
    
    OpenLANE Design ASIC Flow:
    i. Synthesis - 
    In this the RTL synthesis is done to obtain equivalent netlist. Yosys is used for synthesis along with abc. The work of abc is to optimize the design when gated netlist gets generated. The abc scripts are used for this called as synthesis strategies. These strategies targets the least area, best timing, etc. Different designs can use different strategies to achieve the objectives. And for exploration, synthesis exploration utility is used which can be used to generate reports that shows how design delay/area is affected by the strategy. Based on this the best strategy can be obtained to continue with. The image below shows hows synthesis exploration looks like. 
    ![Synthesis_Exploration](/week_6/day_1/SoC_design_and_OpenLANE/img/Synthesis_Exploration.png)
    
    OpenLane also has another utility called design exploration which is used to sweep and explore design configurations. The design exploration generates report which look like the image below. 
    ![Design_Exploration](/week_6/day_1/SoC_design_and_OpenLANE/img/Design_Exploration.png)
    
    The OpenLANE design exploration utility is also used for regression testing(CI). The image below gives glimpse for it. 
    ![OpenLANE_Regression_Testing](/week_6/day_1/SoC_design_and_OpenLANE/img/OpenLANE_Regression_Testing.png)
    
    ii. Design for Test (Inserting Testing Structure)- 
    For this, the tool that is used is Fault. Basically, DFT (Design For Test) is done for the testability of the chip after the fabrication process. It is optional. The images below shows the basic of DFT.
    ![DFT](/week_6/day_1/SoC_design_and_OpenLANE/img/DFT.png)
    
    iii. Physical Design-
    This is a automated process and the tool used for this is OpenRoad. The image below describes it. 
    ![Physical_Implementation](/week_6/day_1/SoC_design_and_OpenLANE/img/Physical_Implementation.png)
    
    During physical design to address the issue of Antenna Rule Violation, OpenLane uses the Fake Antenna Diode Cells. About this violation and solution is explained in the images below.
    ![Antenna_Rule_Violation_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Antenna_Rule_Violation_1.png)
    ![Antenna_Rule_Violation_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Antenna_Rule_Violation_2.png)
    ![Antenna_Rule_Violation_3](/week_6/day_1/SoC_design_and_OpenLANE/img/Antenna_Rule_Violation_3.png)
    
    OpenLANE provides an option to configure to use either the OpenRoad or OpenLANE approach to deal with this violation.
    
    iv. Logical Equivalence Check (LEC)-
    Yosys is again used for this. This is done to check the design equivalence of netlist and the design obtained after physical implementation/design.
    The image below describes it. 
    ![LEC](/week_6/day_1/SoC_design_and_OpenLANE/img/LEC.png)
    
    v. Signoff-
    The signoff of an OpenLANE includes Static Timing Analysis(STA), Design Rule Checking(DRC) and Layout Versus Schematic (LVS). The images below shows these steps.
    ![Signoff_1](/week_6/day_1/SoC_design_and_OpenLANE/img/Signoff_1.png)
    ![Signoff_2](/week_6/day_1/SoC_design_and_OpenLANE/img/Signoff_2.png)

