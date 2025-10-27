# Library Binding and Placement: 
The Placement & Routing step of Physical Design Flow includes-
1. Netlist binding and initial place design-
    The Placement and Routing involves the following steps.
    The first step is
    i. Bind netlist with physical cells
    In reality, the design of gates or flip flops does not have the shape as they are represented (curved shaped) instead they have the box shape. The images below explain it well.
    ![Binding_and_Placement_Cell_Shape_1](/week_6/day_2/Library_Binding_and_Placement/img/Binding_and_Placement_Cell_Shape_1.png)
    ![Binding_and_Placement_Cell_Shape_2](/week_6/day_2/Library_Binding_and_Placement/img/Binding_and_Placement_Cell_Shape_2.png)
    
    These box shaped cells are present in library. This library contains information about every cell like timing information. The library can be classified into two categories (generally), one library consists of the shapes and size, and the other library consists about timing (delay) information. 
    ![Binding_and_Placement_Library_1](/week_6/day_2/Library_Binding_and_Placement/img/Binding_and_Placement_Library_1.png)
    
    The library also provides option for a particular cell (in shape, size, etc).
    ![Binding_and_Placement_Library_2](/week_6/day_2/Library_Binding_and_Placement/img/Binding_and_Placement_Library_2.png)
     
    The second step is
    ii. Placement
    After binding netlist with physical cells, these cells needs to be placed on the chip (core). This is shown in the images below. 
    ![Placement_1](/week_6/day_2/Library_Binding_and_Placement/img/Placement_1.png)
    ![Placement_2](/week_6/day_2/Library_Binding_and_Placement/img/Placement_2.png)
    
    In the image above, one can see that since the orange FF1 is close to Din1 the reason being that the Din1 is input to FF1. And same reason is for orange FF2. This reason is not correct for yellow cells. Although they are very close, which will make the delay between them very little. But yellow FF1 is not close to its input which will cause a larger delay. The solution for this will be discussed in the next point, optimize placement. The complete placement of the example netlist is shown below. 
    ![Placement](/week_6/day_2/Library_Binding_and_Placement/img/Placement.png)
    
2. Optimize placement using estimated wire-length and capacitance
    The third step is
    iii. Optimize Placement
    This is the stage where we estimate wire length and capacitance and, based on that, insert repeaters. Repeaters are basically the buffer which will recondition the original signal, make a new signal which is the replicated original signal and will move it forward. And that's how signal integrity is maintained. The images below shows the optimized placement using buffer (wherever necessary to maintain the signal integrity).
    ![Optimize_Placement_1](/week_6/day_2/Library_Binding_and_Placement/img/Optimize_Placement_1.png)
    ![Optimize_Placement_2](/week_6/day_2/Library_Binding_and_Placement/img/Optimize_Placement_2.png)
    
3. Final placement optimization-
    In the previous point, the optimization of the orange and yellow set of cells is done. (Note- The optimization is based on the transition analysis of the path such as slew rate, delay, wire capacitance, etc. And the placement optimization is based on these parameters to keep everything under permissible bound) 
    The image below shows the placement optimization of remaining set of cells. The image below shows the final placement of the example netlist.
    
4. Need for libraries and characterization-
    In every stage of Physical Design Flow, one thing is common and that is the cells from library that are used in the design. The libraries characterization is very important as it contains all the timing information, shape and size information of the cells. The images below show the same thing but in visuals. How to characterize it is not taught. 
    ![Library_Characterization_1](/week_6/day_2/Library_Binding_and_Placement/img/Library_Characterization_1.png)
    ![Library_Characterization_2](/week_6/day_2/Library_Binding_and_Placement/img/Library_Characterization_2.png)
    ![Library_Characterization_3](/week_6/day_2/Library_Binding_and_Placement/img/Library_Characterization_3.png)
    
