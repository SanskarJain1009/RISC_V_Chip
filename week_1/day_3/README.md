# Day 3: Combinational and sequential optmizations
It included-
1. Introduction to optimizations-
    This included constant propogation for combinational logic and sequential constant for sequential logic. Sequential logic also involves state optimisation, retiming and sequential logic cloning which are discussed in short. 

2. Combinational Logic Optimization-
    In this part, logic optimization for the opt_check.v, opt_check2.v and opt_check3.v is shown. There resultant netlist is of 2 input AND Gate, 2 input OR Gate and 3 input AND Gate respectively for each design is attached below. 
    ![opt_check](/week_1/day_2/img/combinational_logic_optimization/opt_check.png)
    ![opt_check](/week_1/day_2/img/combinational_logic_optimization/opt_check2.png)
    ![opt_check](/week_1/day_2/img/combinational_logic_optimization/opt_check3.png)
    
    opt_check4.v, multiple_module_opt.v (flatten) and multiple_module_opt2.v (without flatten) is given as assignment to work on. The obtained netlist is attached below.
    ![opt_check](/week_1/day_2/img/combinational_logic_optimization/opt_check4.png)
    ![multiple_module_opt](/week_1/day_2/img/combinational_logic_optimization/multiple_module_opt.png)
    ![multiple_module_opt2](/week_1/day_2/img/combinational_logic_optimization/multiple_module_opt2.png)
    
3. Sequential Logic Optimization-
    In this, dff_const1.v and dff_const2.v verilog designs are taken as example.
    In dff_const1.v, the 'q' pin changes the value with the positive edge of clock despite the reset is invoked in between. The wave simulated results are attached below.
    ![dff_const1_wave1](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const1_wave1.png)
    ![dff_const1_wave2](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const1_wave2.png)
    
    In dff_const2.v, the 'q' pin output always high, it is not dependent on reset. The wave simulated result is attached below.
    ![dff_const2_wave](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const2_wave.png)
    
    Both the designs are synthesized and visualized. The results are attached below.
    ![synthesized_dff_const1](/week_1/day_2/img/sequential_logic_optimizatoin/synthesized_dff_const1.png)
    ![synthesized_dff_const2](/week_1/day_2/img/sequential_logic_optimizatoin/synthesized_dff_const2.png)
    
    dff_const3.v is also taken as example. This example shows although there is constant value present but still there is no space for optimization. The simulated result and synthesized circuit is attached below.
    ![dff_const3_wave](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const3_wave.png)
    ![synthesized_dff_const3](/week_1/day_2/img/sequential_logic_optimizatoin/synthesized_dff_const3.png)
    
    dff_const4.v and dff_const5.v are given as assignment. The simulated results and the synthesized and mapped netlist generated is attached below for both.
    ![dff_const4_wave](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const4_wave.png)
    ![synthesized_dff_const4](/week_1/day_2/img/sequential_logic_optimizatoin/synthesized_dff_const4.png)
    
    ![dff_const5_wave](/week_1/day_2/img/sequential_logic_optimizatoin/dff_const5_wave.png)
    ![synthesized_dff_const5](/week_1/day_2/img/sequential_logic_optimizatoin/synthesized_dff_const5.png)
    
    
