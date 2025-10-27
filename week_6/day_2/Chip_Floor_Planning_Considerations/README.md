# Chip Floor Planning Considerations: 
It included-

1. Utilization factor and aspect ratio-
    The first step of Floor Planning in Physical Design (PD) is -
    i. Define Width and Height of Core and Die
    ![Define_Widht_and_Height_of_Core_and_Die](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Define_Widht_and_Height_of_Core_and_Die.png)
    
    The dimensions of a chip are dependent on the dimensions of the logic gate and the flip flops.
    The below images explains the core and die along with utilization factor and aspect ratio with examples. 
    ![Die_and_Core_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_1.png)
    ![Die_and_Core_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_2.png)
    ![Die_and_Core_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_3.png)
    ![Die_and_Core_4](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_4.png)
    ![Die_and_Core_5](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_5.png)
    ![Die_and_Core_6](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_6.png)
    ![Die_and_Core_7](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_7.png)
    ![Die_and_Core_8](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_8.png)
    ![Die_and_Core_9](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Die_and_Core_9.png)
    
2. Concept of pre-placed cells-
    The second step of Floor Planning in Physical Design (PD) is-
    ii. Define Locations of Pre-Places Cells
    In Floorplanning, defining the locations of pre-placed cells basically means that we granularize the top level design and these block together makes up the top level design. Every block is placed on the core before the automatic placement and routing, this before hand placing the blocks makes there place in core invariant to the automated process of placement and routing, i.e, there location gets fixed which will not be changed in later process.
    The preplaced cells are also explained in the images below.
    ![Pre_Placed_Cells_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pre_Placed_Cells_1.png)
    ![Pre_Placed_Cells_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pre_Placed_Cells_2.png)
    ![Pre_Placed_Cells_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pre_Placed_Cells_3.png)
    ![Pre_Placed_Cells_4](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pre_Placed_Cells_4.png)
    
    In the image below, you can see the pre-placed cells in the core. The blocks shown below take input value, so they are placed closed to the input. So, that when design automation starts these blocks won't change their location.
    ![Pre_Placed_Cells_4](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pre_Placed_Cells.png)

3. De-coupling Capacitors-
    The third step of Floor Planning in Physical Design (PD) is-
    iii. Surround pre-placed cells with decoupling capacitor.
    The images below explain and visually describe why decoupling capacitor is needed.
    ![Decoupling_Capacitor_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Decoupling_Capacitor_1.png)
    ![Decoupling_Capacitor_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Decoupling_Capacitor_2.png)
    ![Decoupling_Capacitor_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Decoupling_Capacitor_3.png)
    
4. Power Planning-
    The fourth step of Floor Planning in Physical Design (PD) is-
    iv. Power Planning
    The decoupling capacitor addition solves the problem of local communication. Power planning is needed for global communication.
    Suppose in the image below, the macro is repeated which will power to be divided for every element in all those macro. There is necessity of signal preservation from one macro so that it doesn't change before reaching the load of the connected macro. In the images this is shown. In the first block, a signal is depicted which is going from low to high and we want to retain that signal, by retain it means that signal should not exceed noise figure parameters. This is caused because the power is being supplied and getting divided in so many blocks. This is also shown in the image below. This is caused because there is no decoupling capacitor which is decoupling power supply from macro blocks. It is not feasible to put decoupling capacitor everywhere in the chip. Some critical blocks gets decoupled using decoupling capacitor but not all. 
    ![Power_Planning_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_1.png)
    ![Power_Planning_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_2.png)
    ![Power_Planning_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_3.png)
    
    The red coloured wire is a 16-bit bus which is far from the power supply. So, there can be power drop there which can affect the signal. Let's see the Vdd and GND value at the red wire. The images below describe what can go wrong.
    ![Power_Planning_Necessity_1_What_can_go_wrong](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Necessity_1_What_can_go_wrong.png)
    ![Power_Planning_Necessity_2_What_can_go_wrong](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Necessity_2_What_can_go_wrong.png)
    ![Power_Planning_Necessity_3_What_can_go_wrong](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Necessity_3_What_can_go_wrong.png)
    
    All this is caused because of only 1 power supply.
    The solution to this problem is what if the power supply is done from multiple places. This is exactly the solution, which is shown in the image below.
    ![Power_Planning_Reason_Solution_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Reason_Solution_1.png)
    ![Power_Planning_Reason_Solution_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Reason_Solution_2.png)
    ![Power_Planning_Reason_Solution_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Power_Planning_Reason_Solution_3.png)
    
5. Pin Placement-
    The fifth step of Floor Planning in Physical Design (PD) is-
    v. Pin Placement
    After all the netlist connections are done, the input and output needs to be noted down separately so that the pin placement can be done for these signals. The images below shows how after netlist design connections are completed, pin placement is done.
    ![Pin_Placement_Netlist_1](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pin_Placement_Netlist_1.png)
    ![Pin_Placement_Netlist_2](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pin_Placement_Netlist_2.png)
    ![Pin_Placement_Netlist_3](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pin_Placement_Netlist_3.png)
    ![Pin_Placement](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Pin_Placement.png)
    
    The sixth step of Floor Planning in Physical Design (PD) is-
    iv. Logic Cell Placement Blockage
    Configuration needs to be done so that the die area selected for pins won't get used during automated placement and routing.
    ![Logic_Cell_Placement_Blockage](/week_6/day_2/Chip_Floor_Planning_Considerations/img/Logic_Cell_Placement_Blockage.png)
    
    
    
    
    
    
